# The Workbench: Two-Speed Methodology for Clarifying Physical Theories

**Version:** 1.0 synthesized edition  
**Purpose:** Provide one unified methodology with two operating modes:

1. **Flash Workbench** — a quick, uniform first-pass overview for rapid LLM analysis.
2. **Extended Workbench** — a thorough schema for deep audits, cross-LLM consistency, and drift-resistant evaluation.

This document synthesizes the strongest recurring elements across the uploaded Workbench drafts into a single coherent methodology. It removes duplicated formulations, resolves inconsistent scoring conventions, and preserves the essential discipline: The Workbench does **not** decide which theory is true. It clarifies what a theory claims, what it has earned the right to claim, what it merely accommodates, what it forbids, what would count against it, and what remains incomplete.

---

## Orientation: What This Synthesis Resolves

The source drafts mostly agree on the core Workbench idea but differ in structure and granularity. This synthesis resolves the major overlaps and inconsistencies as follows:

| Issue | Unified decision |
|---|---|
| Quick vs thorough use | Use two modes: **Flash** for fast triage; **Extended** for full audit. |
| MVT criteria count | Use **10 criteria**, with incompleteness transparency as mandatory criterion 10. |
| Function classes | Use a canonical taxonomy that includes ontology, dynamics, reconstruction, consistency filters, effective theories, computational validators, observer frameworks, diagnostic arguments, and endpoint phenomenology. |
| Seven-tuple vs 7+1 tuple | Use the extended interface `S+ = (A, Ω, C, Φ, R, Σ, M, O)`, where `O` is the Gödel-safe escape hatch for uncaptured components. |
| Scoring vocabulary | Use **Strong / Partial / Weak / Undeclared / Undecidable-Open / Not Applicable**. For inverse constraints, add **Strong / Moderate / Weak / None**. |
| Role of LLMs | LLMs are **clerks and drafting assistants**, not authorities. Every populated field must be evidence-backed and human-adjudicated. |
| Diagnostic rules | Keep A–J, but label each as a diagnostic rule with explicit epistemic status, not as an overclaimed theorem. |
| Incompleteness | Make incompleteness mandatory for both the theory being analyzed and the Workbench analysis itself. |

---

# Part I — Flash Workbench

## 1. Purpose of the Flash Version

The Flash Workbench is the fast-pass version of the methodology. It is designed for a first overview of a theory, paper, research program, or dispute. It should be usable by any capable LLM without requiring the full extended schema.

The Flash version answers:

- What is this framework?
- What function class does it belong to?
- What problem does it address?
- What does it claim to explain?
- Does it derive, explain, accommodate, or postulate those claims?
- What does it forbid?
- What would weaken or falsify it?
- What remains incomplete?
- What is the quick Workbench verdict?

The Flash version is not a final assessment. It is triage. Its output should identify whether the theory deserves a full Extended Workbench audit.

---

## 2. Flash Non-Negotiables

Every Flash analysis must obey these rules:

1. **Do not judge truth.** Classify claims; do not declare the theory true or false.
2. **Declare function class first.** Do not score a reconstruction mechanism as if it were a full ontology.
3. **Do not call accommodation derivation.** Parameter fitting, vacuum selection, or model choice is accommodation unless a derivation is shown.
4. **Ask what the theory forbids.** A theory with no exclusion power has weak scientific teeth.
5. **Ask what would count against it.** A serious theory must expose possible failure conditions.
6. **Mark missing fields explicitly.** Use `Undeclared`, `Not Discussed`, or `Not Applicable`; do not fill gaps with speculation.
7. **State incompleteness.** The theory’s unresolved claims are part of the result, not an embarrassment to hide.
8. **Treat the LLM as a clerk.** The LLM drafts; the human reviewer adjudicates.

---

## 3. Flash Schema

Use this compact schema for rapid analysis.

```yaml
flash_workbench_report:
  target:
    name:
    source:
    domain:
    theory_or_framework_type:

  problem_frame:
    problem_addressed:
    hard_constraints:
      -
    what_a_complete_solution_requires:

  function_class:
    primary:
    secondary:
      -
    category_error_warnings:
      -

  core_claims:
    - claim:
      explanation_level: Derives | Explains | Accommodates | Postulates | Undeclared
      justification:
      evidence_or_quote:
      confidence: High | Medium | Low

  substrate_snapshot:
    ingredients:
    dynamics:
    reconstruction_claim:
    invariant_content:
    empirical_contact:

  falsifiability_snapshot:
    what_it_forbids:
      -
    what_would_count_against_it:
      -
    inverse_constraint: Strong | Moderate | Weak | None | Undeclared | Not Applicable
    discriminating_test:

  incompleteness_snapshot:
    unproven_core_claims:
      -
    open_questions:
      -
    effect_on_main_claim:

  flash_verdict:
    what_it_has_earned:
    what_it_has_not_earned:
    full_audit_needed: Yes | No
    next_questions:
      -
```

---

## 4. Flash Report Template

Use this Markdown output when a fast readable answer is preferred.

```markdown
# Flash Workbench Report: [Theory / Paper / Framework]

## 1. What it is
[One paragraph. Identify the framework without judging truth.]

## 2. Problem addressed
[State the physical problem and the hard constraints any solution must satisfy.]

## 3. Function class
- Primary class: [class]
- Secondary classes: [if any]
- Category-error warnings: [what not to compare it against]

## 4. Main claims and explanation level
| Claim | Level | Why | Evidence |
|---|---|---|---|
| ... | Derives / Explains / Accommodates / Postulates | ... | quote / section / not provided |

## 5. What it forbids
[List the observations, structures, assumptions, or rival theories it excludes.]

## 6. Falsifiability and inverse constraint
- Failure condition: [what would break or weaken it]
- Inverse constraint: Strong / Moderate / Weak / None / Undeclared / Not Applicable
- Discriminating test: [if any]

## 7. Main incompleteness
[What it cannot currently prove, decide, or reconstruct.]

## 8. Flash verdict
[What the framework has earned the right to claim; what it has not earned; whether it needs a full Extended audit.]
```

---

## 5. Flash Prompt for Any LLM

