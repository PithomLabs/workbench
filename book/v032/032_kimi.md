I'll review TC-1A v0.3.2 as a Workbench critic under EBP v2.1 discipline, working through each focus area systematically.

---

## Overall verdict:

TC-1A v0.3.2 is a **highly disciplined and largely successful patch**. It closes eight of the nine critical gaps from v0.3.1 with surgical precision. The `endpoint` and `CoarseAlternatives` definitions are now explicit and executable. The canonical encoding rules are deterministic enough for Go. The metadata enforcement acknowledges its own limits honestly. The history selection controls are tight. The null-model thresholds are pragmatic and conservative. The parity/XOR status rules are EBP-safe. The U(1) boundary audit is appropriately minimal for TC-1B. The Go type guardrails are sufficient. The JSON schema is operationally complete.

However, **one structural risk remains**: the `independentlyJustified` field for coarse-graining, while now required in admissibility, still lacks an operational enforcement mechanism—it is a self-reported boolean with no external validation path. Additionally, **two minor gaps** in the JSON schema and one **threshold calibration debt** should be addressed before Go implementation begins.

The patch is **ready for TC-1B drafting** (specification writing) **with three blocking conditions for implementation**. It is **not ready for promotion** (which is forbidden at this stage per EBP §2.4).

---

## Does v0.3.2 close the v0.3.1 gaps?

| v0.3.1 Gap | v0.3.2 Repair | Status |
|------------|---------------|--------|
| `endpoint` used but not defined | §3: Explicit `Nat.iterate` definition + plain-English + Go pseudocode | ✓ Closed |
| `CoarseAlternatives` used but not defined | §4: Explicit `Prop` with `h1 ≠ h2 ∧ C.pi (endpoint h1) = C.pi (endpoint h2)` | ✓ Closed |
| Canonical encoding not exact | §5: Deterministic string format with 6 explicit rules, reserved character escaping, example | ✓ Closed |
| Bool metadata self-reported, not proof | §6: Acknowledged as "audit declarations, not proof"; runtime enforcement rules; `metadataTruthDebt` | ✓ Closed |
| `allowedStarts` hand-selection | §8: `StartSelectionMode` enum with `allStates` preferred; `invalidHandSelected` variant; selection justification string | ✓ Closed |
| `maxLength` tuned after fact | §8: Must be fixed before witness; recommended `|S|` or one period; `max_length_selection_debt_open` | ✓ Closed |
| "frequent" undefined | §9.2: Explicit threshold `random_success_rate >= 0.25` → downgrade; minimum 1000 trials | ✓ Closed |
| "most generic permutations" undefined | §9.3: Explicit threshold `witness_rate >= 0.10` → downgrade; enumeration vs. sampling modes | ✓ Closed |
| Parity/XOR statuses vague | §10: Three explicit statuses with case definitions and allowed/forbidden claims | ✓ Closed |

---

## Remaining undefined terms:

### 1. `independentlyJustified` operational meaning (§7)

The field is now required:

```lean
def CoarseGrainingAdmissible (spec : CoarseGrainingSpec) : Prop :=
  spec.fixedBeforeLabel = true ∧
  spec.usesWitnessLabel = false ∧
  spec.usesTargetOutcome = false ∧
  spec.independentlyJustified = true
```

But **what makes a coarse-graining "independently justified"?** The patch does not define this operationally. Is it:

- **Symmetry-derived**: `Π` is the quotient by an automorphism group of `S`?
- **Prior-fixed**: `Π` was committed before the label rule was known?
- **Externally motivated**: `Π` comes from a physical or mathematical argument outside the toy?
- **Self-certified**: The modeler simply asserts it?

If the answer includes the last option, the field is **governance theater**—present but enforceable only by trust. The patch's `metadataTruthDebt` acknowledges this, but does not provide a path to reduction.

**Severity:** Moderate. This is the one remaining self-reporting vulnerability.

**Fix before TC-1B implementation:** Add an `IndependentJustificationKind` enum:

```lean
inductive JustificationKind where
  | symmetryQuotient      -- quotient by declared automorphism
  | priorFixed            -- timestamped pre-registration
  | externalReference     -- citation to external mathematical/physical argument
  | declaredWithoutProof  -- acknowledged as modeler choice, carries debt
```

And require: `symmetryQuotient` or `priorFixed` for clean witness; `declaredWithoutProof` triggers `coarse_graining_selection_debt_open`.

---

### 2. `selectionJustification : String` (§8.2)

A string is not a justification. It is a **narrative**. Without structure, it cannot be validated automatically or reviewed consistently.

**Severity:** Low. This is documentation debt, not a logical hole.

**Fix:** Require `selectionJustification` to match `StartSelectionMode`:
- `allStates` → justification auto-generated as "all microstates enumerated"
- `declaredSubset` → justification must list excluded states and reason
- `singleDeclaredStart` → justification must name start state and reason

