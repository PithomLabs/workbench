I'll review TC-1A v0.3.1 under EBP v2.1 discipline. This is a semantic-boundary patch, not a promotion. I will evaluate whether it repairs v0.3 weaknesses and whether TC-1B should proceed.

---

## Overall verdict:

**Partial repair. The patch improves terminology honesty and introduces useful metadata structures, but several critical debts remain unpaid, some new weaknesses appear, and the patch overstates its own readiness. It is a better patch than v0.3, but not yet sufficient for TC-1B drafting without additional constraint.**

---

## Does v0.3.1 repair the v0.3 weaknesses?

**Yes, partially:**

- Terminology is less physics-loaded (`UnlabeledCount`, `SignedTally`, `SignedTallyCancellationWitness` are improvements).
- `canonical : Prop` is replaced with an explicit encoding strategy (though `encoding_is_canonical : Prop` reintroduces the same problem).
- `fixed_before_label : Prop` and `generated_by_declared_rule : Prop` are replaced with structured metadata (`LabelRuleSpec`, `CoarseGrainingSpec`).
- History enumeration now requires `deduplicate = true` and generation from spec.
- Null-model criteria are significantly expanded and more concrete.
- Forbidden inference rules are explicit.
- Go output schema is specified.

**No, critically:**

- `encoding_is_canonical : Prop` is still a `Prop` promise, not an executable check.
- `handPainted : Bool` in `LabelRuleSpec` is self-reported, not auditable.
- `fixedBeforeWitness : Bool` is self-reported.
- Several "admissibility" conditions are `Prop`-based and not enforced by construction.
- The patch claims "ready to draft TC-1B" while `needToyCheck` and multiple origin debts remain explicitly unpaid.

---

## Remaining undefined terms:

| Term | Location | Problem |
|------|----------|---------|
| `MicroSpace` | §8, §9, §12 | No definition provided. What are its fields? What is `M.State`? |
| `ReversibleUpdate` | §8, §9, §12 | No definition. What is `R`? What makes it reversible? |
| `endpoint` | §8 | Used in `UnlabeledCount` and `SignedTally` but never defined. |
| `CoarseAlternatives` | §9 | Used in `SignedTallyCancellationWitness` but never defined. |
| `CanonicalEncoding` | §3.2 | Described in prose but not formalized as Lean/Go function signature. |
| `RelState` | §3.2 | Defined but never connected to `MicroSpace` or `M.State`. |
| `bijection` | §12.1 | Used informally. What is the Lean type? |
| `iteration` | §12.1 | "endpoint is well-defined by iteration" — iteration of what? |
| `S`, `U`, `Π` | §10.7, §14 | Used throughout null models and entry criteria but never defined in this patch. |
| `toy_check_unpromoted` | §13 | Schema status value; not a defined protocol state in EBP v2.1. |
| `future_promotion_debt` | §11.1 | Used in obstruction table but not defined as a formal `DebtItem` or status category. |

**Critical gap:** The patch references `S`, `U`, `Π` extensively in null models and TC-1B entry criteria, but these are undefined. They appear to be carry-overs from v0.3 that the patch assumes the reader knows. Under EBP v2.1 §2.1, entry requires only `owner + claim`, but promotion (and TC-1B drafting) requires inspectable maps. These are not inspectable.

---

## Hidden imports still present:

| Import/Hidden Assumption | Evidence | Severity |
|--------------------------|----------|----------|
| **Amplitude-adjacent intuition** | §6.3: "It is amplitude-adjacent but not quantum amplitude" — the phrase "amplitude-adjacent" smuggles the very physics connection the patch forbids. | High |
| **Time/evolution ontology** | §12.1: "endpoint is well-defined by iteration" assumes a temporal/sequential structure without defining iteration rule. | High |
| **State-space finiteness** | `Fintype CoarseState` in §7.2 assumes finite coarse state space, but `M.State` finiteness is never stated. | Medium |
| **Equality on histories** | §5.2: "h₁ = h₂ iff start₁ = start₂ and length₁ = length₂" assumes histories are fully determined by start and length, ignoring path structure. If `R` is deterministic, this holds; if not, it doesn't. The patch never states determinism. | High |
| **Integer arithmetic as natural** | §8.2: `foldl (acc + witnessValue ...)` assumes integer summation is the natural combination rule. The `whySummationDebt` acknowledges this but doesn't resolve it. | Medium |
| **"Downgrade" ontology** | §10 null-model results use `downgrade_to_*` statuses. These are not defined in EBP v2.1. What does "downgrade" mean operationally? Does it unpromote? Add debt? Modify the idea? | Medium |
| **Quantum interference as the implicit target** | Throughout: The patch repeatedly forbids "quantum interference" claims, but this very repetition reveals the implicit target. The null models are designed to rule out classical explanations *of a quantum-like phenomenon*. This is not a hidden import of physics, but it is a hidden import of *intent* — the witness is designed to look like something quantum-adjacent while denying it. | High |