```text
You are applying the Flash Workbench, a quick first-pass methodology for clarifying physical theories.

Your task is not to decide whether the theory is true. Your task is to classify its claims, expose missing declarations, and identify whether a full audit is needed.

Analyze the provided source using this schema:
1. What is the theory/framework?
2. What physical problem does it address?
3. What hard constraints must any solution satisfy?
4. What is its function class?
5. What are its main claims?
6. For each claim, classify it as Derives, Explains, Accommodates, Postulates, or Undeclared.
7. What does the theory forbid?
8. What would count against it?
9. Can observations constrain its substrate or core assumptions? Score inverse constraint: Strong / Moderate / Weak / None / Undeclared / Not Applicable.
10. What are its open gaps or incompleteness declarations?
11. Give a Flash Workbench verdict: what it has earned, what it has not earned, and whether a full Extended Workbench audit is needed.

Rules:
- Do not call accommodation derivation.
- Do not infer truth from author confidence.
- If a field is not discussed, write Not Discussed or Undeclared.
- If the criterion does not apply to the function class, write Not Applicable.
- Provide quotes or source locations where possible.
```

---

## 6. Flash Anti-Drift Checklist

Before accepting a Flash output, check:

| Check | Pass condition |
|---|---|
| Function class first | The answer classifies the framework before scoring it. |
| No truth verdict | The answer does not say the theory is true or false. |
| Explanation ladder used | Claims are classified as Derives / Explains / Accommodates / Postulates. |
| No upgrade drift | “Suggests” was not upgraded to “derives.” |
| Missing fields explicit | Undeclared fields are not silently filled. |
| Falsifier present or absent | The answer states what would count against the theory, or says none is declared. |
| Inverse constraint stated | The answer says whether data can constrain the substrate. |
| Incompleteness included | Open claims and limitations are explicitly stated. |

---

# Part II — Extended Workbench

## 1. What The Workbench Is

The Workbench is a Gödel-humble, invariant-oriented methodology for clarifying theories in physics. It is a structured protocol for making theories inspectable.

It asks any theory the same hard questions:

- What is it made of?
- How do its ingredients behave?
- How does it recover known physics?
- What invariant content survives translation between descriptions?
- What does it derive rather than merely accommodate?
- What does it forbid?
- What would count against it?
- What can data constrain about its substrate?
- What can it not currently prove?

The Workbench is especially useful in domains where theories are mathematically sophisticated, conceptually overlapping, and easy to overstate: quantum gravity, cosmology, black-hole physics, foundations of quantum mechanics, high-energy theory, condensed-matter analogues, and beyond.

Its guiding principle is:

> A serious theory must declare what it is made of, what it explains, what it forbids, and what it cannot yet decide.

---

## 2. What The Workbench Is Not

The Workbench is not:

- a theory of everything;
- a theory generator;
- a theorem prover;
- a software product;
- a database;
- a replacement for peer review;
- a machine that tells us what is true;
- a scoring game that produces winners and losers;
- a formal system claiming completeness.

A low Workbench score does not mean a theory is false. It usually means the theory is incomplete, underspecified, overclaimed, or being compared against the wrong kind of framework.

---

## 3. The Two Foundational Axioms

### Axiom 1 — Invariant-Content Orientation

The Workbench seeks what survives valid translation among different frameworks.

In physics, the deepest content is often not the native language of any single theory. It is what remains stable when descriptions change.

Examples of invariant content include:

- anomaly content;
- conserved charges;
- entropy laws;
- scattering structures;
- universality classes;
- semiclassical limits;
- empirical constraints;
- low-energy effective behavior.

The Workbench therefore asks:

> What survives change of description?

This avoids the blind-men-and-the-elephant problem. A string theorist, loop quantum gravity theorist, causal-set theorist, holographer, amplitudes theorist, or condensed-matter theorist may each describe part of the same structure. The Workbench asks what survives translation among those descriptions.

### Axiom 2 — Incompleteness Humility

The Workbench cannot prove its own completeness. It cannot guarantee that its categories are final. It cannot decide every proposition about every possible future theory.

A future framework may require a new primitive, a new relation, a new form of reconstruction, or a new way of organizing physical content.

Therefore The Workbench must always allow:

- `Undeclared`
- `Not Discussed`
- `Undecidable / Open`
- `Not Applicable`
- `Outside Current Formalism`
- `Requires Future Proof`
- `Requires New Category`

This is not weakness. It is epistemic hygiene.

---

## 4. Objects of Analysis

The Workbench can analyze:

- a single paper;
- a theory;
- a research program;
- a proposed mechanism;
- a no-go argument;
- a computational method;
- a phenomenological endpoint;
- a dispute among multiple frameworks;
- a private hypothesis or draft theory.

The first task is always to determine what kind of object is being analyzed. Many physics debates remain confused because frameworks with different functions are treated as if they were rivals of the same type.

---

## 5. Function-Class Taxonomy

Function class is the most important first filter. A framework may belong to more than one class, but each role must be analyzed separately.

| Function class | Role | Examples | MVT applicable? |
|---|---|---|---|
| **Candidate ontology** | Proposes what is fundamentally real: constituents, degrees of freedom, structures. | Causal sets, spin networks, string/M-theory, fuzzball microstate geometries. | Partially; full MVT requires dynamics too. |
| **Candidate dynamics** | Proposes equations, amplitudes, channels, update rules, or constraints. | Spin foams, group field theory, string field theory, causal dynamical triangulations. | Partially; full MVT requires ontology too. |
| **Candidate ontology + dynamics** | Proposes both substrate and behavior as a standalone fundamental candidate. | Mature unification programs when both substrate and dynamics are declared. | Yes. |
| **Reconstruction mechanism** | Shows how effective observables, spacetime, entropy, matter, or geometry arise from deeper data. | AdS/CFT, island formula, tensor networks, holographic codes. | No, unless it also claims standalone ontology. |
| **Consistency filter / no-go constraint** | Rules out inadmissible combinations of assumptions or candidate theories. | Anomaly matching, swampland, positivity bounds, AMPS firewall argument. | No. |
| **Computational validator** | Computes, simulates, or tests consistency in a controlled regime. | Lattice gauge theory, conformal bootstrap, CDT simulations. | No. |
| **Effective theory** | Describes observed regimes without claiming fundamental completeness. | GR, Standard Model, EFT of inflation, low-energy EFTs. | No. |
| **Observer / measurement framework** | Explains records, reference frames, measurement, or observers. | Decoherence, quantum Darwinism, consistent histories, quantum reference frames. | Usually no; depends on claims. |
| **Diagnostic argument** | Exposes an inconsistent assumption set or trilemma. | Firewall-style arguments, paradox analyses. | No. |
| **Endpoint phenomenology** | Describes possible late-stage or boundary behavior. | Remnants, final-state proposals, evaporation endpoint models. | Usually no. |