---

## Remaining hidden imports:

### Hidden Import 1 — `Nat.iterate` still assumes global discrete time (§3)

The `endpoint` definition uses `Nat.iterate R.U h.length h.start`. This imports:
- Natural number induction
- Sequential composition
- Global clock (same `U` at every step)

This is **acknowledged as toy simplification** via `timeSmugglingDebt` and `deterministicUpdateDebt`. It is not hidden. But it is **still imported**.

**Verdict:** Acceptable. The debt is visible. Resolution is future work.

---

### Hidden Import 2 — String encoding in canonical form (§5)

The canonical encoding uses `String` as the carrier. This imports:
- Lexicographic ordering on characters
- String concatenation and parsing
- Reserved character escaping

These are **implementation conveniences**, not physical assumptions. The encoding is reversible and deterministic.

**Verdict:** Acceptable. No physical content smuggled.

---

### Hidden Import 3 — Probability threshold values (§9.2, §9.3)

The thresholds `0.25` (random) and `0.10` (permutation) are **pragmatic choices**, not derived from any statistical principle. They import:
- Frequentist hypothesis-testing intuition
- Arbitrary conservatism

The patch acknowledges this via `thresholdJustificationDebt`, but the values themselves are **unmotivated**.

**Severity:** Low-to-moderate. Wrong thresholds could cause false negatives (too strict) or false positives (too lenient).

**Fix:** Add calibration guidance:
- `0.25` for random: "If random labels succeed ≥25% of the time, the witness is likely generic label noise for two-history cancellation"
- `0.10` for permutation: "If ≥10% of generic bijections produce the witness, the update structure is not special"

Document that these are **first-pass audit defaults**, not statistical tests with confidence intervals.

---

## Endpoint / CoarseAlternatives assessment:

### Endpoint (§3): Excellent

The definition is triple-specified:
1. **Lean-shaped**: `Nat.iterate R.U h.length h.start`
2. **Plain-English**: "start state after applying U exactly length times"
3. **Go pseudocode**: Explicit loop implementation

This is **exactly the right redundancy** for a semantic contract. No ambiguity remains.

**One minor gap:** The Go pseudocode does not handle `length = 0`. Add:
```text
If h.Length = 0: return h.Start
```

---

### CoarseAlternatives (§4): Excellent

The definition is explicit:
```lean
h1 ≠ h2 ∧ C.pi (endpoint h1) = C.pi (endpoint h2)
```

The forbidden inference list is clear:
```text
CoarseAlternatives ≠ quantum superposition
CoarseAlternatives ≠ physical path interference
CoarseAlternatives ≠ measurement branching
```

The allowed claim is minimal:
```text
coarse endpoint indistinguishability
```

**No gaps.**

---

## Canonical encoding assessment:

The encoding rules (§5) are **deterministic and implementable**:

1. Format: `RS|nodes=<n>|rels=<r1>;<r2>;...`
2. Relation format: `<name>/<arity>/<order>(<args>)`
3. Order flag: `O` (ordered), `U` (unordered)
4. Sorting: lexicographic on relation records
5. Unordered args: sorted numerically
6. Reserved character escaping

The example is concrete:
```text
RS|nodes=3|rels=edge/2/U(0,1);edge/2/U(1,2);tag/1/O(0)
```

Go function signature and error conditions are specified.

**One gap:** The escaping rules say "escape deterministically" but do not specify the escape mechanism. Add:
```text
Escape rule: prefix reserved char with backslash; backslash itself escaped as \\
```

**Verdict:** Ready for Go implementation with this one addition.

---

## Metadata enforcement assessment:

The patch handles the self-reported metadata problem **honestly and correctly**:

§6.2:
> "Metadata fields are audit declarations, not proof."

§6.3: Runtime rejection rules for invalid metadata combinations.

§6.4: `metadataTruthDebt` acknowledges the limit:
> "Go checked the declaration, not the real-world history of how the rule was chosen."

This is **epistemic honesty at its best**. The protocol does not pretend to solve the verification problem; it makes the verification debt visible.

The suggested future reductions (pre-registration, versioned artifacts, git timestamps, review logs, reproducible hashes) are appropriate.

**Verdict:** Correctly handled. No further action needed for TC-1B.

---

## History selection assessment:

The controls are **tight and enforceable**:

- `StartSelectionMode` enum with `invalidHandSelected`
- `allStates` preferred; `declaredSubset` and `singleDeclaredStart` carry debt
- `deduplicate : Bool` with runtime rejection if false
- `fixedBeforeWitness : Bool` with debt if false
- `maxLength` fixed before witness; recommended `|S|` or one period
- `selectionJustification : String` (though see undefined terms above)

