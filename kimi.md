Here is the comprehensive documentation. It treats The Workbench strictly as a **conceptual discipline**—a set of protocols, taxonomies, and diagnostic habits that can be applied to any theoretical claim in physics, with or without computational assistance.

---

# The Workbench: A Manual for Clarifying Physical Theories
## *Version 1.0 — "Incomplete by Design"*

---

## 1. What The Workbench Is (and Is Not)

**The Workbench is a referee's grammar for theoretical physics.** It is not a theory of physics. It is not software. It is not an artificial intelligence that judges truth. It is a **structured discipline for exposing what a theory actually claims, what it forbids, and what it cannot yet decide.**

When you apply The Workbench to a paper, a research program, or a private hypothesis, you are performing a **clarification ritual**. You are not proving the theory right or wrong. You are forcing it to declare its own epistemic status so that others—and the future version of yourself—can see where the real work remains.

**What The Workbench is not:**
- It is not a formal system claiming completeness. (It is Gödel-humble; see Section 2.)
- It is not a theory generator. It does not discover new physics.
- It is not a replacement for peer review. It is a **precondition** for meaningful peer review.
- It is not a software tool. No installation, no login, no database. It is a methodology you apply with pen, paper, and judgment.

---

## 2. The Two Axioms

Every application of The Workbench begins by acknowledging two constraints:

**Axiom 1 — Invariant-Content Orientation.**  
The Workbench seeks structures that survive valid translations among frameworks: exact invariants, universal invariants, and empirical constraints. These are the closest thing to "what nature actually does" that human theories can approximate.

**Axiom 2 — Incompleteness Humility.**  
No evaluative framework rich enough to be useful can prove its own completeness, consistency, or universal adequacy. The Workbench cannot certify that its seven-tuple interface captures all possible future theories. It is a **sufficient checklist**, not a necessary ontology.

These axioms are complementary. The first tells you what to look for. The second tells you what you are not allowed to claim.

---

## 3. The Core Methodology: A Five-Phase Protocol

To clarify any theory using The Workbench, proceed through five phases. You may abort at any phase if you discover the theory is not yet mature enough to evaluate.

### Phase 1: Ingestion
Read the paper, listen to the talk, or examine the proposal. Do not yet judge it. Your only job is to identify the **function class** (Section 6) and the **target sector** (what physical phenomenon the theory addresses).

### Phase 2: Extraction
Map the theory onto the **Seven-Tuple Evaluative Interface** (Section 4). If the theory does not fit, use the **Other** slot and explain why. Extract answers to the **Eleven Essential Questions** (Section 5). Tag each claim with the **Explanation Ladder** (Section 7).

### Phase 3: Diagnosis
Run the **Diagnostic Rules** (Section 8) against the extracted structure. Identify category errors, missing inverse constraints, accommodation disguised as derivation, and hidden assumptions.

### Phase 4: Declaration
Draft the **Incompleteness Declaration** (Section 9). This is mandatory. No theory passes through The Workbench without explicitly stating what it cannot yet prove.

### Phase 5: Assessment
Locate the theory against the **Minimum Viable Theory (MVT) Threshold** (Section 10). Produce a **scorecard** that is honest, provisional, and revisable.

---

## 4. The Seven-Tuple Evaluative Interface

The default interface for expressing any candidate theory is:

$$\mathfrak{S} = (\mathcal{A}, \Omega, \mathcal{C}, \Phi, \mathcal{R}, \Sigma, \mathcal{M})$$

| Symbol | Meaning | What to Declare |
|--------|---------|-----------------|
| $\mathcal{A}$ | Observable algebra / categories | What are the basic measurable quantities? |
| $\Omega$ | Admissible states | What states are allowed on that algebra? |
| $\mathcal{C}$ | Causal or pre-causal structure | What is the fundamental notion of "before" and "after"? |
| $\Phi$ | Dynamics | What evolves the system? (The most commonly missing slot.) |
| $\mathcal{R}$ | Coarse-graining / renormalization | How do you get from micro to macro? |
| $\Sigma$ | Symmetries, anomalies, consistency constraints | What no-go results must the theory respect? |
| $\mathcal{M}$ | Reconstruction maps | How do you recover spacetime, matter, and thermodynamics? |