### Function-Class Rule

Do not compare across function classes as if all frameworks are doing the same job.

A reconstruction mechanism should not be criticized for failing to provide ontology unless it claims to be an ontology. A consistency filter should not be criticized for failing to make a positive prediction unless it claims to be a predictive theory. An effective theory should not be dismissed for not being fundamental.

Use `Not Applicable` when a criterion does not apply to a framework’s function class.

---

## 6. The Extended Theory Interface: `S+`

The Workbench uses a default inspectability interface:

```text
S+ = (A, Ω, C, Φ, R, Σ, M, O)
```

This is not a claim that every possible theory must literally be built from these components. It is a sufficient checklist for making theories visible.

| Symbol | Name | What to declare | Diagnostic risk if missing |
|---|---|---|---|
| `A` | Observable algebra / structures / categories | What are the basic measurable or physically meaningful quantities? | Vague ontology. |
| `Ω` | Admissible states | What states are allowed? What is excluded? | Undefined state space. |
| `C` | Causal, pre-causal, relational, or ordering structure | How is before/after, adjacency, dependence, or causal order encoded? | Hidden background assumptions. |
| `Φ` | Dynamics / evolution / amplitudes / constraints | What changes, evolves, constrains, or generates histories? | Kinematics mistaken for physics. |
| `R` | Coarse-graining / renormalization / emergence map | How does micro become macro? How do scales relate? | No bridge between levels. |
| `Σ` | Symmetries, anomalies, consistency constraints, selection rules | What must be preserved? What is forbidden? | Consistency filters bypassed. |
| `M` | Reconstruction maps | How does known physics emerge from the substrate? | Rhetorical emergence. |
| `O` | Other / escape hatch | What vital component is not captured above? Why not? | Procrustean forcing or hidden category. |

### `O` Escape Hatch Template

```yaml
other_component:
  name:
  role:
  why_not_captured_by_S_plus:
  relation_to_existing_slots:
  evaluation_implication:
  does_it_require_new_workbench_category: Yes | No | Unclear
```

### Slot Scoring Rule

- A declared, controlled slot may score `Strong` or `Partial`.
- A vague slot scores `Weak`.
- A missing slot scores `Undeclared`.
- A slot explicitly unresolved for principled reasons scores `Undecidable / Open`.
- A slot irrelevant to the function class scores `Not Applicable`.

The Workbench does not punish honest gaps. It punishes hidden gaps.

---

## 7. The Eleven Essential Questions

Every Extended Workbench audit must answer these eleven questions.

| # | Question | Diagnostic purpose |
|---|---|---|
| 1 | What are the basic ingredients? | Prevents vague ontology. |
| 2 | How do those ingredients change, relate, or evolve? | Identifies dynamics or its absence. |
| 3 | How does the theory recover space, time, and gravity? | Tests reconstruction. |
| 4 | How does the theory recover known matter physics? | Prevents Standard Model bypass. |
| 5 | What invariant survives changes of description? | Identifies durable physical content. |
| 6 | Does it derive, explain, accommodate, or postulate known facts? | Prevents fake explanations. |
| 7 | What does the theory forbid? | Reveals exclusion power. |
| 8 | What observation, theorem, calculation, or consistency result would count against it? | Tests falsifiability. |
| 9 | Can known data constrain its basic ingredients? | Tests inverse constraint. |
| 10 | What concrete prediction, bound, or discriminating constraint does it offer? | Tests accountability. |
| 11 | What can it not currently prove, and why? | Enforces incompleteness transparency. |

A theory that cannot answer questions 7, 8, and 11 is not necessarily wrong, but it is not yet transparent enough to evaluate seriously.

---

## 8. Reconstruction Maps

A theory becomes physically meaningful when it can reconstruct known physics from its deeper ingredients.

The reconstruction family is:

```text
M = {
  M_geometry,
  M_gravity,
  M_matter,
  M_amplitudes,
  M_thermodynamics,
  M_observers,
  M_cosmology
}
```

Not every framework must address every sector. But it must be explicit about which sectors it addresses and which it does not.

Each reconstruction map must declare:

| Field | Question |
|---|---|
| Domain | What deep ingredients does the map use? |
| Codomain | What effective object does it reconstruct? |
| Approximation scheme | Perturbative, semiclassical, thermodynamic, large-N, numerical, dual, etc.? |
| Control parameter | `1/N`, `hbar`, coupling, energy scale, curvature, entropy, lattice spacing, etc.? |
| Validity regime | When is the reconstruction trusted? |
| Failure mode | When and how does it break down? |
| Invariant preserved | What exact, universal, or empirical invariant survives? |
| Inverse constraint | Can effective data constrain the underlying structure? |
| Evidence | Source quote, theorem, equation, calculation, simulation, or observation. |

### Emergence Rule

A theory claiming “spacetime emerges” must say:

- emerges from what;
- by what map;
- in what limit;
- using what approximation;
- with what control parameter;
- preserving what invariant;
- failing under what conditions;
- and whether observed spacetime can constrain the substrate.

Without this, “emergence” is rhetoric, not a Workbench-grade claim.

---

## 9. Invariant Content

The Workbench classifies invariant content into three main types.

| Type | Meaning | Examples |
|---|---|---|
| **Exact invariant** | Preserved under exact symmetry, equivalence, or duality. | Anomaly polynomial, conserved charge, dual partition function, exact symmetry relation. |
| **Universal invariant** | Stable across coarse-graining, RG flow, or universality class. | Entropy scaling, hydrodynamic laws, critical exponents. |
| **Empirical constraint** | Observed fact any viable theory must recover in tested regimes. | Standard Model content, tested Lorentz invariance, CMB spectrum, equivalence principle. |

Invariant claims must remain provisional and evidence-indexed. Cross-framework convergence increases confidence only when shared assumptions are checked.

### Convergence Tracker

