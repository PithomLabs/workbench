# Elephant Bridge Protocol v2.1

## Lean-First, Tool-Agnostic, Minimal Operational Kernel

**Document status:** Working specification  
**Version:** 2.1  
**Purpose:** Define the smallest operational form of the Elephant Bridge Protocol that preserves creativity, imagination, rigor, and anti-fragile epistemology without becoming bureaucracy.  
**Primary contract language:** Lean-style structures, inductive types, definitions, theorem obligations, counterexamples, and executable checks.  
**Schema policy:** No YAML-first or JSON-first schema. Prose ideas are canonical at entry. Lean structures become the promotion and debt-payment language.  
**Tool policy:** Tool-agnostic. Pithom Theory Workbench, GitHub, Lean, Coq, Isabelle, notebooks, local files, and future systems may implement the protocol, but none defines the protocol.

---

## 0. Executive Summary

EBP v2.1 is the minimal, Occam-compliant operational form of the Elephant Bridge Protocol.

Its core doctrine is:

```text
Ideas enter free.
Promotion costs debt.
Debt does not kill.
Debt is forever payable.
New evidence can create new debt.
No final-truth claim may be promoted.
```

The protocol exists to protect two things at the same time:

1. **The theorist's imagination.** Any idea may enter as a one-line claim.
2. **The search's epistemic integrity.** No idea may be promoted until its unpaid obligations are visible and sufficiently discharged.

EBP v2.1 is intentionally not a theory of everything, not a theory generator, not a truth engine, not a gatekeeping institution, and not a replacement for academia, journals, arXiv, peer review, or human judgment.

It is a **notebook with a conscience**.

A notebook preserves imagination.  
A conscience prevents overclaiming.

---

## 1. Why v2.1 Exists

EBP v1 preserved the spirit of the Blind Men and the Elephant: each theory may touch a real part of the whole, but no single theory should be accepted wholesale or rejected wholesale without extracting the features that survive.

EBP v2 corrected a deeper problem: even the protocol's own preferred assumptions can become dogma. TBA, E8, optimality, Bohmian decomposition, holography, relational amplitude spaces, and Lean formalization are all useful candidates or tools, but none should be sacred.

EBP v2.1 corrects an operational problem: if the protocol demands too much structure at entry, it becomes a bureaucracy and kills immature but potentially fertile ideas.

Therefore v2.1 separates **entry** from **promotion**.

```text
Entry is cheap.
Promotion is expensive.
```

This is the entire shift.

An idea may enter with no map, no invariant, no Lean object, no null model, no obstruction, and no proof.

But it may not be promoted while those debts remain unpaid.

---

## 2. The Doctrine

### 2.1 The Primary Rule

```text
Ideas enter free. Promotion costs debt.
```

### 2.2 The Debt Rule

```text
Debt does not kill.
Debt only blocks promotion.
```

An idea with unpaid debt is not rejected. It is alive, unpromoted, and available for future work.

### 2.3 The Forever-Payable Rule

```text
Debt is forever payable.
```

An idea from today may pay its debt tomorrow, next year, or years later. The protocol does not impose artificial expiration dates.

### 2.4 The Living-Ledger Rule

```text
New evidence can create new debt.
```

A promoted idea can become unpromoted again if a new obstruction, counterexample, stronger null model, or faithfulness problem appears.

### 2.5 The No-Final-Truth Rule

```text
No final-truth claim may be promoted.
```

Promotion never means nature has been proven. It means a claim has paid enough operational debt to be treated as a serious candidate artifact.

### 2.6 The Tool-Agnostic Rule

```text
No tool owns the protocol.
```

Lean is a powerful debt-payment language. PTW may become an implementation. GitHub may become a registry. None is the protocol itself.

### 2.7 The Lean-First Promotion Rule

```text
Lean is not required for entry.
Lean is one of the strongest ways to retire debt.
```

The entry artifact is prose. The promoted artifact should increasingly become formal, executable, falsifiable, or at least sharply inspectable.

---

## 3. The Minimum Pipeline

The entire operational pipeline is:

```text
Capture -> Clarify -> Debt -> Test -> Promote
```

The theorist should not experience this as form-filling. The theorist should experience it as:

```text
I can throw an idea into the workbench, and it will quietly track what the idea still owes.
```

---

## 4. Stage 1: Capture

### 4.1 The Only Required Entry

An idea enters as:

```text
owner + claim
```

Optional:

```text
source
```

That is all.

No map required.  
No invariant required.  
No bridge type required.  
No maturity stage required.  
No Lean required.  
No null model required.  
No obstruction required.  
No review required.