---

## Terminology assessment:

### `ClassicalCount` → `UnlabeledCount`: **Better.**
- "Unlabeled" accurately describes the operation (counting without witness labels).
- Removes the "classical" physics loading.
- **Remaining issue:** "Count" still sounds like a measure. "Tally" would be more honest, but the distinction between `UnlabeledCount` (Nat) and `SignedTally` (Int) is clear.

### `SignedCount` → `SignedTally`: **Better.**
- "Tally" is bookkeeping-language, not measure-language.
- Explicitly finite and combinatorial.
- **Remaining issue:** The type is `Int`, which is signed integer arithmetic. The patch acknowledges this is "not algebra-neutral" but doesn't provide an alternative. The debt is noted but not retired.

### `NonAdditiveWitness` → `SignedTallyCancellationWitness`: **Better, but problematic.**
- More descriptive of the mechanism.
- "Cancellation" is accurate for `+1 + (-1) = 0`.
- **Remaining issue:** The name is very long and still contains "Witness," which in EBP v2.1 §6.5 (obstruction work) suggests evidence of something. The patch forbids calling this "quantum interference," but "cancellation witness" still implies something was witnessed. "SignedTallyZeroEvent" would be more neutral.

### `SignLabel` → `WitnessLabel`: **Adequate.**
- Removes "sign" which sounds like amplitude sign.
- "WitnessLabel" is finite and test-oriented.
- **Remaining issue:** "Witness" still implies evidential status. "TestLabel" or "BookkeepingLabel" would be more honest.

### Overall: **Moderate improvement.** The terms are less physics-loaded but retain some evidential framing. The patch does not fully escape the gravitational pull of the quantum-adjacent intent.

---

## Label-rule and coarse-graining metadata assessment:

### Label-rule metadata (`LabelRuleSpec`):

**Strengths:**
- `handPainted : Bool` makes the concern explicit.
- `usesTargetOutcome : Bool` prevents result-driven labeling.
- `fixedBeforeWitness : Bool` addresses temporal ordering.
- `validForWitness : Bool` bundles admissibility.

**Weaknesses:**
- `handPainted : Bool` is **self-reported**. A malicious or careless theorist can set `handPainted = false`. There is no mechanism to audit this.
- `fixedBeforeWitness : Bool` is also self-reported. Same problem.
- `LabelRuleAdmissible` is a `Prop`. Under EBP v2.1 §4, `Prop` fields are acceptable for theorem obligations, but for promotion, these need to be checkable or constructible. The patch provides no way to verify `fixedBeforeWitness` or `handPainted`.
- `randomLabel` in `LabelRuleKind` is interesting but undefined. What distribution? What seed? Who draws?
- `other` in `LabelRuleKind` is an escape hatch. Any rule can claim `other` and bypass classification.

**Verdict:** The metadata is a better discipline marker than v0.3's bare `Prop`s, but it is still **trust-based, not enforcement-based**. The patch does not solve the hand-painting problem; it only makes the problem visible.

### Coarse-graining metadata (`CoarseGrainingSpec`):

**Strengths:**
- `fixedBeforeLabel : Bool` addresses the selection-timing concern.
- `usesWitnessLabel : Bool` prevents circular coarse-graining.
- `usesTargetOutcome : Bool` prevents result-driven coarse-graining.
- `independentlyJustified : Bool` is a useful discipline marker.

