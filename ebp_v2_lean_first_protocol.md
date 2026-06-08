# Elephant Bridge Protocol v2

## Lean-First, Tool-Agnostic Conjecture Refinery

**Document status:** Working specification  
**Version:** EBP v2 / Lean-first overhaul  
**Primary contract language:** Lean 4 structures, inductive types, theorem stubs, proof terms, counterexamples, executable checkers  
**Artifact policy:** Markdown may explain; Lean defines.  
**Tool dependency:** None. PTW, GitHub, local files, databases, web UIs, theorem-prover frontends, and agent systems are implementation targets, not foundations.  

---

## 0. Executive Summary

Elephant Bridge Protocol v2 is a Lean-first, tool-agnostic method for exploring theoretical physics and mathematics without smuggling preferred assumptions into the search process.

The original Elephant Bridge Protocol had the right moral center: theories are partial probes of reality; bridges are hypotheses; no analogy should be promoted into proof; no grand claim should survive without maps, assumptions, invariants, obstructions, null models, and formal obligations.

But v1 was still colored by a preferred research stack: relational amplitude substrate, TBA kernel, duality mapping, optimality filtering, Bohmian decomposition, theta-series dictionaries, extremal packing/coding, holography, and guidance mechanisms.

EBP v2 separates the **protocol** from all **research priors**.

The new doctrine is:

```text
Theories are partial probes.
So are protocols.
So are kernels.
So are our favorite assumptions.

No theory is sacred.
No bridge is sacred.
No heuristic is sacred.
No substrate is sacred.
No ontology is sacred.

Only survival under constraint earns promotion.
```

EBP v2 does not ask whether string theory, loop quantum gravity, E8 geometry, holography, Bohmian mechanics, causal sets, tensor networks, spectral geometry, amplitudes, or any other framework is true wholesale.

It asks:

```text
Which features survive when we formalize the claim,
state the assumptions,
declare the alternatives,
define the map,
prove or test invariant preservation,
attach null models,
attach obstructions,
and expose unpaid formal debt?
```

In EBP v2, **Lean is not merely a backend**. Lean is the canonical schema language. What earlier versions represented as YAML or JSON should now be represented as Lean `inductive`, `structure`, `class`, `def`, `theorem`, `example`, and executable finite checkers.

Markdown remains useful for humans. Lean is the machine-checkable contract.

---

## 1. What Changed from EBP v1

EBP v1 treated the Elephant Bridge Protocol as a disciplined methodology for theory work. It correctly insisted that a protocol is not a finished theory, that speculative bridges require maps and obligations, and that the protocol is not a truth engine.

However, EBP v1 also embedded a specific research stack:

```text
Layer 0 — Constraint Substrate
  relational amplitude space
  no assumed background time
  admissibility constraints

Layer 1 — TBA Kernel
  Duality Mapping
  Optimality Filtering
  Bohmian Decomposition

Layer 2 — Bridge Mechanisms
  spectral lifting
  entanglement renormalization
  holographic reconstruction
  theta-series dictionary
  extremal packing/coding
  domain-wall projection
  actualization/guidance
  effective continuum limit
```

Those are valuable candidate modules. They are not neutral foundations.

EBP v2 makes the following changes:

| EBP v1 element | EBP v2 replacement |
|---|---|
| TBA Kernel | Optional heuristic module family |
| Relational amplitude substrate | Substrate hypothesis slot |
| Optimality filtering | Selection-principle registry |
| Bohmian decomposition | Actualization/measurement hypothesis registry |
| E8/extremal geometry | Candidate feature, not default attractor |
| S+ v3 YAML/JSON-style schema | Lean-first structures and theorem obligations |
| PTW-centered implementation | Tool-agnostic protocol, with PTW as one possible implementation |
| Documentation-first artifacts | Lean-first contracts plus minimal human explanation |

The soul remains:

```text
Extract features.
Map bridges.
Preserve invariants.
Track debts.
Attach null models.
Declare obstructions.
Prove, test, demote, or kill.
```

---