### 4.2 Minimal Lean Kernel

The minimum Lean-style operational core is:

```lean
abbrev Timestamp := Nat

inductive DebtItem
| needMap
| needInvariant
| needToyCheck
| needNullModel
| needObstruction
| needFaithfulnessReview
deriving DecidableEq, Repr

structure Idea where
  owner : String
  claim : String
  source : Option String
  born : Timestamp
  debt : List DebtItem
  containsFinalTruthClaim : Bool
deriving Repr
```

This is the smallest stable unit of EBP v2.1.

### 4.3 Why There Is No YAML Schema

EBP v2.1 rejects YAML-first and JSON-first schemas as the primary protocol language because they can become static paperwork.

The schema is instead a Lean-style contract:

```text
inductive types define allowed categories.
structures define artifact shape.
definitions define operational rules.
theorems define obligations.
counterexamples define disproofs or demotions.
```

A tool may serialize Lean-shaped records into JSON, SQLite, Markdown, a database, or Git history. That is implementation detail, not protocol foundation.

---

## 5. Stage 2: Clarify

Clarification is optional and creative.

A theorist may add:

```text
a paragraph
a sketch
a metaphor
an equation
a source
a diagram
a rough map
a proposed invariant
a counterexample worry
a rival interpretation
```

The protocol should not interrupt imagination. It should quietly observe what has been supplied and what remains unpaid.

A theorist can write naturally:

```text
Maybe boundary information capacity is the shared invariant behind area, entropy, spin-network punctures, and CFT state counting.
```

The system should infer possible debts:

```text
needs map
needs invariant
needs toy check
needs null model
needs obstruction
needs faithfulness review
```

If the paragraph already contains an invariant, the invariant debt may be retired or marked partially retired.

If it contains a map, the map debt may be retired or marked partially retired.

The theorist should not need to fill a rigid checklist at the moment of inspiration.

---

## 6. Stage 3: Debt

### 6.1 Full Starting Debt

Every fresh idea starts with the default debt list:

```lean
def fullDebt : List DebtItem :=
  [ DebtItem.needMap
  , DebtItem.needInvariant
  , DebtItem.needToyCheck
  , DebtItem.needNullModel
  , DebtItem.needObstruction
  , DebtItem.needFaithfulnessReview
  ]
```

### 6.2 Fresh Idea Constructor

```lean
def freshIdea
  (owner claim : String)
  (source : Option String)
  (born : Timestamp)
  : Idea :=
{
  owner := owner,
  claim := claim,
  source := source,
  born := born,
  debt := fullDebt,
  containsFinalTruthClaim := false
}
```

### 6.3 Alive Versus Promoted

```lean
def ideaAlive (_ : Idea) : Bool :=
  true

def ideaPromoted (i : Idea) : Bool :=
  i.debt.isEmpty && !i.containsFinalTruthClaim
```

This captures the central philosophy:

```text
Every idea is alive.
Only debt-free, non-final-truth ideas are promoted.
```

### 6.4 Retiring Debt

```lean
def retireDebt (d : DebtItem) (i : Idea) : Idea :=
  { i with debt := i.debt.filter (fun x => x != d) }
```

Debt retirement should happen one move at a time.

```text
One useful move retires one debt.
```

### 6.5 Adding Debt

```lean
def addDebt (d : DebtItem) (i : Idea) : Idea :=
  if i.debt.contains d then i else { i with debt := d :: i.debt }
```

This prevents duplicate coarse debt categories while allowing new evidence to reinstate unpaid work.

### 6.6 Filing an Obstruction

```lean
def fileObstruction (i : Idea) : Idea :=
  addDebt DebtItem.needObstruction i
```

A new obstruction does not delete the idea. It simply makes the idea owe obstruction work again.

### 6.7 Marking Final Truth Language

```lean
def markFinalTruthClaim (i : Idea) : Idea :=
  { i with containsFinalTruthClaim := true }
```

Any artifact that claims final truth is blocked from promotion until the language is corrected.

---

## 7. Stage 4: Test

Testing is debt payment.

The protocol does not demand that every idea be fully tested immediately. It asks for the next smallest useful move.

### 7.1 Map Debt

An idea owes a map when it claims a relation between structures, theories, regimes, or descriptions.

Examples:

```text
E8 structure -> gauge symmetry
boundary area -> information capacity
spin-network punctures -> entropy contribution
CFT state count -> boundary distinguishability
```

Debt is retired when the idea supplies at least a candidate domain, codomain, and translation rule.

Lean-shape:

```lean
structure CandidateMap where
  Domain : Type
  Codomain : Type
  map : Domain -> Codomain
```

A candidate map does not prove the bridge. It simply makes the claim inspectable.

### 7.2 Invariant Debt

An idea owes an invariant when it claims that something survives translation, emergence, approximation, duality, or reconstruction.

Examples:

```text
capacity
entropy scaling
spectrum
symmetry
causal order
correlation structure
anomaly cancellation
code distance
```

Lean-shape:

```lean
structure CandidateInvariant (X : Type) where
  holds : X -> Prop
```

or, when the invariant is numerical:

```lean
structure NumericalInvariant (X : Type) where
  value : X -> Nat
```

Debt is retired when the invariant is stated sharply enough that it can be preserved, violated, or compared.

### 7.3 Toy Check Debt

An idea owes a toy check when it has a map and invariant but no finite test.

Toy checks are not proof of physics. They are wind tunnels.

```text
Toy success does not prove reality.
Toy failure can kill bad structure early.
```

Lean-shape:

```lean
def preservesInvariant
  {A B : Type}
  (f : A -> B)
  (IA : A -> Nat)
  (IB : B -> Nat)
  : Prop :=
  forall a : A, IB (f a) = IA a
```

A weaker scaling check may be:

```lean
def preservesOrdering
  {A B : Type}
  (f : A -> B)
  (IA : A -> Nat)
  (IB : B -> Nat)
  : Prop :=
  forall a1 a2 : A, IA a1 <= IA a2 -> IB (f a1) <= IB (f a2)
```

Exact preservation and scaling preservation should be kept separate.

### 7.4 Null Model Debt

An idea owes a null model when it claims uniqueness, necessity, explanatory superiority, or special status.

A null model asks:

```text
Can a simpler or rival model explain the same thing?
```

Lean-shape:

```lean
structure NullModel where
  Carrier : Type
  explains : Prop
```

A null model does not automatically refute an idea. It blocks inflated claims such as:

```text
Only this structure can explain the invariant.
```

### 7.5 Obstruction Debt

An idea owes obstruction work when known blockers, no-go results, or contradiction risks apply.

Examples:

```text
chirality obstruction
anomaly obstruction
Lorentz recovery problem
Born rule problem
continuum-limit problem
faithfulness problem
parameter padding
normalization artifact
```

Lean-shape:

```lean
structure Obstruction where
  assumptions : Prop
  forbidden : Prop
  noGo : assumptions -> Not forbidden
```

Obstruction debt can be retired by:

```text
showing the obstruction does not apply
showing the idea must be modified
showing the idea fails
marking the idea as analogy only
```

Retirement does not always mean victory. Sometimes it means honest downgrade.

### 7.6 Faithfulness Review Debt

Faithfulness review asks one question:

```text
Does the formalization match the intended claim?
```

Answer choices:

```text
yes
no
contested
```

This should not become a committee system at the minimum layer.

One reviewer is enough for the first pass.

Lean can prove the wrong theorem if the definitions are weak, distorted, or smuggle in the conclusion. Faithfulness review protects the protocol from fake formal confidence.

---

## 8. Stage 5: Promote

Promotion means an idea is allowed to be treated as a mature candidate artifact.

It does not mean the idea is true.

Promotion requires:

```text
all current debt retired
no final-truth claim
faithfulness review passed
```

The minimal Lean decision is:

```lean
def ideaPromoted (i : Idea) : Bool :=
  i.debt.isEmpty && !i.containsFinalTruthClaim
```

A promoted idea may later become unpromoted if new debt is filed.

Promotion is current status, not eternal certification.

---

## 9. The Living Ledger

The ledger is living because knowledge is living.

An idea can move like this:

```text
Alive with debt -> promoted -> new obstruction filed -> alive with debt again -> repaired -> promoted again
```

There is no shame in returning to debt.

The goal is not to preserve prestige. The goal is to preserve contact with constraint.

### 9.1 The Only Temporal Rule

```text
New evidence creates new debt.
```

There are no mandatory scheduled reviews.

There is no expiration date.

There is no death penalty for being unfinished.

### 9.2 Dormant Versus Active

To avoid an infinite graveyard consuming attention, distinguish existence from attention.

This is optional, but useful:

```lean
inductive Attention
| dormant
| active
deriving DecidableEq, Repr
```

The operational principle:

```text
Alive does not mean active.
Unpromoted does not mean prioritized.
Dormant does not mean dead.
```

Only debt-moving ideas should consume active attention.

---

## 10. The Seamless Accounting Principle

