Good. Now the EBP kernel:Now I have everything I need. Let me produce the full Workbench review.

---

```text
─────────────────────────────────────────────────────────────────
WORKBENCH REVIEW — TC-1A v0.3.2 under EBP v2.1
Artifact: "TC-1A v0.3.2 — Definition and Enforcement Patch"
Reviewer role: critic / gap auditor (not promoter)
─────────────────────────────────────────────────────────────────

Overall verdict:
  TC-1A v0.3.2 closes the majority of the v0.3.1 gaps and is a
  genuine semantic improvement. It does not overclaim. It does not
  promote. It retains correct debt posture throughout.
  Six residual issues remain. Four of them would block Go
  implementation without further edits; none blocks spec-drafting.
  Status: alive / clarified / unpromoted / conditionally ready to
  draft TC-1B spec (not yet ready to implement TC-1B in Go).

─────────────────────────────────────────────────────────────────

Does v0.3.2 close the v0.3.1 gaps?
  Mostly. Ten of the listed cracks are repaired at the definitional
  level. Six residual issues survive into the patch (detailed below).
  None is a fatal defect; four are Go-implementation blockers.

─────────────────────────────────────────────────────────────────

Remaining undefined terms:
  1. "same effective information" (§10.3, Case 1) — used to assign
     `downgrade_to_classical_parity_artifact` but not operationalized.
     No Go-computable criterion is given for what counts as equivalent
     information content between parity/XOR and the main mechanism.

  2. "declared substrate mechanism" (§10.3, Case 2) — used to
     distinguish Case 2 from Case 1, but "substrate mechanism" is
     neither defined in this patch nor carried forward from v0.3.1
     with an explicit pointer. The Go case-selection logic cannot be
     implemented without this.

  3. `ArgOrder` (§5.2 Go function) — referenced in the encoding
     error condition ("If ArgOrder is unknown: return error") but not
     defined or imported in this patch. Presumably lives in TC-1A
     v0.3.1; needs an explicit carry-forward definition here.

  4. `CoarseGraining M` and `RelState` (§4.2 and §5.1) — both
     are referenced as known types but are not re-stated in the
     carry-forward definitions (§2). A TC-1B implementer reading
     only v0.3.2 cannot reconstruct them.

─────────────────────────────────────────────────────────────────

Remaining hidden imports:
  - `Nat.iterate` is invoked in §3 without Lean import or namespace
    declaration. This is a Mathlib function. If TC-1B Lean requires
    it, the import must be made explicit; if it is being used only as
    pseudocode, that should be stated clearly.
  - The encoding escape rule in §5.2 states "escape reserved
    characters" with the character list, but the escape *convention*
    (backslash? percent-encoding? doubling?) is not specified. This
    is a hidden import of a convention that must be chosen and named.
  - `CoarseGrainingAdmissible` in §7.2 references `CoarseGraining M`
    which carries `pi : M.State -> CoarseCell` — `CoarseCell` is
    never defined in this patch.

─────────────────────────────────────────────────────────────────

Endpoint / CoarseAlternatives assessment:
  ENDPOINT — CLOSED.
  §3 gives a precise Lean definition: `Nat.iterate R.U h.length
  h.start`. The plain-English restatement and the Go pseudocode are
  consistent with the Lean form. This gap is retired.
  Residual: `Nat.iterate` import needed in Lean context (see above).

  COARSEALTERNATIVES — SUBSTANTIALLY CLOSED. ONE RESIDUAL.
  §4 defines: `h1 ≠ h2 ∧ C.pi (endpoint h1) = C.pi (endpoint h2)`.
  The definition is correct and the forbidden-inference list is a good
  guardrail. Residual: `History M R` is a structure with `start` and
  `length` fields, but the patch does not add `deriving DecidableEq`
  to `History`. In Lean, `h1 ≠ h2` requires a decision procedure;
  in Go it would require field-by-field equality comparison. Neither
  is blocked, but the Lean side needs the annotation added. Small fix.

─────────────────────────────────────────────────────────────────

Canonical encoding assessment:
  SUBSTANTIALLY IMPROVED. TWO IMPLEMENTATION GAPS REMAIN.

  The format `RS|nodes=N|rels=r1;r2;...` and the relation-record
  structure are well-specified. The sort rule (lexicographic on
  encoded string), the node-count inclusion, and the argument-order
  rules are concrete enough to code from.

  Gap 1 — Escape convention not named. The list of reserved
  characters is given (| ; / ( ) , \) but the escape mechanism is
  not. Two implementations could produce different encodings for the
  same RelState if one uses backslash-escape and the other uses
  percent-encoding. This breaks the "deterministic and reproducible"
  requirement stated in §5.2. One sentence needed: specify the
  escape convention by name or by example.

  Gap 2 — "Sort arguments numerically" is underspecified. The
  example uses integer node identifiers (0, 1, 2), and the rule
  makes sense for that case. But the patch does not explicitly say
  nodes are identified by non-negative integers in the canonical
  encoding. If node identifiers could be strings or opaque types,
  "numerically" is meaningless. Recommend: add "Nodes are identified
  by their zero-indexed position in a fixed enumeration of M.State."

  fullGraphIsomorphismDebt is honestly retained. No complaint.

─────────────────────────────────────────────────────────────────

Metadata enforcement assessment:
  WELL HANDLED. BEST SECTION IN THE PATCH.

  §6.2's explicit statement — "Bool metadata records declared
  discipline. It does not prove historical fact." — is exactly the
  right framing and is EBP-safe. The `metadataTruthDebt` is named
  correctly. The list of debt-reduction mechanisms (pre-registration,
  git timestamps, locked configs, report hashes) is practical and
  honest without being bureaucratic.

  §6.3 gives a Go-executable rejection list. All eight conditions are
  concrete boolean comparisons. This is implementable.

  ONE REMAINING GAP: what happens to the run when runtime validation
  fails? The patch gives the status string `invalid_by_declared_
  metadata` but does not specify whether execution:
    (a) aborts immediately and produces no witness result, or
    (b) continues but marks the entire report as invalid.
  For TC-1B Go, this decision must be explicit. Recommend: abort and
  emit a minimal report with only the `runtime_validation` block and
  no witness fields.

─────────────────────────────────────────────────────────────────

History selection assessment:
  SUBSTANTIALLY IMPROVED. ONE LOGICAL GAP.

  The `StartSelectionMode` inductive type is a good addition. The
  `allStates` / `declaredSubset` / `singleDeclaredStart` /
  `invalidHandSelected` taxonomy closes the v0.3.1 hand-selection
  loophole at the declarative level.

  `maxLength` fix is correct in principle: fixing it before witness
  evaluation and recommending orbit period or |S| as the default
  value.

  Gap — `mode = allStates` is not validated against `allowedStarts`.
  A run could declare `mode = allStates` while supplying a shorter
  list. The patch does not say Go must ignore `allowedStarts` when
  `mode = allStates` and enumerate `M.State` directly. Without this
  rule, the mode field is just another self-reported declaration (same
  `metadataTruthDebt` problem, but avoidable here). Recommended fix:
  "When `mode = allStates`, Go must enumerate all states in `M.State`
  directly. The `allowedStarts` field is ignored."

  `selectionJustification : String` is an honest declaration field.
  The patch does not try to make it machine-verifiable, which is
  correct. No complaint.

─────────────────────────────────────────────────────────────────

Null-model threshold assessment:
  THRESHOLDS ARE REASONABLE AS FIRST-PASS AUDIT RULES.
  `thresholdJustificationDebt` is correctly retained.

  For the random-label null: P(random success) ≈ 0.5 for a
  two-history witness under uniform random labeling. A downgrade
  threshold of >= 0.25 means the witness must succeed at less than
  half the random-baseline rate to survive. This is conservative and
  appropriate. The consequence is that nearly all simple two-history
  witnesses will be downgraded on this null, which is the correct
  behavior at this stage.

  For the generic-permutation null: >= 0.10 threshold is defensible
  as a first pass. The 10% bar means the mechanism must be present
  in fewer than 1 in 10 bijections to avoid downgrade.

  ONE INTERNAL INCONSISTENCY: the random null recommends a minimum of
  1000 trials before the result is "powered," but the permutation null
  flags "underpowered" only below 100. This asymmetry is unexplained.
  For consistency, either raise the permutation minimum to match (1000
  or full enumeration), or add a sentence justifying why 100 is
  sufficient for the permutation null while 1000 is needed for random.

─────────────────────────────────────────────────────────────────

Parity/XOR status assessment:
  THREE STATUSES ARE CLEAR AND EBP-SAFE. TWO TERMS UNIMPLEMENTABLE.

  The three-case taxonomy (full downgrade / survives with debt /
  survived) correctly prevents overclaiming at all levels. The
  forbidden-claim language in each case is appropriate.

  Gap 1 — "Same effective information" (Case 1 trigger) has no
  operationalization. In Go, the parity/XOR checker needs a concrete
  rule to decide which case applies. Without it, Case 1 vs Case 2
  is a judgment call the implementer must make ad hoc, which is a
  new hand-selection loophole introduced at the null-model level.

  Gap 2 — "Declared substrate mechanism" (Case 2 condition) is
  not defined. Until it is, Case 2 cannot be distinguished from
  Case 1 in code or in review.

  Recommended fix: For TC-1B's toy system, define both terms
  concretely. Example: "same effective information = parity/XOR
  uses only endpoint parity, not history-path information";
  "substrate mechanism = the specific RelState-to-WitnessLabel
  function defined by LabelRuleSpec."

─────────────────────────────────────────────────────────────────

U(1) / phase boundary assessment:
  SUFFICIENT FOR TC-1B. NO GAPS.

  §11's boundary audit checklist is a clean, minimal, correct
  treatment. All fields are boolean, all initialized to false, and
  the JSON schema is reproduced in §13.2. The `u1ExtensionDebt` is
  correctly labeled as a later-phase obligation, not a TC-1B blocker.

  The two-label embedding into U(1) is acknowledged but explicitly
  not claimed. This is good EBP posture: naming the extension
  possibility without using it is the right boundary behavior for
  a Phase 0 toy check.

─────────────────────────────────────────────────────────────────

Go type-guardrail assessment:
  ADEQUATE FOR PREVENTING THE WORST CONFUSIONS.
  TWO MINOR RESIDUAL GAPS.

  The critical prohibition — `Probability ≠ SignedTally`,
  `Amplitude ≠ SignedTally` — is explicit and correct. The
  `WitnessLabel` typed constant set (Plus / Minus) prevents free
  integer assignment. The `UnlabeledCount` / `SignedTally` split
  is a useful operational distinction.

  Gap 1 — `WitnessStatus` and `NullModelStatus` are typed as
  `string`. In Go, this does not prevent arbitrary string assignment.
  A set of typed constants should be defined (e.g., `const
  WitnessFound WitnessStatus = "witness_found"`). Without this,
  the type names are documentation, not enforcement.

  Gap 2 — No type is defined for `CoarseCell` (the output of `Π`).
  If the coarse projection maps `M.State -> CoarseCell`, TC-1B needs
  a Go type for coarse cells, otherwise the `CoarseAlternatives`
  check degenerates to comparing untyped interface values.

─────────────────────────────────────────────────────────────────

JSON report schema assessment:
  FOUR USEFUL NEW SECTIONS. TWO MISSING FIELDS.

  The four new schema blocks (runtime_validation, boundary_audit,
  null_model_power, selection_audit) are well-formed and concrete.
  The field names are consistent with the text.

  Missing field 1 — Parity/XOR status. §10 defines three named
  statuses but §13 adds no schema field to record which status was
  assigned. TC-1B's report will have no canonical place to emit
  the parity null result. A `parity_null_status` field is needed.

  Missing field 2 — `independentlyJustified` downgrade. §7.2
  defines `witness_found_with_coarse_graining_selection_debt` as
  a named downgrade status, but §13 has no schema field for it.
  A `coarse_graining_independence_status` field should be added.

  Missing field 3 (minor) — No schema version field. If the report
  schema changes between TC-1B and TC-1C, version-less reports
  become ambiguous. Recommend adding `"schema_version": "TC-1B-1"`.

─────────────────────────────────────────────────────────────────

independentlyJustified inconsistency (criterion 6, expanded):
  A LOGICAL INCONSISTENCY EXISTS. REQUIRES RESOLUTION BEFORE Go.

  §7.2 updates `CoarseGrainingAdmissible` to require
  `independentlyJustified = true`. This means a coarse-graining
  with `independentlyJustified = false` fails admissibility.

  But §6.3's runtime rejection table does not list
  `independentlyJustified = false` as an invalid condition. It
  only appears in §7.2 as a downgrade (not a rejection).

  These are logically incompatible. If `CoarseGrainingAdmissible`
  requires it, then `false` means inadmissible — which should
  produce `invalid_by_declared_metadata`. If `false` only produces
  a downgrade, then the admissibility predicate should not require it.

  One of these must be corrected:
    Option A: Add `independentlyJustified = false` to the §6.3
              rejection list (treat it as invalid, not downgraded).
    Option B: Remove `independentlyJustified = true` from
              `CoarseGrainingAdmissible` and define a separate
              downgrade predicate that checks it.
  Option B is preferred: it preserves the three-outcome structure
  (invalid / downgraded / clean) without inflating the invalid list.

─────────────────────────────────────────────────────────────────

Should TC-1B be drafted next?
  YES — draft TC-1B spec.
  NO — do not implement TC-1B in Go yet.
  NO — do not promote any result.

  "Draft TC-1B spec" is safe now. The core structures (`endpoint`,
  `CoarseAlternatives`, metadata fields, history modes, null-model
  thresholds, boundary audit, type guardrails) are defined at
  sufficient precision to write the specification. The six residual
  issues are small enough that they can be resolved inline during
  spec drafting without requiring a v0.3.3 patch.

  "Implement TC-1B in Go" requires first resolving the four
  Go-blocking issues listed below.

─────────────────────────────────────────────────────────────────

Required edits before TC-1B Go implementation:

  [G-1] Escape convention: name the exact escape rule for reserved
        characters in canonical encoding (e.g., "backslash-escape
        with \\ for backslash itself").

  [G-2] Node identifier assumption: state explicitly that nodes are
        zero-indexed integers in canonical encoding, or specify how
        non-integer node labels are ordered.

  [G-3] Parity case operationalization: define "same effective
        information" and "substrate mechanism" concretely in terms
        of TC-1B's specific LabelRuleSpec and RelState types.

  [G-4] Runtime validation outcome: specify that a validation failure
        aborts execution and emits a minimal invalid report, with no
        witness fields populated.

  [G-5] `mode = allStates` enforcement: add a rule that Go must
        enumerate M.State directly when mode = allStates, ignoring
        the `allowedStarts` list.

  [G-6] `independentlyJustified` inconsistency: adopt Option B —
        remove it from `CoarseGrainingAdmissible` and handle it via
        a separate downgrade predicate with a named schema field.

  Required schema additions before Go:
  [S-1] `parity_null_status` field in report.
  [S-2] `coarse_graining_independence_status` field in report.
  [S-3] `schema_version` field in report.

  Required Lean annotation:
  [L-1] Add `deriving DecidableEq` to `History M R`.
  [L-2] Add `import Mathlib.Data.Nat.Basic` or equivalent for
        `Nat.iterate`, or mark it as pseudocode only.

─────────────────────────────────────────────────────────────────

Smallest useful next move:
  WRITE TC-1B SPEC DRAFT.
  Include a §0 "Carry-Forward Definitions" section that re-states
  RelState, CoarseGraining M, CoarseCell, and ArgOrder explicitly.
  Resolve [G-6] (the independentlyJustified inconsistency) in the
  draft — it is the only logical contradiction in v0.3.2 and it
  costs one sentence to fix.
  Mark [G-1], [G-2], [G-3] as open TC-1B-spec debt items to be
  resolved in the same draft before any Go implementation begins.
  Do not instantiate S, U, or Π until the spec is complete.

─────────────────────────────────────────────────────────────────
```