## 2. What EBP v2 Is

EBP v2 is:

1. A **Lean-first conjecture refinery**.
2. A **tool-agnostic bridge protocol** for speculative and mature theory work.
3. A **bias-exposure machine** for assumptions hidden inside research programs.
4. A **feature survival protocol** for extracting what remains useful after whole theories fail.
5. A **formal obligation factory** that converts ideas into definitions, theorem stubs, counterexamples, executable checks, no-go lemmas, and review gates.
6. A **null-model discipline** that prevents beautiful structures from being treated as necessary before alternatives are defeated.
7. A **human-machine review contract**: Lean checks formal cores; humans judge faithfulness and physical interpretation.

EBP v2 is designed for any setting where a speculative bridge might be useful but dangerous:

```text
quantum gravity
high-energy theory
mathematical physics
foundations of quantum mechanics
cosmology
holography
emergent spacetime
gauge theory
constructive field theory
tensor networks
formalized mathematics
AI-assisted theory exploration
```

---

## 3. What EBP v2 Is Not

EBP v2 is not:

- a Theory of Everything;
- a theory generator;
- a proof that any ontology is true;
- a proof of Yang-Mills mass gap;
- a proof of Navier-Stokes smoothness;
- a proof that E8 is physically fundamental;
- a proof that holography is universal;
- a proof that Bohmian mechanics is the final interpretation;
- a proof that relational amplitude is the substrate of reality;
- a replacement for physics;
- a replacement for empirical testing;
- a replacement for human judgment;
- a reason to drown research in schemas and documentation;
- a license for AI agents to promote their own suggestions.

EBP v2 does not say:

```text
This framework is true.
This bridge is real.
This ontology is final.
This formalization proves the universe.
```

It says:

```text
Here is the formal claim.
Here is its status.
Here are its assumptions.
Here are its alternatives.
Here is the map.
Here is the invariant.
Here are the null models.
Here are the obstructions.
Here are the formal obligations.
Here is the promotion or demotion gate.
```

---

## 4. The Lean-First Rule

The central rule of EBP v2 is:

```text
Markdown explains.
Lean defines.
Lean checks.
Human review judges faithfulness.
```

A theory note may begin as prose, but it cannot be promoted unless its formal core is represented in Lean or explicitly marked as not yet formalizable.

The canonical protocol objects are not YAML schemas. They are Lean types.

For example, claim status is not a text field:

```lean
inductive ClaimStatus
| derived
| simulated
| assumed
| imported
| speculative
| analogical
| refuted
| open
```

Bridge relation is not a string:

```lean
inductive BridgeRelation
| identity
| duality
| complementarity
| emergence
| approximation
| regularization
| analogy
| conflict
| unknown
```

A bridge is not a paragraph:

```lean
structure BridgeSpec where
  Source : Type
  Target : Type
  relation : BridgeRelation
  sourceStatus : ClaimStatus
  targetStatus : ClaimStatus
  mapStatus : ClaimStatus
  map : Source → Target
```

An invariant claim is not rhetoric:

```lean
structure InvariantSpec (α : Type) where
  Holds : α → Prop
```

A map-preservation claim is a proposition:

```lean
def PreservesInvariant
  {α β : Type}
  (M : α → β)
  (Iα : α → Prop)
  (Iβ : β → Prop) : Prop :=
  ∀ x : α, Iα x → Iβ (M x)
```

A null model is not an objection in prose:

```lean
structure NullModel where
  Carrier : Type
  status : ClaimStatus
  explainsSameInvariant : Prop
```

An obstruction is not a warning label:

```lean
structure ObstructionSpec where
  assumptions : Prop
  forbidden : Prop
  noGo : assumptions → ¬ forbidden
```

A formal obligation is not a to-do item:

```lean
structure FormalObligation where
  statement : Prop
  status : ClaimStatus
  critical : Bool
```

A bridge earns promotion only through a gate:

```lean
structure PromotionGate where
  hasMap : Prop
  hasInvariant : Prop
  hasNullModel : Prop
  hasObstruction : Prop
  hasFormalObligation : Prop
  faithfulnessReviewed : Prop
  noFinalTruthClaim : Prop
```