The accounting process should be mostly invisible.

The theorist should write naturally. The system should infer debt movements.

Example:

```text
The invariant is boundary distinguishability capacity I(B).
```

The system may infer:

```text
needInvariant retired or partially retired.
```

Example:

```text
Map area A(B) to capacity I(B) by monotone scaling.
```

The system may infer:

```text
needMap partially retired.
needToyCheck still unpaid.
```

Example:

```text
A tensor-network-only explanation may reproduce the same capacity behavior.
```

The system may infer:

```text
needNullModel retired or partially retired.
```

The user should not be forced to think like a clerk. The protocol should behave like a quiet assistant.

---

## 11. The Three-Lane Workflow

The minimal user-facing workflow has three lanes:

```text
Inbox -> Workbench -> Promoted
```

### 11.1 Inbox

Raw ideas.

Requirements:

```text
owner
claim
```

### 11.2 Workbench

Ideas with active debt-paying work.

Each card shows:

```text
claim
owner
debt checklist
next smallest useful move
notes/history
```

### 11.3 Promoted

Ideas with current debt retired and no final-truth language.

Promoted means:

```text
serious candidate artifact
```

not:

```text
truth
```

---

## 12. The Next Smallest Useful Move

Every idea should always have one visible next move.

Examples:

```text
Define the invariant in one sentence.
Name the domain and codomain.
Write the simplest map.
Find one null model.
State one obstruction.
Run one toy check.
Ask whether the formalization matches the claim.
Remove final-truth language.
```

The next move should be small enough to do now.

If a task cannot be reduced to a next smallest useful move, it is too large.

---

## 13. What to Remove Ruthlessly

EBP v2.1 removes anything that does not prevent a failure worse than its overhead.

Kill at entry:

```text
mandatory profiles
mandatory theory taxonomy
mandatory bridge type
mandatory Lean formalization
priority scoring
cost estimates
maturity-stage bureaucracy
multi-reviewer approval
full S+ records
large reports
dashboards before artifacts
formalization-cost estimates
incubation tracks
```

Keep:

```text
Idea
Debt
Retire debt
Reintroduce debt
Promotion requires debt paid
Final-truth claims block promotion
```

The ruthless test for every process:

```text
What failure mode does this prevent?
Is that failure worse than the overhead this process creates?
```

If not, kill the process.

---

## 14. Minimal Session Rule

Every working session should produce at least one of these:

```text
new idea captured
one debt retired
one obstruction filed
one null model filed
one toy check run
one faithfulness issue found
one idea promoted or unpromoted
```

If a session produces none of these, it was probably entropy.

---

## 15. Relationship to Lean

Lean is not the entry gate. Lean is the strongest promotion instrument.

### 15.1 What Lean Is For

Lean helps retire debt by turning claims into:

```text
definitions
structures
inductive types
theorem stubs
proofs
counterexamples
no-go results
executable finite checks
```

### 15.2 What Lean Is Not For

Lean does not prove nature.

Lean does not decide physical faithfulness.

Lean does not replace empirical tests.

Lean does not replace human judgment.

Lean proves only that a formal result follows from formal assumptions.

### 15.3 Lean-First Means Promotion-First, Not Entry-First

Lean-first does not mean every idea must begin in Lean.

It means promoted claims should increasingly have Lean-shaped obligations and, where possible, Lean-checked cores.

---

## 16. Relationship to Tools

EBP v2.1 is tool-agnostic.

It may be implemented in:

```text
plain Markdown
Lean files
Git repositories
local databases
Pithom Theory Workbench
Coq or Isabelle
Jupyter-style notebooks
paper sidecars
formal artifact registries
```

But none of these is required for the protocol to exist.

The protocol is the operational law:

```text
Ideas enter free. Promotion costs debt.
```

---

## 17. Relationship to PTW

Pithom Theory Workbench should be overhauled later as an implementation of EBP v2.1, but EBP v2.1 is not based on PTW.

PTW should eventually provide:

```text
one-line idea capture
automatic debt attachment
seamless debt inference
three-lane workflow
Lean debt-payment modules
living ledger
promotion/unpromotion history
artifact export
```

But PTW must not reintroduce bureaucracy.

The PTW rule should be:

```text
Make the accounting invisible.
Make the promotion criteria explicit.
```

---

## 18. Example: Causal Boundary Coin

### 18.1 Capture

```text
Owner: Researcher
Claim: Boundary information capacity may be the shared invariant behind area, entropy, spin labels, and CFT state counting.
Source: optional
```

The idea enters alive.

Debt:

