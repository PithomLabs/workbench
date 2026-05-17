# The Workbench
## A Methodology for Clarifying Theories in Physics

*Version 1.0 — Incomplete by Design*

---

## Preface

This document is a working methodology, not a software specification and not a theory of physics. The Workbench is a structured set of questions, classification schemes, and diagnostic rules that, when applied to any proposed theory or candidate framework in physics, force the argument's logical structure into the open — where it can be examined, compared, and honestly scored.

The Workbench does not tell you which theory is correct. It tells you what kind of claim each theory is making, what it has genuinely derived versus merely accommodated, where its explanatory structure is solid and where it is hiding gaps, and which apparent disagreements between theories are real disagreements versus category confusion.

Any competent language model can serve as the analytical engine. The Workbench provides the methodology; the LLM provides the reasoning labor. The analyst provides the judgment about whether the outputs are being applied faithfully.

One foundational principle governs everything that follows: **no framework rich enough to evaluate fundamental theories can certify its own completeness**. The Workbench is permanently incomplete and explicitly revisable. It is useful precisely because it is honest about this.

---

## Part I: What The Workbench Is

### 1.1 The core problem it solves

Physics debates — particularly in fundamental and theoretical physics — suffer from a specific kind of confusion that is distinct from the honest difficulty of hard problems. It is the structural confusion of participants operating at different levels of a question without a shared vocabulary for noticing this. Two physicists argue about which theory "solves" a problem. One is proposing an ontology; the other is proposing a computational tool. Neither is wrong, but they are not answering the same question. The debate continues for decades.

The Workbench solves this by enforcing clarity about:

- What kind of thing a theory is (its function class)
- What it has actually proven versus what it has inserted by assumption
- Whether it can be run backwards from data to constrain its own foundations
- What it forbids, not just what it allows
- Where it is honestly incomplete versus where it is hiding incompleteness

### 1.2 What The Workbench is not

It is not a theory of physics. It makes no claim about what is fundamentally real.

It is not a scoring system that produces winners and losers. A low score means a theory is incomplete, not wrong.

It is not a software system, a database, or an automated reasoning engine. It is a methodology — a structured protocol for disciplined analysis that can be carried out by a human analyst, an LLM, or both in collaboration.

It is not a formal system in the mathematical sense. Its diagnostic rules are not derived theorems. They are disciplined heuristics with varying epistemic statuses, each of which is stated explicitly.

### 1.3 The role of an LLM

A language model is well-suited to applying The Workbench because the methodology's primary operations — classification, gap detection, comparison, and structured summarization — are exactly the operations LLMs perform competently. The analyst supplies the structured prompts from this document. The LLM applies them to the theory under examination. The analyst reviews the outputs for faithfulness to the methodology and exercises final judgment.

The LLM should not be asked to determine whether a theory is physically correct. It should be asked to classify, score, and expose gaps according to The Workbench's criteria. These are distinct tasks.

---

## Part II: Core Concepts

Before applying The Workbench, the analyst must understand its six core concepts. These are not optional background — they are the operational vocabulary of every step that follows.

### 2.1 Function Class

The single most clarifying question The Workbench asks about any framework is: what is it actually doing? The answer is its function class, and comparing theories across function classes is the most common source of structural confusion in theoretical physics.

There are seven recognized function classes:

**Candidate ontology.** Proposes what is fundamentally real — the basic constituents, degrees of freedom, or structure of the universe. Examples: causal sets, loop quantum gravity spin networks, string/M-theory, fuzzball microstate geometries.

**Candidate dynamics.** Proposes the equations, amplitudes, or update rules that govern how the ontological constituents evolve. Examples: group field theory, spin foam amplitudes, causal dynamical triangulations, string field theory. Note that ontology and dynamics are often bundled in the same framework but are conceptually distinct — a framework may have well-developed ontology and underdeveloped dynamics, or vice versa.

**Reconstruction mechanism.** Proposes how effective observables, spacetime geometry, or physical quantities arise from more fundamental substrate data. Examples: AdS/CFT, the Island formula, tensor networks, holography. A reconstruction mechanism answers "how do we compute X from Y?" — it does not answer "what is Y made of?"

**Consistency filter.** Proposes constraints that rule out inadmissible theories or combinations of assumptions. Examples: anomaly matching conditions, swampland conjectures, EFT positivity bounds, the AMPS firewall argument. A consistency filter eliminates; it does not construct.