This is the new schema language.

---

## 5. Why No YAML or JSON Schema

YAML and JSON are useful for transport and persistence, but they are too weak to be the protocol’s epistemic core.

They can say:

```text
field exists
field has text
field has a list
```

They cannot naturally enforce:

```text
this map has the right type
this invariant is preserved
this obstruction blocks promotion
this null model defeats uniqueness
this theorem depends on these assumptions
this claim cannot be promoted without faithfulness review
```

EBP v2 therefore treats YAML/JSON as optional export formats only.

The canonical object is Lean.

A Go application, a database, a web UI, a CLI, or a future PTW overhaul may serialize Lean metadata into JSON if needed. But the source of epistemic authority is not the serialization format. It is the Lean representation plus human review.

The replacement for schema is:

```text
Lean inductive types
Lean structures
Lean typeclasses
Lean theorem stubs
Lean examples
Lean counterexamples
Lean executable checkers
Lean promotion gates
```

---

## 6. The New EBP v2 Pipeline

The EBP v2 pipeline is:

```text
Idea
→ Feature extraction
→ Claim typing
→ Assumption exposure
→ Alternative registry
→ Bridge relation declaration
→ Lean type construction
→ Map definition
→ Invariant definition
→ Null model construction
→ Obstruction construction
→ Formal obligation generation
→ Executable toy check if possible
→ Faithfulness review
→ Promotion, demotion, or rejection
```

This is intentionally narrower than v1. It removes passive documentation as a default activity.

A task is allowed only if it produces at least one of:

```text
Lean definition
Lean structure
Lean theorem stub
Lean proof
Lean counterexample
Lean executable checker
Lean no-go theorem
Lean promotion gate
source-linked faithfulness review
```

Everything else is supporting context, not core work.

---

## 7. The EBP v2 Core Type System

A minimal EBP v2 Lean core should begin with these files:

```text
EBPv2/Core/ClaimStatus.lean
EBPv2/Core/ClaimType.lean
EBPv2/Core/BridgeRelation.lean
EBPv2/Core/EvidenceStatus.lean
EBPv2/Core/Feature.lean
EBPv2/Core/Assumption.lean
EBPv2/Core/Alternative.lean
EBPv2/Core/Invariant.lean
EBPv2/Core/BridgeSpec.lean
EBPv2/Core/NullModel.lean
EBPv2/Core/Obstruction.lean
EBPv2/Core/FormalObligation.lean
EBPv2/Core/Faithfulness.lean
EBPv2/Core/PromotionGate.lean
EBPv2/Core/ProcessGate.lean
```

### Claim Type

```lean
inductive ClaimType
| mathematicalStructure
| physicalOntology
| dynamics
| observable
| measurementProcedure
| approximationLimit
| interpretation
| metaphorHeuristic
| selectionPrinciple
| actualizationHypothesis
| substrateHypothesis
| reconstructionMechanism
| consistencyFilter
```

### Evidence Status

```lean
inductive EvidenceStatus
| explicitSource
| equationOrDerivation
| authorClaim
| reviewerInference
| communityContext
| notDiscussed
| unsupported
| formalized
| kernelChecked
| empiricalInput
| executableToyResult
```

### Feature

```lean
structure Feature where
  Carrier : Type
  claimType : ClaimType
  status : ClaimStatus
  evidence : EvidenceStatus
```

### Assumption

```lean
inductive AssumptionRole
| explicit
| hidden
| inherited
| speculative
| privileged
| removable
| forbidden

structure Assumption where
  proposition : Prop
  role : AssumptionRole
  status : ClaimStatus
```

### Alternative

```lean
structure Alternative where
  Carrier : Type
  relationToPreferred : BridgeRelation
  status : ClaimStatus
  canExplainSameInvariant : Prop
```

### Selection Principle Registry

