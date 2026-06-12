# TC-1A v0.3.2 — Definition and Enforcement Patch

## Phase 0.0 Lean-First Semantic Contract Repair

### The Elephant Workbench Companion

---

# 0. Status

This artifact patches **TC-1A v0.3.1**.

It does **not** introduce a new toy model.

It does **not** implement Go code.

It does **not** prove physics.

It does **not** promote TBA, E₈, D₄, triality, Bohmian guidance, quantum interference, or Born-rule recovery.

Status:

> alive / unpromoted / definition-and-enforcement patch / debt-bearing

Purpose:

> Close the final pre-TC-1B cracks found in review: undefined predicates, vague enforcement rules, self-reported metadata, history-selection loopholes, null-model thresholds, and canonical encoding drift.

---

# 1. Why This Patch Exists

TC-1A v0.3.1 repaired terminology and added metadata, but review found several remaining gaps:

```text
endpoint was used but not defined
CoarseAlternatives was used but not defined
CanonicalEncoding was described but not exact
Bool metadata was self-reported, not proof
allowedStarts could still be hand-selected
maxLength could still be tuned after the fact
"frequent" random success was undefined
"most generic permutations" was undefined
parity/XOR downgrade statuses needed sharper rules
independentlyJustified existed but was not enforced
```

This patch does not expand the theory.

It only tightens the contract before TC-1B.

---

# 2. Core Carry-Forward Definitions

TC-1B must explicitly inherit the following structures.

## 2.1 MicroSpace

```lean
structure MicroSpace where
  State : Type
  finiteState : Fintype State
  asRelState : State -> RelState
```

Meaning:

* `State` is the finite microstate type.
* `finiteState` guarantees finite enumeration.
* `asRelState` connects each microstate to relational content.

Debt:

```text
needFaithfulnessReview:
  asRelState may be representational rather than physically relational
```

---

## 2.2 ReversibleUpdate

```lean
structure ReversibleUpdate (M : MicroSpace) where
  U    : M.State -> M.State
  Uinv : M.State -> M.State
  left_inv  : forall s : M.State, Uinv (U s) = s
  right_inv : forall s : M.State, U (Uinv s) = s
  nontrivial : exists s : M.State, U s ≠ s
```

Meaning:

`U` is a deterministic bijective update.

This is a toy assumption.

It is not physical time, unitarity, Hamiltonian dynamics, or quantum evolution.

Debt:

```text
timeSmugglingDebt:
  global discrete update remains a toy simplification

deterministicUpdateDebt:
  branching or nondeterministic alternatives are deferred
```

---

# 3. Endpoint Definition

## 3.1 Problem

TC-1A v0.3.1 used:

```lean
endpoint h
```

without redefining it inside the patch.

## 3.2 Patch

A history is:

```lean
structure History (M : MicroSpace) (R : ReversibleUpdate M) where
  start  : M.State
  length : Nat
```

The endpoint is the result of iterating `R.U` from `h.start` for `h.length` steps.

Lean-shaped:

```lean
def endpoint
  {M : MicroSpace}
  {R : ReversibleUpdate M}
  (h : History M R) : M.State :=
  Nat.iterate R.U h.length h.start
```

Plain-English version:

```text
endpoint(h) = start state after applying U exactly length times
```

TC-1B Go requirement:

```text
Endpoint(h):
  s := h.Start
  repeat h.Length times:
    s = U(s)
  return s
```

---

# 4. CoarseAlternatives Definition

## 4.1 Problem

TC-1A v0.3.1 used:

```lean
CoarseAlternatives C h1 h2
```

but did not define it.

## 4.2 Patch

Two histories are coarse alternatives when they are distinct histories but have the same coarse endpoint.

Lean-shaped:

```lean
def CoarseAlternatives
  {M : MicroSpace}
  {R : ReversibleUpdate M}
  (C : CoarseGraining M)
  (h1 h2 : History M R) : Prop :=
  h1 ≠ h2 ∧ C.pi (endpoint h1) = C.pi (endpoint h2)
```

Plain-English version:

```text
h1 and h2 are different histories,
but Π cannot distinguish their final coarse state.
```

Forbidden inference:

```text
CoarseAlternatives ≠ quantum superposition
CoarseAlternatives ≠ physical path interference
CoarseAlternatives ≠ measurement branching
```

Allowed claim:

```text
coarse endpoint indistinguishability
```

---

# 5. Canonical Encoding Enforcement

## 5.1 Problem