```yaml
convergence:
  target:
  invariant_type: Exact | Universal | Empirical
  supporting_frameworks:
    -
  independence_score: High | Medium | Low
  shared_assumptions:
    -
  evidence_basis:
    - theorem | calculation | simulation | observation | duality | analogy
  confidence: High | Medium | Low
  revisable: true
  notes:
```

Convergence is not immortality. It is provisional evidential weight.

---

## 10. The Explanation Ladder

The Workbench distinguishes explanation from accommodation.

| Level | Name | Meaning | Unification implication |
|---|---|---|---|
| 4 | **Derives** | Follows from equations or constraints without extra input. | Strong unification claim permitted in declared regime. |
| 3 | **Explains** | Follows from a mechanism with reduced arbitrariness. | Partial unification claim. |
| 2 | **Accommodates** | Fits by choosing parameters, vacua, initial conditions, or model variants. | No deep unification claim. |
| 1 | **Postulates** | Inserted as an assumption. | No explanatory credit. |

### Accommodation Prohibition

Do not call accommodation derivation.

Examples:

- Selecting a Standard-Model-like vacuum from a large landscape usually **accommodates** the Standard Model.
- Forcing the Standard Model gauge group, chirality, anomaly cancellation, and matter content from deeper structure may **derive** or **explain** it.
- Simply assuming `SU(3) × SU(2) × U(1)` **postulates** it.

Accommodation is scientifically useful. It is not the same as explanation.

---

## 11. The Inverse Constraint

Forward prediction asks:

> Given the substrate, what observables follow?

The inverse constraint asks:

> Given observables, what can be constrained about the substrate?

A strong theory should not only compute forward; it should allow known or possible data to constrain its deeper ingredients.

| Score | Meaning |
|---|---|
| **Strong** | Specific observational, mathematical, or computational handles constrain substrate parameters in a controlled way. |
| **Moderate** | Some constraints exist in restricted regimes or special cases. |
| **Weak** | Constraints exist only in principle, idealized regimes, or inaccessible conditions. |
| **None** | No known path from data to substrate constraints. |
| **Undeclared** | The theory does not discuss inverse constraint. |
| **Not Applicable** | The function class is not expected to have a substrate. |

A theory with no inverse constraint is not automatically false. But it has weak empirical grip.

---

## 12. Diagnostic Rules A–J

The Workbench uses diagnostic rules to expose structural vulnerabilities. These are not all theorems. Each rule must carry an epistemic status.

| Rule | Name | Status | Trigger | Output |
|---|---|---|---|---|
| A | Inverse-Check | Definition rule | No path from observations to substrate. | Inverse constraint warning. |
| B | Duality-Humility | Category rule | Exact duality is used to privilege one side ontologically. | Ontological-priority warning. |
| C | Lorentz-Accounting | Structural constraint | Lorentz modification is claimed without protocol or bound. | Missing-bound warning. |
| D | Parameter-Space Warning | Diagnostic heuristic | Large parameter space is used to fit the target. | Accommodation warning. |
| E | Anomaly-Matching | Structural physics constraint | SM reconstruction does not address anomaly content. | Consistency warning. |
| F | Apples-to-Apples | Category rule | Different function classes are ranked on the same metric. | Category-error warning. |
| G | Empirical-Anchoring | Scoring rule | No empirical contact or tested-regime recovery. | No-unification-score warning. |
| H | Locality-Typing | Semantic hygiene rule | “Locality” or “nonlocality” is claimed without type. | Require algebraic / causal / metric distinction. |
| I | Convergence Tracker | Diagnostic heuristic | Multiple frameworks recover same result. | Check independence and shared assumptions. |
| J | Translation-Horizon | Epistemic metaphor / constraint | A framework claims final closure under all descriptions. | Humility warning. |

### Proof Status Labels

Use one of these labels whenever a rule is invoked:

- `definition_rule`
- `category_rule`
- `scoring_rule`
- `semantic_hygiene_rule`
- `diagnostic_heuristic`
- `community_standard`
- `structural_physics_constraint`
- `known_theorem`
- `theorem_candidate`
- `metaphor`

This prevents diagnostic rules from being overclaimed as mathematical theorems.

---

## 13. The Falsifiability Engine

Every serious proposal should produce at least one of the following outputs, unless its function class makes the criterion not applicable.

| Output | Meaning | Required declaration |
|---|---|---|
| **No-go theorem** | Rules out a class of theories or assumptions. | What class is ruled out, under what assumptions? |
| **Bound** | Limits a correction, coupling, scale, parameter, entropy, dimension, etc. | What quantity is bounded and by what evidence? |
| **Universality claim** | Says many systems flow to the same behavior. | What class flows to what invariant? |
| **Inverse constraint** | Says known or possible data restricts deeper ingredients. | What data constrains what substrate feature? |
| **Discriminating signature** | Predicts a measurable, calculable, or simulatable difference from alternatives. | What would differ from GR+SM or another baseline? |
| **Failure diagnostic** | States exactly what would break or severely weaken the theory. | What observation, theorem, or calculation counts against it? |
| **Incompleteness declaration** | States what remains unproven, undecidable, or uncontrolled. | What gap remains and what would close it? |

A framework producing none of these is not necessarily wrong. But it is not yet physics-grade in the Workbench sense. It may be descriptive, speculative, pre-theoretic, or purely mathematical.

The Workbench itself does not predict nature. It forces theories to declare what would make them fail.

---

## 14. Minimal Viable Theory Threshold

The MVT threshold applies only to frameworks claiming to be standalone fundamental or unification candidates. It should not be used to dismiss effective theories, reconstruction mechanisms, computational validators, or consistency filters merely because they are not full theories of everything.

A candidate crosses the MVT threshold only if it addresses all ten criteria.