**Critical rule:** The seven-tuple is a **sufficient interface**, not a universal ontology. If your theory genuinely requires an eighth component, a different decomposition, or no decomposition at all, you must declare:

> **Other:** *What it is. Why it escapes the tuple. What evaluative visibility is lost as a result.*

The Workbench does not reject theories that do not fit. It **penalizes opacity**.

---

## 5. The Eleven Essential Questions

For any theory, answer the following. Use **Undeclared** if missing. Use **Undecidable — [reason]** if the answer is currently unprovable within the theory's own formalism.

| # | Question | Diagnostic Purpose |
|---|----------|-------------------|
| 1 | What are the most basic ingredients? | Exposes hand-waving about "fundamental stuff." |
| 2 | How do those ingredients change (or relate without time)? | Exposes missing dynamics ($\Phi$). |
| 3 | How do you recover ordinary space, time, and gravity? | Tests the reconstruction map ($\mathcal{M}$). |
| 4 | How do you recover the Standard Model? | Tests empirical anchoring. |
| 5 | What exact thing survives all changes of description? | Identifies provisional invariants. |
| 6 | Does the theory **derive**, **explain**, **accommodate**, or **postulate** known facts? | Prevents fake explanations. |
| 7 | What does the theory **forbid**? | This is its power. No exclusion = no teeth. |
| 8 | What observation would prove it wrong? | Falsifiability check. |
| 9 | Can real data constrain the basic ingredients? | Inverse constraint strength. |
| 10 | What is one concrete prediction for the next 5–10 years? | Accountability. |
| **11** | **What can you not currently prove, and why?** | **The Incompleteness Declaration.** |

If a theory cannot answer #7, #8, or #11 with specificity, it is **not yet transparent enough to evaluate**.

---

## 6. Function Classes: The Most Important Filter

The single greatest source of confusion in theoretical physics is **comparing across function classes**. The Workbench forces you to label what kind of thing your theory is before evaluating it.

| Function Class | Role | Examples | Evaluated on MVT? |
|----------------|------|----------|-------------------|
| **Candidate Ontology + Dynamics** | What is fundamentally real, and how it behaves | String theory, Loop Quantum Gravity, Causal Sets | **Yes** |
| **Reconstruction Mechanism** | How effective observables arise | AdS/CFT, Tensor Networks, Holographic QEC | **No** |
| **Consistency Filter** | What rules out inadmissible candidates | Swampland, Anomaly Matching, Cobordism, AMPS Firewall | **No** |
| **Computational Validator** | Numerical or mathematical existence test | Lattice QCD, CDT Simulations, Conformal Bootstrap | **No** |
| **Effective Theory** | What is observed at low energy | GR, Standard Model, EFT of Gravity | **No** |

**Rule:** Comparing a Reconstruction Mechanism to a Candidate Ontology on "unification" grounds is a **category error**. The Workbench flags this immediately.

---

## 7. The Explanation Ladder

When a theory claims to "explain" a feature, classify it rigorously:

| Level | Name | Meaning | Unification Claim? |
|-------|------|---------|-------------------|
| 4 | **Derives** | Follows from deeper equations with no extra input | **Yes** |
| 3 | **Explains** | Follows from a mechanism with fewer free parameters | **Partial** |
| 2 | **Accommodates** | Fits by choosing parameters or model space | **No** |
| 1 | **Postulates** | Inserted as an assumption | **No** |

**Rule:** Do not call accommodation "derivation." Accommodation is legitimate physics, but it does not warrant unification claims.

---

## 8. The Diagnostic Rules (A–J)

The Workbench applies ten diagnostic rules to any extracted theory. Each rule carries a **proof status** to prevent overclaiming.