The `invalidHandSelected` mode is a **clever anti-pattern**: it makes the forbidden case representable and rejectable, rather than merely absent.

**One gap:** `maxLength` recommendation "one full period of U, if period is computable" assumes period computability. For small `|S|`, period is computable by cycle detection. For larger `|S|`, this may not be feasible. Add:
```text
If period is not computable: maxLength = |S| as conservative default.
```

---

## Null-model threshold assessment:

### Random Label Threshold (§9.2)

- Threshold: `random_success_rate >= 0.25` → downgrade
- Minimum trials: 1000
- Underpowered flag if < 100 trials

**Assessment:** Conservative and appropriate. For two independent fair labels, P(cancellation) = 0.5. The threshold 0.25 is below this, catching cases where the label structure is weaker than pure randomness. 1000 trials gives reasonable precision.

**One gap:** The threshold does not account for **multiple comparison**. If many coarse states are tested, the probability of at least one false witness increases. Add:
```text
If testing multiple coarse states: apply Bonferroni-style correction or report family-wise error rate.
```

### Generic Permutation Threshold (§9.3)

- Threshold: `witness_rate >= 0.10` → downgrade
- Full enumeration preferred for small `|S|`
- Sampling with fixed seed for larger `|S|`
- Underpowered flag if < 100 permutations sampled without full enumeration

**Assessment:** Appropriate. 10% is conservative—if 1 in 10 random bijections produce the witness, the update is not structurally special.

**One gap:** No guidance on **how to sample** permutations. Add:
```text
Sampling method: uniform random permutation via Fisher-Yates shuffle with fixed seed.
```

---

## Parity/XOR status assessment:

The three statuses (§10) are **EBP-safe and clear**:

| Status | Meaning | Allowed Claim | Forbidden Claim |
|--------|---------|-------------|-----------------|
| `downgrade_to_classical_parity_artifact` | Parity explains witness | "toy signed-tally pattern exists, but parity null explains it" | "interference-like structure survived" |
| `survives_with_parity_debt_open` | Parity replicates arithmetic but not mechanism | "witness survives parity null only with open parity debt" | (none stronger) |
| `parity_null_survived` | Parity cannot replicate | "witness survived parity/XOR null at toy level" | "quantum interference derived" |

The required additional evidence for `survives_with_parity_debt_open` is appropriately demanding.

**Verdict:** Excellent. No gaps.

---

## U(1) / phase boundary assessment:

The boundary audit (§11) is **minimal and correct**:

```json
{
  "label_carrier": "finite_two_label",
  "continuous_phase_used": false,
  "complex_numbers_used": false,
  "u1_structure_used": false,
  "mapping_to_u1_claimed": false,
  "hilbert_space_used": false,
  "born_rule_used": false
}
```

The `u1ExtensionDebt` is explicit:
> "WitnessLabel can be embedded into a richer U(1) structure, but TC-1B does not derive U(1)..."

This **prevents the most common overclaim path**: "We used +1 and -1, which are like complex phases, therefore we have phase structure."

**Verdict:** Sufficient for TC-1B. No action needed.

---

## Go type-guardrail assessment:

The type distinctions (§12) are **operationally sufficient**:

```go
type UnlabeledCount int
type SignedTally int
type WitnessLabel uint8

const (
    WitnessPlus WitnessLabel = iota
    WitnessMinus
)

type WitnessStatus string
type NullModelStatus string
```

The forbidden aliases are explicit:
```go
// Forbidden:
// type Probability = SignedTally
// type Amplitude = SignedTally
```

This prevents **accidental type conflation**—the most common implementation-level overclaim.

**One suggestion:** Add a `type Probability float64` that is **deliberately unused** in TC-1B, with comment:
```go
// Probability is defined but not used in TC-1B.
// Its existence marks the boundary: no probability calculations at this stage.
```

This makes the absence visible.

---

## JSON report schema assessment:

The additions (§13) are **operationally complete**:

1. `runtime_validation`: Metadata, history, coarse-graining, label rule validity
2. `boundary_audit`: U(1), complex, Hilbert space, Born rule flags
3. `null_model_power`: Trial counts, underpowered flags, enumeration vs. sampling
4. `selection_audit`: Mode, rule, maxLength, fixed-before status

**Two gaps:**

1. **No `witness_strength` field** (suggested in v0.3.1 review). Add:
```json
{
  "witness_strength": {
    "total_histories_evaluated": 0,
    "coarse_alternative_pairs": 0,
    "null_models_passed": 0,
    "null_models_total": 9
  }
}
```

2. **No `debt_retirement_log`**. The schema has `debt.retired`, `debt.remaining`, `debt.new`, but no **chronological log** of which debts were retired when and by what evidence. Add:
```json
{
  "debt_log": [
    {
      "debt_item": "needMap",
      "action": "retired",
      "evidence": "canonical encoding defined",
      "timestamp": "..."
    }
  ]
}
```