```lean
inductive SelectionPrinciple
| extremalOptimality
| symmetry
| anomalyCancellation
| renormalizationFixedPoint
| computationalUniversality
| causalConsistency
| entropyBound
| empiricalMinimality
| noGoSurvival
| categoricalUniversality
| perturbativeRobustness
| uniqueness
| unknown
```

### Substrate Hypothesis Registry

```lean
inductive SubstrateHypothesis
| relationalAmplitude
| causalOrder
| algebraicObservableNet
| categoryFunctorStructure
| informationCodeSpace
| continuumFieldOntology
| discreteGraphSubstrate
| computationalRewriteSystem
| operationalOnly
| unknown
```

### Actualization Hypothesis Registry

```lean
inductive ActualizationHypothesis
| bohmianGuidance
| decoherenceRecords
| consistentHistories
| relationalQuantumMechanics
| qbistOperational
| objectiveCollapse
| manyWorldsBranching
| noOntologyClaim
| unknown
```

These registries are not commitments. They are slots.

No entry is privileged by the protocol.

---

## 8. The Central EBP v2 Record

The Lean-first replacement for schema is a dependent structure.

```lean
structure EBPv2Record where
  Domain : Type
  Codomain : Type
  claimType : ClaimType
  claimStatus : ClaimStatus
  relation : BridgeRelation
  sourceFeature : Feature
  targetFeature : Feature
  assumptions : List Assumption
  alternatives : List Alternative
  map : Domain → Codomain
  invariantSource : Domain → Prop
  invariantTarget : Codomain → Prop
  preservesInvariant : Prop
  hasNullModel : Prop
  hasObstruction : Prop
  hasFormalObligation : Prop
  faithfulnessReviewed : Prop
  noFinalTruthClaim : Prop
```

This structure does not prove the bridge. It makes the bridge inspectable.

A stronger version can require the proof directly:

```lean
structure CheckedBridge where
  Domain : Type
  Codomain : Type
  map : Domain → Codomain
  invariantSource : Domain → Prop
  invariantTarget : Codomain → Prop
  proof : ∀ x : Domain, invariantSource x → invariantTarget (map x)
```

A failed bridge may be represented by a counterexample:

```lean
structure BridgeCounterexample where
  Domain : Type
  Codomain : Type
  map : Domain → Codomain
  invariantSource : Domain → Prop
  invariantTarget : Codomain → Prop
  witness : Domain
  sourceHolds : invariantSource witness
  targetFails : ¬ invariantTarget (map witness)
```

A no-go result is represented by obstruction:

```lean
structure NoGoBridge where
  assumptions : Prop
  bridgeExists : Prop
  theorem : assumptions → ¬ bridgeExists
```

This is the heart of EBP v2.

---

## 9. How EBP v2 Handles Favorite Assumptions

EBP v2 does not ban speculative assumptions. It bans hidden privilege.

### Relational Amplitude

Allowed as:

```lean
SubstrateHypothesis.relationalAmplitude
```

Not allowed as default ontology.

### No Background Time

Allowed as an assumption:

```lean
structure NoBackgroundTimeAssumption where
  proposition : Prop
  status : ClaimStatus := ClaimStatus.speculative
```

Not allowed as protocol foundation.

### Duality Mapping

Allowed as a heuristic module:

```lean
BridgeRelation.duality
BridgeRelation.complementarity
```

Not allowed as universal metaphysics.

### Optimality

Allowed as:

```lean
SelectionPrinciple.extremalOptimality
```

Not allowed as proof of physical ontology.

### Bohmian Guidance

Allowed as:

```lean
ActualizationHypothesis.bohmianGuidance
```

Not allowed as final interpretation.

### E8 / Leech / Packing / Coding

Allowed as a feature:

```lean
Feature where
  Carrier := SomeExtremalStructure
  claimType := ClaimType.mathematicalStructure
  status := ClaimStatus.imported -- or formalized/kernelChecked if actually proved
  evidence := EvidenceStatus.formalized
```

Not allowed as ontology without a bridge.

### Holography

Allowed as a reconstruction mechanism:

```lean
ClaimType.reconstructionMechanism
```

