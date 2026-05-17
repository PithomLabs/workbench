# The Workbench: A Methodological Guide for Theory Clarification

## Preamble: What The Workbench Is (And Isn't)

The Workbench is not a software application, a database, or a website. It does not have a backend, a UI, or a knowledge graph. 

**The Workbench is a strict epistemic discipline—a conceptual schema and a set of diagnostic rules used to clarify, audit, and compare theoretical physics frameworks.** It is an operational protocol for forcing epistemic humility, exposing category errors, and mapping the exact standing of any claim in fundamental physics.

In this methodology, you (the evaluator) act as the workbench operator. An LLM (Large Language Model) acts as your semantic processor—capable of parsing dense physics literature, extracting claims, and mapping them to The Workbench’s schema. The LLM does not decide what is true; it merely forces a theory’s claims into a rigorously typed structure where missing declarations, overclaims, and category errors become instantly visible.

This document outlines how to apply The Workbench methodology to any theory in physics using an LLM.

---

## Phase 1: Intake and Function-Class Declaration

The most common error in theoretical physics is comparing frameworks that occupy entirely different functional roles. The first step of The Workbench is to stop this category error at the door.

### 1.1 Define the Function Class
Before any other analysis, the theory must be assigned one (or more) of the following function classes:

| Function Class | Role | Examples |
|---|---|---|
| **Candidate Ontology** | Proposes what is fundamentally real | Causal sets, LQG, String/M-theory |
| **Candidate Dynamics** | Proposes equations/update rules | Spin foams, String field theory, Asympland safety |
| **Reconstruction Mechanism** | Translates substrate to effective observables | AdS/CFT, Tensor networks, Holography |
| **Consistency Filter** | Rules out inadmissible candidates | Swampland, Anomaly matching, AMPS Firewall |
| **Effective Theory** | Describes observed emergent physics | GR, Standard Model, EFT of gravity |
| **Computational Validator** | Numerical/mathematical existence test | Lattice gauge theory, Bootstrap |
| **Observer Framework** | Explains how records/observers arise | Decoherence, Quantum Darwinism |

**The Rule:** If a theory is classified as a *Reconstruction Mechanism*, it cannot be evaluated as a *Candidate Ontology*. If it is a *Consistency Filter*, it cannot be scored on its ability to "unify" physics. 

---

## Phase 2: The Substrate Mapping ($\mathfrak S^+$)

Any serious framework must declare its structural commitments. The Workbench uses an extended 7+1 tuple to map these. You will instruct the LLM to extract or infer these from the literature:

**$\mathfrak S^+ = (\mathcal A, \Omega, \mathcal C, \Phi, \mathcal R, \Sigma, \mathcal M, \mathcal O)$**

*   **$\mathcal A$ (Algebra):** Observable algebras, nets, or categories.
*   **$\Omega$ (States):** Admissible states on $\mathcal A$.
*   **$\mathcal C$ (Causality):** Causal or pre-causal adjacency.
*   **$\Phi$ (Dynamics):** Quantum channels, constraints, or evolution maps.
*   **$\mathcal R$ (Renormalization):** Coarse-graining/RG maps.
*   **$\Sigma$ (Symmetries/Constraints):** Anomalies, cobordism, consistency conditions.
*   **$\mathcal M$ (Reconstruction):** The family of bidirectional maps that recover effective physics.
*   **$\mathcal O$ (Other):** *The Gödel-safe escape hatch.* Any component vital to the theory that does not fit the above must be declared here, along with why it doesn't fit and how it affects evaluation.

**The Rule:** A slot left blank is scored as "Undeclared." A slot filled with hand-waving is scored as "Weak." The Workbench does not punish honest gaps; it punishes hidden ones.

---

## Phase 3: The Explanation Audit

Theories frequently claim to "explain" phenomena when they merely accommodate them. The Workbench enforces a strict four-tier ladder. Instruct the LLM to classify every major claim of the theory into one of these modes:

| Mode | Definition | Workbench Implication |
|---|---|---|
| **Derives** | Follows from deeper equations with no additional input | Valid unification claim |
| **Explains** | Follows from a mechanism with reduced arbitrariness | Partial unification claim |
| **Accommodates** | Fit by parameter choice or model selection | No unification claim permitted |
| **Postulates** | Inserted as an assumption | Zero unification claim |

*Example:* String theory compactifications "accommodate" the Standard Model (via landscape vacuum selection); they do not "derive" it. The Workbench flags any claim to the contrary.

---

## Phase 4: The Diagnostic Rule Check

The Workbench replaces overclaimed "theorems" with ten diagnostic heuristics. Run the theory through these rules to expose its structural vulnerabilities.