| # | Criterion | Question |
|---|---|---|
| 1 | Substrate and dynamics declared | Are the fundamental variables and candidate dynamics explicitly stated? |
| 2 | Dependency choices declared | Which components are foundational, derived, emergent, optional, or gauge? |
| 3 | Reconstruction maps supplied | Are controlled maps provided for geometry, gravity, and matter? |
| 4 | GR and SM recovery | Does it recover General Relativity and the Standard Model in tested regimes? |
| 5 | Controlled semiclassical limit | Is there a systematic bridge to classical spacetime? |
| 6 | Consistency filters satisfied | Are anomaly, RG, EFT, black-hole, and other relevant consistency filters addressed? |
| 7 | Nontrivial inverse constraint | Can observational or calculational data constrain the substrate? |
| 8 | Discriminating test declared | Is there a test, calculation, simulation, theorem, or observation that distinguishes it from alternatives? |
| 9 | Exclusion power demonstrated | Does it forbid at least one plausible class of alternatives or observations? |
| 10 | Incompleteness transparency | Does it honestly state unresolved gaps and what would close them? |

### MVT Scoring

| Score | Meaning |
|---|---|
| **Strong** | Well-supported, controlled, and declared in the relevant regime. |
| **Partial** | Some sectors are covered, but significant gaps remain. |
| **Weak** | Mostly conjectural, extrapolated, or underdeveloped. |
| **Undeclared** | Missing declaration. Silence is not neutrality. |
| **Undecidable / Open** | Explicitly unresolved, with a reason and closure condition. |
| **Not Applicable** | Wrong function class for this criterion. |

### MVT Rule

MVT failure is not theory failure.

A framework can fail MVT and still be valuable as a reconstruction mechanism, consistency filter, computational validator, effective theory, observer framework, or diagnostic argument.

---

## 15. Incompleteness Declaration

Every Extended Workbench report must include an incompleteness declaration.

```yaml
incompleteness_declaration:
  unproven_core_claims:
    -
  undecidable_or_open_questions:
    -
  uncontrolled_approximations:
    -
  missing_reconstruction_maps:
    -
  effect_on_unification_claim:
  what_would_close_the_gap:
    -
  predictions_or_results_remaining_valid_despite_gap:
    -
  confidence_in_declaration: High | Medium | Low
```

A theory that admits its gaps is easier to evaluate than one that hides them. The Workbench rewards honest incompleteness.

---

## 16. Evidence Discipline

Every populated field in an LLM-assisted Workbench audit should identify its evidential status.

| Evidence status | Meaning |
|---|---|
| `explicit_quote` | The source directly states the claim. |
| `equation_or_derivation` | The claim follows from a displayed equation or derivation in the source. |
| `author_claim` | The authors claim it, but the Workbench has not verified it. |
| `reviewer_inference` | The analyst infers it from the source. |
| `community_context` | The claim relies on background knowledge outside the source. |
| `not_discussed` | The source does not address the field. |
| `unsupported` | The LLM or analyst cannot support the claim. |

### Evidence Rule

Do not turn “the paper claims X” into “X is established.”

The trusted record must distinguish:

1. The paper claims X.
2. The reviewer accepts that the paper claims X.
3. The reviewer does or does not accept X as established.

These are different statements.

---

## 17. LLM Operating Protocol

The Workbench may use any LLM, but the LLM is not an authority.

### LLM Can Do

- parse papers;
- extract claims;
- identify assumptions;
- map claims into `S+`;
- draft answers to the eleven questions;
- propose explanation-ladder classifications;
- flag missing declarations;
- detect overclaim language;
- propose preliminary scorecards;
- compare function classes;
- produce structured YAML or Markdown.

### LLM Cannot Do

- judge truth;
- certify the scorecard;
- verify its own hallucinations;
- replace physical intuition;
- replace expert review;
- decide whether a theory is finally correct.

### Human Role

The human reviewer must:

- verify extractions against the source;
- correct overclaims;
- assign final explanation levels;
- judge function class;
- adjudicate inverse constraints;
- certify or reject scorecards;
- decide whether the analysis itself is fair.

The rule:

> The human is the referee. The LLM is the clerk.

---

## 18. Anti-Drift Rules for LLMs

These rules are mandatory when using LLMs to produce Workbench reports.

1. **Structured output only.** Do not allow free-form essays until the schema is complete.
2. **No silent inference.** Each populated field must say whether it is explicit, inferred, or unsupported.
3. **No explanation upgrades.** Do not upgrade `Accommodates` to `Explains`, or `Explains` to `Derives`, without evidence.
4. **No function-class drift.** A framework cannot be scored as a TOE candidate unless it claims ontology plus dynamics.
5. **No popularity weighting.** Do not treat community prominence as evidence of validity.
6. **No source laundering.** Do not turn author rhetoric into Workbench findings.
7. **No completeness pretense.** Always include incompleteness for both theory and analysis.
8. **No missing-field smoothing.** Missing data must remain visible.
9. **No overbroad verdict.** Verdicts must be regime-bounded.
10. **Adversarial second pass required.** Re-read the output assuming the authors and the LLM overclaimed.

---

## 19. Paper-to-Workbench Workflow

Use this process for papers, talks, or theory documents.

| Stage | Actor | Output |
|---|---|---|
| 1. Ingest | Human / LLM | Source text, metadata, stated target problem. |
| 2. Frame | Human / LLM | Problem, hard constraints, completion conditions. |
| 3. Parse | LLM / reviewer | Sections, equations, claims, definitions. |
| 4. Extract | LLM | Draft `S+`, claims, invariants, reconstructions. |
| 5. Validate | Human / rules | Unsupported fields, overclaims, category errors. |
| 6. Diagnose | Human / LLM | Diagnostic rule triggers A–J. |
| 7. Score | Human-adjudicated | Explanation ladder, inverse constraint, MVT. |
| 8. Declare | Human-adjudicated | Incompleteness declaration. |
| 9. Report | Human / LLM | Flash or Extended Workbench report. |
| 10. Review | Human / second LLM | Adversarial audit and corrections. |
| 11. Archive | Human | Trusted claim map with provenance. |

---

## 20. Extended Extraction Schema

Use this schema when the goal is cross-LLM uniformity.