| Rule | Name | Status | What It Does |
|------|------|--------|--------------|
| **A** | Inverse-Check | Definition Rule | No inverse declared → explanatory power is weak by definition. |
| **B** | Duality-Humility | Category Rule | Exact dual descriptions have no ontological priority. |
| **C** | Lorentz-Violation Accounting | Structural Constraint | Any Lorentz modification must declare a protocol or bound. |
| **D** | Accommodation Warning | Diagnostic Heuristic | Large parameter spaces trigger a warning, not a falsification. |
| **E** | Anomaly-Matching | Structural Physics Constraint | Any SM reconstruction must account for anomaly content. |
| **F** | Apples-to-Apples | Category Rule | Disjoint function classes cannot be ranked on MVT. |
| **G** | Empirical-Anchoring | Scoring Rule | No empirical contact → no unification score. |
| **H** | Locality-Typing | Semantic Rule | "Locality" must specify algebraic, causal, or metric. |
| **I** | Convergence Tracker | Diagnostic Heuristic | Cross-framework agreement increases provisional weight, never immortality. |
| **J** | Closure-Under-Translation | Metaphor | The "elephant" is a limit we approximate, never reach. |

**How to use:** Run these rules against your extracted seven-tuple. Flag every trigger. Do not treat them as theorems; treat them as **diagnostic lenses**.

---

## 9. The Incompleteness Declaration

This is the **mandatory thirteenth item** of the admission rule (or the mandatory answer to Question 11). Every theory must submit:

> **What I cannot currently prove, what effect that has on my claims, and what would close the gap.**

**Template:**
- **Unproven core claims:** Specific statements assumed without derivation.
- **Undecidable or open questions:** What is outside the theory's current formal control?
- **Effect on unification claim:** Does this gap prevent full TOE status?
- **What would close the gap:** A concrete criterion (e.g., "rigorous proof of semiclassical limit").
- **What remains valid despite the gap:** Which predictions or structures survive the incompleteness?

**The Workbench rewards honesty.** A theory that declares its gaps clearly scores higher than one that hides them.

---

## 10. The Minimum Viable Theory (MVT) Threshold

A theory is **ready to be taken seriously as a candidate TOE** only if it satisfies all ten criteria with adequate scores:

| Criterion | Score Options |
|-----------|---------------|
| 1. Ingredients and dynamics declared | Strong / Partial / Weak / Undeclared |
| 2. Dependency choices declared | Strong / Partial / Weak / Undeclared |
| 3. Reconstruction maps for geometry, gravity, matter | Strong / Partial / Weak / Undeclared |
| 4. Recovery of GR and SM in tested regimes | Strong / Partial / Weak / Undeclared |
| 5. Controlled semiclassical limit | Strong / Partial / Weak / **Undecidable** |
| 6. Consistency filters (anomaly, RG, EFT, BH) | Strong / Partial / Weak / **Undecidable** |
| 7. Nontrivial inverse constraint | Strong / Weak / None |
| 8. Discriminating test declared | Yes / No / **Undecidable** |
| 9. Exclusion of at least one alternative class | Yes / No / Partial |
| 10. **Incompleteness Transparency** | Strong / Weak / None |

**Critical rule:** MVT failure ≠ framework failure. A theory can fail MVT and still be valuable as a reconstruction mechanism, consistency filter, or effective theory.

---

## 11. Using LLMs with The Workbench

The Workbench is methodology, not software. However, you may enlist an LLM as a **drafting assistant** to accelerate the manual labor of clarification.

**What an LLM can do:**
- **Parse** a paper or transcript into the seven-tuple structure.
- **Draft** answers to the Eleven Questions.
- **Suggest** explanation-ladder classifications.
- **Flag** potential category errors by comparing function-class labels.
- **Propose** incompleteness gaps based on phrases like "we leave this for future work."

**What an LLM cannot do:**
- **Judge** truth. It drafts; you adjudicate.
- **Certify** a scorecard. Every LLM output must be human-reviewed.
- **Detect** its own hallucinations. You must verify every extraction against the source text.

