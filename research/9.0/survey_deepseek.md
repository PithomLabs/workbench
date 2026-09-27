# Survey and Revision of Assumptions: BM + CDT + AS as TOE Candidate

## Framing

Per the Reality-First discipline, assumptions must be explicitly stated, classified as necessary or contingent, and checked against the 15 maps. Any assumption that violates the maps must be revised or retired. The goal is not to make the synthesis pretty but to make it coherent — meaning: no assumption contradicts another, and every assumption is grounded in a map's shine domain.

The three theories overlap on the Dance (dynamics) but diverge on the Dancer (what exists) and the Stage (where it exists). Below is the survey and revision.

---

## Part 1 — The Stage

### 1.1 Assumptions Survey

| Theory | Stage assumption | Grounded in |
|---|---|---|
| **BM** | Fixed $\mathbb{R}^{3N}$ configuration space; smooth manifold | DOF (state space), Geometry (manifold) |
| **CDT** | 4D triangulation with causal time-slicing; emerges from simplex gluing | Calculus (path integral), Topology (causal structure) |
| **AS** | Continuous Euclidean manifold at all scales; effective metric $g_{\mu\nu}(k)$ | Calculus (RG flow), Geometry (metric) |

### 1.2 Conflicts

- **Dimensionality:** BM assumes fixed 3+1. CDT computes $d_s$ running from 2 (UV) to 4 (IR). AS computes $g_{\mu\nu}(k)$ running.
- **Continuity:** BM and AS assume smooth manifolds. CDT has discrete simplicial structure at Planck scale.
- **Signature:** BM and CDT (Lorentzian version) assume Lorentzian. AS is typically Euclidean.
- **Background:** BM is background-dependent. CDT is background-independent. AS is background-dependent (on a fixed topology).

### 1.3 Revised Stage Assumptions

**Retire:**
- BM's $\mathbb{R}^{3N}$ as fundamental. Demote to IR-emergent.
- AS's fixed Euclidean manifold. Replace with effective manifold at scale $k$.

**Retain:**
- CDT's causal time-slicing as the fundamental Stage structure.
- CDT's simplicial building blocks as the UV Stage.
- AS's effective metric as the coarse-grained description.

**Revised Stage:**

$$
\boxed{
\begin{aligned}
&\textbf{Fundamental:} \quad \text{CDT triangulation with causal structure.} \\
&\textbf{Effective:} \quad g_{\mu\nu}(k) = \text{AS coarse-grained metric.} \\
&\textbf{IR-emergent:} \quad \mathbb{R}^{3+1} = \text{BM configuration space.}
\end{aligned}
}
$$

The Stage is not one object. It is a **three-level structure**: discrete causal (UV) → continuous metric (mid) → flat Euclidean/Lorentzian (IR).

**Mercury:** the scale $k_*$ at which the discrete-to-continuous transition occurs. Prediction: $k_* \approx M_P$.

---

## Part 2 — The Dancer

### 2.1 Assumptions Survey

| Theory | Dancer assumption | Grounded in |
|---|---|---|
| **BM** | $N$ point particles with definite positions; wavefunction on configuration space | DOF (state space), Algebra (observables) |
| **CDT** | No fundamental matter; matter is added as a field on the triangulation | (Silent on matter content) |
| **AS** | Field content is input; flows to fixed point; matter content is a boundary condition | (Silent on matter content) |

### 2.2 Conflicts

- **Ontology:** BM asserts definite configurations. CDT has no definite configuration (path integral). AS is silent on ontology.
- **Particles vs fields:** BM is particles-first. CDT and AS are fields-first.
- **Wavefunction:** BM's wavefunction is fundamental. CDT/AS have no wavefunction at the fundamental level.
- **Matter content:** BM assumes $N$ particles. CDT/AS require matter content as an input.

### 2.3 Revised Dancer Assumptions

**Retire:**
- BM's point particles as fundamental. Demote to IR-emergent.
- BM's wavefunction as fundamental at all scales. Demote to IR-emergent.
- CDT/AS silence on matter content. Replace with explicit statement: matter content is an input.

**Retain:**
- BM's definite configuration as an IR ontology.
- AS's field content as a scale-dependent input.
- CDT's ability to host matter fields on the triangulation.

**Revised Dancer:**

$$
\boxed{
\begin{aligned}
&\textbf{Fundamental:} \quad \text{No fundamental matter; fields on CDT triangulation.} \\
&\textbf{IR-emergent:} \quad \text{Definite configurations } Q(t) \in \mathbb{R}^{3N}. \\
&\textbf{Input:} \quad \text{Field content (gauge group, representations).}
\end{aligned}
}
$$

The Dancer is not fundamental at the UV. It is a **coarse-grained description** of fields on the CDT triangulation. The point-particle picture is an IR limit.

**Mercury:** the scale at which the field-to-particle transition occurs. Prediction: $k_{\rm particle} \sim$ electroweak scale (not Planck).

---

## Part 3 — The Dance

### 3.1 Assumptions Survey