**Effective theory.** Describes physics in a regime without claiming to be the fundamental description. Examples: General Relativity, the Standard Model, EFT of inflation. An effective theory's failure to be fundamental is not a defect.

**Computational validator.** Tests whether a theory is mathematically self-consistent or numerically viable. Examples: lattice gauge theory, conformal bootstrap, CDT simulations.

**Observer framework.** Addresses how records, reference frames, and measurement arise. Examples: decoherence, quantum Darwinism, consistent histories, quantum reference frames.

**The rule:** Never compare theories across function classes on a shared metric unless you have first checked that the metric applies to both classes. Asking "which is better, AdS/CFT or loop quantum gravity?" is a category error: one is a reconstruction mechanism, the other is a candidate ontology. They could both be correct simultaneously.

### 2.2 The Explanation Ladder

When a theory claims to "explain" a physical phenomenon, The Workbench demands you classify what kind of explanation is actually being offered. There are four levels:

**Derives (Level 4).** The phenomenon follows from the theory's equations and constraints with no additional input. No free parameters were adjusted, no extra assumptions inserted. This is the strongest form of explanation.

**Explains (Level 3).** The phenomenon follows from a mechanism that the theory describes, with fewer free parameters than alternatives. There is genuine reduction of arbitrariness, but some input is still required.

**Accommodates (Level 2).** The phenomenon fits within the theory by choosing appropriate values for free parameters. The theory is consistent with the phenomenon but did not predict it. Fine-tuning is allowed. This is legitimate physics but it does not constitute unification or deep explanation.

**Postulates (Level 1).** The phenomenon is inserted as an assumption. The theory does not explain it; it takes it as given.

**The rule:** Never call accommodation "derivation." A theory that accommodates the Standard Model by scanning a landscape of 10^500 vacua has not explained the Standard Model. This is legitimate physics, but it is not unification.

### 2.3 The Inverse Constraint

Every theory makes forward predictions: given the substrate, compute observables. The inverse constraint is the reverse question: given observables, can we constrain the substrate?

A theory with a strong inverse constraint allows data to actually tell us something about its fundamental degrees of freedom. A theory with no inverse constraint can be consistent with any data — which means the data cannot help us test or refine it.

Inverse constraint strength is scored as:

- **Strong:** A specific observational handle exists and constrains the substrate parameters. The direction from data to substrate is controlled.
- **Moderate:** Some constraint exists in restricted regimes or special cases.
- **Weak:** The constraint exists in principle but is practically inaccessible, or applies only to highly idealized cases far from physical reality.
- **None:** No known path from observational data to substrate constraints.

**The rule:** A theory that cannot be constrained by any data in any regime is not yet physics. It may be mathematics, it may be a consistent framework, but it has not made contact with the physical world in a way that allows revision.

### 2.4 The Minimal Viable Theory Threshold

The MVT threshold is a checklist of ten criteria a theory must satisfy to be taken seriously as a fundamental candidate — not just as a useful tool, not just as an interesting framework, but as a genuine contender for describing reality at the deepest level.

Failing the MVT threshold does not mean a theory is worthless. It means it is incomplete. Most current theories fail multiple criteria. Honest identification of which criteria are failed — and why — is more useful than vague claims of completeness.

The ten MVT criteria are:

1. **Substrate declared.** The fundamental variables and candidate dynamics are explicitly stated. No undefined "stuff."
2. **Dependency choices declared.** The theory states which of its components are foundational and which are derived.
3. **Reconstruction maps supplied.** Controlled maps exist showing how spacetime geometry, gravity, and matter arise from the substrate, with declared approximation schemes, validity regimes, and failure modes.
4. **GR and SM recovery.** General Relativity and the Standard Model are recovered in tested regimes.
5. **Controlled semiclassical limit.** A controlled approximation scheme connects the substrate to classical physics.
6. **Consistency filters satisfied.** Anomaly cancellation, RG consistency, EFT consistency, and black hole thermodynamic consistency are satisfied.
7. **Nontrivial inverse constraint.** At least one path exists from observational data to constraints on substrate parameters.
8. **Discriminating test declared.** At least one test — observational, computational, or mathematical — would distinguish this theory from alternatives.
9. **Exclusion power demonstrated.** The theory forbids at least one plausible class of alternatives. A theory that is compatible with everything explains nothing.
10. **Incompleteness declared.** The theory explicitly states which of its core claims are currently unproven, undecidable within its own formalism, or dependent on uncontrolled approximations — and whether these gaps affect its central claims.

### 2.5 The Scorecard

Every criterion in The Workbench is scored on a five-point scale:

- **Strong:** Well-supported, controlled, and declared.
- **Partial:** Some sectors covered; significant gaps remain.
- **Weak:** Mostly conjectural, extrapolated, or underdeveloped.
- **Undeclared:** The theory does not address this criterion. This is scored lower than Weak — silence is not neutrality.
- **Undecidable / Open:** The theory explicitly acknowledges this as an unresolved question that may not be answerable within current mathematics or physics. This scores higher than Undeclared — honesty about limits is treated as a virtue, not a defect.

**The rule:** A theory that scores Undecidable with a clear declaration of why and what would close the gap is ranked above a theory that scores Weak without acknowledgment. The Workbench rewards epistemic hygiene.

### 2.6 The Invariant Hierarchy

Not all physical facts are equal. The Workbench classifies the content any fundamental theory must reproduce into three types:

**Exact invariants.** Preserved under exact symmetry, equivalence, or duality. Examples: anomaly polynomials, conserved charges, the CPT theorem, KMS conditions. Any admissible theory must reproduce these exactly.

**Universal invariants.** Preserved across renormalization group flow or universality classes. Examples: black hole entropy scaling, critical exponents, hydrodynamic laws. These are less rigid than exact invariants — a future theory may refine them — but they carry strong evidential weight.

**Empirical constraints.** The hard observational floor. Any admissible theory must reproduce the Standard Model content, tested Lorentz invariance, the CMB spectrum, the equivalence principle, and black hole thermodynamics in their tested regimes. Failure here is disqualifying.

The invariant hierarchy matters because it tells you what kind of agreement counts. A theory that reproduces an exact invariant by construction has done something different from a theory that reproduces an empirical constraint by parameter fitting.

---

## Part III: The Methodology — Step by Step

The Workbench is applied in eight steps. Each step has a defined output. Each can be executed by prompting an LLM with the structured language provided below.

### Step 0 — Frame the dispute

Before analyzing any theory, state the question it is answering. This sounds obvious. It is not. Many debates in theoretical physics persist because participants are answering different questions while believing they share one.

The framing step requires:

1. State the physical phenomenon or problem the theory addresses.
2. Identify the load-bearing constraint — the no-go result, trilemma, or established observation that any solution must satisfy.
3. State what "solving" the problem would require.

**Prompt for LLM:**

> "I want to analyze [theory/framework] using a structured methodology. Before scoring, I need you to: (1) state in one paragraph what physical problem or question this theory is addressing, (2) identify any established no-go results, trilemmas, or hard constraints that any proposed solution must satisfy, and (3) state precisely what a complete solution would need to provide — not what this theory provides, but what the problem demands."

**Expected output:** A clear problem statement, a list of hard constraints, and a specification of what completion would look like. If the LLM cannot produce this, the theory's problem statement is itself unclear — which is a significant finding.

---

### Step 1 — Assign Function Class

Assign the theory to one or more function classes from Section 2.1. A theory may belong to more than one class, but each class must be declared separately with its own analysis.

**Prompt for LLM:**

> "Using the following function class taxonomy, assign [theory] to one or more classes. For each class you assign, explain in one paragraph what the theory is doing in that capacity. If the theory is commonly described as doing something it is not actually doing — for example, described as 'solving' a problem when it is functioning as a reconstruction mechanism — flag this as a potential category error.
>
> Function classes: Candidate ontology / Candidate dynamics / Reconstruction mechanism / Consistency filter / Effective theory / Computational validator / Observer framework.
>
> After assigning classes, identify any apparent competitors to this theory and check whether the comparison is valid given their respective function classes."

**Expected output:** Function class assignments with justification, and a list of any comparisons in the literature that constitute category errors.

**What to watch for:** The most common category error in theoretical physics is comparing a reconstruction mechanism with a candidate ontology on the question of which one "explains" the fundamental structure of reality. If the LLM assigns two competing theories to different function classes, that finding should be highlighted prominently.

---

### Step 2 — Apply the Explanation Ladder

For each major physical phenomenon the theory claims to explain, assign it a level on the explanation ladder (Derives / Explains / Accommodates / Postulates).

**Prompt for LLM:**

> "For [theory], I need you to score its explanatory status for each of the following physical phenomena it claims to address: [list phenomena — e.g., the emergence of spacetime, the Standard Model particle content, the black hole entropy formula, unitarity of Hawking radiation].
>
> For each phenomenon, use this ladder:
> - Derives (Level 4): follows from the theory's equations with no additional input
> - Explains (Level 3): follows from a mechanism, with reduced free parameters
> - Accommodates (Level 2): fits by choosing parameter values; consistent but not predictive
> - Postulates (Level 1): inserted as an assumption
>
> Be specific. If the theory derives a result in a restricted sector but accommodates it in the general case, say so. Do not call accommodation derivation."

