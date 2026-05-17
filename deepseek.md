# The Workbench: A Manual Methodology for Clarifying Physical Theories Using LLM Assistance

*Version 1.0 – No software required. Just principles, a checklist, and an LLM as your assistant.*

---

## What is The Workbench?

The Workbench is a **discipline tool** – a structured way to analyse any physical theory (from a paper, a talk, or your own idea) and assess its clarity, completeness, and testability. It does not tell you whether the theory is *true*. It tells you:

- What the theory actually says (its substrate, dynamics, reconstruction claims).
- What it forbids and what would falsify it.
- Whether it *derives* empirical facts or merely *accommodates* them.
- Where it is incomplete or undecidable.

You can apply The Workbench **manually** or with the help of a large language model (LLM) as a reasoning assistant. No custom software is required – just this document, a text editor, and an LLM of your choice.

---

## Core concepts (in plain language)

| Concept | What it means | Why it matters |
|---------|---------------|----------------|
| **Substrate** | The fundamental “stuff” the theory assumes (e.g., strings, spin networks, causal relations) | Prevents hand‑waving about “fundamental” |
| **Dynamics** | How the substrate changes over time (or without time) | Without dynamics, you have kinematics, not a physical theory |
| **Reconstruction** | How ordinary space, time, gravity, and matter emerge from the substrate | The bridge between the primitive and what we observe |
| **Invariant** | Something that stays the same under different descriptions or regimes (exact, universal, or empirical) | The “elephant” – the real physics |
| **Explanation ladder** | Derives > Explains > Accommodates > Postulates | Exposes whether a claim is deep or just fitting data |
| **MVT criteria** | Nine checks for a serious Theory of Everything candidate | A reality check for grandiose claims |
| **Incompleteness declaration** | Admitting what the theory cannot currently prove | Honesty is scored higher than hidden gaps |

---

## What you need before you start

- A **theory description** – a paper, a set of notes, or an oral presentation transcript.
- Access to an **LLM** (ChatGPT, Claude, Gemini, etc.) – optional but highly recommended for extracting claims and filling templates.
- A **text editor** to record your analysis.

---

## Step‑by‑step procedure

### Step 1: Ingest the theory

Read the theory description. If using an LLM, paste the text and ask:

> *“Summarise this physical theory in 200 words. List its fundamental ingredients, the rules they obey, and the main phenomena it claims to explain.”*

Keep the output as a reference.

### Step 2: Extract the substrate (the “stuff”)

Use the seven‑tuple as a checklist. For each component, ask the LLM (or yourself) to find what the theory says – or explicitly note that it is missing.

| Component | Question | Example answer (string theory) |
|-----------|----------|--------------------------------|
| 𝒜 – Observable algebra | What are the measurable quantities at the most basic level? | “String field operators, vertex operators” |
| Ω – States | What are the allowed states? | “Fock space of string excitations” |
| 𝒞 – Causal structure | How is causality encoded? (Even pre‑spacetime) | “Worldsheet lightcones; bulk causality emerges” |
| Φ – Dynamics | What is the evolution law? | “Worldsheet CFT, string field equations” |
| ℛ – Coarse‑graining | How do you go from micro to macro? | “RG flow on worldsheet, compactification scale” |
| Σ – Constraints | What symmetries, anomalies, or consistency conditions must hold? | “Anomaly cancellation, modular invariance” |
| ℳ – Reconstruction maps | How do you recover spacetime, gravity, matter? | “AdS/CFT, compactification, scattering amplitudes” |

**If a component is not mentioned**, write `[UNDECLARED]`. The Workbench will flag it as a gap.

**LLM prompt template:**

> *“For each of the following seven categories, extract what the theory says. If nothing is said, write ‘UNDECLARED’. Categories: 𝒜 (observable algebra), Ω (states), 𝒞 (causal structure), Φ (dynamics), ℛ (coarse‑graining), Σ (constraints), ℳ (reconstruction maps).”*

### Step 3: Identify invariants

List what the theory preserves under dualities (exact), under coarse‑graining (universal), and what empirical facts it must match.

| Invariant type | Question | Example |
|----------------|----------|---------|
| **Exact** | What is the same in any equivalent description? | Anomaly polynomial, CPT theorem, central charge |
| **Universal** | What survives RG flow or changes of scale? | Black hole entropy law, critical exponents |
| **Empirical** | What observed data must the theory reproduce? | Standard Model particle content, Lorentz invariance (tested regime) |

**LLM prompt:**