**Protocol for LLM-assisted Workbench application:**
1. **Ingest:** Feed the source material to the LLM with a strict system prompt: *"Map this to the Workbench seven-tuple. Provide verbatim quotes or mark 'not_discussed.' Do not infer."*
2. **Extract:** Receive the draft YAML. Manually verify every field.
3. **Diagnose:** Run the Diagnostic Rules yourself. The LLM may suggest triggers; you decide.
4. **Declare:** Draft the Incompleteness Declaration. The LLM may suggest gaps; you certify.
5. **Assess:** Compute the MVT scorecard. The LLM may propose scores; you lock them.

**The human is the referee. The LLM is the clerk.**

---

## 12. Workflow for Assessing Any Theory

**Step 1: Identify the function class.**  
Is this a candidate ontology, a reconstruction mechanism, a consistency filter, or an effective theory? If the authors do not declare it, you must assign it before proceeding.

**Step 2: Map the seven-tuple.**  
Fill what is present. Mark "not_discussed" for missing slots. Use "Other" if necessary.

**Step 3: Answer the Eleven Questions.**  
Demand specificity. Reject vague answers. Flag "Undecidable" where appropriate.

**Step 4: Classify every major claim on the Explanation Ladder.**  
Be ruthless. "Our framework naturally incorporates the Standard Model" is almost always **accommodates**, not **derives**.

**Step 5: Run Diagnostic Rules A–J.**  
Flag every trigger. Write a brief justification for each flag.

**Step 6: Draft the Incompleteness Declaration.**  
If the authors did not provide one, construct it from their hedges, caveats, and future-work sections.

**Step 7: Produce the MVT Scorecard.**  
Score each criterion. Add a one-paragraph verdict: *What this theory actually is, what it actually does, and what remains open.*

**Step 8: Publish or archive.**  
Share the scorecard with the authors. Invite correction. The Workbench is falsifiable: if a theory violates a Workbench constraint yet succeeds empirically, the constraint is revised.

---

## 13. Example: The Black Hole Information Paradox

When The Workbench is applied to the Page-curve debate, the following clarification emerges automatically:

- **Island Formula:** Reconstruction mechanism. Derives the curve's shape in semiclassical regimes. Cannot constrain the substrate. **Not a TOE candidate.**
- **Fuzzballs:** Candidate ontology. Proposes what black holes are made of. Lacks dynamics ($\Phi$) to derive the evaporation process. **MVT: Incomplete.**
- **AMPS Firewall:** Consistency filter. A no-go theorem on combining unitarity, EFT, and smooth horizons. **Not a physical prediction.**
- **Remnants:** Phenomenological placeholder. Violates EFT consistency filters. **Excluded unless modification protocol provided.**

**The pseudo-debate ("which solution is right?") dissolves.** The real question is: *Which function class owns the inverse constraint from the Page curve to the fundamental substrate?* Currently: none do.

This is the Workbench's value. It does not solve the paradox. It reveals that most of the "competing approaches" were never competing at all.

---

## 14. Constraints & Limitations

The Workbench cannot:
- Select among admissible substrates without an MVT candidate.
- Derive $\Phi$ (dynamics is outside meta-scope).
- Resolve parameter problems by itself.
- Prevent disagreement on minimal commitments.
- Guarantee any framework will cross MVT.
- Replace genuine theoretical creativity.
- **Prove its own consistency or completeness.**
- Decide all propositions about all candidate theories.
- Certify that a candidate's undecidable gaps are harmless.

Acknowledging these is part of taking The Workbench seriously.

---

## 15. How to Start Using The Workbench Today

You need no installation, no account, and no funding.

1. Print the **One-Page Checklist** (Section 12, Step 7).
2. Pick a paper from your field.
3. Fill the seven-tuple by hand.
4. Answer the Eleven Questions.
5. Run the Diagnostic Rules.
6. Draft the Incompleteness Declaration.
7. Score it on MVT.
8. Share the result with a colleague.

If you do this for three papers, you will discover that The Workbench is not a tool you use. It is a **habit of mind** that makes you a more disciplined theorist and a more incisive critic.

---

**Do you need clarification on any section, or would you like me to expand the LLM-assisted protocol with specific prompt templates for automated extraction?**