**Weaknesses:**
- All `Bool` fields are self-reported. Same trust problem as label metadata.
- `independentlyJustified : Bool` is particularly vague. Justified by what? To whom?
- `CoarseGrainingAdmissible` is a `Prop` with no enforcement mechanism.
- The patch states: "A coarse-graining may be simple, but it must not be selected after the desired witness is known." True, but **how is this enforced?** The metadata records the intent, not the history of selection.
- §7.3 notes `coarseSelectorObstruction` and `coarsePaintingObstruction`, but these are filed as debts, not resolved.

**Verdict:** The metadata prevents *careless* result-driven `Π`, but not *malicious* result-driven `Π`. For a toy check at Phase 0.0, this may be acceptable, but the patch should not claim this debt is retired. It is only partially addressed.

---

## History enumeration assessment:

**Strengths:**
- `HistoryEnumerationSpec` with `allowedStarts`, `maxLength`, `deduplicate` is concrete.
- `deduplicate = true` is required, preventing duplicate-history inflation.
- Generation from spec rather than hand-selection is mandated.
- Extensional equality (`start` + `length`) is explicit.

**Weaknesses:**
- `allowedStarts : List M.State` is **still a hand-selected list**. The patch forbids "hand-selected histories" but allows "hand-selected starting states." If `allowedStarts` is chosen after the desired witness is known, the same manufacturing problem exists.
- No constraint on how `allowedStarts` is chosen. Is it all of `M.State`? A random subset? A principled subset?
- History equality is extensional by `start` and `length` only. If `R` is non-deterministic or if histories have internal structure (branching, relations), two histories with same start and length may differ. The patch assumes `History` is fully determined by `(start, length)`, which assumes deterministic update.
- `maxLength : Nat` is arbitrary. Why that length? The patch provides no guidance.
- The debt section (§5.3) lists `historySelectionObstruction` and `duplicateHistoryObstruction`, but the repair only addresses duplicates, not selection.

**Verdict:** The patch improves on v0.3 by preventing duplicate counting, but it **does not prevent hand-selected starting states**, which is the deeper problem. The history enumeration is better but not fully constrained.

---

## Null-model criteria assessment:

**Significant improvement over v0.3.** The patch specifies 9 null models with concrete pass/fail criteria and result statuses.

**Strengths:**
- Constant label, endpoint-only label, random label, identity coarse-graining, constant coarse-graining, generic permutation, parity/XOR, and cycle-length nulls cover a wide space.
- Random label null requires distributional reporting (trials, success rate, seed).
- Generic permutation null requires rate reporting.
- Hand-painted label is explicitly rejected as "invalid success."
- Result statuses are concrete (`downgrade_to_*`).

**Weaknesses:**
- **Result statuses are undefined.** What does `downgrade_to_trivial_counting` mean operationally? Does it add debt? Unpromote? Modify the artifact? The patch uses these as if they are EBP v2.1 states, but they are not.
- **No threshold for "frequent" random success.** §10.3 says "if random success frequent" but doesn't define frequent. 1/2 for two histories is stated, but for larger spaces, what's the threshold?
- **Generic permutation null is expensive.** How many permutations? All of them? A sample? The patch says "permutations_tested" in Go output but doesn't specify minimum.
- **Parity/XOR null criterion is vague.** "If XOR/parity reproduces the witness" — what does "reproduces" mean? Exact match? Same qualitative behavior?
- **Cycle-length null assumes cyclic structure.** What if `U` is not cyclic? This null may be inapplicable without a check.
- **No null model for the summation rule itself.** The patch notes `whySummationDebt` but doesn't test whether alternative combination rules (e.g., min/max, XOR, product) also produce cancellation.

**Verdict:** The null-model criteria are **strong enough for a toy-check spec**, but they need operational definitions for result statuses and thresholds. They do not fully prevent result-driven interpretation, but they make it much harder.

---

## Go output schema assessment:

**Strengths:**
- JSON schema is explicit and structured.
- `artifact_status` enforces "toy_check_unpromoted."
- `forbidden_inference_audit` with explicit booleans is excellent discipline.
- `debt` section with `retired`, `remaining`, `new` aligns with EBP v2.1 living ledger.
- `instance_spec` captures all parameters for reproducibility.