```text
needMap
needInvariant
needToyCheck
needNullModel
needObstruction
needFaithfulnessReview
```

### 18.2 Clarify

Researcher adds:

```text
The invariant is boundary distinguishability capacity I(B).
```

Retire or partially retire:

```text
needInvariant
```

### 18.3 Map

Researcher adds:

```text
Area, state count, spin-boundary labels, and code-cut capacity each map into I(B) by capacity-preserving or capacity-scaling maps.
```

Retire or partially retire:

```text
needMap
```

### 18.4 Toy Check

A finite model tests exact preservation and scaling preservation.

Retire:

```text
needToyCheck
```

or leave debt if the toy model fails.

### 18.5 Null Model

Researcher adds:

```text
A tensor-network-only explanation may reproduce the same capacity behavior.
```

Retire:

```text
needNullModel
```

but downgrade uniqueness claims.

### 18.6 Obstruction

Researcher states:

```text
The bridge may fail if the maps preserve only chosen normalization rather than invariant structure.
```

Retire or modify:

```text
needObstruction
```

### 18.7 Faithfulness

Reviewer asks:

```text
Does the Lean toy invariant actually represent the intended boundary-capacity claim?
```

If yes:

```text
needFaithfulnessReview retired
```

### 18.8 Promotion

If all debts are retired and no final-truth language exists, the idea is promoted to a candidate bridge artifact.

It is not declared true.

It is simply mature enough to carry forward.

---

## 19. Example: E8 Gauge Symmetry Idea

### 19.1 Capture

```text
Claim: E8 structure may control Standard Model gauge symmetries.
```

It enters alive.

No rejection.

### 19.2 Debt

It owes:

```text
map
invariant
toy check
null model
obstruction
faithfulness review
```

### 19.3 Obstruction Appears

Someone files:

```text
Direct E8 unification faces chirality and representation-content problems.
```

This does not kill the idea.

It creates or preserves obstruction debt.

### 19.4 Possible Outcomes

The idea may become:

```text
promoted after serious repair
modified into E8-structural rather than E8-literal
left dormant
converted into a null model
rejected as a promoted claim but preserved as historical idea
```

Debt, not deletion, carries the epistemic state.

---

## 20. Promotion Is Not Truth

This must be repeated because it prevents overclaiming.

```text
Promoted means: current operational debt is paid.
Promoted does not mean: nature is proven.
```

A promoted idea can still be:

```text
wrong
incomplete
physically unfaithful
empirically false later
superseded by a better null model
```

Promotion is a status of research hygiene, not metaphysical victory.

---

## 21. The Door and the Throne

EBP v2.1 has two regimes.

### The Door

```text
Wide open.
Ideas enter free.
No premature formalism.
No punishment for incompleteness.
No gatekeeping of imagination.
```

### The Throne

```text
Guarded by debt.
No unpaid claim is promoted.
No final-truth language survives.
No metaphor becomes a map without work.
No beautiful idea escapes null models.
```

The protocol is gentle at the door and brutal at the throne.

---

## 22. The Anti-Bureaucracy Contract

EBP v2.1 must never become a paperwork machine.

Therefore:

```text
No form before imagination.
No mandatory schema at entry.
No mandatory Lean at entry.
No mandatory review at entry.
No mandatory classification at entry.
No large report unless it retires debt.
No dashboard before artifact.
```

The accounting exists only to prevent accidental promotion.

If accounting becomes the work, the protocol has failed.

---

## 23. The Anti-Fragile Epistemology

An anti-fragile research protocol improves when attacked.

EBP v2.1 welcomes:

```text
objections
counterexamples
null models
faithfulness failures
formalization failures
new no-go results
better rival explanations
```

because each creates clearer debt.

The purpose is not to protect ideas from criticism.

The purpose is to protect the search from unearned certainty.

---

## 24. Minimal Implementation Checklist

A tool implementing EBP v2.1 needs only:

```text
create idea
show debt
retire debt
add debt
mark final-truth claim
show alive/promoted status
record notes/history
show next smallest useful move
```

Everything else is optional.

---

## 25. The Final Doctrine

```text
Ideas enter free.
Promotion costs debt.
Debt does not kill.
Debt is forever payable.
New evidence creates new debt.
No final-truth claim may be promoted.
Lean is not required for entry.
Lean is one of the strongest ways to retire debt.
The protocol is tool-agnostic.
The accounting must be seamless.
Creativity lives at the door.
Rigor guards the throne.
```

Or shorter:

> **EBP v2.1 is a notebook with a conscience: wide open to imagination, ruthless against unearned promotion.**