Not allowed as universal principle unless defended by maps, regimes, and null models.

---

## 10. Faithfulness Review

Lean can prove what was formalized. It cannot guarantee that the formalization faithfully represents the intended physical claim.

EBP v2 therefore requires a faithfulness layer.

```lean
inductive FaithfulnessStatus
| unreviewed
| faithfulEnoughForToyModel
| faithfulEnoughForMathClaim
| physicallyContested
| tooWeak
| smugglesConclusion
| rejected

structure FaithfulnessReview where
  informalClaim : String
  formalStatement : Prop
  status : FaithfulnessStatus
  reviewerRequired : Bool
```

A theorem cannot be promoted merely because it compiles.

Promotion requires:

```lean
structure PromotionReady where
  hasKernelCheck : Prop
  hasFaithfulnessReview : Prop
  hasAssumptionAudit : Prop
  hasNullModelComparison : Prop
  hasObstructionReview : Prop
  noFinalTruthClaim : Prop
```

This prevents Lean from becoming a new authority myth.

---

## 11. Null Models as First-Class Citizens

In EBP v2, a bridge is not serious until a rival explanation is formalized or explicitly marked open.

```lean
structure NullModelSpec where
  Carrier : Type
  targetClaim : Prop
  nullExplanation : Prop
  weakerThanPreferred : Prop
  defeatsUniqueness : Prop
```

A null model does not always refute a bridge. It can downgrade the bridge:

```text
Preferred bridge works.
Null model also works.
Therefore uniqueness claim fails.
```

Lean form:

```lean
def UniquenessDefeated
  (Preferred : Prop)
  (Null : Prop) : Prop :=
  Preferred ∧ Null
```

This is essential for E8, holography, causal boundary invariants, tensor networks, and any proposed TOE route.

---

## 12. Obstruction-First Protocol

Every promoted bridge needs at least one obstruction attached.

```lean
structure ObstructionLedger where
  obstruction : ObstructionSpec
  appliesToClaim : Prop
  resolved : Prop
```

For example, a direct E8 gauge-unification route may be blocked under representation/chirality assumptions. A Bohmian quantum-gravity route may be blocked unless Lorentz invariance, Born-rule recovery, foliation risk, time, and QFT particle creation are addressed. A string/LQG complementarity route may be blocked if no dictionary exists.

EBP v2 does not assume these obstructions are fatal to every variant. It forces the variant to say why the obstruction applies or does not apply.

---

## 13. Promotion and Demotion

Promotion is conservative.

A claim may move upward only if the appropriate gate is satisfied.

```lean
inductive PromotionLevel
| proseIdea
| typedClaim
| bridgeCandidate
| leanDefined
| toyChecked
| nullModelCompared
| obstructionReviewed
| theoremProved
| faithfullyReviewed
| empiricallyAnchored
| promotedCorpus
```

Demotion is not failure. Demotion is epistemic hygiene.

```lean
inductive DemotionReason
| noMap
| noInvariant
| nullModelDefeatsUniqueness
| obstructionApplies
| proofFailed
| formalizationUnfaithful
| empiricalConflict
| overclaims
| unclearMaturity
| wrongFunctionClass
```

A demoted bridge can still be useful as analogy, heuristic, or research seed.

---

## 14. Process Economy: Ruthless Mode

EBP v2 must not become an endless documentation machine.

The process law is:

```text
No Lean object, no task.
No map, no task.
No invariant, no task.
No null model, no promotion.
No obstruction, no promotion.
No faithfulness review, no promotion.
No kill condition, no process.
```

Lean representation:

```lean
inductive ProcessPurpose
| createDefinition
| createTheoremStub
| proveTheorem
| createCounterexample
| createNullModel
| createObstruction
| createExecutableChecker
| performFaithfulnessReview
| closeDebt
| documentationOnly

structure ProcessRecord where
  purpose : ProcessPurpose
  producesLeanArtifact : Prop
  closesFormalDebt : Prop
  hasKillCriterion : Prop
  hasOwner : Prop
  noFinalTruthClaim : Prop


def ProcessAllowed (P : ProcessRecord) : Prop :=
  (P.producesLeanArtifact ∨ P.closesFormalDebt) ∧
  P.hasKillCriterion ∧
  P.hasOwner ∧
  P.noFinalTruthClaim
```