TC-1A v0.3.1 said:

```text
CanonicalEncoding(RelState) -> string
```

but did not specify exact string rules.

## 5.2 Patch

For TC-1B, canonical encoding must be deterministic and reproducible.

Recommended first encoding:

```text
RS|nodes=<nodeCount>|rels=<relationRecord1>;<relationRecord2>;...
```

Each relation record:

```text
<relationTypeName>/<arity>/<order>(<arg1>,<arg2>,...)
```

Where:

```text
order = O for ordered
order = U for unordered
```

Rules:

```text
1. Escape reserved characters in names: | ; / ( ) , \
2. Sort relation records lexicographically by their encoded string.
3. For ordered relations, preserve argument order.
4. For unordered relations, sort arguments numerically before encoding.
5. Include nodeCount even if no relations exist.
6. Do not infer graph isomorphism beyond this canonical encoding.
```

Example:

```text
RS|nodes=3|rels=edge/2/U(0,1);edge/2/U(1,2);tag/1/O(0)
```

Go function signature:

```go
func CanonicalEncoding(rs RelState) (string, error)
```

Required Go behavior:

```text
If relation arity does not match argument length:
  return error

If relation name contains reserved characters:
  escape deterministically

If ArgOrder is unknown:
  return error
```

Debt retained:

```text
fullGraphIsomorphismDebt:
  this encoding is a practical canonical representation, not a proof of all graph-isomorphism equivalence
```

---

# 6. Metadata Enforcement Boundary

## 6.1 Problem

TC-1A v0.3.1 replaced `Prop` fields with booleans, but booleans can be self-reported falsely.

## 6.2 Patch

Metadata fields are **audit declarations**, not proof.

Required language:

```text
Bool metadata records declared discipline.
It does not prove historical fact.
Go enforces declared admissibility.
EBP records remaining trust/audit debt.
```

This applies to:

```text
handPainted
fixedBeforeWitness
fixedBeforeLabel
usesTargetOutcome
usesWitnessLabel
independentlyJustified
validForWitness
deduplicate
```

## 6.3 Runtime Enforcement

TC-1B Go must reject or mark invalid any run where:

```text
LabelRuleSpec.handPainted = true
LabelRuleSpec.fixedBeforeWitness = false
LabelRuleSpec.usesTargetOutcome = true
LabelRuleSpec.validForWitness = false
CoarseGrainingSpec.fixedBeforeLabel = false
CoarseGrainingSpec.usesWitnessLabel = true
CoarseGrainingSpec.usesTargetOutcome = true
HistoryEnumerationSpec.deduplicate = false
```

Runtime status:

```text
invalid_by_declared_metadata
```

## 6.4 Audit Debt

Even when the declared metadata is valid, the run still carries:

```text
metadataTruthDebt:
  Go checked the declaration, not the real-world history of how the rule was chosen.
```

This debt can be reduced later by:

```text
pre-registration
versioned artifacts
git commit timestamps
review logs
locked configuration files
reproducible report hashes
```

---

# 7. Coarse-Graining Independent Justification

## 7.1 Problem

TC-1A v0.3.1 included:

```lean
independentlyJustified : Bool
```

but did not require it in admissibility.

## 7.2 Patch

For TC-1B, `independentlyJustified` is required for a clean witness.

Updated admissibility:

```lean
def CoarseGrainingAdmissible (spec : CoarseGrainingSpec) : Prop :=
  spec.fixedBeforeLabel = true ∧
  spec.usesWitnessLabel = false ∧
  spec.usesTargetOutcome = false ∧
  spec.independentlyJustified = true
```

If `independentlyJustified = false`, the run is not invalid, but the witness status is downgraded.

Status:

```text
witness_found_with_coarse_graining_selection_debt
```

Allowed claim:

```text
toy witness found, but coarse-graining independence remains unpaid
```

Forbidden claim:

```text
robust toy witness
```

---

# 8. History Enumeration Enforcement

## 8.1 Problem

TC-1A v0.3.1 prevented duplicate histories but still allowed hand-selection through:

```lean
allowedStarts : List M.State
maxLength : Nat
```

## 8.2 Patch

TC-1B must classify history enumeration mode.

```lean
inductive StartSelectionMode where
  | allStates
  | declaredSubset
  | singleDeclaredStart
  | invalidHandSelected
```

Updated history spec:

```lean
structure HistoryEnumerationSpec (M : MicroSpace) where
  mode : StartSelectionMode
  allowedStarts : List M.State
  maxLength : Nat
  deduplicate : Bool
  fixedBeforeWitness : Bool
  selectionJustification : String
```

