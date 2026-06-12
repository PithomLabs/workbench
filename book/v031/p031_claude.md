---

## EBP v2.1 Workbench Critique — TC-1A v0.3.1

**Critic role:** Workbench reviewer. Not promoting the artifact. Not assessing physics. Assessing patch adequacy as a semantic-boundary repair before TC-1B is drafted.

---

**Overall verdict:**

Genuine improvement over v0.3. The patch moves several critical fields from unexecutable `Prop` to auditable `Bool`, replaces misleading names with procedurally neutral ones, and gives null models concrete pass/fail status codes. These are real gains. However, the patch does not fully close any of its own major stated problems. It relocates several weaknesses rather than eliminating them. The self-reporting Boolean pattern, the `allowedStarts` hand-selection loophole, the undefined null-model thresholds, and the absent sub-schemas in the Go output are specific remaining liabilities. v0.3.1 is a genuine debt-acknowledging patch, not a resolved one. TC-1B may be drafted but not finalized against this patch.

---

**Does v0.3.1 repair the v0.3 weaknesses?**

Partially. The patch converts all four named Props to auditable structures. `canonical : Prop` becomes a `CanonicalRelState` with a concrete encoding procedure (for Go) plus an acknowledged residual `encoding_is_canonical : Prop` on the Lean side. `fixed_before_label : Prop` becomes `CoarseGrainingSpec.fixedBeforeLabel : Bool`. `fixed_before_test : Prop` is subsumed into `LabelRuleSpec.fixedBeforeWitness : Bool`. `generated_by_declared_rule : Prop` becomes `LabelRuleSpec.handPainted : Bool` plus `LabelRuleKind`. The direction of travel is correct. The remaining problem is that converting a `Prop` to a self-reported `Bool` does not eliminate the epistemic gap — it renames it. An actor who would have asserted the `Prop` falsely will assert the `Bool` falsely with equal ease. This is acknowledged nowhere in the patch and is the deepest unfixed structural weakness.

---

**Remaining undefined terms:**

`CoarseAlternatives C h1 h2` — used in the `alternatives_exist` field of `SignedTallyCancellationWitness` (Section 9) but not defined anywhere in this patch. The natural reading is "both histories share a coarse state under Π," but this must be stated explicitly. As written it is an undefined predicate inside a structure that is supposed to be the witness. This is a genuine hole.

`endpoint h` — used in `UnlabeledCount` and `SignedTally` (Section 8) without definition. The intended meaning is the state reached by iterating `R` from `h.start` for `h.length` steps, but this assumption is not stated in this patch and will need to appear in TC-1B or a cited prior artifact.

"stricter review" — mentioned in the `usesCoarseState = true` case (Section 6.2) but entirely procedurally undefined. Who conducts it, on what evidence, by what criteria?

"most" (Section 10.7, permutation null) and "frequent" (Section 10.3, random null) — both are key pass/fail threshold words that are not quantified. The random null correctly states that P(SignedTally = 0) = 1/2 for two independent fair labels, which is useful math. But "frequent" is left undefined as the triggering condition for downgrade. A 40% success rate is frequent. So is 52%. The patch cannot govern what it does not define.

---

**Hidden imports still present:**

`CoarseAlternatives` — origin unspecified; referenced as if defined elsewhere but not cited.

`endpoint` — same status.

`MicroSpace`, `ReversibleUpdate M` — structural carry-forwards from prior TC-1A versions. Acceptable as a family, but TC-1B should cite the version they inherit from.

`Fintype` — Lean Mathlib import; acceptable in context, but TC-1B should name the Mathlib dependency explicitly.

`witnessValue` — defined in Section 6.3 as a local definition, but its use in `SignedTally` (Section 8.2) depends on the claim that mapping labels to integers is "not quantum amplitude." That epistemic claim is asserted but is itself an open debt item (`signedBookkeepingFaithfulnessDebt`). The import here is not code but a philosophical position that is borrowed without resolution.

---

**Terminology assessment:**

`ClassicalCount` → `UnlabeledCount`: repair is genuine. "Classical" was doing theoretical work. "Unlabeled" is descriptive and morally neutral. No overclaim survives the rename.