**Weaknesses:**
- `schema_version` is `"tc-1b-go-report-v0.1"` — versioned but not linked to EBP v2.1 protocol version.
- `artifact_status` value `"toy_check_unpromoted"` is not an EBP v2.1 defined state. EBP v2.1 uses `alive`, `promoted`, `dormant`. The patch invents a new status without defining its relationship to EBP states.
- `null_model_results` has empty objects `{}` for each null. No sub-schema is provided. What fields must each null model result contain?
- `main_witness_result.histories` is a list but no element schema is provided.
- `distributional_summary` is at top level but seems to only apply to random label null. Why is it not under `null_model_results.random_label`?
- No field for `owner` or `born` timestamp, which are mandatory in EBP v2.1 §2.1.
- No field for `source` or `notes`.
- No field for EBP `DebtItem` enum values; `debt.retired` and `debt.remaining` are untyped lists.

**Verdict:** The schema is **a good start but insufficient for a complete artifact record**. It needs sub-schemas for null model results, history elements, and alignment with EBP v2.1 core structures. It should not invent new status values without definition.

---

## Should TC-1B proceed?

**Conditional yes for drafting, no for execution.**

The patch has improved terminology, added useful metadata, expanded null models, and specified a Go output schema. These are genuine repairs.

However, **TC-1B execution should not proceed** until:

1. `MicroSpace`, `ReversibleUpdate`, `endpoint`, `CoarseAlternatives`, `S`, `U`, `Π` are defined.
2. `encoding_is_canonical : Prop` is replaced with an executable canonical encoding or a theorem obligation with a proof sketch.
3. Self-reported `Bool` fields (`handPainted`, `fixedBeforeWitness`, `fixedBeforeLabel`) have audit mechanisms or are replaced with construction-based guarantees.
4. `allowedStarts` selection is constrained (e.g., must be all states, or random with seed, or justified by independent criterion).
5. Null-model result statuses are defined operationally.
6. Go output schema sub-structures are specified.
7. `artifact_status` values are aligned with EBP v2.1 states or explicitly extended with definitions.

---

## Required edits before TC-1B:

| # | Edit | Priority |
|---|------|----------|
| 1 | Define `MicroSpace`, `ReversibleUpdate`, `endpoint`, `CoarseAlternatives` in Lean-shaped code. | Critical |
| 2 | Define `S`, `U`, `Π` or explain they are parameters to be instantiated in TC-1B. | Critical |
| 3 | Replace `encoding_is_canonical : Prop` with executable `canonicalEncoding` function or theorem stub with proof obligation. | High |
| 4 | Add audit mechanism for `handPainted` and `fixedBeforeWitness` (e.g., require hash of rule source code, or require rule to be from closed enumerable family). | High |
| 5 | Constrain `allowedStarts` selection in `HistoryEnumerationSpec` (e.g., add `selectionRule` field with options: `allStates`, `randomSubset`, `independentCriterion`). | High |
| 6 | Define operational meaning of `downgrade_to_*` statuses (map to EBP debt actions). | Medium |
| 7 | Specify sub-schema for each null model result in Go output. | Medium |
| 8 | Add `owner`, `born`, `source` fields to Go output schema per EBP v2.1 §2.1. | Medium |
| 9 | Align `artifact_status` with EBP v2.1 states or define extension formally. | Medium |
| 10 | Add null model for alternative combination rules (address `whySummationDebt`). | Low |

---

## Smallest useful next move:

**Define `MicroSpace` and `ReversibleUpdate` with minimal fields, and specify `endpoint` as iteration of the update rule.**

This is the foundational dependency for everything else. Without knowing what a micro-space is and what makes an update reversible, the rest of the patch floats on undefined terms.

Specifically:

```lean
structure MicroSpace where
  State : Type
  [finiteState : Fintype State]
  -- What else? Relations? No, relations are in RelState.
  -- Is MicroSpace just a finite type? If so, say so.

structure ReversibleUpdate (M : MicroSpace) where
  step : M.State -> M.State
  involutive : ∀ s : M.State, step (step s) = s  -- or bijective?
```

And:

```lean
def endpoint {M : MicroSpace} {R : ReversibleUpdate M} (h : History M R) : M.State :=
  -- iteration of R.step h.length times starting from h.start
```

This one move unlocks the ability to evaluate whether the rest of the patch is coherent.

---

**Final note:** This patch is a genuine improvement. The terminology is more honest, the metadata is more structured, and the null models are more comprehensive. But it still contains self-reported fields masquerading as enforcement, undefined core terms, and an overclaim of readiness. Treat it as **progress on debt, not debt retirement**.