```yaml
workbench_extended_report:
  metadata:
    target_name:
    source_type: paper | talk | theory_note | dispute | research_program | other
    source_identifier:
    analyst:
    llm_used:
    date:
    analysis_mode: Flash | Extended
    confidence_overall: High | Medium | Low

  problem_frame:
    physical_problem:
    target_sector:
    hard_constraints:
      - constraint:
        evidence:
    completion_conditions:
      -
    scope_boundaries:
      -

  function_class:
    primary_class:
    secondary_classes:
      -
    claims_standalone_unification: Yes | No | Ambiguous
    category_errors_to_avoid:
      -
    applicable_scorecards:
      - MVT | Reconstruction | ConsistencyFilter | EffectiveTheory | DiagnosticArgument | Other

  S_plus:
    A_observables:
      declaration:
      evidence_status:
      evidence:
      score:
    Omega_states:
      declaration:
      evidence_status:
      evidence:
      score:
    C_causal_or_relational_structure:
      declaration:
      evidence_status:
      evidence:
      score:
    Phi_dynamics:
      declaration:
      evidence_status:
      evidence:
      score:
    R_coarse_graining_or_emergence:
      declaration:
      evidence_status:
      evidence:
      score:
    Sigma_symmetries_constraints:
      declaration:
      evidence_status:
      evidence:
      score:
    M_reconstruction_maps:
      geometry:
      gravity:
      matter:
      amplitudes:
      thermodynamics:
      observers:
      cosmology:
    O_other:
      name:
      role:
      why_not_captured:
      evaluation_implication:

  eleven_questions:
    basic_ingredients:
    dynamics_or_relations:
    spacetime_gravity_recovery:
    matter_recovery:
    invariant_content:
    explanation_status_summary:
    forbidden_alternatives:
    falsifiers_or_weakeners:
    inverse_constraints:
    predictions_or_discriminators:
    incompleteness:

  reconstruction_maps:
    - sector:
      domain:
      codomain:
      approximation_scheme:
      control_parameter:
      validity_regime:
      failure_mode:
      invariant_preserved:
      inverse_constraint:
      evidence:
      score:

  invariants:
    exact:
      - target:
        evidence:
        confidence:
    universal:
      - target:
        evidence:
        convergence_tracker:
    empirical:
      - target:
        tested_regime:
        evidence:

  claims:
    - claim:
      source_location:
      author_language:
      workbench_restatement:
      explanation_level: Derives | Explains | Accommodates | Postulates | Undeclared
      evidence_status:
      assumptions_added:
        -
      regime:
      confidence:

  inverse_constraint:
    overall_score: Strong | Moderate | Weak | None | Undeclared | Not Applicable
    per_component:
      - component:
        relevant_data:
        constraint_path:
        accessibility:
        strength:
        evidence:

  diagnostic_rules:
    A_inverse_check:
      triggered: Yes | No | Not Applicable
      status_label:
      justification:
    B_duality_humility:
      triggered:
      status_label:
      justification:
    C_lorentz_accounting:
      triggered:
      status_label:
      justification:
    D_parameter_space_warning:
      triggered:
      status_label:
      justification:
    E_anomaly_matching:
      triggered:
      status_label:
      justification:
    F_apples_to_apples:
      triggered:
      status_label:
      justification:
    G_empirical_anchoring:
      triggered:
      status_label:
      justification:
    H_locality_typing:
      triggered:
      status_label:
      justification:
    I_convergence_tracker:
      triggered:
      status_label:
      justification:
    J_translation_horizon:
      triggered:
      status_label:
      justification:

  falsifiability_engine:
    no_go_theorem:
    bound:
    universality_claim:
    inverse_constraint:
    discriminating_signature:
    failure_diagnostic:
    incompleteness_declaration:

  MVT_scorecard:
    applicable: Yes | No
    reason_if_not_applicable:
    criteria:
      substrate_and_dynamics:
      dependency_choices:
      reconstruction_maps:
      GR_and_SM_recovery:
      semiclassical_limit:
      consistency_filters:
      inverse_constraint:
      discriminating_test:
      exclusion_power:
      incompleteness_transparency:
    critical_gaps:
      -

  incompleteness_declaration:
    unproven_core_claims:
      -
    undecidable_or_open_questions:
      -
    uncontrolled_approximations:
      -
    missing_reconstruction_maps:
      -
    effect_on_unification_claim:
    what_would_close_the_gap:
      -
    results_remaining_valid_despite_gap:
      -

  category_errors_exposed:
    - false_comparison:
      why_invalid:
      valid_comparison_instead:

  adversarial_review:
    likely_overclaims:
      -
    downgraded_claims:
      - claim:
        from:
        to:
        reason:
    unsupported_fields:
      -
    remaining_uncertainties:
      -

  final_verdict:
    what_it_is:
    what_it_has_genuinely_accomplished:
    what_it_has_not_earned:
    live_question:
    next_evidence_needed:
    analysis_limitations:
```

---

## 21. Extended Report Template

```markdown
# Extended Workbench Report: [Theory / Paper / Framework]

## 1. Metadata
- Source:
- Domain:
- Analysis mode:
- Confidence:

## 2. Problem frame
[State problem, hard constraints, and completion conditions.]

## 3. Function class
[Primary and secondary classes. State whether MVT applies.]

## 4. `S+` substrate mapping
| Slot | Declaration | Evidence | Score |
|---|---|---|---|
| A | ... | ... | ... |
| Ω | ... | ... | ... |
| C | ... | ... | ... |
| Φ | ... | ... | ... |
| R | ... | ... | ... |
| Σ | ... | ... | ... |
| M | ... | ... | ... |
| O | ... | ... | ... |

## 5. Eleven essential questions
[Answer all eleven. Use Undeclared / Not Applicable where needed.]

## 6. Reconstruction maps
[Map each claimed reconstruction sector.]

## 7. Invariant content
[Exact, universal, empirical; include convergence tracker where relevant.]

## 8. Explanation ladder
| Claim | Level | Reason | Evidence | Regime |
|---|---|---|---|---|

## 9. Inverse constraint
[Score and explain whether data can constrain substrate.]

## 10. Diagnostic rules A–J
[State triggered rules and implications.]

## 11. Falsifiability engine
[No-go, bound, universality, inverse constraint, discriminating signature, failure diagnostic, incompleteness.]

## 12. MVT scorecard
[Only if applicable; otherwise explain why Not Applicable.]

## 13. Incompleteness declaration
[Unproven claims, open questions, effect on core claims, closure conditions.]

## 14. Category errors exposed
[False comparisons, invalid rankings, accommodation-as-derivation claims.]

## 15. Adversarial review
[Downgrades, unsupported fields, missing evidence, likely LLM drift.]

## 16. Workbench verdict
[What the framework is, what it has earned, what it has not earned, and what remains live.]

## 17. Limitations of this analysis
[State source limits, expertise limits, unavailable evidence, and undecidable parts.]
```

