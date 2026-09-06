## claude

**Deep Research Prompt — copy/paste as-is**

---

**Objective:** Survey the mathematical literature relevant to proving that a specific dynamical system possesses a unique compact global attractor with a Sinai-Ruelle-Bowen (SRB) measure, derived from tracing out an environment via influence-functional methods — and assess what's needed to make this rigorous rather than assumed. This is background research for a theoretical-physics program (a Bohmian-mechanics/number-theoretic synthesis); the goal is a literature map, not new derivations.

**Research questions, organized by dependency:**

1. **Deriving dissipation from a unitary theory.** What is the current state of the art in using Feynman-Vernon influence-functional methods (open quantum systems, system-bath coupling) to derive genuine phase-space volume contraction in a reduced subsystem? Include: Caldeira-Leggett-type models and their rigorous mathematical treatments; conditions under which tracing out bath degrees of freedom provably yields a dissipative (non-unitary, volume-contracting) reduced dynamics; known obstructions or no-go results.

2. **Hyperbolicity of dissipative dynamical systems.** What are the standard methods for proving uniform hyperbolicity (Axiom A) versus weaker notions (singular hyperbolicity, partial hyperbolicity) for a nonlinear dissipative flow? Include: the history and difficulty of such proofs for known chaotic systems (e.g., the Lorenz attractor / Tucker's proof); which weaker hyperbolicity classes still support SRB-measure existence theorems; numerical/empirical methods (Lyapunov spectrum estimation) used as precursors to rigorous proof.

3. **SRB measure existence and computation.** Survey the Ruelle-Bowen existence theorems for SRB measures on hyperbolic attractors, and Bowen/Chernov results on ergodicity and the Bernoulli property. Include the Kaplan-Yorke conjecture and Ledrappier-Young dimension formulas connecting Lyapunov exponents to attractor (Hausdorff/fractal) dimension — specifically, methods for computing dimension from a Lyapunov spectrum in finite- and infinite-dimensional settings.

4. **Adelic and p-adic dynamical systems.** Survey work on dynamical systems and ergodic theory over p-adic fields and adelic spaces (restricted products over primes plus the archimedean/real place). Include p-adic dynamics (Benedetto, Silverman and related), any existing renormalization-group-style arguments for universal dimension ratios in adelic or multi-place dynamical settings, and any existing results (or explicit absence of results) on attractors/SRB measures specifically in adelic configuration spaces.

5. **Product/factorized invariant measures in coupled systems.** What is known about when an SRB measure for a coupled multi-component dynamical system factorizes across components (vs. only weakly correlates, with quantifiable error terms)? This bears on whether an "independence lemma" of the form $\rho(\lambda|\text{settings}) \approx \rho(\lambda)$ can be derived from kernel locality plus initial factorization, or whether such factorization is generically false for coupled attractors.

6. **Geometric measure theory on singular/fractal measures.** Survey normal currents (Federer-Fleming), fractal/Hausdorff-measure divergence theorems, and Ahlfors-regularity — specifically, methods for generalizing continuity-equation/equivariance proofs (standard in smooth dynamics) to flows supported on singular fractal sets.

**Exclusion criteria (important):** Exclude sources that merely share keywords without domain relevance — e.g., anything about "attractors" in machine-learning/LLM-behavior contexts, popular-science or press coverage of Claude/Kimi/AI model comparisons, non-peer-reviewed physics-crank content (self-published "theory of everything" claims on social media), and general audience explainer content. Prioritize peer-reviewed mathematics/mathematical-physics literature (journals, arXiv math-ph/math.DS/math.NT preprints) over blog posts or forum discussions, except where a specific named result is best documented informally.

**Deliverable format:** For each of the six question areas, provide: (a) the most relevant 3-5 papers/results with full citations, (b) a plain-language summary of what each establishes, (c) an explicit note on whether the result applies directly to this problem or would require nontrivial extension, and (d) an assessment of which sub-problem currently has the least literature support (i.e., where the biggest open gap is).