| Theory | Dance assumption | Grounded in |
|---|---|---|
| **BM** | Guidance equation $\dot Q = \nabla S / m$; quantum potential | Calculus (flow) |
| **CDT** | Path integral over triangulations with causal constraints | Calculus (path integral) |
| **AS** | Wetterich equation $\partial_k \Gamma_k = \frac12 \text{Tr}[...]$ | Calculus (RG flow) |

### 3.2 Conflicts

- **Type of dynamics:** BM is deterministic trajectory. CDT is stochastic path integral. AS is deterministic RG flow.
- **Time:** BM uses physical time. CDT uses causal time-slicing. AS uses RG scale $k$.
- **Reversibility:** BM is time-reversible. CDT is Euclidean (not time-reversible in the usual sense). AS is dissipative (RG flow is one-way).
- **Relation to Stage:** BM's dynamics is on the Stage. CDT's dynamics generates the Stage. AS's dynamics describes the Stage's scale-dependence.

### 3.3 Revised Dance Assumptions

**The three flows are distinct but related:**

- **Guidance flow (BM):** IR dynamics, given Stage + Dancer.
- **Path integral (CDT):** UV dynamics, generating Stage.
- **RG flow (AS):** Scale-dependent dynamics, connecting UV and IR.

**Revised Dance:**

$$
\boxed{
\begin{aligned}
&\textbf{UV:} \quad \text{CDT path integral (generates triangulations).} \\
&\textbf{mid:} \quad \text{AS RG flow (coarse-grains triangulations to metric).} \\
&\textbf{IR:} \quad \text{BM guidance (evolves configurations on the emergent metric).}
\end{aligned}
}
$$

**The key structural claim:** The three flows are **the same flow at different scales**. The CDT path integral is the UV limit of the AS RG flow, which is the UV limit of the BM guidance flow.

**Mercury:** the matching condition that makes the three flows compatible.

$$
\boxed{
\alpha_{\rm CDT} = \alpha_{\rm AS} = \alpha_{\rm BM} = \alpha
}
$$

If the three exponents agree, the flows are the same. If they disagree, the synthesis fails.

**This is the Mercury. Compute $\alpha$.**

---

## Part 4 — The Revised Synthesis

### 4.1 Coherence Conditions

The synthesis is coherent iff:

1. **Stage:** CDT triangulation → AS effective metric → BM configuration space, with matching at $k_*$.
2. **Dancer:** CDT fields → AS running content → BM configurations, with matching at $k_{\rm particle}$.
3. **Dance:** CDT path integral → AS RG flow → BM guidance, with matching $\alpha$.

### 4.2 The Mercury

$$
\boxed{
\begin{aligned}
&\textbf{Compute } \alpha \textbf{ from CDT.} \\
&\textbf{Compute } \alpha \textbf{ from AS.} \\
&\textbf{Compute } \alpha \textbf{ from BM (fractional guidance).} \\
&\textbf{Compare.}
\end{aligned}
}
$$

**If all three agree:** the synthesis is coherent. The three theories describe the same physics at different scales.

**If they disagree:** the synthesis fails. One or more theories must be revised.

### 4.3 The Null

$$
M_{\rm null} = \text{any two of the three} + \text{generic third}
$$

If the null reproduces the matching, the third is spectator.

### 4.4 Kill Conditions

- **Kill D:** $\alpha_{\rm CDT} \neq \alpha_{\rm AS}$ or $\alpha_{\rm AS} \neq \alpha_{\rm BM}$.
- **Kill E:** The matching scale $k_*$ does not exist or is not unique.
- **Kill F:** The fractional BM guidance equation cannot be formulated consistently.

---

## Part 5 — Constitutional Compliance

| Article | Requirement | Assessment |
|---|---|---|
| I — Four components | No silent substitution | **PASS** — Stage/Dancer/Dance separated |
| II — Sharp corners | Arithmetic tested where it shines | **PASS** — no arithmetic forced |
| III — Decision tree | No claim past its Q | **PASS** — claims are at Q1–Q2 |
| IV — Null discipline | Matched generic null | **DEFINED** — null specified |
| V — Promotion chain | Typed, null, ablation | **PARTIAL** — null defined, not run |
| VI — Kill conditions | Tested, not just stated | **PARTIAL** — conditions stated, not tested |
| VII — Do not overclaim | Correct classification | **PASS** — claims marked as programmatic |

---

## Part 6 — The One-Sentence Summary

$$
\boxed{
\begin{aligned}
&\textbf{BM, CDT, AS each assume different Stages, Dancers, and Dances.} \\
&\textbf{Revised synthesis: three-level structure (UV / mid / IR).} \\
&\textbf{Mercury: } \alpha_{\rm CDT} = \alpha_{\rm AS} = \alpha_{\rm BM}. \\
&\textbf{Next step: compute the three } \alpha \textbf{'s.}
\end{aligned}
}
$$

**The synthesis is coherent iff the three flows are the same flow at different scales. The Mercury tests this. Compute $\alpha$.**
