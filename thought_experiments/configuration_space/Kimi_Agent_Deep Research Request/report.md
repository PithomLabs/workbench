# Bell-Type Bohmian QFT Jump Processes and Measurement-Induced Phase Transitions: A Deep Literature Review

**Research Agent:** Deep Research System
**Date of Search:** 2026-06-21
**Databases Searched:** arXiv, Google Scholar, Web of Science (via search), APS, IOPscience, Springer, Nature
**Search Rounds:** 12+

---

## 1. Executive Summary

### Core Question

Does the existing physics literature contain a direct connection between **Bell-type Bohmian quantum field theory stochastic jump processes** and **measurement-induced phase transitions (MIPT)**—specifically, whether Bell's physically fixed jump rate for a fermionic lattice Hamiltonian acts as an effective monitoring/measurement rate that places the system in an area-law or volume-law entanglement phase?

### Final Status: `not_done_but_adjacent_literature_exists`

### Key Findings

The literature contains **extensive independent development** of both Bell-type QFT jump processes and MIPT/monitored quantum trajectories, but **no direct bridge connecting the two has been established**. The specific question of whether Bell's jump rate formula for fermionic lattice models can be mapped to, compared with, or distinguished from monitored quantum trajectories in MIPT remains **entirely open**.

**What exists:**

1. **Bell-type QFT** is well-developed mathematically. The exact jump-rate formula for fermion number configurations on a lattice was derived by Dürr, Goldstein, Tumulka, and Zanghi (2004–2005) following Bell's 1986 proposal. Global existence of the process was proved by Georgii and Tumulka (2005). The process has been applied to simple QFT models but **not** to Kitaev chains, Majorana chains, or any entanglement-scaling study.

2. **MIPT** is a thriving field with hundreds of papers since 2018–2019. The transition from volume-law to area-law entanglement under increasing measurement rates is well-documented in random quantum circuits, monitored free fermions (with caveats below), interacting Majorana chains, and other systems. Key papers by Skinner, Ruhman, and Nahum (2019); Li, Chen, Fisher, and Ludwig (2018); Alberton, Buchhold, and Diehl (2021); Fava, Piroli, Swann, Bernard, and Nahum (2023); and Foster et al. (2025) define the field.

3. **Quantum trajectories and Bohmian mechanics** have been compared at a formal level. Nassar and Miret-Artés (2013, 2017) developed continuous quantum measurement within the Bohmian framework. Various papers discuss Bohmian trajectories versus quantum jump trajectories, but **no rigorous map** between Bell-type jumps and Lindblad quantum jumps has been constructed.

**What does NOT exist:**

