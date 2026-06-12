Overall verdict:

TC-1A v0.3.2 is a debt-bearing semantic-enforcement patch. It does what it
claims on the box: it tightens definitions, narrows the loop-holes the v0.3.1
review flagged, and refuses to import physics. v0.3.1 left the door cracked on
seven points. v0.3.2 closes six of them cleanly and leaves one (the
Boundary-Audit runtime enforcement) as a soft gap. The patch is honest about
its remaining debt, and the surviving debts are all non-blocking for a
TC-1B *spec draft*. It is not yet safe to implement TC-1B in Go without
filling the small list under "Required edits before TC-1B" below.

Does v0.3.2 close the v0.3.1 gaps?

- endpoint definition            : closed
- CoarseAlternatives definition  : closed
- canonical encoding determinism : mostly closed (escape rule under-specified)
- self-reported metadata honesty : closed
- runtime enforcement strength   : closed for the listed fields; boundary
                                   audit is report-only, not runtime-checked
- independentlyJustified rule    : closed
- allowedStarts / maxLength      : closed (StartSelectionMode + fixedBeforeWitness)
- random-label threshold         : closed (0.25 default; 100/1000 trial split
                                   is internally inconsistent and should be
                                   reconciled)
- generic-permutation threshold  : closed (0.10 default; same trial-split issue)
- parity / XOR status rules      : closed (three statuses, EBP-safe)
- U(1) / phase boundary audit    : partially closed (audit schema exists;
                                   no runtime reject; no "valid" boolean)
- Go type-level guardrails       : closed for the types named; lint-time
                                   only, not compile-time
- JSON report schema additions   : closed (four new blocks; selection_audit
                                   is missing a `boundary_audit_valid` peer)
- TC-1B-safety                   : safe to *draft*, not yet safe to *implement*

Remaining undefined terms:

- "LabelRuleSpec" / "CoarseGrainingSpec" / "HistoryEnumerationSpec" are used
  by name throughout §6.3, §7.2, §8.2, but only HistoryEnumerationSpec is
  re-shaped in §8.2. The other two are referenced from v0.3.1 and not
  re-declared. A reader of v0.3.2 alone cannot reconstruct the field lists
  for LabelRuleSpec or CoarseGrainingSpec.
- `validForWitness : Bool` is referenced as a runtime-rejection trigger in
  §6.3 but never appears in any structure declaration shown in this patch.
- "Same effective information" in §10.3 Case 1 is not defined. Two parity
  encodings that *look* different could be informationally equivalent, but
  there is no rule for deciding equivalence.