## 8.3 Clean History Rule

Cleanest TC-1B rule:

```text
mode = allStates
allowedStarts = all states in M.State
deduplicate = true
fixedBeforeWitness = true
```

This is preferred for the first toy check.

## 8.4 If Using a Subset

If `mode = declaredSubset` or `singleDeclaredStart`, the run must carry:

```text
history_selection_debt_open
```

Unless there is a pre-registered reason.

Invalid:

```text
mode = invalidHandSelected
```

Runtime status:

```text
invalid_history_selection
```

## 8.5 maxLength Rule

`maxLength` must be fixed before witness evaluation.

If not:

```text
max_length_selection_debt_open
```

Recommended first value:

```text
maxLength = one full period of U, if period is computable
```

or for very small systems:

```text
maxLength = |S|
```

Reason:

For a finite bijective update, orbits are periodic. Testing up to `|S|` gives a simple first coverage rule.

Debt:

```text
finiteRecurrenceDebt:
  finite bijective systems eventually cycle; long histories may add no new structure
```

---

# 9. Null-Model Threshold Rules

## 9.1 Problem

TC-1A v0.3.1 used vague words:

```text
frequent
most
```

## 9.2 Random Label Null Threshold

For the first two-history witness:

```text
P(SignedTally = 0) = 1/2
```

Therefore, a single two-history cancellation is weak by default.

TC-1B rule:

```text
If random_success_rate >= 0.25 for equivalent witness conditions:
  status = downgrade_to_random_label_artifact
```

Reason:

A robust mechanism should not be easily reproduced by random labels. The threshold is intentionally conservative.

Required report fields:

```text
random_trials
random_seed
random_success_count
random_success_rate
random_threshold
random_status
```

If fewer than 100 random trials are run:

```text
random_null_underpowered
```

Recommended minimum:

```text
random_trials >= 1000
```

unless full enumeration is possible.

---

## 9.3 Generic Permutation Null Threshold

For small `|S|`, enumerate all permutations if feasible.

If not feasible, sample with fixed seed.

TC-1B rule:

```text
If generic_permutation_witness_rate >= 0.10:
  status = downgrade_to_generic_permutation_artifact
```

Reason:

If many generic bijections produce the same witness, the chosen `U` is probably not structurally special.

Required report fields:

```text
permutation_mode: full_enumeration | sampled
permutations_tested
permutation_seed
witnesses_found
witness_rate
witness_rate_threshold
permutation_status
```

If fewer than 100 permutations are sampled and full enumeration was not done:

```text
permutation_null_underpowered
```

---

## 9.4 Threshold Status Warning

Thresholds are Workbench defaults, not physics constants.

They may be revised.

Any threshold revision must be versioned.

Debt:

```text
thresholdJustificationDebt:
  random and permutation thresholds are pragmatic first-pass audit rules, not physical criteria.
```

---

# 10. Parity/XOR Null Status Rules

## 10.1 Problem

TC-1A v0.3.1 said to downgrade if XOR/parity reproduces the witness, but did not define coexistence cases.

## 10.2 Patch

Use three statuses:

```text
downgrade_to_classical_parity_artifact
survives_with_parity_debt_open
parity_null_survived
```

## 10.3 Status Definitions

### Case 1 — Equivalent replication

If parity/XOR reproduces the witness using the same effective information:

```text
status = downgrade_to_classical_parity_artifact
```

Meaning:

The main witness is explained by classical parity bookkeeping.

Allowed claim:

```text
toy signed-tally pattern exists, but parity null explains it
```

Forbidden claim:

```text
interference-like structure survived
```

---

### Case 2 — Arithmetic pattern only

If parity/XOR reproduces the arithmetic cancellation but not the declared substrate mechanism:

```text
status = survives_with_parity_debt_open
```

Required additional evidence:

```text
substrate-derived label origin
history-dependence not endpoint-only
coarse-graining independence
robustness across update families
failure of simpler parity encodings
```

Allowed claim:

```text
witness survives parity null only with open parity debt
```

---

### Case 3 — Parity/XOR fails

If parity/XOR cannot reproduce the witness under the same constraints:

```text
status = parity_null_survived
```

Allowed claim:

```text
witness survived the parity/XOR null at toy level
```

Forbidden claim:

```text
quantum interference derived
```

---

# 11. U(1) / Phase Boundary Audit