`SignedCount` → `SignedTally`: better. "Count" implied positive integers. "Tally" does not resist signed values. The risk of confusion with a signed measure is low given the patch's surrounding guardrails. Acceptable.

`NonAdditiveWitness` → `SignedTallyCancellationWitness`: this is the most important rename and it is correct. The original name was actively wrong — the mechanism uses additive integer arithmetic. The new name is accurate and long enough to resist casual paraphrase into physics language. Acceptable.

`SignLabel` → `WitnessLabel`: better. "Sign" was doing amplitude work implicitly. "WitnessLabel" is procedurally neutral. The warning in Section 6.3 that "mapping labels to integers introduces signed bookkeeping" is appropriately placed. Acceptable.

Residual concern: the word "cancellation" in `SignedTallyCancellationWitness` still carries a faint acoustic echo of destructive interference. Given the forbidden-inference list in Section 2.2, this is monitored. It is not a blocking concern but should remain in view at TC-1C and later.

---

**Label-rule and coarse-graining metadata assessment:**

The `LabelRuleSpec` and `CoarseGrainingSpec` structures are genuine improvements over unexecutable Props. The `LabelRuleKind` enumeration including `handPaintedInvalid` as an explicit variant is a useful design: it makes invalid usage nameable rather than simply forgettable. The `LabelRuleAdmissible` and `CoarseGrainingAdmissible` predicates give TC-1B a concrete validity condition to check.

The self-reporting problem is not solved. `handPainted : Bool` and `fixedBeforeWitness : Bool` are declared by the same person constructing the experiment. There is no procedural mechanism — in either the Lean contract or the Go output schema — that enforces or verifies these declarations externally. The patch's admissibility checks test the declared values, not the facts behind them. This is a structural limitation that the patch does not acknowledge and should.

`independentlyJustified : Bool` appears in `CoarseGrainingSpec` but is **not required by `CoarseGrainingAdmissible`**. This is the most consequential gap in this section. Independent justification of Π is the strongest available guard against result-driven coarse-graining. It appears in the metadata but is silently omitted from the enforced conditions. TC-1B should either require it or explain why it is deferred.

The `usesCoarseState = true` warning is noted but "stricter review" remains undefined. This is a promise of a future guardrail, not a guardrail.

---

**History enumeration assessment:**

The `HistoryEnumerationSpec` with `deduplicate = true` is a genuine repair over an unguarded `List`. Required deduplication and exhaustive bounded enumeration from a declared spec are the right structural choices.

The `allowedStarts` hand-selection problem is the primary remaining weakness here. The patch correctly flags `historySelectionObstruction` in the debt section. But the structure of the patch effectively moves the hand-selection surface from the history list to the `allowedStarts` list. Choosing `allowedStarts = {s₁, s₂}` after observing which starts produce the desired witness is functionally indistinguishable from the hand-selection the patch is trying to prevent. The Go output schema does not currently require reporting how `allowedStarts` was chosen. TC-1B should either restrict `allowedStarts` to a principled rule (e.g., all states, or all states reachable from a specified initial state) or flag the choice in the output as a named decision requiring justification.

`maxLength` carries the same problem: choosing a maximum history length after observing which lengths produce the witness is result-driven parameter selection. The patch does not address this.

The extensional history equality definition (`h₁ = h₂ iff start₁ = start₂ ∧ length₁ = length₂`) is sound only if U is deterministic — meaning there is exactly one path from a given start in a given number of steps. For a deterministic bijective update, this is correct. But the patch does not state this assumption explicitly. If U were non-deterministic, start + length would not uniquely identify a history. TC-1B should assert determinism of U as a named premise before relying on this equality.

---

**Null-model criteria assessment:**

The nine null models with named downgrade status codes (`downgrade_to_trivial_counting`, `downgrade_to_endpoint_artifact`, etc.) are a genuine contribution. The random label null's explicit probability calculation (P = 1/2 for two histories) is exactly the right level of rigor for this phase.

Two threshold problems require resolution before TC-1B produces a defensible report:

For the generic permutation null (Section 10.7): "if the witness appears for most generic permutations" — what fraction constitutes "most"? The report format requires `witness_rate`, which is good. But the downgrade rule is triggered by an unspecified threshold. A rate of 55% and a rate of 5% require different interpretations. The patch should specify a threshold (e.g., "if witness_rate > X%, downgrade").