**Expected output:** A table with each claimed phenomenon and its explanation level, with justification. Any phenomenon scored as Derives at Level 4 should be examined especially carefully — genuine derivations are rare.

**What to watch for:** A theory that claims to "explain" many things but scores Level 2 on all of them has a significant problem: it is descriptively rich but explanatorily weak. This is legitimate physics but does not warrant unification claims.

---

### Step 3 — Test the Inverse Constraint

For each component of the theory's substrate, assess whether observational data can constrain it.

**Prompt for LLM:**

> "For [theory], I need to assess the inverse constraint — the ability to go from observational data backwards to constrain the theory's fundamental parameters or substrate variables.
>
> For each major substrate component [list them, or ask the LLM to identify them], answer:
> 1. What observational data is in principle relevant to constraining this component?
> 2. Is that data currently accessible, or does it require experiments beyond current technology?
> 3. If the data were obtained, how tightly would it constrain the substrate?
> 4. Score the inverse constraint as Strong / Moderate / Weak / None.
>
> Then give an overall inverse constraint assessment for the theory as a whole."

**Expected output:** Per-component inverse constraint scores and an overall assessment. A theory with no inverse constraint on any component is not yet in contact with the physical world.

**What to watch for:** Theories that make correct predictions (strong forward direction) while being completely unconstrained by data (no inverse direction) are mathematically interesting but not empirically progressive. This combination should be flagged explicitly.

---

### Step 4 — Score the MVT Threshold

Apply all ten MVT criteria from Section 2.4.

**Prompt for LLM:**

> "Score [theory] against the following ten Minimal Viable Theory criteria. For each, give a score of Strong / Partial / Weak / Undeclared / Undecidable, followed by a one-paragraph justification.
>
> 1. Substrate and dynamics declared
> 2. Dependency choices declared
> 3. Reconstruction maps supplied (geometry, gravity, matter)
> 4. GR and SM recovery in tested regimes
> 5. Controlled semiclassical limit
> 6. Consistency filters satisfied (anomaly, RG, EFT, BH thermodynamics)
> 7. Nontrivial inverse constraint from data to substrate
> 8. Discriminating test declared
> 9. Exclusion power — at least one plausible alternative class is ruled out
> 10. Incompleteness declaration — the theory explicitly states its unresolved gaps
>
> After scoring all ten, identify which gaps are most critical — i.e., which failures most directly undermine the theory's central claims."

**Expected output:** A scored MVT table with justifications, plus an identification of the critical gaps — the failures that are not merely incomplete but that undermine the theory's core purpose.

---

### Step 5 — Run the Falsifiability Engine

Every serious theory must produce at least one output from the falsifiability engine. The engine has seven output types:

**Prompt for LLM:**

> "For [theory], identify whether it produces any of the following outputs. For each output type it does produce, state the specific claim. For each it does not produce, state whether this is because the theory is incomplete or because it is genuinely not applicable given the theory's function class.
>
> Output types:
> 1. No-go theorem: rules out a class of substrates or alternatives
> 2. Bound: places a quantitative limit on a correction, coupling, or scale
> 3. Universality claim: predicts that many different substrates flow to the same effective behavior
> 4. Inverse constraint: states what observational data constrains about the substrate
> 5. Discriminating signature: predicts a measurable or checkable difference from alternatives
> 6. Failure diagnostic: states exactly what observation or theorem would break the theory
> 7. Incompleteness declaration: states which claims are currently unprovable within the theory's own formalism, and why this does or does not affect the theory's central claims
>
> A theory that produces none of these is not yet physics. It may be a consistent mathematical framework, but it has not made a falsifiable claim."

**Expected output:** A list of which engine outputs the theory produces, with the specific claims, and a clear statement of which outputs are absent and what their absence implies.