> *“List all exact invariants, universal invariants, and empirical constraints mentioned or implied by this theory. If none, state ‘None declared’.”*

### Step 4: Apply the explanation ladder

Take the main claims of the theory (e.g., “explains the Standard Model”, “derives GR limit”). Classify each on the ladder:

| Level | Meaning | Example |
|-------|---------|---------|
| **Derives** | Follows from equations with no extra input | Unitarity → Page curve in holographic codes |
| **Explains** | Follows from a mechanism with reduced arbitrariness | QCD colour confinement from lattice (still some parameters) |
| **Accommodates** | Fits by choosing parameters or a vacuum | String compactification to SM (landscape) |
| **Postulates** | Inserted as an assumption | Cosmological constant value |

**LLM prompt:**

> *“For each major claim of the theory, classify it as Derives, Explains, Accommodates, or Postulates. Explain your reasoning briefly.”*

**The Workbench rule:** If a claim is marked Accommodates or Postulates, it does **not** count as a deep explanation. The theory cannot boast “unification” on that basis.

### Step 5: Run the MVT checklist (for TOE claims)

If the theory claims to be a Theory of Everything, evaluate it against the nine MVT criteria. Score each as: **Strong / Partial / Weak / Undeclared / Undecidable**.

| Criterion | Question |
|-----------|----------|
| 1. Substrate & dynamics | Are 𝒜, Ω, 𝒞, Φ clearly declared? |
| 2. Dependency choices | Are the relationships among components stated? |
| 3. Reconstruction maps | Does it recover geometry, gravity, and matter? |
| 4. GR & SM recovery | Does it reproduce GR and the Standard Model in tested regimes? |
| 5. Controlled semiclassical limit | Is there a systematic approximation to classical spacetime? |
| 6. Consistency filters | Does it satisfy anomaly cancellation, EFT positivity, etc.? |
| 7. Inverse constraint | Can observation back‑constrain the substrate? (e.g., “If we see X, then the Hilbert space dimension is at most N”) |
| 8. Discriminating test | Does it predict a measurable difference from GR+SM? |
| 9. Exclusion power | Does it forbid a plausible class of alternatives? |
| *10. Incompleteness transparency* | Does it honestly state what it cannot yet prove? |

**LLM prompt for each criterion:**

> *“For MVT criterion [number], evaluate the theory as Strong, Partial, Weak, Undeclared, or Undecidable. Provide a one‑sentence justification.”*

### Step 6: Fill the falsifiability engine

Every serious theory should produce at least one of these outputs. If it does not, the Workbench will flag it as **empirically weak**.

| Output | What to write |
|--------|---------------|
| **No‑go theorem** | “This theory forbids X, where X is …” |
| **Bound** | “Parameter Y must be less than Z (from current experiments)” |
| **Universality claim** | “All theories of class C must reproduce behaviour B” |
| **Inverse constraint** | “If experiment E measures value V, then substrate parameter P lies in range R” |
| **Discriminating signature** | “In experiment F, our theory predicts difference D compared to GR+SM” |
| **Failure diagnostic** | “If observation O is made, this theory is falsified” |
| **Incompleteness declaration** | “We cannot currently prove that …; this gap does/does not affect our main claim because …” |

**LLM prompt:**

> *“Generate a falsifiability table for the theory. For each of the seven outputs, either provide a concrete statement or write ‘None declared’.”*

### Step 7: Write the incompleteness declaration

Inspired by Gödel, every theory should be honest about its limits. Ask the LLM (or yourself):

> *“What are the main unproven claims, undecidable questions, or formal gaps in this theory? Do these gaps affect the theory’s core predictions? What evidence would close each gap?”*

Record the answer as a paragraph. The Workbench will treat a theory that hides its gaps as **less trustworthy** than one that admits them.

### Step 8: Produce the final scorecard

Compile your answers into a one‑page summary. Use this template:

```
THEORY: [Name / arXiv ID]

SUBSTRATE:
  𝒜: [declared / UNDECLARED]
  Ω: [declared / UNDECLARED]
  𝒞: [declared / UNDECLARED]
  Φ: [declared / UNDECLARED]
  ℛ: [declared / UNDECLARED]
  Σ: [declared / UNDECLARED]
  ℳ: [declared / UNDECLARED]
  Other components: [if any]

INVARIANTS:
  Exact: [list]
  Universal: [list]
  Empirical: [list]

EXPLANATION LADDER (main claims):
  - Claim 1: Derives / Explains / Accommodates / Postulates
  - Claim 2: ...
  (etc.)

MVT SCORECARD:
  1. Substrate & dynamics: Strong/Partial/Weak/Undeclared/Undecidable
  2. Dependency choices: ...
  3. Reconstruction maps: ...
  4. GR & SM recovery: ...
  5. Semiclassical limit: ...
  6. Consistency filters: ...
  7. Inverse constraint: ...
  8. Discriminating test: ...
  9. Exclusion power: ...
  10. Incompleteness transparency: ...

FALSIFIABILITY OUTPUTS:
  - No‑go theorem: [statement or NONE]
  - Bound: [statement or NONE]
  - Universality claim: [statement or NONE]
  - Inverse constraint: [statement or NONE]
  - Discriminating signature: [statement or NONE]
  - Failure diagnostic: [statement or NONE]
  - Incompleteness declaration: [paragraph]

OVERALL ASSESSMENT:
  (One paragraph: what is clear, what is missing, whether the theory is ready for serious evaluation as a TOE, and what single experiment would most directly test it.)
```

### Step 9: Review and iterate

Share the scorecard with colleagues or with the theory’s author. Ask: “Did I misrepresent any claim? Is the explanation ladder correct? What inverse constraints did I miss?”

Use the LLM again to refine any ambiguous entries.

---

## Example: Analysing a toy theory

**Theory name:** *“Qubit Lattice Emergent Gravity”* (imaginary)

After Step 2 (substrate), the LLM extracts:
- 𝒜 = Pauli operators on a 3D cubic lattice of N qubits.
- Ω = product states, entangled states.
- 𝒞 = nearest‑neighbour interactions define a causal lightcone.
- Φ = discrete time unitary circuit (Floquet).
- ℛ = block‑spinning to larger lattices.
- Σ = local U(1) symmetry on each qubit (gauge).
- ℳ = continuum limit yields massless spin‑2 mode → GR.

Step 4 (explanation ladder):
- “Recovers GR in continuum limit” → Explains (still needs control parameter 1/N).
- “Predicts BH entropy area law” → Derives (from entanglement entropy across a surface).
- “Matches Standard Model” → Postulates (no derivation of gauge group).

Step 5 (MVT):
- Criterion 5 (semiclassical limit) → Weak (only large‑N limit, not proven).
- Criterion 7 (inverse constraint) → Undeclared.
- Criterion 10 (incompleteness transparency) → Weak (does not mention that the continuum limit may not exist).

The scorecard reveals that the toy theory is interesting but far from a TOE. That is the Workbench’s value: it shows exactly where the gaps are.

---

## Using an LLM effectively – best practices

- **Break the analysis into small prompts.** Do not ask for everything at once.
- **Ask for justifications.** “Why do you classify this as Accommodates?” forces reasoning.
- **Use few‑shot examples.** Provide the LLM with a completed example (like the toy theory above) before asking it to analyse a new one.
- **Cross‑check with a second LLM.** Different models may give different classifications. Disagreement highlights ambiguity in the original paper.
- **Always keep a human in the loop.** The Workbench is a **decision support tool**, not an autopilot. The final scorecard is your responsibility.

---

## Limitations of the manual Workbench

| Limitation | Mitigation |
|------------|------------|
| LLMs can misinterpret physics claims | Always verify against the original source. |
| Subjectivity in explanation ladder | Use the ladder’s strict definitions; when uncertain, choose the lower (more critical) level. |
| Missing inverse constraints – the LLM may not infer them | Explicitly ask: “If experiment X had outcome Y, what would that tell us about the substrate?” |
| The Workbench does not generate new physics | It only clarifies and evaluates. Discovery is still your job. |

---

## When not to use The Workbench

- **During early brainstorming** – it is too structured and may kill creativity. Use it after you have a concrete proposal.
- **For purely mathematical results** (no claim to physical reality) – the empirical criteria do not apply.
- **For established effective theories** (e.g., Standard Model) – they already pass the empirical checks; the Workbench would be trivial.

---

## Final word

The Workbench is a **mirror** for physical theories. It reflects back their clarity, their hidden assumptions, and their testability. Used honestly, it prevents self‑deception and accelerates the elimination of bad ideas. Used with an LLM, it becomes a fast, always‑available critic that never tires of asking the same hard questions.

No software to install. No programming required. Just a checklist, a text editor, and a willingness to be honest about what your theory can and cannot do.

**Now go analyse a paper.** The Workbench is waiting.