## 11.1 Problem

A two-label system can be embedded into U(1):

```text
plus  -> 1
minus -> -1
```

But TC-1B does not derive U(1), complex phase, Hilbert space, or amplitude.

## 11.2 Patch

TC-1B must include a boundary audit:

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

## 11.3 Debt

```text
u1ExtensionDebt:
  WitnessLabel can be embedded into a richer U(1) structure, but TC-1B does not derive U(1), phase continuity, complex amplitudes, or Hilbert-space structure.
```

This is later-phase debt.

It is not a TC-1B blocker.

---

# 12. Go Type-Level Guardrails

## 12.1 Problem

String labels in JSON are not enough.

## 12.2 Patch

TC-1B Go should use distinct types:

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

Forbidden:

```go
type Probability = SignedTally
type Amplitude = SignedTally
```

Required rule:

```text
No probability, amplitude, phase, or Born-rule type may be created in TC-1B.
```

Go types are operational guardrails.

They do not prove physical semantics.

---

# 13. Updated Go Report Schema Additions

Add these fields to the TC-1B report.

## 13.1 Runtime validation

```json
{
  "runtime_validation": {
    "metadata_valid": true,
    "history_selection_valid": true,
    "coarse_graining_valid": true,
    "label_rule_valid": true,
    "invalid_reason": ""
  }
}
```

## 13.2 Boundary audit

```json
{
  "boundary_audit": {
    "label_carrier": "finite_two_label",
    "continuous_phase_used": false,
    "complex_numbers_used": false,
    "u1_structure_used": false,
    "mapping_to_u1_claimed": false,
    "hilbert_space_used": false,
    "born_rule_used": false
  }
}
```

## 13.3 Null-model power

```json
{
  "null_model_power": {
    "random_trials": 1000,
    "random_underpowered": false,
    "permutations_tested": 100,
    "permutation_underpowered": false,
    "full_permutation_enumeration": false
  }
}
```

## 13.4 Selection audit

```json
{
  "selection_audit": {
    "start_selection_mode": "allStates",
    "allowed_starts_rule": "all microstates",
    "max_length_rule": "|S|",
    "fixed_before_witness": true,
    "selection_debt_open": false
  }
}
```

---

# 14. Updated TC-1B Entry Criteria

TC-1B may be drafted when the following are explicitly included:

```text
endpoint definition
CoarseAlternatives definition
canonical encoding algorithm
metadata enforcement rules
history selection mode
maxLength rule
random-label threshold
generic-permutation threshold
parity/XOR status rules
U(1) boundary audit
Go type-level guardrails
updated report schema
```

TC-1B may be executed only when:

```text
S is concrete
U is concrete and deterministic/bijective
Π is concrete
LabelRuleSpec is concrete
HistoryEnumerationSpec is concrete
endpoint is implemented
CoarseAlternatives is implemented
CanonicalEncoding is implemented
runtime validation is implemented
at least constant-label and endpoint-only nulls are implemented
report schema is produced
```

---

# 15. Status After This Patch

TC-1A v0.3.2 retires part of:

```text
needMap
needObstruction
needNullModel
needFaithfulnessReview
needToyCheckPreparation
```

It does not retire:

```text
needToyCheck
originOfSignsDebt
whySummationDebt
signedBookkeepingFaithfulnessDebt
u1ExtensionDebt
physicsMapDebt
humanPhysicsReviewDebt
thresholdJustificationDebt
metadataTruthDebt
```

Final status:

> alive / clarified / still unpromoted / ready to draft TC-1B

---

# 16. Next Artifact

Next artifact:

> TC-1B — First Go-Executable Toy Check Specification

TC-1B must instantiate:

```text
S
U
Π
endpoint
CoarseAlternatives
CanonicalEncoding
WitnessLabel
HistoryEnumerationSpec
LabelRuleSpec
UnlabeledCount
SignedTally
SignedTallyCancellationWitness
Null Models
Go Type Guardrails
JSON Report
Boundary Audit
```

Allowed result:

> toy-level signed-tally cancellation witness survives/fails null models

Forbidden result:

> quantum interference
> Born-rule recovery
> physical amplitude
> TBA support
> quantum mechanics derived

---

# 17. Final Reminder

This patch exists to make TC-1B boring, auditable, and hard to overclaim.

If TC-1B succeeds, it earns only:

> a controlled toy-level signed-tally result under declared constraints

If TC-1B fails, it earns:

> useful obstruction information

Both are progress under EBP.