- The escape mechanism in §5.2 rule 1 ("Escape reserved characters in
  names: | ; / ( ) , \") is named but not specified. Backslash-style
  escaping? Percent-encoding? Length-doubling? This is a real source of
  implementation drift.
- "One full period of U" in §8.5 is referenced as a maxLength candidate
  but period-detection is not defined for non-cyclic U on Fintype (the
  iterates of a bijective function on a finite type are *always* periodic,
  so "if period is computable" is the wrong hedge — the period is always
  computable by brute force at |S|, but no rule says so).
- "Audit" as a term: §6 distinguishes "declared discipline" from
  "historical fact", but `audit` is later reused in `boundary_audit`,
  `selection_audit`, `null_model_power` without a unifying definition.

Remaining hidden imports:

None of physics, quantum mechanics, complex amplitudes, U(1), Hilbert space,
or the Born rule are imported. The patch stays inside the toy discrete
bijection lane. The forbidden-claim lists in §7.2, §10.3 Case 1, §11.2 are
EBP-correct. No smuggling detected.

One soft import remains: §11's `u1ExtensionDebt` is acknowledged as
"later-phase debt, not a TC-1B blocker", but the boundary_audit JSON in
§13.2 is the only place a future draft can fail-fast on U(1) leakage. That
is acceptable, but the debt should be tagged `u1ExtensionDebt` *in the
report schema*, not just in the prose.

Endpoint / CoarseAlternatives assessment:

Both are now well-defined. §3 gives endpoint as Nat.iterate R.U with a
plain-English gloss and a Go recipe. §4 gives CoarseAlternatives as
h1 ≠ h2 ∧ C.pi (endpoint h1) = C.pi (endpoint h2) and explicitly forbids
promoting it to "superposition / interference / branching". The forbidden-
inference block in §4.2 is the strongest single move in the patch from an
overclaiming-prevention standpoint.

One residual: `History` in §3.1 is declared but does not bind `R` via
the dependency-of-correctness check. A future `History` that lives
outside the `R.U` orbit will still be accepted by `endpoint`. That is
acceptable for a toy patch but is debt, not a blocker.

Canonical encoding assessment:

§5 is a serious attempt. The `RS|nodes=N|rels=…` form is deterministic
up to:
  (a) the missing escape rule (see "Remaining undefined terms"),
  (b) the relation-record sort key (lexicographic on the *encoded* form,
      which means the escape is needed first, so (a) and (b) couple).

Rules 1–6 are otherwise sufficient for a first Go pass. The debt line
`fullGraphIsomorphismDebt` is the right posture.

Missing: no rule for what to do when `arity = 0` (nullary relations) or
when the same relation name appears with mixed arities across records.
These are rare but real edge cases that the spec should at least name.

Metadata enforcement assessment:

§6 is the strongest part of the patch. The phrase "Bool metadata records
declared discipline. It does not prove historical fact." is exactly the
EBP-correct framing. Runtime rejection in §6.3 is concrete and
machine-checkable. `metadataTruthDebt` is honestly carried forward.

The only softening: §6.3 lists runtime rejects for the *label-rule* and
*history-enumeration* and *coarse-graining* fields, but the
*boundary_audit* fields (U(1), complex, Hilbert) are not in the
runtime-validation block in §13.1. They are report-only, which is
acceptable for TC-1B but should be flagged.

History selection assessment:

§8 closes the hand-selection loophole via `StartSelectionMode`. The
cleanest-rule prescription in §8.3 is correct as a default. §8.5 fixes
maxLength before witness, with a recommended |S| rule for small systems.
The `finiteRecurrenceDebt` line correctly notes that for bijective U on
a Fintype, maxLength > |S| adds no new orbit structure.

Gap: `selectionJustification : String` can be empty for non-allStates
modes. The patch says "unless there is a pre-registered reason" but does
not enforce non-emptiness of that string at runtime. Add to §6.3
runtime-reject list.

Null-model threshold assessment:

The 0.25 random and 0.10 permutation thresholds are pragmatic first-pass
audit thresholds. §9.4 correctly tags them as Workbench defaults, not
physics. This is the right EBP posture.

Internal inconsistency: §9.2 says "If fewer than 100 random trials are
run → random_null_underpowered" while the recommended minimum is 1000.
These should be reconciled. Either the underpowered threshold rises to
1000 to match the recommendation, or 1000 is the *preferred* number and
100 is the *minimum below which the null is meaningless*. Pick one.

Same issue for §9.3 on the permutation side.

Also: the witness-rate denominator is not defined. "witness_rate" of
0.10 for permutations — over how many permutations? Over the same
StartSelectionMode? Over all declared starts? TC-1B will need this
explicit.

Parity/XOR status assessment:

§10.3's three-status rule is clear and EBP-safe. Case 1 forbids
"interference-like structure survived". Case 3 forbids "quantum
interference derived". The required-additional-evidence list in Case 2
is the right minimum. The only soft spot is the
"same effective information" definition gap noted above.

U(1) / phase boundary audit assessment:

§11 plus §13.2 deliver the audit schema. Good. The gap is that §13.1
`runtime_validation` does not include `boundary_audit_valid` and §6.3
does not list boundary-audit field combinations that auto-reject. The
boundary audit is therefore a human-readability check, not a runtime
fence. That is acceptable for a *spec draft* and should be tightened
before *implementation*.

The `u1ExtensionDebt` line in §11.3 is correctly classified as
later-phase. Don't move it.

Go type-guardrail assessment:

§12 is the second-strongest part of the patch. The forbidden-type list
is unambiguous. The type aliases force intent at the call site.

Gap: this is a lint / code-review check, not a Go compile-time
guarantee. Two honest options:
  (a) Add a TC-1B-specific test file `types_blacklist_test.go` that
      greps the AST / `go/types` package for any of the forbidden
      identifiers and fails the build.
  (b) Document explicitly that this is a code-review gate, not a
      compile-time gate.
The patch should pick (a) or (b) before TC-1B *implementation*; for
TC-1B *drafting* the current text is fine.

JSON report schema assessment:

§13's four new blocks cover the surface. Missing / inconsistent:
  - No `boundary_audit_valid` boolean in runtime_validation.
  - `selection_audit.selection_debt_open` is a Bool but no rule maps
    it to the `invalid_history_selection` status in §8.4.
  - No field for `metadataTruthDebt_remaining` even though the debt is
    named in §6.4. A report that wants to carry this debt needs a
    place to write it down.
  - The schema is prose, not a JSON Schema. That is fine for a
    patch-level spec, but TC-1B should publish a `tc1b_report.schema.json`
    or equivalent.

Should TC-1B be drafted next?

Yes — **draft TC-1B spec**. Not implement. Not promote. The v0.3.2
patch tightens the contract enough to specify TC-1B without re-opening
the v0.3.1 cracks. The remaining items below are spec-time fixes, not
go-back-to-TC-1A fixes.

Required edits before TC-1B:

1. Reconcile the random-trial underpowered threshold (100) with the
   recommended minimum (1000). Same for the permutation side. Pick one
   number as "below this the null is meaningless" and one as "below
   this we still report, but with a low-power flag".
2. Specify the canonical-encoding escape mechanism exactly. One sentence
   is enough (e.g. "precede each reserved character with `\`; the `\` is
   reserved and must itself be escaped as `\\`").
3. Add `validForWitness` and the full field list of `LabelRuleSpec` and
   `CoarseGrainingSpec` to the patch (currently carried by reference to
   v0.3.1). TC-1B should not have to read two patch files to know its
   own type.
4. Add `selectionJustification` non-emptiness to the §6.3 runtime-reject
   list whenever `mode ≠ allStates`.
5. Add `boundary_audit_valid : Bool` to the §13.1 `runtime_validation`
   block, or explicitly document that boundary_audit is human-read
   only.
6. Define "same effective information" for parity/XOR Case 1, or
   narrow Case 1 to "parity / XOR reproduces the witness using a
   function of the same relation records".
7. Add a `metadataTruthDebt_remaining : Bool` (or named-debt list) to
   the JSON schema so the debt named in §6.4 has a home in the report.
8. Decide lint vs. compile for the Go type guardrails and write one
   sentence committing to the choice in §12.

Smallest useful next move:

Open TC-1B as a *specification-only* document. Do not write Go yet.
The first section of TC-1B should be a one-page re-declaration of
LabelRuleSpec, CoarseGrainingSpec, and HistoryEnumerationSpec, with
every field the v0.3.2 patch references by name, so TC-1B is
self-contained. That single move retires the largest remaining
ambiguity in this patch (item 3 above) and unblocks the rest of the
drafting.