- No paper applies Bell-type QFT jump processes to Kitaev chains, Majorana chains, transverse-field Ising chains, or any other system studied in the MIPT literature.
- No paper compares the Bell jump rate σ(q|q') to a measurement strength or critical measurement rate pc in MIPT.
- No paper studies entanglement scaling (area-law vs. volume-law) along individual Bell histories or their ensembles.
- No paper constructs a formal map between Bell-type stochastic jumps and monitored quantum trajectories, continuous measurement, or Lindblad unravelings.
- No paper uses Bohmian conditional wave functions to derive an effective measurement-like dynamics for a subsystem undergoing Bell jumps.

**Critical caveats from the MIPT literature:**

The MIPT literature reveals an important subtlety: in **one-dimensional free-fermion systems with U(1) charge conservation**, there is **no true MIPT** in the thermodynamic limit. The system is always in an area-law phase for any finite measurement rate. This was established through large-scale numerics (system sizes up to L = 18,000) and nonlinear sigma model field theory by multiple groups (Niederegger, Vovk, Starchl, and Sieberer 2025/2026; Liao, Matheussen, and Zhang 2026; Yin, Bo, and García-García 2026). The earlier claim of a BKT-type transition by Alberton, Buchhold, and Diehl (2021) was a finite-size effect. This significantly constrains the choice of candidate toy models for any Bell-to-MIPT mapping.

**What remains genuinely open:**

The central open question is whether Bell jumps, through conditional wave functions or effective subsystem states, induce a monitoring-like entanglement transition rather than merely tracking hidden-variable motion under an unchanged universal wave function. This requires either: (a) applying Bell-type jump processes to a system that is known to exhibit MIPT (such as multi-flavor Majorana chains or interacting monitored systems), or (b) constructing a formal map between Bell jump rates and effective measurement strengths.

---

## 2. Search Method

### Databases Searched

| Database | Coverage | Access |
|----------|----------|--------|
| arXiv | Full preprint database | Open access |
| Google Scholar | Citation-indexed literature | Open access |
| APS (Physical Review) | Peer-reviewed journals | Abstract/paywall |
| IOPscience | Journal of Physics A, etc. | Abstract/paywall |
| Springer | Book chapters, journals | Abstract/paywall |
| Nature/PNAS | High-impact journals | Abstract/paywall |
| Semantic Scholar | Citation graphs | Open access |
| INSPIRE-HEP | HEP literature | Open access |

### Exact Search Queries Used

**Cluster A (Bell-type QFT):**
- "Bell-type quantum field theory jump process"
- "Bell beables for quantum field theory fermion number lattice"
- "Bell 1986 beables quantum field theory"
- "Dürr Goldstein Tumulka Zanghi Bell-type quantum field theories"
- "minimal jump rates Bohmian mechanics"
- "fermion number beables lattice Bohmian"
- "Bohmian QFT creation annihilation jump rates"
- "stochastic process configuration space Bohmian quantum field theory"
- "Kitaev chain Bohmian mechanics"
- "Majorana chain Bohmian mechanics"

**Cluster B (MIPT):**
- "measurement-induced phase transition volume law area law entanglement"
- "monitored quantum circuits entanglement transition"
- "quantum Zeno phase measurement induced transition"
- "Majorana chain measurement induced phase transition"
- "Kitaev chain measurement induced phase transition"
- "monitored fermions area law volume law"
- "free fermion monitored measurement induced transition controversy"
- "continuous monitoring measurement induced phase transition"

**Cluster C (Bridge):**
- "Bohmian mechanics quantum trajectories continuous measurement"
- "Bohmian conditional wave function measurement"
- "Bell-type QFT Lindblad unraveling"
- "quantum jump trajectories Bohmian mechanics"
- "hidden variables monitored quantum systems"
- "pilot-wave theory quantum Zeno effect"
- "conditional wave function entanglement Bohmian mechanics"

**Cluster D (Entanglement):**
- "Bohmian mechanics entanglement entropy"
- "conditional wave function entanglement entropy"
- "pilot wave theory area law entanglement"
- "Bohmian QFT holography"

### Inclusion/Exclusion Criteria

**Included:**
- Peer-reviewed articles and preprints
- Books and review articles by recognized experts
- Citations with clear relevance to the bridge question

**Excluded:**
- Papers using similar terminology but referring to unrelated concepts (e.g., "Bell inequalities" in entanglement testing unrelated to Bell-type QFT)
- Papers on Bohmian mechanics in non-relativistic quantum mechanics that do not discuss QFT jumps
- Papers on MIPT in systems without fermionic degrees of freedom (unless particularly relevant)

### Limitations

- Some older papers (pre-2000) may have been missed in database indexing.
- Full-text access was limited for some paywalled journals; reliance on abstracts and arXiv preprints where available.
- The search was conducted in English only.
- No direct consultation with authors.

---

## 3. Paper Table

| # | Citation | Year | Authors | Title | Category | Relevance Score (1–10) | What It Claims | What It Does NOT Claim | Why It Matters |
|---|----------|------|---------|-------|----------|----------------------|---------------|----------------------|---------------|
| 1 | PRL 93, 090402 (2004) | 2004 | Dürr, Goldstein, Tumulka, Zanghi | Bohmian Mechanics and Quantum Field Theory | **Background** | 9 | Bell-type QFT uses fermion number as beable; jump rate formula derived from Hamiltonian matrix elements. | Does NOT apply to specific lattice models like Kitaev chain; does NOT discuss entanglement scaling. | Foundational paper defining the jump process for QFT. |
| 2 | J. Phys. A 38, R1 (2005) | 2005 | Dürr, Goldstein, Tumulka, Zanghi | Bell-Type Quantum Field Theories | **Background** | 9 | Comprehensive review of Bell-type QFT; jump rates for particle creation/annihilation; process is Markovian pure jump on configuration space. | Does NOT connect to measurement theory or MIPT; no entanglement analysis. | Core reference for Bell-type QFT formalism. |
| 3 | Commun. Math. Phys. 254, 129 (2005) | 2005 | Dürr, Goldstein, Tumulka, Zanghi | Quantum Hamiltonians and Stochastic Jumps | **Background** | 8 | General method for associating stochastic jump processes to quantum Hamiltonians; process additivity. | Does NOT discuss specific physical models or entanglement. | Mathematical foundation for jump rate construction. |
| 4 | Markov Proc. Rel. Fields 11, 1 (2005) | 2005 | Georgii, Tumulka | Global Existence of Bell's Time-Inhomogeneous Jump Process | **Background** | 7 | Proves global existence and non-explosion of Bell's jump process under suitable assumptions. | Does NOT compute physical observables or entanglement. | Mathematical rigor for the Bell process. |
| 5 | Phys. Rev. X 9, 031009 (2019) | 2019 | Skinner, Ruhman, Nahum | Measurement-Induced Phase Transitions in the Dynamics of Entanglement | **Background** | 8 | Introduces MIPT in random quantum circuits; volume-law to area-law transition as measurement rate increases. | Does NOT discuss Bohmian mechanics or Bell jumps; circuits are discrete not continuous. | Foundational MIPT paper. |
| 6 | Phys. Rev. Lett. 126, 170602 (2021) | 2021 | Alberton, Buchhold, Diehl | Entanglement Transition in a Monitored Free-Fermion Chain | **Background** | 8 | Claims BKT-type entanglement transition in continuously monitored 1D free fermions. | Does NOT mention Bohmian mechanics. **Later work (2025–2026) showed this is a finite-size effect; no true transition in thermodynamic limit.** | Sparked controversy resolved by larger-scale studies. |
| 7 | Phys. Rev. X 13, 041045 (2023) | 2023 | Fava, Piroli, Swann, Bernard, Nahum | Nonlinear Sigma Models for Monitored Dynamics of Free Fermions | **Background** | 8 | Field theory for MIPT in multi-flavor Majorana chains; (log L)² entanglement scaling in "thermal metal" phase. | Does NOT connect to Bohmian jumps; flavor number is a control parameter, not a jump rate. | Key paper showing MIPT exists in multi-flavor but not single-flavor free fermions. |
| 8 | arXiv:2510.23706 (2025) | 2025 | Foster, Guo, Jian, Ludwig | Free-Fermion MIPT in the Presence of Fermion Interactions | **Strong adjacent** | 7 | MIPT for interacting Majorana fermions in class DIII; conjectures noninteracting critical theory with dangerously irrelevant mass. | Does NOT discuss Bohmian mechanics or Bell jumps. | Shows MIPT requires either interactions or multiple flavors in 1D fermions. |
| 9 | Phys. Rev. B (2026) | 2026 | Niederegger, Vovk, Starchl, Sieberer | Absence of Measurement- and Unraveling-Induced Entanglement Transitions in Continuously Monitored 1D Free Fermions | **Background** | 8 | Proves no true MIPT in 1D free fermions for any unraveling; area law always in thermodynamic limit. | Does NOT discuss Bohmian mechanics. | Resolves controversy; constrains toy model choices. |
| 10 | arXiv:2605.10758 (2026) | 2026 | Yin, Bo, García-García | No MIPT in Monitored Non-Interacting 1D Fermions | **Background** | 8 | Confirms absence of MIPT in disordered/quasiperiodic 1D free fermions; finite-size effect explanation. | Does NOT discuss hidden variables or Bell jumps. | Large-scale numerics (L ≤ 18,000) confirming area law for all measurement rates. |
| 11 | PRL 111, 150401 (2013) | 2013 | Nassar, Miret-Artés | Dividing Line between Quantum and Classical Trajectories: Bohmian Time Constant | **Strong adjacent** | 6 | Introduces "Bohmian time constant" for continuous measurement; Bohmian framework for open quantum systems. | Does NOT connect to Bell-type QFT jumps or MIPT. | Bridge paper between Bohmian mechanics and continuous measurement. |
| 12 | Springer (2017) | 2017 | Nassar, Miret-Artés | Bohmian Mechanics, Open Quantum Systems and Continuous Measurements | **Strong adjacent** | 6 | Comprehensive Bohmian treatment of continuous measurement; quantum Langevin-Bohm equation. | Does NOT discuss Bell-type jumps for field theories or MIPT. | Most complete Bohmian-continuous-measurement treatment. |
| 13 | arXiv:2302.12820 (2023) | 2023 | Fava et al. | NLSM for Monitored Dynamics of Free Fermions | **Background** | 7 | Derives effective field theory for monitored free fermion MIPT using replica trick. | Does NOT mention Bohmian mechanics or hidden variables. | Field-theoretic approach to MIPT. |
| 14 | J. Phys. A 44, 345304 (2011) | 2011 | Colin, Wiseman | The Zig-Zag Road to Reality | **Background** | 5 | Compares Bell-type model with Bohmian trajectories for QFT; discusses zig-zag motion for fermions. | Does NOT discuss MIPT or entanglement scaling. | Comparative analysis of Bohmian QFT models. |
| 15 | Phys. Rev. Lett. 132, 110403 (2024) | 2024 | Poboiko, Gornyi, Mirlin | Measurement-Induced Phase Transition for Free Fermions above One Dimension | **Background** | 7 | MIPT exists in d > 1 free fermions; maps to SU(R) replica nonlinear sigma model. | Does NOT discuss Bohmian mechanics. | Shows dimensionality matters for MIPT in free fermions. |
| 16 | SciPost Phys. 14, 3, 031 (2023) | 2023 | Kells, Meidan, Romito | Topological Transitions in Weakly Monitored Free Fermions | **Background** | 6 | Topological transitions in monitored free fermions; Kitaev modes as order parameter. | Does NOT discuss Bell jumps or Bohmian mechanics. | Connects MIPT to topological physics. |
| 17 | Phys. Rev. B 108, 115135 (2023) | 2023 | Lavasani, Luo, Vijay | Monitored Quantum Dynamics and the Kitaev Spin Liquid | **Background** | 6 | Monitored dynamics of Kitaev spin liquid; Majorana parton evolution. | Does NOT discuss Bohmian mechanics or Bell jumps. | Kitaev-specific MIPT study. |
| 18 | Entropy 26, 272 (2024) | 2024 | Zhou | Entanglement Phase Transitions in Non-Hermitian Kitaev Chains | **Background** | 5 | Entanglement transitions in non-Hermitian Kitaev chains; Majorana edge modes. | Does NOT discuss Bohmian mechanics. | Non-Hermitian extension relevant to Lindblad dynamics. |
| 19 | arXiv:2503.21427 (2025) | 2025 | Li, Zhong, Yu | Measurement-Induced Entanglement Phase Transition in Free Fermion Systems (Review) | **Background** | 7 | Reviews MIET in free fermions; discusses controversies about 1D MIPT existence. | Does NOT mention Bohmian mechanics or Bell jumps. | Comprehensive review of free-fermion MIPT status. |
| 20 | Phys. Rev. B 111, 224301 (2025) | 2025 | Klocke, Simm, Zhu, Trebst, Buchhold | Entanglement Dynamics in Monitored Kitaev Circuits | **Background** | 6 | Loop models for monitored Kitaev circuits; quantum Lifshitz scaling. | Does NOT discuss Bohmian mechanics. | Detailed Kitaev MIPT study. |
| 21 | arXiv:2509.10229 (2025) | 2025 | Tzemos, Contopoulos, Zanias | Bohmian Chaos and Entanglement in a Two-Qubit System | **False friend** | 3 | Studies entanglement and chaos in Bohmian two-qubit system. | Uses "Bohmian" for trajectory analysis of qubits, NOT Bell-type QFT jumps. | Only marginally related; non-QFT setting. |
| 22 | arXiv:1512.09084 (2015) | 2015 | Bartolomeo, Caticha | Entropic Dynamics: Schrödinger Equation and Its Bohmian Limit | **False friend** | 2 | Derives Schrödinger equation from entropic dynamics; Bohmian limit as special case. | Does NOT discuss jumps, QFT, or MIPT. | Foundational/philosophical paper. |
| 23 | Found. Phys. 48, 1808 (2018) | 2018 | Vink | Particle Trajectories for Quantum Field Theory | **Background** | 5 | Jump dynamics for fermionic occupation numbers in relativistic QFT; cumulative jump probabilities. | Does NOT discuss entanglement scaling or MIPT. | Alternative trajectory approach for QFT. |
| 24 | arXiv:quant-ph/0506066 (2005) | 2005 | Dürr, Goldstein, Tumulka, Zanghi | Bell's Jump Process in Discrete Time | **Background** | 6 | Discrete-time analog of Bell's jump process; convergence to continuous process. | Does NOT discuss specific Hamiltonians or entanglement scaling. | Useful for numerical simulation of Bell jumps. |
| 25 | Phys. Rev. B 109, 024301 (2024) | 2024 | Qian, Wang | Steering-Induced Phase Transition in Measurement-Only Quantum Circuits | **Background** | 4 | Steering-induced phase transitions in measurement-only circuits. | Does NOT discuss Bohmian mechanics or Bell jumps. | Related phase transition phenomenon. |

---

## 4. Bell-Type QFT Findings

### The Standard Bell-Type Jump-Rate Formula

The Bell-type jump process is a continuous-time Markov pure jump process on the configuration space of fermion number occupations on a spatial lattice. For a quantum system with state vector Ψ_t and Hamiltonian H, the **jump rate** from configuration q' to q is given by:

$$\sigma_t(q|q') = \frac{\left[\frac{2}{\hbar} \text{Im} \langle \Psi_t | P(q) H P(q') | \Psi_t \rangle \right]^+}{\langle \Psi_t | P(q') | \Psi_t \rangle}$$

where P(q) is the projection onto the joint eigenspace of fermion number operators with eigenvalues q(x) at each lattice site x, and [·]⁺ denotes the positive part (max(·, 0)). This formula ensures that the process has |Ψ_t|² as its equivariant distribution at all times.

The process was introduced by Bell in his 1986 paper "Beables for Quantum Field Theory" (reprinted in *Speakable and Unspeakable in Quantum Mechanics*, 1987). The mathematical foundations were developed by Dürr, Goldstein, Tumulka, and Zanghi in a series of papers (2003–2005), with global existence proofs by Georgii and Tumulka (2005).

### Key Properties

| Property | Description |
|----------|-------------|
| **Configuration space** | Lattice fermion number occupations q(x) ∈ {0, 1} |
| **Beables** | Fermion number density (Bell's choice) |
| **Process type** | Markov pure jump process (continuous time) |
| **Jump mechanism** | Particle creation/annihilation via H_I; deterministic drift via H_0 |
| **Equivariance** | |Ψ_t|² is preserved by construction |
| **Free Dirac** | Deterministic motion of n(r) (no jumps) |
| **Interaction H_I** | Integral operator in fermion number representation → jump process |

### Has the Formula Been Applied to Fermionic Lattice Models?

**No.** The existing literature applies Bell-type QFT to:
- Free Dirac fields (deterministic motion only)
- Simple interaction terms B(r)F*(r)F(r) (particle number conserved; jumps only in occupation numbers)
- Relativistic QFT with cut-offs

There is **no published work** applying the Bell jump process to:
- The Kitaev chain
- The transverse-field Ising chain (Jordan-Wigner fermions)
- Interacting Majorana chains
- Any Hubbard-type or tight-binding lattice model

### Grassmann Variables vs. Occupation Numbers

Bell's original proposal uses **occupation-number configurations** (fermion number eigenstates), not Grassmann variables. The fermion operators anticommute, but the beables are the commuting fermion number operators N(x) = F*(x)F(x). This is a key simplification: the configuration space is a product of {0, 1} at each site, not a Grassmann algebra.

### Has Any Paper Studied Entanglement Scaling of Bell Histories?

**No.** There is no literature on entanglement entropy (bipartite or otherwise) computed along Bell-type jump histories or their ensembles. The Bohmian literature discusses entanglement primarily in the context of:
- Nonlocal correlations in EPR-type setups
- The conditional wave function and effective collapse
- Decoherence and the emergence of classicality

But there is **no study** of area-law vs. volume-law scaling in the context of Bell-type or Bohmian dynamics.

---

## 5. MIPT Findings

### Which Models Are Closest to the Proposed Toy Model?

The research question asks about fermionic lattice Hamiltonians with Bell-type jump processes. The closest MIPT literature involves:

| Model | MIPT Status | Key Reference |
|-------|-------------|---------------|
| 1D free fermion chain (U(1) conserved) | **No true MIPT** — area law for all measurement rates in thermodynamic limit | Niederegger et al. (2026); Liao et al. (2026); Yin et al. (2026) |
| Multi-flavor Majorana chain (class BDI/DIII) | **MIPT exists** — (log L)² entanglement in "thermal metal" phase | Fava et al. (2023) |
| Interacting Majorana chain (class DIII) | **MIPT exists** — volume-law to area-law | Foster et al. (2025) |
| 2D free fermions | **MIPT exists** — area × log to area law | Poboiko, Gornyi, Mirlin (2024) |
| Monitored Kitaev spin liquid | Topological MIPT | Lavasani, Luo, Vijay (2023) |
| Monitored Kitaev circuits | Loop-model MIPT | Klocke et al. (2025) |

### The Free-Fermion Controversy (Critical for This Project)

A crucial finding for the proposed research is that **1D free fermions with U(1) charge conservation do not exhibit a true MIPT**. The apparent transition observed in early numerical work (Alberton, Buchhold, Diehl 2021) was a finite-size effect. The correlation length grows exponentially with the inverse measurement rate, making the true area-law phase inaccessible at moderate system sizes. This was established by:

1. **Niederegger, Vovk, Starchl, and Sieberer (2025/2026):** Used replica Keldysh field theory to derive a nonlinear sigma model showing that for 0 ≤ φ < π/2, entanglement ultimately obeys an area law beyond an exponentially large scale ln(l_*) ~ J/[γ cos(φ)].

2. **Yin, Bo, and García-García (2026):** Performed GPU-accelerated numerics up to L = 18,000, confirming the critical monitoring strength is consistent with zero. Analytical mapping to nonlinear sigma model with symmetry change BDI → AIII.

3. **Liao, Matheussen, and Zhang (2026):** Showed disorder does not change the conclusion; same NLSM applies with modified parameters.

**Implication:** A Bell-type toy model built on a single-species free fermion chain (the simplest case) would **not** be expected to show a measurement-rate-dependent entanglement transition, because the corresponding monitored system does not show one.

### Critical Measurement Rates

For systems that DO show MIPT, approximate critical measurement rates are known:

| Model | Critical Rate | Notes |
|-------|-------------|-------|
| Random Clifford circuits (1D) | p_c ≈ 0.16 (projective) | Skinner et al. (2019) |
| Multi-flavor Majorana chain | Depends on flavor number N | Fava et al. (2023) |
| 2D free fermions | γ_c/J ≈ 0.3 (numerical) | Poboiko et al. (2024) |
| Interacting DIII Majorana | Conjectured noninteracting fixed point | Foster et al. (2025) |

### Observables Used in MIPT Studies

| Observable | What It Detects |
|------------|----------------|
| von Neumann entanglement entropy S_A | Primary order parameter; volume-law ↔ area-law |
| Second Rényi entropy S_2 | Easier to compute numerically; same scaling |
| Purity tr(ρ_A²) | Alternative to entropy |
| Mutual information I(A:B) | Nonlocal correlations; KPZ scaling in noisy circuits |
| Number variance (δN)² | Charge fluctuation proxy; related to entanglement |
| Connected correlation functions | Algebraic vs. exponential decay distinguishes phases |

---

## 6. Bridge Analysis

This is the most critical section. The core question is whether a formal map exists between Bell-type stochastic jumps and monitored quantum trajectories in MIPT.

### Is There a Known Formal Map?

**No.** The literature contains no direct map between Bell-type jumps and monitored quantum trajectories. The two frameworks differ in fundamental ways:

| Feature | Bell-Type Jumps | Monitored Quantum Trajectories |
|---------|----------------|-------------------------------|
| **Stochasticity source** | Deterministic rate from Hamiltonian + wave function | Random measurement outcomes |
| **What jumps** | Beable configuration (actual particle positions/numbers) | Quantum state (conditional wave function) |
| **Jump rate** | Fixed by physical Hamiltonian and Ψ | Tunable measurement strength/rate |
| **Wave function evolution** | Universal Ψ evolves unitarily (Schrödinger) | Conditional Ψ evolves stochastically (SSE) |
| **Observables** | Position/number beables have definite values | All observables are probabilistic |
| **Equivariance** | |Ψ|² distribution preserved | Born rule for measurement outcomes |

### Key Category Errors to Avoid

1. **Bell jumps are NOT measurements.** A Bell jump is a change in the actual configuration of beables, not a measurement collapse. The universal wave function does not collapse during a Bell jump; it continues to evolve unitarily according to the Schrödinger equation.

2. **Bell jumps do NOT update the universal wave function.** The wave function Ψ_t evolves deterministically. Only the beable configuration Q_t is stochastic. In monitored quantum trajectories, the conditional wave function itself is stochastic.

3. **Bell jump rates are NOT tunable.** The rate σ(q|q') is completely determined by the Hamiltonian and the wave function. There is no external "measurement strength" parameter.

### Could Bell Jumps Induce Effective Measurement-Like Dynamics?

This is the central open question. Several indirect routes could be explored:

**Route 1: Conditional Wave Function**

In Bohmian mechanics, the conditional wave function of a subsystem is defined by evaluating the universal wave function at the actual configuration of the environment. During a Bell jump that changes a fermion number in the environment, the conditional wave function of the subsystem undergoes a discontinuous change. This **resembles** a measurement-induced collapse, but:
- The change is deterministic (given the jump), not stochastic
- The jump itself is stochastic, but its rate is fixed by the Hamiltonian
- There is no "outcome" in the measurement sense

**Route 2: Effective Subsystem State**

If one traces over the beable configuration (rather than the quantum state), the effective density matrix of a subsystem might show dephasing or decoherence due to the jumps in the environment. This has not been studied.

**Route 3: Stochastic Unraveling Analogy**

The Bell process can be viewed as an "unraveling" of the quantum master equation, but one that is not associated with any Lindblad operators or measurement scheme. It is a fundamentally different type of unraveling.

### What Mathematical Object Would Make the Comparison Well-Typed?

To compare Bell jumps to MIPT measurement rates, one would need:

1. **A Bell-type process for a finite lattice fermion model** (e.g., Kitaev chain, Hubbard model) — this has not been constructed.

2. **An entanglement entropy computed along Bell histories** — this has not been defined or computed.

3. **A map from the Bell jump activity to an effective measurement rate** — this would require interpreting the jump probability per unit time as a "measurement strength." This is conceptually problematic because Bell jumps are physical configuration changes, not information extraction.

4. **Alternatively, a comparison of the conditional wave function's entanglement scaling** — define the effective entanglement of the conditional wave function during Bell evolution and compare to monitored trajectory entanglement.

### What Has Been Done in Related Directions?

| Paper | What They Did | Gap |
|-------|--------------|-----|
| Nassar & Miret-Artés (2013, 2017) | Bohmian framework for continuous measurement; quantum Langevin-Bohm equation | No connection to Bell jumps or lattice models |
| Bauer, Bernard, Tilloy (2015) | Computed quantum jump rates for general Lindbladians | No Bohmian connection |
| Various quantum trajectory papers | Unraveling Lindblad equations with stochastic jumps | Bell jumps are not Lindblad unravelings |
| Colin & Wiseman (2011) | Compared Bell-type and Bohmian models for fermions | No MIPT or entanglement scaling discussed |

---

## 7. Candidate Toy Models

Based on the literature review, here are ranked candidate toy models for exploring the Bell-to-MIPT question:

### Model 1: Multi-Flavor Majorana Chain (Class BDI/DIII)

| Property | Description |
|----------|-------------|
| **Hamiltonian** | H = -i∑_{a=1}^N ∑_j (J_1 γ_{2j-1,a} γ_{2j,a} + J_2 γ_{2j,a} γ_{2j+1,a}) |
| **Why relevant** | This system shows a genuine MIPT with N flavors; entanglement scales as (log L)² in the "thermal metal" phase |
| **Phase diagram** | Established via NLSM field theory (Fava et al. 2023) |
| **Bell jump rates** | Moderate complexity — need to construct Bell process for Majorana fermions |
| **Particle-number changing** | No (quadratic Hamiltonian preserves parity) |
| **Free/Interacting** | Free (Gaussian) for fixed N |
| **Expected obstruction** | Majorana representation requires mapping to Dirac fermions for Bell beables |
| **First finite-size test** | Compute Bell jump rate for N=2 flavors, L=10–20 sites; track conditional wave function entanglement |

### Model 2: Interacting Majorana Chain (Class DIII)

| Property | Description |
|----------|-------------|
| **Hamiltonian** | H = H_free + H_int with quartic Majorana interactions |
| **Why relevant** | Foster et al. (2025) conjecture the MIPT is described by noninteracting DIII theory with dangerously irrelevant mass |
| **Phase diagram** | Conjectured; needs numerical verification |
| **Bell jump rates** | More complex — interactions create/annihilate fermion pairs |
| **Particle-number changing** | Parity-conserving but allows pair creation/annihilation |
| **Free/Interacting** | Interacting (non-Gaussian) |
| **Expected obstruction** | Interacting field theory is harder to regularize on lattice |
| **First finite-size test** | Numerical simulation of Bell process with interaction terms |

### Model 3: Finite Kitaev Chain (Single Flavor)

| Property | Description |
|----------|-------------|
| **Hamiltonian** | H = -μ/2 ∑_j c_j† c_j - t/2 ∑_j (c_j† c_{j+1} + h.c.) + Δ/2 ∑_j (c_j c_{j+1} + h.c.) |
| **Why relevant** | The simplest fermionic lattice model; exactly solvable; topological phase transition |
| **Phase diagram** | Well-known ground-state phase diagram (topological/trivial) |
| **Bell jump rates** | Relatively simple — can be computed from matrix elements |
| **Particle-number changing** | Yes (Δ terms change fermion number by 2) |
| **Free/Interacting** | Free (quadratic) |
| **Expected obstruction** | **1D free fermions do NOT show MIPT** (area law for all measurement rates). This model may not show the desired transition. |
| **First finite-size test** | Construct Bell process; compute conditional wave function entanglement vs. measurement-rate equivalent |

### Model 4: Monitored Random Quantum Circuit (Reference)

| Property | Description |
|----------|-------------|
| **Hamiltonian** | None (discrete-time random unitaries + projective measurements) |
| **Why relevant** | The canonical MIPT system; known critical exponents (ν ≈ 4/3 in 1D) |
| **Phase diagram** | Well-established volume-law ↔ area-law transition |
| **Bell jump rates** | N/A — no Hamiltonian to define Bell jumps |
| **Particle-number changing** | Depends on gate set |
| **Free/Interacting** | Interacting (Haar-random gates) |
| **Expected obstruction** | No Hamiltonian means no Bell process can be defined; this is a reference model only |
| **First finite-size test** | Compare entanglement scaling in monitored circuits to any Bell-process model |

### Recommendation

**Model 1 (multi-flavor Majorana chain)** is the strongest candidate because:
1. It has a proven MIPT in the monitored setting
2. It is free/Gaussian, making Bell jump rates computable
3. The NLSM field theory provides analytical control
4. It directly connects to existing MIPT literature

---

## 8. Gap Statement

> The literature appears to contain extensive work on Bell-type QFT jump processes and extensive work on MIPT/monitored quantum trajectories, but **no direct study comparing Bell's physically fixed jump rate to MIPT critical measurement rates**. The open bridge is whether Bell jumps, through conditional wave functions or effective subsystem states, induce a monitoring-like entanglement transition rather than merely tracking hidden-variable motion under an unchanged universal wave function.

More specifically, the following gaps have been identified:

1. **No Bell-type process has been constructed for any fermionic lattice model** (Kitaev, Majorana, Ising, or Hubbard). All existing Bell-type QFT work uses continuum or abstract lattice regularizations.

2. **No entanglement scaling study exists for Bell histories.** The area-law vs. volume-law question has never been asked in the context of Bohmian or Bell-type dynamics.

3. **No formal map exists between Bell jumps and Lindblad quantum jumps.** The category error (beable configuration change vs. quantum state update) has not been resolved or circumvented.

4. **The conditional wave function's role in entanglement production during Bell jumps is unexplored.** This is potentially the most promising route for constructing a bridge.

5. **The free-fermion MIPT controversy implies that simple toy models may not show the desired transition**, requiring more sophisticated (multi-flavor or interacting) models.

---

## 9. EBP 2.1 Ledger

```json
{
  "main_claim": "Bell-type QFT stochastic jump processes for fermionic lattice Hamiltonians may act as effective monitoring dynamics that induces an entanglement phase transition (area-law vs. volume-law) in the conditional wave function, analogous to MIPT.",
  "status": "unverified_hypothesis",
  "needMap": "No formal map between Bell jumps and monitored quantum trajectories exists. Need to construct either: (a) a direct mapping from Bell jump rates to effective measurement strengths, or (b) a simulation protocol comparing Bell history entanglement to monitored trajectory entanglement.",
  "needInvariant": "Need to identify whether there is an invariant (conserved quantity) under Bell jumps that prevents or enables entanglement transitions. The U(1) charge conservation in free fermions may be relevant.",
  "needToyCheck": "Need to implement Bell-type jump process for a specific fermionic lattice model (recommended: multi-flavor Majorana chain) and compute conditional wave function entanglement entropy scaling.",
  "needNullModel": "The null model is that Bell jumps do NOT induce any entanglement transition — the conditional wave function remains in an area-law phase (or whatever phase the unitary evolution would produce) regardless of jump activity. This is consistent with the absence of MIPT in 1D free fermions.",
  "needObstruction": "Key obstructions: (1) Bell jumps are configuration changes, not state updates; (2) Jump rates are fixed by Hamiltonian, not tunable; (3) Universal wave function evolves unitarily, never collapses; (4) 1D free fermions do not show MIPT under any measurement protocol.",
  "needFaithfulnessReview": "Need to verify that any claimed bridge does not conflate ontological jumps (beables) with epistemic updates (measurement outcomes). The conditional wave function approach (Dürr-Goldstein-Zanghi) is the most promising faithful framework.",
  "promotion_status": "unpromoted_literature_review_only"
}
```

---

## 10. Final Recommendation

### Recommended Next Step: `derive_conditional_wave_function_bridge`

The most productive path forward is:

1. **Construct the Bell-type jump process for a multi-flavor Majorana chain** (Model 1 above). This is the simplest system known to exhibit MIPT in the monitored setting.

2. **Define and compute the conditional wave function entanglement entropy** along Bell histories. Specifically, for a bipartition of the chain, compute the entanglement entropy of the conditional wave function as a function of time.

3. **Compare to monitored trajectory entanglement** for the same Hamiltonian and measurement protocol. The key question is whether the Bell jump activity (which is fixed by the Hamiltonian) corresponds to a particular effective measurement rate in the monitored system.

4. **If a transition is found**, characterize its critical properties and compare to known MIPT universality classes.

5. **If no transition is found**, determine whether this is due to: (a) the Bell process being fundamentally different from monitored dynamics, (b) the specific model choice, or (c) a general obstruction preventing Bell jumps from inducing measurement-like effects.

### Alternative: `implement_Bell_rate_calculator`

A more modest first step is to implement a numerical Bell jump rate calculator for a specific fermionic lattice model (e.g., the Kitaev chain) and characterize the jump statistics (mean jump rate, jump size distribution, spatial correlations). This provides baseline data for any future entanglement study.

### What NOT to Do

- **Do not** claim that Bohmian mechanics "explains" MIPT or holography without explicit calculation.
- **Do not** conflate Bell jumps with measurement collapses.
- **Do not** assume that any jump process is equivalent to any other — the mathematical structure matters.

---

## Summary: What We Know / What We Do Not Know / What to Test Next

### What We Know

1. The Bell-type jump-rate formula for fermion number configurations on a lattice is well-established (Dürr-Goldstein-Tumulka-Zanghi 2004–2005).

2. MIPT is a well-studied phenomenon in monitored quantum circuits and interacting fermionic systems, with clear volume-law to area-law transitions.

3. **1D single-flavor free fermions do NOT show a true MIPT** — they are always in an area-law phase for any finite measurement rate in the thermodynamic limit (Niederegger et al. 2026; Yin et al. 2026).

4. Multi-flavor Majorana chains and interacting Majorana systems DO show genuine MIPT (Fava et al. 2023; Foster et al. 2025).

5. No published work connects Bell-type QFT jumps to MIPT or even studies entanglement scaling in Bell histories.

### What We Do Not Know

1. Whether Bell jumps can induce an effective measurement-like dynamics for a subsystem.

2. Whether the conditional wave function entanglement along Bell histories shows any transition-like behavior.

3. Whether the fixed Bell jump rate for a given Hamiltonian corresponds to a particular point in a monitored system's phase diagram.

4. Whether multi-flavor or interacting models are needed for any nontrivial entanglement scaling in Bell dynamics.

### What to Test Next

1. **Implement** the Bell-type jump process for a multi-flavor Majorana chain.

2. **Compute** the conditional wave function entanglement entropy along Bell histories.

3. **Compare** to monitored trajectory entanglement for the same system.

4. **Characterize** any transition-like behavior and determine whether it maps to known MIPT physics.

---

## References

[^1^] J.S. Bell, "Beables for Quantum Field Theory," Phys. Rep. 137, 49–54 (1986). Reprinted in *Speakable and Unspeakable in Quantum Mechanics* (Cambridge University Press, 1987).

[^2^] D. Dürr, S. Goldstein, R. Tumulka, and N. Zanghì, "Bohmian Mechanics and Quantum Field Theory," Phys. Rev. Lett. 93, 090402 (2004).

[^3^] D. Dürr, S. Goldstein, R. Tumulka, and N. Zanghì, "Bell-Type Quantum Field Theories," J. Phys. A 38, R1 (2005).

[^4^] D. Dürr, S. Goldstein, R. Tumulka, and N. Zanghì, "Quantum Hamiltonians and Stochastic Jumps," Commun. Math. Phys. 254, 129 (2005).

[^5^] H.-O. Georgii and R. Tumulka, "Global Existence of Bell's Time-Inhomogeneous Jump Process for Lattice Quantum Field Theory," Markov Proc. Rel. Fields 11, 1 (2005).

[^6^] B. Skinner, J. Ruhman, and A. Nahum, "Measurement-Induced Phase Transitions in the Dynamics of Entanglement," Phys. Rev. X 9, 031009 (2019).

[^7^] O. Alberton, M. Buchhold, and S. Diehl, "Entanglement Transition in a Monitored Free-Fermion Chain: From Extended Criticality to Area Law," Phys. Rev. Lett. 126, 170602 (2021).

[^8^] M. Fava, L. Piroli, T. Swann, D. Bernard, and A. Nahum, "Nonlinear Sigma Models for Monitored Dynamics of Free Fermions," Phys. Rev. X 13, 041045 (2023).

[^9^] M.S. Foster, H. Guo, C.-M. Jian, and A.W.W. Ludwig, "Free-Fermion Measurement-Induced Volume- to Area-Law Entanglement Transition in the Presence of Fermion Interactions," arXiv:2510.23706 (2025).

[^10^] C. Niederegger, T. Vovk, E. Starchl, and L.M. Sieberer, "Absence of Measurement- and Unraveling-Induced Entanglement Transitions in Continuously Monitored One-Dimensional Free Fermions," Phys. Rev. B (2026) [arXiv:2510.19459].

[^11^] C. Yin, F. Bo, and A.M. García-García, "No Measurement Induced Phase Transition in the Entanglement Dynamics of Monitored Non-Interacting One-Dimensional Fermions," arXiv:2605.10758 (2026).

[^12^] Y. Liao, M. Matheussen, and X. Zhang, "Measurement-Induced Phase Transitions in Disordered Fermions," arXiv:2605.05306 (2026).

[^13^] A.B. Nassar and S. Miret-Artés, "Dividing Line between Quantum and Classical Trajectories in a Measurement Problem: Bohmian Time Constant," Phys. Rev. Lett. 111, 150401 (2013).

[^14^] A.B. Nassar and S. Miret-Artés, *Bohmian Mechanics, Open Quantum Systems and Continuous Measurements* (Springer, 2017).

[^15^] M. Bauer, D. Bernard, and A. Tilloy, "Computing the Rates of Measurement-Induced Quantum Jumps," J. Phys. A 48, 25FT02 (2015).

[^16^] S. Colin and H.M. Wiseman, "The Zig-Zag Road to Reality," J. Phys. A 44, 345304 (2011).

[^17^] A. Lavasani, Z.-X. Luo, and S. Vijay, "Monitored Quantum Dynamics and the Kitaev Spin Liquid," Phys. Rev. B 108, 115135 (2023).

[^18^] K. Klocke et al., "Entanglement Dynamics in Monitored Kitaev Circuits," Phys. Rev. B 111, 224301 (2025).

[^19^] I. Poboiko and A.D. Mirlin, "Quantum Dynamics of Monitored Free Fermions: Evolution of Quantum Correlations and Scaling at Measurement-Induced Phase Transition," arXiv:2512.01772 (2025).

[^20^] H.-Z. Li, J.-X. Zhong, and X.-J. Yu, "Measurement-Induced Entanglement Phase Transition in Free Fermion Systems," J. Phys.: Condens. Matter 37, 273002 (2025).

[^21^] S. Goldstein, R. Tumulka, and N. Zanghì, "Bohmian Trajectories as the Foundation of Quantum Mechanics," in *Quantum Trajectories* (CRC Press, 2011).

[^22^] R. Tumulka and H.-O. Georgii, "Some Jump Processes in Quantum Field Theory," in *Interacting Stochastic Systems* (Springer, 2005).

[^23^] G. Kells, D. Meidan, and A. Romito, "Topological Transitions in Weakly Monitored Free Fermions," SciPost Phys. 14, 031 (2023).

[^24^] D. Dürr, S. Goldstein, R. Tumulka, and N. Zanghì, "Bell's Jump Process in Discrete Time," arXiv:quant-ph/0506066 (2005).

[^25^] J.C. Vink, "Particle Trajectories for Quantum Field Theory," Found. Phys. 48, 1808 (2018).