**The most important output:** The failure diagnostic (#6) is the single most revealing test. A theory that cannot state what would break it is unfalsifiable. Ask the LLM to press for a specific answer here, not a vague one.

---

### Step 6 — Expose Category Errors

With all previous steps complete, look across the landscape of theories competing to address the same problem and identify structural confusions in how they are being compared.

**Prompt for LLM:**

> "Given the following set of theories or frameworks that are commonly presented as addressing [problem]: [list them].
>
> Using the function class assignments from Step 1 and the MVT scores from Step 4:
>
> 1. Identify any pairs of theories being compared in the literature that are in different function classes. Explain why the comparison is a category error and what valid comparison would look like.
>
> 2. Identify any theories being credited with explaining phenomena that they actually only accommodate. Explain the distinction.
>
> 3. Identify what the debate is actually about once function-class confusion is removed. State the real question that distinguishes the remaining serious candidates.
>
> 4. If the competing theories are all responses to the same no-go constraint or trilemma, identify which assumption each one abandons and what it proposes as a replacement."

**Expected output:** A structural map of the debate, with category errors named, false comparisons removed, and the real question at the center of the dispute stated as precisely as possible.

---

### Step 7 — Produce the Workbench Report

The final output is a structured report that consolidates all previous steps. The report has a fixed format.

**Prompt for LLM:**

> "Produce a Workbench Report for [theory] with the following sections:
>
> **Function class:** [one sentence]
> **Problem addressed:** [one paragraph]
> **Hard constraints it must satisfy:** [list]
> **Explanation ladder scores:** [table]
> **Inverse constraint assessment:** [per component, with overall score]
> **MVT scorecard:** [table with scores and critical gaps identified]
> **Falsifiability engine outputs:** [list of what is and is not produced]
> **Category errors exposed:** [any false comparisons with other theories]
> **Incompleteness declaration:** [what the theory cannot currently prove or decide]
> **Workbench verdict:** [one paragraph stating what the theory has genuinely accomplished, what its critical gaps are, and what the live question is for advancing it]
>
> The verdict must not declare the theory true or false. It must state precisely what kind of claim the theory is making, what it has earned the right to claim, and what remains to be done."

---

## Part IV: Principles and Constraints

The Workbench operates under a fixed set of principles that constrain how it may be applied. These are not suggestions. Violating them produces outputs that look like Workbench analysis but are not.

### 4.1 The Invariant-Content Principle

The closest thing to ground truth is the content that survives valid translations among serious frameworks. When multiple independent frameworks converge on the same structure — black hole entropy scaling, anomaly polynomials, the CPT theorem — that convergence carries evidential weight. But convergence is provisional, not permanent. A future framework may reveal that earlier convergence was coincidental or regime-limited.

The practical consequence: when assessing a theory's claims, weight its reproductions of multiply-convergent results more heavily than its reproductions of framework-specific results.

### 4.2 The Incompleteness Principle

No framework rich enough to evaluate fundamental theories can certify its own completeness. The Workbench itself cannot certify that its seven concept categories are universal, that its MVT criteria are final, that all propositions about candidate theories are decidable, or that a future Theory of Everything must satisfy its current interface.

The practical consequence: every Workbench Report must include an incompleteness declaration — not just for the theory being analyzed, but for the analysis itself where relevant.

### 4.3 The Transparency Principle

A theory that honestly declares its unresolved gaps is scored above a theory that hides equivalent gaps. The scoring system (Strong / Partial / Weak / Undeclared / Undecidable) is designed so that explicit acknowledgment of limits is always better than silence. Undeclared is always scored lower than Undecidable.

The practical consequence: when applying The Workbench, do not penalize a theory for having gaps. Penalize it for concealing them.

### 4.4 The Accommodation Prohibition

Accommodation must never be called derivation. This is the single rule most frequently violated in the theoretical physics literature. A theory that reproduces a result by choosing appropriate parameter values has not explained that result. This is legitimate science — parameter fitting is how effective theories work — but it does not warrant claims of fundamental explanation or unification.

The practical consequence: every Level 2 (Accommodates) or Level 1 (Postulates) score on the explanation ladder must be stated explicitly in the report, even when the theory under analysis presents it as stronger.

### 4.5 The Function Class Rule

No theory may be assessed on criteria that do not apply to its function class. A reconstruction mechanism cannot be criticized for failing to propose an ontology. A consistency filter cannot be criticized for failing to make predictions. A computational validator cannot be criticized for not being a candidate theory.

The practical consequence: before scoring any criterion, confirm that the criterion applies to the theory's function class. If it does not apply, score it Not Applicable with a one-sentence explanation.

### 4.6 The No-Sovereign-Framework Rule

No single embedded theory has priority within The Workbench. String theory, loop quantum gravity, and every other framework are assessed by the same criteria. The Workbench does not favor approaches that have more practitioners, more publications, or longer history.

The practical consequence: when an LLM has been trained on data that reflects the physics community's current consensus, it will have implicit biases toward well-represented frameworks. The analyst should watch for outputs that treat a framework's popularity as evidence for its validity and prompt the LLM to re-examine where needed.

### 4.7 The Exclusion Principle

A theory that is compatible with all possible observations, or that can accommodate any data by parameter adjustment, is not yet physics. Every serious candidate must be able to say what it forbids — what class of observations, what class of alternative theories, what class of mathematical structures it rules out.

The practical consequence: the exclusion power criterion (MVT criterion 9) and the failure diagnostic (falsifiability engine output 6) are not optional. If a theory produces neither, that finding must be stated prominently in the report.

---

## Part V: Applying The Workbench to Different Theory Types

The methodology applies to any framework in fundamental or theoretical physics, but different theory types require different emphases. Here is guidance for common cases.

### 5.1 Candidate ontologies (e.g., loop quantum gravity, causal sets, string theory)

These are the most demanding applications. A candidate ontology must eventually pass all ten MVT criteria. The most common failures are: reconstruction maps that exist only in special sectors (MVT criterion 3), SM recovery that is accommodated rather than derived (explanation ladder, criteria 4), and inverse constraints that are weak or absent (MVT criterion 7).

Key emphasis: press hard on the reconstruction maps. An ontology that proposes fundamental ingredients but cannot show how spacetime and matter emerge from them — with controlled approximations and declared failure modes — has not yet earned its ontological claim.

### 5.2 Reconstruction mechanisms (e.g., AdS/CFT, Island formula, tensor networks)

The most important question for a reconstruction mechanism is: what does it reconstruct, in what regime, and what is its inverse? A reconstruction mechanism is not responsible for the underlying ontology, but it must be honest that it is not providing one. The most common error is treating a successful reconstruction as an explanation of the fundamental physics, when it is an explanation of how to compute from the fundamental physics — which may be entirely different.

Key emphasis: the inverse constraint test and the function-class assignment are the critical steps. Always check whether the mechanism is being credited with explanatory power it does not have.

### 5.3 Consistency filters and no-go results (e.g., AMPS firewall, swampland conjectures, anomaly matching)

These are constraints, not theories. They should not be scored on criteria that apply only to candidate theories — they are not expected to provide reconstruction maps or SM recovery. They should be scored on: how sharp is the constraint? What exactly does it rule out? Under what assumptions does it hold? What happens if an assumption fails?

Key emphasis: state the assumptions precisely. A no-go result is only as strong as its assumptions. When a no-go result appears to conflict with a candidate theory, the first question is always: which assumption of the no-go result does the candidate theory deny, and is that denial controlled?

### 5.4 Effective theories (e.g., General Relativity, Standard Model, EFT of inflation)

Effective theories are not expected to be fundamental. They should be scored on: how well-defined is their regime of validity? How controlled is their breakdown? What are the inverse constraints from their data to the underlying (unknown) fundamental theory?

Key emphasis: effective theories often have excellent inverse constraints within their regime, and this is a genuine virtue. An effective theory that tightly constrains what the fundamental theory must reproduce is contributing to the search for fundamental physics, even if it is not itself fundamental.

### 5.5 Novel or speculative frameworks

For frameworks that are early-stage, speculative, or outside the mainstream, apply the MVT checklist to determine not whether the theory is complete, but what its current status honestly is. A novel framework that clearly identifies its own gaps, makes at least one discriminating prediction, and provides a genuine inverse constraint — even in a restricted sector — is more scientifically valuable than a mature framework that hides its incompleteness.

---

## Part VI: Worked Example — The Black Hole Information Paradox

The following is a condensed illustration of The Workbench applied to the black hole information paradox debate, assessing four competing approaches: the Island formula, fuzzballs, the firewall, and remnants.

### Step 0 — Frame the dispute

The problem: does a black hole that forms and evaporates via Hawking radiation preserve quantum information, or destroy it? The hard constraint is the AMPS argument, which proves that three assumptions cannot simultaneously hold after the Page time — unitarity of Hawking radiation, smooth crossing of the horizon for infalling observers, and standard EFT validity outside the horizon. Any proposed resolution is a response to this trilemma: it must declare which assumption it abandons and provide a controlled replacement.

### Step 1 — Function class assignment

| Framework | Function Class | Notes |
|---|---|---|
| AMPS Firewall | Consistency filter (no-go) | Proves a contradiction; does not resolve it |
| Island formula | Reconstruction mechanism | Computes Page curve; does not explain microscopic mechanism |
| Fuzzballs | Candidate ontology + dynamics | Proposes what BHs are made of; within string theory |
| Remnants | Candidate ontology (endpoint modification) | Proposes what BHs evaporate into |

**Immediate finding:** "Island formula versus firewall" is a category error. These are in different function classes — one is a reconstruction mechanism, the other is a no-go constraint. They are not competitors. The firewall identifies which assumption must give; the island formula is one attempt to give it coherently.

### Step 2 — Explanation ladder

| Framework | Phenomenon | Level | Notes |
|---|---|---|---|
| Island formula | Page curve shape | Derives (4) | Given JT gravity setup |
| Island formula | Microscopic mechanism of information escape | Accommodates (2) | Formula works; physical story absent |
| Island formula | Replica wormhole saddles | Postulates (1) | Inserted; justified by consistency, not derived |
| Fuzzballs | BH entropy (extremal D1-D5) | Derives (4) | Genuine microstate count |
| Fuzzballs | General astrophysical BH behavior | Accommodates (2) | No explicit solutions constructed |
| Remnants | Information conservation | Postulates (1) | Asserted; no mechanism |

### Step 3 — Inverse constraint

| Framework | Inverse Constraint | Score |
|---|---|---|
| Island formula | Page curve shape does not discriminate among substrates | None |
| Fuzzballs (extremal) | BH entropy constrains string microstate count | Moderate |
| Fuzzballs (astrophysical) | No fuzzball solutions exist; no data path | Weak |
| Firewall | Not applicable (consistency filter) | N/A |
| Remnants | Sub-Planckian; no observational handle | None |

**Critical finding:** The Island formula has no inverse constraint at the substrate level. This means it cannot, even in principle with better data, tell us what the fundamental degrees of freedom of quantum gravity are. It solves the paradox computationally while leaving the physical mechanism entirely open.

### Step 4 — MVT threshold (condensed)

The Island formula fails MVT criteria 1 (substrate undeclared — it is agnostic about the underlying theory), 7 (no inverse constraint), 9 (cannot exclude alternative microscopic theories that would also preserve unitarity), and scores Undecidable on criterion 5 (semiclassical limit relies on non-perturbative path integral saddles whose existence is assumed).

Fuzzballs fail MVT criterion 3 for astrophysical BHs (reconstruction maps incomplete), criterion 7 for the same reason, and criterion 8 (discriminating tests exist in principle but are practically inaccessible for stellar-mass black holes, with the partial exception of gravitational wave echo predictions).

Remnants fail MVT criteria 7, 8, 9, and are effectively disqualified by the theoretical infinite-species problem — requiring infinitely many distinct remnant species to account for all possible initial states, which produces divergent virtual corrections in quantum field theory.

### Step 5 — Falsifiability engine

The Island formula produces a universality claim (unitarity is preserved regardless of substrate) and an incompleteness declaration (if the collaboration between Penington and Almheiri et al. is taken seriously). It does not produce a discriminating signature or a failure diagnostic that is observationally accessible.

Fuzzballs produce, marginally, a discriminating signature: fuzzball geometries have no horizon and predict, in principle, a modified Hawking radiation spectrum and gravitational wave echoes after binary mergers. Current LIGO data does not show echoes, which begins to constrain fuzzball models. This is the only approach in the group with a current observational handle, however weak.

Remnants produce no falsifiability engine outputs accessible to observation.

### Step 6 — Category errors exposed

The central category error: the firewall and the island formula are not competitors. The firewall is a constraint; the island formula is one way of satisfying it. Debating "firewall vs. islands" conflates a no-go theorem with a reconstruction mechanism.

The secondary category error: fuzzballs and the island formula are frequently presented as competing solutions at the same level of explanation. They are not. Fuzzballs propose what black holes are. The island formula proposes how to compute. They answer different questions and could both be correct — if fuzzball microstates turn out to be the correct ontology underlying the replica wormhole saddles in the island formula calculation.

### Workbench verdict

The real question, once category confusion is cleared away, is: what do the replica wormhole saddles in the island formula correspond to physically? The formula demonstrates that a non-perturbative saddle of the gravitational path integral restores unitarity, but it does not identify what physical structure that saddle represents. Fuzzballs are the most concrete candidate for that physical structure, but only in the extremal regime. The live scientific question is whether a fuzzball-like microstate interpretation of the replica wormholes can be constructed for astrophysical black holes. Everything else in the debate — firewall arguments, remnant proposals — is either a constraint the candidates must satisfy or a proposal that has already failed on theoretical grounds.

---

## Part VII: Limitations and Incompleteness Declaration

In keeping with the Transparency Principle, The Workbench's own limitations must be stated explicitly.

**The Workbench cannot select among admissible substrates.** If two theories both pass the MVT threshold, The Workbench has no mechanism for choosing between them. That choice requires new data, new mathematical results, or new theoretical insights — none of which The Workbench can generate.

**The Workbench cannot derive dynamics.** The choice of dynamical equations governing a substrate is outside the Workbench's scope. It can assess whether dynamics have been declared and whether they are consistent, but it cannot generate them.

**The Workbench cannot certify its own completeness.** The seven function classes may be incomplete. The ten MVT criteria may not cover all relevant dimensions. A future fundamental theory may require concepts that the current Workbench vocabulary cannot capture. The Workbench's interface is a default, not a universal.

**The Workbench is not immune to LLM limitations.** When applied using a language model, the analysis is subject to the LLM's training biases, knowledge cutoff, and tendency to produce plausible-sounding outputs that reflect consensus rather than disciplined reasoning. The analyst must review every output for faithfulness to the methodology. In particular, watch for: explanation levels that reflect the community's framing rather than the Workbench's criteria, inverse constraint scores that are too generous, and failure to flag category errors involving well-established frameworks.

**The Workbench cannot replace physical intuition.** It can clarify the structure of arguments. It cannot substitute for the theoretical creativity required to actually advance physics.

**The Workbench cannot prove a theory is wrong.** It can demonstrate that a theory is incomplete, that it has not earned its claims, that it produces no inverse constraints, and that it cannot be falsified. These are important findings. They are not the same as falsification.

---

## Appendix A: Quick Reference — The Eight Prompts

For rapid application, here are the eight prompts in condensed form:

**Step 0 — Frame:**
"State the physical problem, identify the hard constraints any solution must satisfy, and specify what a complete solution requires."

**Step 1 — Function class:**
"Assign [theory] to one or more function classes. Flag any category errors in how it is compared to other theories."

**Step 2 — Explanation ladder:**
"For each major claim, score: Derives (4) / Explains (3) / Accommodates (2) / Postulates (1). Do not call accommodation derivation."

**Step 3 — Inverse constraint:**
"For each substrate component, assess whether observational data can constrain it. Score Strong / Moderate / Weak / None."

**Step 4 — MVT scorecard:**
"Score all ten MVT criteria as Strong / Partial / Weak / Undeclared / Undecidable. Identify the critical gaps."

**Step 5 — Falsifiability engine:**
"Does the theory produce any of: no-go theorem, bound, universality claim, inverse constraint, discriminating signature, failure diagnostic, incompleteness declaration? For each absent output, state the implication."

**Step 6 — Category errors:**
"Across all theories addressing this problem, identify false comparisons, accommodation claimed as derivation, and what the real question is once confusion is removed."

**Step 7 — Report:**
"Produce a Workbench Report: function class, explanation ladder, MVT scorecard, falsifiability outputs, category errors, incompleteness declaration, and a verdict that states what the theory has earned the right to claim and what remains to be done."

---

## Appendix B: Diagnostic Rule Reference

The following diagnostic rules govern The Workbench's analysis. Each is labeled with its epistemic status — they are not all equally certain.

| Rule | Statement | Status |
|---|---|---|
| A | If no inverse constraint is declared, the theory cannot claim strong explanatory power in that sector | Definition rule |
| B | Dual descriptions have no ontological priority within the Workbench's scoring system | Category discipline rule |
| C | Any modification of Lorentz invariance must declare a modification protocol | Methodological rule |
| D | Large unexplained parameter spaces trigger an accommodation label, not a derivation label | Explanation audit heuristic |
| E | Any Standard Model reconstruction must address anomaly content | Structural physics constraint |
| F | Do not compare theories across function classes on unification metrics | Category discipline rule |
| G | No empirical contact means no unification score | Scoring rule |
| H | "Locality" must specify algebraic, causal, or metric type — unspecified locality is not a claim | Semantic hygiene rule |
| I | When N independent frameworks produce structure X, X gains provisional weight as invariant content, but this is never permanent | Bayesian convergence heuristic |
| J | The goal — a complete theory that survives all translations — is a limit we approximate, never certify | Epistemic constraint |

---

*This document is version 1.0. It will be revised as the methodology is applied and tested. Revisions will be listed here. The incompleteness of this document is a feature, not a defect.*