---

## 22. Applying The Workbench to Different Theory Types

### Candidate Ontologies

Press hardest on:

- declared substrate;
- dynamics;
- reconstruction maps;
- GR and SM recovery;
- inverse constraint;
- controlled semiclassical limit;
- incompleteness declaration.

Common failure: proposing fundamental ingredients without showing how spacetime, gravity, and matter emerge.

### Reconstruction Mechanisms

Press hardest on:

- domain and codomain;
- validity regime;
- control parameters;
- what substrate is assumed rather than supplied;
- whether reconstruction is bidirectional;
- what physical ontology, if any, the mechanism implies.

Do not score them as failed TOEs unless they claim TOE status.

### Consistency Filters and Diagnostic Arguments

Press hardest on:

- assumptions;
- theorem status;
- scope of exclusion;
- what class of theories is ruled out;
- whether loopholes remain;
- whether the result is a theorem, conjecture, heuristic, or argument.

Do not ask them to provide full ontology unless they claim to.

### Effective Theories

Press hardest on:

- tested regime;
- empirical success;
- breakdown scale;
- parameters;
- relation to deeper theories;
- what is deliberately not explained.

Do not penalize them for not being fundamental.

### Computational Validators

Press hardest on:

- what is computed;
- assumptions and discretizations;
- convergence controls;
- finite-size effects;
- numerical regime;
- what the computation validates and what it does not.

### Observer Frameworks

Press hardest on:

- records;
- reference frames;
- measurement assumptions;
- ontology of observers;
- whether the framework explains or postulates the Born rule, classicality, or objectivity.

### Endpoint Phenomenology

Press hardest on:

- consistency with EFT;
- conservation laws;
- entropy accounting;
- observable signatures;
- whether it is a mechanism or a placeholder.

---

## 23. Worked Micro-Example: Black-Hole Information Paradox

The Workbench clarifies that commonly named “solutions” are often not direct competitors.

| Proposal | Function class | Workbench clarification |
|---|---|---|
| Island formula | Reconstruction mechanism | Computes Page-curve behavior in semiclassical gravitational path integrals; does not by itself identify the microscopic substrate. |
| Fuzzballs | Candidate ontology / microphysical proposal | Proposes microstate structure; strongest in controlled regimes; broader dynamics and astrophysical generality remain open. |
| AMPS firewall | Consistency filter / diagnostic argument | Exposes tension among unitarity, EFT outside the horizon, and smooth horizons; not itself a positive ontology. |
| Remnants | Endpoint phenomenology | A possible endpoint class; must survive entropy, EFT, and observational consistency checks. |

The pseudo-question “Which one solves the paradox?” is often malformed. A better Workbench question is:

> Which proposal supplies a controlled inverse constraint from Page-curve behavior or black-hole observables back to a fundamental substrate, while satisfying consistency filters and reconstructing semiclassical physics in the appropriate regime?

---

# Part III — Evaluation of the Workbench Itself

## 1. Overall Goal

The Workbench’s overall goal is not to automate truth-finding. Its goal is to make theoretical claims inspectable, comparable, and accountable.

It does this by forcing each theory to declare:

- its function class;
- its substrate or lack of substrate;
- its dynamics or lack of dynamics;
- its reconstruction maps;
- its invariant content;
- its explanation status;
- its inverse constraints;
- its exclusion power;
- its falsifiability outputs;
- its incompleteness.

The deepest value of The Workbench is that it dissolves false debates. Many “competing” theories are not competing at all; they occupy different functional roles. The Workbench does not solve physics problems directly. It clarifies which problem is actually being discussed.

---

## 2. Accuracy Assessment

The Workbench is accurate as a **methodological clarification framework** when used with discipline.

Its strongest accurate claims are:

1. **Function-class clarity prevents category errors.** This is a robust methodological point.
2. **Accommodation is not derivation.** This is essential for preventing exaggerated unification claims.
3. **Missing inverse constraints weaken empirical grip.** A framework that cannot be constrained by data has limited physical accountability.
4. **Reconstruction maps need domains, codomains, regimes, and failure modes.** Without these, emergence claims are underspecified.
5. **Incompleteness transparency is better than hidden gaps.** This improves epistemic hygiene.
6. **LLMs need structured prompts and adversarial review.** Without this, they will tend to summarize, over-agree, and smooth away missing fields.

However, The Workbench is not accurate if treated as a physical theory, a proof system, or an authority. Its rules are a mixture of definitions, category disciplines, heuristics, structural physics constraints, and metaphors. They must not be overclaimed as theorems unless separately proven.

---

## 3. Limitations of The Workbench

The limitations are not optional footnotes. They are central to the methodology.

### 3.1 It Cannot Tell Which Theory Is True

The Workbench can clarify what a theory claims and whether its claims are earned. It cannot decide final truth. If two theories both pass relevant criteria, deciding between them requires new data, new mathematics, or new theoretical insight.

### 3.2 It Cannot Generate New Dynamics

The Workbench can identify missing dynamics. It cannot invent the correct equations of motion, amplitudes, channels, or constraints.

### 3.3 It Cannot Certify Its Own Completeness

The categories in this document may be incomplete. Future physics may require new function classes, new reconstruction concepts, or new scoring dimensions.

The `O` slot exists because the Workbench must remain revisable.

### 3.4 It Can Be Misused as Bureaucracy

Over-structuring early speculation can kill creativity. The Workbench is best used after a proposal has enough content to analyze. It is a clarification discipline, not a brainstorming substitute.

### 3.5 It Depends on Source Quality

If the source paper is vague, promotional, incomplete, or mathematically inaccessible to the analyst, the Workbench report will inherit those limits. The correct output in that case is not a confident score but explicit uncertainty.

### 3.6 It Depends on Human Judgment

Explanation levels, function classes, and inverse-constraint strength often require expert judgment. Two honest analysts may disagree. The Workbench should expose that disagreement rather than hide it.

### 3.7 It Is Vulnerable to LLM Failure Modes

LLMs may:

- hallucinate missing details;
- overstate author claims;
- convert “suggests” into “derives”;
- reflect community popularity as if it were evidence;
- miss subtle mathematical assumptions;
- fail to distinguish a theorem from a conjecture;
- smooth away incompleteness.