Documentation-only work is allowed only when it directly supports a formal artifact or human faithfulness review.

---

## 15. Tool-Agnostic Implementation

EBP v2 is not based on PTW.

Any tool can implement it if it can support:

```text
Lean files
source references
human review records
artifact status tracking
build/check reports
counterexample logs
formal obligation lists
```

Possible implementations:

```text
plain Git repository
Lean project with Markdown notes
local CLI
web workbench
research notebook
database-backed system
PTW vNext
VS Code extension
CI-backed theorem-review pipeline
```

PTW should later be overhauled around EBP v2, but PTW is not the protocol.

The protocol is portable.

---

## 16. Minimal EBP v2 Repository Shape

A tool-agnostic Lean-first repository can look like:

```text
EBPv2/
  Core/
    ClaimStatus.lean
    ClaimType.lean
    BridgeRelation.lean
    EvidenceStatus.lean
    Feature.lean
    Assumption.lean
    Alternative.lean
    Invariant.lean
    BridgeSpec.lean
    NullModel.lean
    Obstruction.lean
    FormalObligation.lean
    Faithfulness.lean
    PromotionGate.lean
    ProcessGate.lean

  Heuristics/
    DualityMapping.lean
    OptimalitySelection.lean
    ActualizationRegistry.lean
    CausalReconstruction.lean
    SpectralReconstruction.lean
    InformationReconstruction.lean

  Examples/
    CausalBoundaryCoin.lean
    CommonInvariantLedger.lean
    ExecutableToyChecker.lean

  Docs/
    ebp_v2_lean_first_protocol.md
    ebp_v2_background_story.md
```

No YAML required.

---

## 17. Relationship to PTW

EBP v2 is independent of PTW.

However, PTW should eventually be overhauled to implement EBP v2 by treating Lean artifacts as first-class citizens.

A future PTW overhaul should:

```text
1. ingest sources;
2. extract candidate claims;
3. create Lean obligation stubs;
4. link prose claims to Lean statements;
5. track theorem status;
6. track null models;
7. track obstruction ledgers;
8. track faithfulness reviews;
9. refuse promotion when gates fail;
10. show the shortest next executable action.
```

But that belongs to a separate PTW design thread.

EBP v2 remains tool-agnostic.

---

## 18. First Use Case: Causal Boundary Coin

The first EBP v2 bridge should not attempt the full TOE.

It should test one invariant:

```text
A finite causal boundary has finite distinguishability capacity.
```

Lean-first target:

```lean
structure BoundarySystem where
  Boundary : Type
  State : Type
  accessible : Boundary → State → Prop
  refines : Boundary → Boundary → Prop

structure BoundaryCapacity (S : BoundarySystem) where
  I : S.Boundary → Nat
  monotone :
    ∀ b₁ b₂ : S.Boundary,
      S.refines b₁ b₂ → I b₁ ≤ I b₂
```

The bridge asks whether area, entropy, spin-network punctures, CFT state-counting, and tensor-network cut capacity can be treated as faces of one common invariant.

The first success is not proving physics.

The first success is building a bridge that can fail.

---

## 19. Final Doctrine

EBP v2 is the protocol after the protocol learned humility.

Theories are partial probes of the elephant.

But so are:

```text
our methods,
our favorite kernels,
our selection principles,
our formalizations,
our tools,
and our stories about what progress should look like.
```

Therefore:

```text
Extract features.
Declare assumptions.
Declare alternatives.
Map bridges.
Prove or test invariants.
Attach null models.
Attach obstructions.
Review faithfulness.
Promote only what survives.
Demote without shame.
Kill without regret.
```

EBP v2 is not a theory of everything.

It is a machine for preventing our search for everything from becoming a machine for fooling ourselves.