---

## Should TC-1B be drafted next?

**Yes: draft TC-1B specification.**

**No: do not implement TC-1B in Go yet.**

**NO: do not promote any result.**

The patch is ready for **specification writing** because:
- All semantic contracts are defined
- All enforcement rules are stated
- All thresholds are specified
- All guardrails are in place

But **three blocking conditions** must be met before **Go implementation**:

1. **Fix `independentlyJustified` operational meaning** (add `JustificationKind` enum)
2. **Add escaping rule to canonical encoding** (backslash prefix)
3. **Add `witness_strength` and `debt_log` to JSON schema**

These are small edits that can be folded into the TC-1B spec.

---

## Required edits before TC-1B:

### Edit 1: Add `JustificationKind` for coarse-graining (§7)

Replace `independentlyJustified : Bool` with:

```lean
inductive JustificationKind where
  | symmetryQuotient
  | priorFixed
  | externalReference
  | declaredWithoutProof

structure CoarseGrainingSpec where
  description : String
  fixedBeforeLabel : Bool
  usesWitnessLabel : Bool
  usesTargetOutcome : Bool
  justification : JustificationKind
```

Update admissibility:
```lean
def CoarseGrainingAdmissible (spec : CoarseGrainingSpec) : Prop :=
  spec.fixedBeforeLabel = true ∧
  spec.usesWitnessLabel = false ∧
  spec.usesTargetOutcome = false ∧
  (spec.justification = JustificationKind.symmetryQuotient ∨
   spec.justification = JustificationKind.priorFixed)
```

`declaredWithoutProof` triggers:
```text
status: witness_found_with_coarse_graining_selection_debt
```

---

### Edit 2: Add canonical encoding escape rule (§5)

Add:
```text
Escape rule: prefix reserved character with backslash (\).
Backslash itself escaped as \\.
Example: relation name "a|b" becomes "a\|b".
```

---

### Edit 3: Add `witness_strength` and `debt_log` to JSON schema (§13)

Add to §13:
```json
{
  "witness_strength": {
    "total_histories_evaluated": 0,
    "coarse_alternative_pairs": 0,
    "null_models_passed": 0,
    "null_models_total": 9
  },
  "debt_log": [
    {
      "debt_item": "string",
      "action": "retired|added|remains",
      "evidence": "string",
      "artifact_version": "string"
    }
  ]
}
```

---

## Smallest useful next move:

**Write the TC-1B specification document that instantiates the 4-cycle sanity fixture with `transitionParity` label rule.**

This is the smallest move because:

1. It tests whether the v0.3.2 contract can produce **any** inhabited example.
2. It forces concrete choices on all undefined parameters (`S`, `U`, `Π`, `LabelRuleKind`, `HistoryEnumerationSpec`).
3. It validates the JSON schema with real data.
4. It risks failure—which is the point of Phase 0.
5. It does not require Go implementation; it is a **paper specification** that can be reviewed before code is written.

**Specific TC-1B spec content:**

```text
Instance: 4-Cycle Sanity Fixture

S:
  nodes: {0, 1, 2, 3}
  relations: {edge(0,1), edge(1,2), edge(2,3), edge(3,0)}
  canonical encoding: "RS|nodes=4|rels=edge/2/U(0,1);edge/2/U(1,2);edge/2/U(2,3);edge/2/U(0,3)"

U:
  cyclic shift: 0→1→2→3→0
  nontrivial: yes (all states move)

Π:
  bipartite quotient: {0,2}→q_even, {1,3}→q_odd
  justification: symmetryQuotient (by parity of node index)
  fixedBeforeLabel: true
  usesWitnessLabel: false
  usesTargetOutcome: false

LabelRuleKind: transitionParity
  description: "Label by parity of transition index in cyclic order"
  rule: even transition → plus, odd transition → minus

HistoryEnumerationSpec:
  mode: allStates
  allowedStarts: {0,1,2,3}
  maxLength: 4
  deduplicate: true
  fixedBeforeWitness: true

Expected witness candidate:
  Histories from 0 to q_even (length 2): 0→1→2 and 0→3→2
  Transition parities: 0→1 (odd, minus), 1→2 (odd, minus) → product? 
  [Note: rule needs refinement—this is why it's a spec, not a result]

Null models to run:
  constant label (expected: no cancellation)
  endpoint-only label (expected: no history-dependence)
  random label (1000 trials, threshold 0.25)
  generic permutation (threshold 0.10)
  parity/XOR (expected: depends on rule refinement)

Report: JSON schema v0.3.2 with all fields populated.
```

This is small enough to write in one session. It is useful because it validates the contract's feasibility before code is committed. And it is honest because the `transitionParity` rule may fail to produce the expected witness, revealing a flaw in the spec.