*   **Rule A (Inverse-Check):** Does the reconstruction map $\mathcal M$ allow working backward from empirical data to constrain the substrate? (Strength: Strong / Weak / None).
*   **Rule B (Duality-Humility):** If the theory relies on exact duality, does it falsely claim one side is "more real"?
*   **Rule C (Lorentz-Accounting):** If it violates Lorentz invariance, is the modification protocol explicitly declared?
*   **Rule D (Parameter-Space Warning):** Does it claim to explain X using a parameter space larger than the space pinned by X? (Triggers "Accommodation" label).
*   **Rule E (Anomaly-Matching):** Does it reconstruct the SM while preserving the exact SM anomaly polynomial?
*   **Rule F (Apples-to-Apples):** Is this theory being compared against a theory in a different function class? (If yes, halt comparison).
*   **Rule G (Empirical-Anchoring):** Is there at least one empirical constraint in the codomain of its maps?
*   **Rule H (Locality-Typing):** When claiming "locality" or "non-locality," does it specify which type (Algebraic, Causal, or Metric)?
*   **Rule I (Convergence Tracker):** Does the theory converge with others on a result? *Check for shared assumptions.* Convergence from independent assumptions is high-value; convergence from shared assumptions is low-value (avoid premature elevation to "universal invariant").
*   **Rule J (Category-Metaphor):** Claims of "fundamentality" must be demonstrably universal in the category of admissible substrates; otherwise, they are metaphors.

---

## Phase 5: The Incompleteness Declaration (The Gödel Slot)

No framework rich enough to evaluate fundamental theories can prove its own completeness. The Workbench requires every theory to submit an Incompleteness Declaration. 

You must extract or infer the following:
1.  **Unproven Core Claims:** What major mathematical results does the theory assume but cannot yet prove? (e.g., Non-perturbative UV fixed point existence).
2.  **Undecidable/Open Questions:** What propositions within the theory cannot currently be resolved?
3.  **Effect on Unification:** Do these gaps undermine its claim to be a Theory of Everything, or just a partial sector description?
4.  **What Would Close the Gap:** What specific mathematical proof or experimental result is required?

**The Rule:** A theory that honestly declares its undecidable gaps scores *higher* on epistemic transparency than one that hides them. Honesty is rewarded; evasion is penalized.

---

## Phase 6: The MVT Scorecard Generation

Finally, generate the Minimum Viable Theory (MVT) scorecard. A theory must clear these criteria to be taken seriously as a fundamental unification candidate. Score each as:

**Strong / Partial / Weak / Undeclared / Undecidable / Not Applicable**

1.  Substrate variables and candidate dynamics defined.
2.  Dependency choices declared.
3.  Controlled reconstruction maps for geometry, gravity, and matter.
4.  Recovery of GR and the Standard Model.
5.  Controlled semiclassical limit.
6.  Consistency filters satisfied.
7.  Nontrivial inverse constraint from observation to substrate.
8.  Discriminating test declared.
9.  Exclusion of a plausible class of alternatives.
10. **Incompleteness transparency** (Did it fill out the Gödel slot honestly?).

---

## Operational Protocol: Using an LLM as The Workbench Engine

To apply this methodology to a paper or theory using an LLM (like GPT-4, Claude, etc.), use the following prompt architecture.

### Step 1: Initialize the LLM with The Workbench Context
Copy the definitions of the Function Classes, the $\mathfrak S^+$ Tuple, the Explanation Ladder, the Diagnostic Rules, and the MVT Scorecard into the LLM's system prompt or the beginning of the conversation. 

*Prompt:* "You are The Workbench, an epistemic auditing system for theoretical physics. Your purpose is not to evaluate if a theory is true, but to enforce strict structural discipline on its claims. You will use the following methodology [Insert Phases 1-6]. You will output only structured YAML or Markdown based on this schema. You will be ruthless in distinguishing 'Derives' from 'Accommodates' and in enforcing Function Classes."

### Step 2: Provide the Source Material
Provide the paper, the Wikipedia article, or a summary of the theory.

*Prompt:* "Please audit the attached paper on [Theory Name, e.g., Asymptotic Safety] using The Workbench protocol. Proceed through all six phases."

### Step 3: Force the Structured Output
The LLM will attempt to write natural language. Stop it. Force it into the schema.

*Prompt:* "Output the audit as follows:
1. Function Class Declaration.
2. Substrate Mapping ($\mathcal A$ through $\mathcal O$).
3. Explanation Audit of major claims.
4. Diagnostic Rule Check (A-J), highlighting any rules that trigger warnings.
5. The Incompleteness Declaration.
6. The 10-point MVT Scorecard with scores and brief justifications."

### Step 4: The Adversarial Review (Crucial)
LLMs are sycophantic; they will try to agree with the paper's authors. You must command the LLM to assume the authors are overclaiming.

*Prompt:* "Review your previous output. The authors have likely overclaimed their explanation mode. Downgrade any claim from 'Derives' to 'Explains' or 'Accommodates' if additional parameters or assumptions were silently inserted. Check Rule A (Inverse Constraint)—if the theory cannot map empirical data back to its substrate, ensure the inverse constraint is scored 'Weak' or 'None'. Revise the output."

---

## Conclusion: What The Workbench Produces

By applying this methodology, you do not generate new physics. You generate something far more urgently needed: **clarity.**

The output of The Workbench is a legible, honest map of what a theory claims, what it actually proves, what it merely accommodates, what category errors it is committing, and precisely where its mathematical and epistemic gaps lie. 

It stops the endless, confused debates between competing frameworks by forcing them into their proper functional lanes. It exposes the difference between a theory that is fundamentally correct but incomplete, and a theory that is complete but merely accommodating reality through parameter fitting.

The Workbench does not tell you what is true. It tells you whether a theory has earned the right to be debated as a serious search for the truth.