The adversarial review pass is mandatory because of this.

### 3.8 It Cannot Replace Peer Review or Physical Intuition

The Workbench clarifies arguments. It does not replace expert physics, creativity, experimental design, or mathematical proof.

### 3.9 It Cannot Prove a Theory False by Itself

It can show that a theory is incomplete, unfalsifiable, weakly constrained, or overclaimed. Those are serious findings, but they are not the same as empirical falsification.

### 3.10 It May Penalize Useful Non-Fundamental Frameworks If Misapplied

Using MVT criteria on an effective theory, computational validator, or reconstruction mechanism can produce unfair results. The function-class rule exists to prevent this.

### 3.11 It Can Overemphasize Explicitness

Some mature research programs contain implicit shared knowledge that papers do not restate. The Workbench should mark missing declarations, but human reviewers may need to supply community context carefully and label it as such.

### 3.12 It Cannot Guarantee Cross-LLM Uniformity Without Enforcement

The Extended schema reduces drift but does not eliminate it. Uniform outputs require strict prompts, evidence fields, adversarial review, and human certification.

---

## 4. When Not to Use The Workbench

Avoid or delay The Workbench when:

- the idea is in early brainstorming and not yet structured;
- the work is purely mathematical and makes no physical claim;
- the question is pedagogical rather than evaluative;
- the framework is already known to be an effective theory and no fundamental claim is being made;
- the analyst lacks enough source material to avoid speculation;
- the method would be used to prematurely dismiss creative hypotheses.

---

## 5. Final Workbench Meta-Verdict

The Workbench is best understood as a **referee’s grammar for theoretical physics**.

It does not discover new physics. It does not certify truth. It does not replace physicists. Its value is that it forces theoretical claims into a form where hidden assumptions, category errors, missing inverse constraints, accommodation disguised as derivation, and unresolved gaps become visible.

The Flash version gives fast triage. The Extended version gives a full audit trail. Together, they provide a two-speed methodology that LLMs can follow consistently while leaving final judgment to human reviewers.

The Workbench succeeds if, after applying it, everyone can see:

- what kind of framework is being discussed;
- what it genuinely explains;
- what it merely accommodates;
- what it forbids;
- what would count against it;
- and what remains open.

That is not final truth. It is disciplined visibility.

---

# Appendix A — One-Prompt Flash Invocation

```text
Apply the Flash Workbench to the attached theory or paper.

Do not decide whether it is true. Classify its claims.

Return:
1. What it is.
2. Problem addressed.
3. Function class.
4. Main claims with explanation levels: Derives / Explains / Accommodates / Postulates.
5. What it forbids.
6. What would count against it.
7. Inverse constraint score: Strong / Moderate / Weak / None / Undeclared / Not Applicable.
8. Main incompleteness.
9. Flash verdict: what it has earned, what it has not earned, and whether a full Extended audit is needed.

Rules: do not call accommodation derivation; mark missing fields; distinguish author claims from established results.
```

---

# Appendix B — One-Prompt Extended Invocation

```text
Apply the Extended Workbench to the attached theory, paper, or dispute.

Your purpose is not to decide whether the theory is true. Your purpose is to produce a structured audit that exposes function class, substrate commitments, reconstruction maps, explanation status, inverse constraints, falsifiability, category errors, and incompleteness.

Output in the following sections:
1. Metadata and source scope.
2. Problem frame: physical problem, hard constraints, completion conditions.
3. Function class: primary, secondary, MVT applicability, category-error warnings.
4. S+ mapping: A, Ω, C, Φ, R, Σ, M, O. For each field include declaration, evidence, evidence status, and score.
5. Eleven essential questions.
6. Reconstruction maps: domain, codomain, approximation, control parameter, validity regime, failure mode, invariant preserved, inverse constraint.
7. Invariant content: exact, universal, empirical; include convergence tracker where relevant.
8. Explanation ladder for every major claim.
9. Inverse constraint analysis.
10. Diagnostic Rules A–J, with triggered status and proof-status label.
11. Falsifiability engine outputs.
12. MVT scorecard if applicable; otherwise explain why not applicable.
13. Incompleteness declaration.
14. Category errors exposed.
15. Adversarial review: downgrade overclaims, flag unsupported fields, identify remaining uncertainty.
16. Final Workbench verdict.
17. Limitations of this analysis.

Rules:
- Every populated field must be explicit_quote, equation_or_derivation, author_claim, reviewer_inference, community_context, not_discussed, or unsupported.
- Do not upgrade suggests to derives.
- Do not infer truth from author confidence.
- Do not score wrong function classes on MVT criteria.
- Use Undeclared, Not Applicable, or Undecidable/Open rather than guessing.
- The final verdict must say what the theory has earned the right to claim and what remains to be done.
```

---

# Appendix C — Adversarial Review Prompt

```text
Review the previous Workbench output adversarially.

Assume the authors and the LLM may have overclaimed.

Check specifically:
1. Did any claim get upgraded from Accommodates to Explains or Derives without evidence?
2. Did any author claim get treated as established fact?
3. Did the report score a reconstruction mechanism, consistency filter, effective theory, or computational validator as if it were a standalone TOE candidate?
4. Did any missing field get silently filled by inference?
5. Is the inverse constraint too generous?
6. Does every reconstruction claim state domain, codomain, approximation, control parameter, validity regime, and failure mode?
7. Does the theory say what it forbids?
8. Does it state what would count against it?
9. Does the incompleteness declaration include unproven core claims and what would close each gap?
10. Are the limitations of the analysis itself stated?

Revise the report conservatively. When uncertain, downgrade the explanation level or mark the field Undeclared / Undecidable / Not Applicable.
```

---

# Appendix D — Minimal Daily-Use Checklist

For quick everyday use, ask only these seven questions:

1. What kind of thing is this: ontology, dynamics, reconstruction, consistency filter, effective theory, validator, observer framework, diagnostic argument, or endpoint phenomenology?
2. What does it claim to explain?
3. Does it derive, explain, accommodate, or postulate that claim?
4. What does it forbid?
5. What would count against it?
6. Can data constrain its substrate or assumptions?
7. What can it not currently prove?

If an answer cannot survive those seven questions, it is not ready for a full Workbench audit.