For the random label null (Section 10.3): "if random success frequent" — same problem. Given the known P = 1/2 baseline for two histories, anything near 50% should trigger downgrade, but this is not stated.

Section 14 permits TC-1B to proceed with only the constant-label and endpoint-only nulls implemented. This is reasonable for an initial run, but the report must then explicitly flag that seven null models are pending and that a positive witness under only two nulls carries very limited evidential weight. The current output schema has placeholder objects for all eight null model fields, which is the right structure, but the mandatory reporting of "null models not yet run" should be explicit.

There is no joint null model that tests the interaction of a suspicious label rule and a suspicious Π simultaneously. This is not a blocker for TC-1B but is a gap in the null-model coverage at scale.

---

**Go output schema assessment:**

The top-level schema structure is good. `artifact_status: "toy_check_unpromoted"` and `forbidden_inference_audit` with explicit Boolean flags are the strongest design choices in the entire patch. The debt tracking with `retired`, `remaining`, `new` arrays is excellent and should be retained in all future versions.

Three specific gaps:

First, the sub-schemas for `null_model_results` entries are empty objects `{}`. Each null model result needs a defined sub-schema. At minimum: `run: bool`, `passed: bool`, `status_code: string`, `notes: string`, plus model-specific fields (e.g., `witness_rate: float` for the permutation null, `random_success_rate: float` for the random null). Without defined sub-schemas, TC-1B Go implementations will produce incompatible outputs.

Second, the `histories` array inside `main_witness_result` is unschematized. Each history record should include at minimum: `start_state`, `length`, `endpoint_state`, `label`, `coarse_state`.

Third, there is no field in the main result for `label_rule_admissible: bool` or `coarse_graining_admissible: bool`. If the admissibility checks are defined in the Lean contract, their pass/fail result should appear explicitly in the Go report. A witness that passed all null models but failed the admissibility check is not a valid witness, and the schema should make this impossible to overlook.

---

**Should TC-1B proceed?**

Yes to draft. No to execution against this patch as-is.

TC-1B can be drafted using the structures defined here. The terminology, null-model enumeration, Lean-shaped contracts, and schema skeleton are sufficient to draft a concrete toy-check spec with a real finite state space. Drafting now is appropriate.

TC-1B should not be marked executable until the following four items are resolved: `CoarseAlternatives` is defined, `endpoint` is defined, the Go output sub-schemas for null model results and history records are filled in, and the `allowedStarts` choice rule is either constrained or declared as a named auditable parameter with a justification field in the output.

---

**Required edits before TC-1B is finalized:**

Define `CoarseAlternatives C h1 h2` explicitly — most likely as `C.pi (endpoint h1) = C.pi (endpoint h2)`.

Define `endpoint h` explicitly as iterated application of U.

Add sub-schemas to all null model result fields in the Go output schema.

Add `label_rule_admissible : bool` and `coarse_graining_admissible : bool` fields to the main witness result in the Go output schema.

Constrain or audit `allowedStarts` selection — add either a principled generation rule or a mandatory justification field to the output schema.

State the determinism assumption on U as a named premise for history equality.

Add numerical thresholds to the permutation null and random null downgrade rules.

Require `independentlyJustified = true` in `CoarseGrainingAdmissible` or formally defer it with a named status in the obstruction ledger.

---

**Smallest useful next move:**

Add the following two definitions to TC-1A v0.3.1 as a micro-patch before TC-1B drafts:

```lean
def endpoint {M : MicroSpace} {R : ReversibleUpdate M}
  (h : History M R) : M.State :=
  Nat.iterate R.update h.length h.start

def CoarseAlternatives {M : MicroSpace}
  (C : CoarseGraining M)
  (h1 h2 : History M R) : Prop :=
  C.pi (endpoint h1) = C.pi (endpoint h2)
```

These two definitions close the most urgent undefined-term debt and allow `SignedTallyCancellationWitness` to be syntactically well-formed. Everything else in the required-edits list above is real but can be resolved in TC-1B itself rather than requiring a further patch to TC-1A.

Phase 0 is not solved. The witness is a bookkeeping structure. No physics is claimed.
