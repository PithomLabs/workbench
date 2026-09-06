# ROUND 3 — FROM CONSOLIDATION TO CONSTRUCTION
## Audit of the synthesis, two new theorems, and the operational form of the attack

Your consolidation is correct in all its major judgments. I endorse: C-not-D; the death of the Reynolds route; Hudson's demotion to a representation constraint; the closure of the naive transplant; the four-gate table; and the strategic conclusion that the next unit of progress is a theorem or a counterexample, not a survey. What follows is (1) an audit with two refinements — one of which corrects my own Round-2 Lemma A, (2) two theorems that are provable *now* and that materially relocate the remaining gap, (3) the precise logical form of the missing structure, and (4) the toy-model program rendered operational, with falsification tests that can be run immediately.

---

## 1. AUDIT: TWO REFINEMENTS TO THE CONSOLIDATION

### 1.1 Correction to the correction: the three-tier osmotic statement

You are right that my Lemma A, read unconditionally ("any deterministic flow, Markov or not"), was too broad, and you identified the correct repair: **u is a scale-dependent object**. The fully correct statement has three tiers:

- **(A1) Fixed differentiable scale:** for any deterministic flow with differentiable coarse trajectories, the forward and backward conditional drifts coincide; u ≡ 0. [CONTRADICTED — transplant at fixed scale.]
- **(A2) Diffusion-limit scale:** in *any* rigorous deterministic stochastic limit (Melbourne–Stuart, Kelly–Melbourne, Gordin, Lorentz-gas class), the emergent process is a diffusion with density ρ_t, and by the reversion identity (Haussmann–Pardoux 1986) its emergent osmotic velocity is **automatically**
 $$u^{\rm eff}=\tfrac{1}{2}\nu\,\nabla\ln\rho_t,$$
 with ν the emergent diffusion matrix. **The form u = c∇ln ρ is therefore free.** No mechanism, ingenuity, or invariant-set geometry is needed to produce ∇ln ρ; any diffusion limit produces it.
- **(A3) Nelson/Madelung corner:** what never emerges generically is the *Nelson pair*: a forward drift of the form b = ∇S/m + u with S self-consistently solving the HJ equation containing Q[ρ_t], at a universal ν = ħ/m, for an open family of initial densities.

This refinement is not cosmetic: it *re-aims the battlefield*. The consolidated gate table should be amended:

| Gate | Original formulation | Amended formulation |
|---|---|---|
| 1 | Deterministic dynamics → effective stochasticity | **Yes, established** — and any such limit *automatically* yields the ∇ln ρ form |
| 3 | Deterministic structure selects Fisher energy | Split: (3a) the *shape* of u: **free**; (3b) the *dynamical role* of Fisher as conserved Hamiltonian energy with self-consistent drift: **no mechanism**; (3c) the coefficient ν = ħ/m universal: **no mechanism** |

Consequence: "osmotic" survives only as an *emergent object of the diffusive corner* — but the diffusive corner is precisely the one Madelung dynamics cannot live in (Theorem 2 below). The program's target remains what you stated in §4: IST → Fisher-as-Hamiltonian-term → Q. The refinement makes this sharper, not softer.

### 1.2 The Γ-convergence concern is even sharper than you stated: a small lemma

Your §9 says the desired Γ-limit must select the *field* √ρ, the coefficient, and the dynamical role. There is a precise sense in which "is a Dirichlet form" is **vacuous** as a selection criterion:

> **Lemma (vacuity of Dirichlet form).** Any local functional of the form ∫ W(ρ)|∇ρ|² dx can be rewritten as λ∫|∇F(ρ)|² dx for infinitely many fields F (choose F with (F′)² ∝ W up to constants). Hence "the emergent energy is a Dirichlet energy of some field" carries **zero** selection content. The content is entirely in: *which F is microscopically realized*, *what role the energy plays* (conserved Hamiltonian term vs. dissipative contribution), and *the constant*.

So the attack must be organized around exactly three questions: (i) is F = √ρ *realized* in the microscopic ontology; (ii) is the energy *conservative and Hamiltonian*; (iii) is the constant *universal*. Everything else is proof technology.

---

## 2. TWO THEOREMS PROVABLE NOW

Both are category-3 items (new theorems within existing mathematics). I give statements and proof cores; both should be written out rigorously as the first deliverable of Round 3.

### Theorem 1 (Linearity of the Madelung transform selects Fisher — constant relocates to the phase)

**Setting.** Let the emergent dynamics be Hamiltonian on density space with energy
$$E[\rho,S]=\int \rho\frac{|\nabla S|^2}{2m}\,dx+\int\rho V\,dx+E_q[\rho],\qquad E_q[\rho]=\int f(\rho,\nabla\rho)\,dx,$$
with f ∈ C², rotation invariant, and no dependence on higher derivatives. Hamilton's equations (Otto/canonical form): ∂_tρ = −∇·(ρ∇S/m), ∂_tS = −|∇S|²/2m − V − δE_q/δρ. Apply the Madelung transform with phase constant κ:
$$\psi=\sqrt{\rho}\;e^{iS/\kappa}.$$

**Claim.** The induced evolution of ψ is linear **iff**
$$E_q=\frac{\kappa^2}{8m}\,I_F[\rho]+\text{(const./null Lagrangian)},\qquad I_F=\int\frac{|\nabla\rho|^2}{\rho}\,dx .$$

**Proof core.** Direct computation gives
$$\partial_t\psi=\frac{i\kappa}{2m}\Delta\psi-\frac{i}{\kappa}V\psi-\frac{i}{\kappa}\Big[\frac{\delta E_q}{\delta\rho}+\frac{\kappa^2}{2m}\frac{\Delta\sqrt\rho}{\sqrt\rho}\Big]\psi .$$
(The kinetic pieces −∇·(√ρ∇S)/m and −iφ|∇S|²/2mκ cancel identically against the Δψ term.) Hence linearity of the induced ψ-evolution ⟺
$$\frac{\delta E_q}{\delta\rho}=-\frac{\kappa^2}{2m}\frac{\Delta\sqrt\rho}{\sqrt\rho}\quad\text{identically.}$$
Now compute the Euler–Lagrange derivative of the general local functional: writing f = a(ρ)|∇ρ|² + b(ρ),
$$\frac{\delta E_q}{\delta\rho}=-2a(\rho)\Delta\rho-a'(\rho)|\nabla\rho|^2+b'(\rho),$$
while
$$-\frac{\kappa^2}{2m}\frac{\Delta\sqrt\rho}{\sqrt\rho}=-\frac{\kappa^2}{4m}\frac{\Delta\rho}{\rho}+\frac{\kappa^2}{8m}\frac{|\nabla\rho|^2}{\rho^2}.$$
Matching the Δρ coefficient forces a(ρ) = κ²/(8mρ); the |∇ρ|² coefficient is then *automatically* consistent (a′ = −κ²/8mρ²), and b′ = 0. Functionals with Δρ-dependence produce fourth-order Euler–Lagrange expressions and cannot match a second-order operator unless degenerate; odd-in-∇ρ terms are killed by rotation invariance. Conversely, E_q = (κ²/8m)I_F gives Schrödinger exactly. Uniqueness up to null Lagrangians follows by the standard exactness argument for local variational expressions. ∎

**Three consequences, each important.**

1. **The "Fisher-selection" problem splits.** The *shape* 1/ρ (equivalently, the field √ρ) is selected by a single demand: **linearity of the emergent complex field**. No stochastic principle is needed for the shape. What remains unexplained is linearity itself — and linearity is the quantum assumption (Polchinski 1991: without it, signaling between ensemble preparations). So the gap is now stated exactly: **"linearity without quantum mechanics."** [Category 4 shrinks to this.]

2. **The ħ problem relocates.** The constant does not sit in the energy independently; it sits in the *phase normalization* κ of the amplitude, and the energy constant is then forced, c = κ²/8m. Therefore the ħ-universality question is exactly the question: *what fixes the universal action unit of the emergent phase?* This is the same constant that appears in Wallstrom's circulation condition ∮∇S·dl ∈ 2πκℤ/m. **Fisher-constant and monodromy-constant are one constant.** This unifies two of your Category-4 items into one structure.

3. **Scope caveat (adversarial self-check).** Theorem 1 is conditional on E_q being a local functional of ρ alone. Allowing S-dependent quantum terms evades the uniqueness proof — but such terms either duplicate the kinetic term, break time-reversal/Galilean structure, or introduce higher-derivative oscillatory dynamics; the classification under those relaxations is a real follow-up problem, not settled here. Closest existing results: Hall–Reginatto's uniqueness *within* the exact-uncertainty ansatz; superposition-principle classifications for nonlinear Schrödinger families. I could not locate Theorem 1 as an explicit standalone statement; it appears to be a straightforward but unpublished assembly.

**Classification:** Theorem 1 — provable now (category 3). Its hypotheses (Hamiltonian emergent dynamics; amplitude transform with a phase constant) are exactly the structural demands identified in Round 2; its conclusion converts the Fisher problem into the **amplitude-linearity + phase-unit problem**.

### Theorem 2 (The diffusive and zero-noise deterministic corners both exclude Madelung)

Two complementary rigidity statements, which together essentially complete T− for the Markov class.

**(2a) Fisher is destroyed in the diffusive corner.** For the emergent Fokker–Planck dynamics with diffusion ν > 0, the Fisher functional — which Madelung dynamics needs as a *conserved* energy — is a *strict Lyapunov function* of the coarse flow. In 1D, for ∂_tρ = νρ_{xx}, with φ = √ρ:
$$\frac{d}{dt}I_F[\rho_t]=-2\nu\!\int\!\rho\,[(\ln\rho)_{xx}]^2dx\;=\;-8\nu\!\int\!\varphi_{xx}^2\,dx-\frac{8\nu}{3}\!\int\!\frac{\varphi_x^4}{\varphi^2}\,dx\;\le\;0 ,$$
with equality only for Gaussian-profile families in the comoving sense; the same strict-decrease conclusion holds for the full Fokker–Planck flow (the drift part is transport and cannot compensate the diffusive decrease at the Madelung-relevant scales). [VERIFIED computation; monotonicity of Fisher under heat flow is standard.] **Interpretation:** any deterministic-limit mechanism that lands in the diffusive corner *actively annihilates* the conserved quantity the program requires. This upgrades Lemma C from "wrong structure" to a quantitative incompatibility.

**(2b) Drift rigidity in the zero-noise corner.** Suppose the coarse limit is pure transport ∂_tρ = −∇·(ρ b̄) with b̄(x) time-independent invariant-data drift (the zero-noise corner of the same theorems, and the structure of any fixed-scale deterministic homogenization). Madelung self-consistency requires b̄ = ∇S/m with S solving ∂_tS + |∇S|²/2m + V + Q[ρ_t] = 0. Differentiating in time and using time-independence of b̄ forces
$$\nabla Q[\rho_t]=-\,m\,\nabla\!\Big(\tfrac{|\bar b|^2}{2m}\Big)\quad\text{for all }t,$$
i.e. Q[ρ_t](x) = −|b̄(x)|²/2m + c(t) for all t. But ρ_t = ρ₀ ∘ Φ_{−t}^{b̄} generally has Δ√ρ_t/√ρ_t varying nontrivially along the flow; forcing it to be a *fixed* spatial profile up to a spatial constant, for an **open family** of initial ρ₀, is generically impossible (already for constant b̄ it confines Q[ρ₀] to the thin class with affine Δ√ρ/√ρ). **Proposition (sketch; to be written rigorously):** *time-independent invariant-data drifts admit Madelung self-consistency only on non-open, nongeneric families of initial data.* [Category 3; proof-sketch level here.]

**Corollary — three trivially runnable exclusion tests.** For any candidate deterministic limit:
- **T1 (curl test):** a Nelson drift must be curl-free (∇×b = 0, since both ∇S and ∇ln ρ are gradients). Any emergent b̄ with nonzero curl is excluded outright. Generic Green–Kubo drifts ∫F(x,y)dμ(y) fail this immediately.
- **T2 (ρ-sensitivity test):** a Madelung drift must depend on ρ_t. Kelly–Melbourne drifts b̄(x) = ∫F dμ are ρ-independent *by construction* → excluded by (2b).
- **T3 (conservation test):** if emergent ν ≠ 0, the conserved-Fisher requirement fails by (2a). If ν = 0, (2b) applies.

Together: **T− is now essentially writable.** Formal statement:

> **T− (Markov-class rigidity).** For every deterministic system whose coarse limit exists within the fast–slow/homogenization framework with coefficients from invariant data (the Melbourne–Stuart/Kelly–Melbourne class and its zero-noise corner), the emergent marginal dynamics is Madelung-consistent with universal coefficient for an open family of initial data **only if** the microscopic law already contains density-coupled (mean-field) structure and an action-scale constant — i.e., only if the answer is inserted. No unassisted mechanism in this class produces the Fisher-Hamiltonian term.

What T− does **not** cover — and this must be stated with equal precision — is the non-Markovian, globally geometric closure slot. That remains the entire positive possibility space.

---

## 3. THE PRECISE FORM OF THE MISSING STRUCTURE

Combining Theorem 1 with the T− program, the residual Category-4 content compresses into a single object:

> **The amplitude-layer requirement.** BM-IST must contain a **phase-coherent amplitude structure**: (i) a field-like observable over the invariant set whose squared norm reproduces conditional configuration measures (so that √ρ is *realized*, not defined); (ii) a phase variable whose circulations are quantized in a universal action unit κ (so that κ = ħ is topological, hence universal); (iii) enough linearity that the emergent complex field obeys a superposition principle.

With (i)–(iii) posited, everything else is existing mathematics: Theorem 1 forces E_q = (κ²/8m)I_F; Wallstrom's condition is (ii); equivariance is DGZ. This is the precise content of verdict C — and it explains, retroactively, why every known selection principle (Chentsov, exact uncertainty, minimum-Fisher, Cramér–Rao, Caticha's entropic metric) is a *stand-in*: each smuggles in either a stochastic-statistical structure or a fixed action constant. They are all shadows of the amplitude layer.

**The one existing deterministic seed — and its three mismatches.** Deterministic dynamics already contains a linear, unitary structure: the **Koopman operator** U_t f = f ∘ Φ_t on L²(I, μ) (Koopman 1931; von Neumann 1932; the "Koopman–von Neumann" wave-mechanical representation of classical mechanics, Mauro 2002). This is the only existing mathematics in which a deterministic system *is* a linear unitary dynamics. It fails to deliver Schrödinger for three theorem-shaped reasons:

1. **Wrong measure:** U_t is unitary w.r.t. the *invariant* measure μ on I, not w.r.t. evolving configuration densities ρ_t dx.
2. **Wrong order:** the generator is the first-order Liouvillian iL, not a second-order operator −(ħ²/2m)Δ + V; there is no Fisher term anywhere in the KVN representation.
3. **Wrong locality/spectrum:** mixing systems have countable Lebesgue spectrum and no nonconstant eigenfunctions (standard ergodic theory; cf. Cornfeld–Fomin–Sinai 1982), so no nontrivial finite-dimensional invariant subspace of "nice" observables exists; the spectral coordinates of von Neumann's representation are violently nonlocal functions on phase space, whereas Schrödinger demands a *local* second-order operator on Q.

Each mismatch is a concrete, attackable gap. None is presently closed. Published IST contains nothing that addresses them: its structures are measures on Cantor/dyadic sets, not amplitude fields with phase units. [This is the strict finding required by your §4 discipline: amplitude coherence is an **additional hypothesis**, not present IST.]

---

## 4. THE TOY-MODEL PROGRAM, MADE OPERATIONAL

Five falsification tests (T1–T3 above, plus):
- **T4 (mass-variance test):** run the same microscopic universe with two slow masses m₁ ≠ m₂; the emergent coefficient must scale as 1/m. In all known mechanisms the coefficient is a Green–Kubo constant independent of m; making it mass-dependent requires putting m into the micro coupling — insertion. Gemini's (Δx)²/Δt → ħ/m scale relation fails this test by assumption, as you concluded.
- **T5 (field-identification test):** if the emergent energy is local, rewrite it as λ∫|∇F(ρ)|² (always possible, per the vacuity lemma) and ask whether F is *independently realized* microscopically. Only a yes is evidence of emergence.

Ranked toy models:

- **TM1 — negative benchmark (runnable now).** Fast–slow hyperbolic family with explicit cat-map fast factor. Compute b̄, ν by the Green–Kubo formulas; run T1–T4. Expected: curl ≠ 0 or ρ-insensitivity or ν model-constant. Deliverable: T− written as a paper with explicit instances. This settles nothing positively but converts Round 2's "no known mechanism" into "no mechanism in this class, theorem."
- **TM2 — closure benchmark.** Self-consistent (Vlasov-like) deterministic coupling. Tests closure and reversibility only. **Cannot test selection** — the ρ-dependence is in the coupling by construction. Explicitly out of scope for Gates 3–4.
- **TM3 — the spectral dilemma (the honest home of the selection question).** Compare two solvable deterministic systems: (a) quasiperiodic flow on T² — Koopman spectrum is pure point, finite-dimensional invariant subspaces exist, closure is trivial — but the emergent dynamics is a torus rotation, carrying no quantum content; (b) mixing map — rich dynamics, but Lebesgue spectrum forbids nice finite-dimensional closure. This suggests a **spectral dilemma**: *either the spectrum is too poor (closure without quantum structure) or too rich (quantum-shaped spectrum without closure).* BM-IST's amplitude layer must live in an intermediate regime — mixed spectrum with locally supported eigenpackets closing onto a second-order operator. This is a conjecture-level organizing principle, not a theorem, but it is *checkable* and it gives T+ its concrete shape: exhibit one deterministic system whose coarse observable algebra closes under a second-order self-adjoint generator on a *local* amplitude field. I flag it as **plausible, unproved, and — to my knowledge — unformulated** in the IST literature.
- **TM4 — the κ test.** Cannot be run until a candidate "home" for the action unit exists in IST. Candidates, in order of IST-nativeness: monodromy unit of invariant-set loops (ties to Wallstrom — your §16's IST-native opportunity); action spacing of a world-lattice (Palmer-style speculation, unproved); p-adic norm scale (Vladimirov-type forms exist, but nothing selects Euclidean Fisher or a universal constant). Until one is specified, ħ-universality is untestable even in principle — which is itself a finding.

---

## 5. LEDGER DELTA AND VERDICT

Only status changes from Round 2:

| Claim | Old status | New status | Driver |
|---|---|---|---|
| Osmotic transplant at fixed scale | Contradicted | Contradicted (precisely scoped, three tiers) | A1/A2/A3 |
| Shape u ∝ ∇ln ρ from deterministic chaos | "No known mechanism" | **Free** in any diffusion limit | A2 |
| Fisher as conserved Hamiltonian energy from deterministic limits | No known mechanism | **Contradicted** in diffusive corner (explicit Lyapunov identity); **contradicted** in zero-noise corner for open families (proposition, sketch-level) | Thm 2a, 2b |
| Fisher *shape* selection | Category 4 | **Reduced**: shape ⟸ linearity of emergent complex field (theorem available) | Thm 1 |
| ħ-universality | Category 4 | Category 4, **relocated** to the phase unit κ of the amplitude transform; unified with Wallstrom constant | Thm 1 + monodromy |
| Markov-class no-go T− | Corollary-level | **Essentially writable** (Thm 2 + tests T1–T3) | Thm 2 |
| Amplitude layer | Implicit | **Explicit single missing structure**; Koopman seed identified with three precise mismatches | §3 |

**Verdict unchanged, sharpened:** C-not-D, now with the Category-4 residue compressed to one structure — *a deterministic phase-coherent amplitude layer with universal action unit* — plus three ordinary theorems (rigorous T−; Theorem 1 written out; monodromy-from-IST). Your Qwen-vs-Gemini/Z classification dispute dissolves as anticipated: the program is **B-shaped once the amplitude layer is posited, C because nothing in published IST posits it.**

**Shortest credible path, restated once more, now with two concrete endpoints:**
- **Settle negatively (near-term):** write T− rigorously via Theorem 2 for the Markov class, with TM1 instances passing tests T1–T4. This is weeks of work, not years, and it permanently closes the homogenization escape route.
- **Settle positively (the real question):** exhibit one deterministic system with a *realized* amplitude observable and a *topologically quantized* phase unit, whose coarse observable algebra closes onto −(κ²/2m)Δ + V. The spectral dilemma of TM3 tells you exactly what regime to search: neither quasiperiodic-poor nor mixing-rich. If no such regime can be exhibited even in a two-mode toy, the amplitude layer is not "missing mathematics" but absent physics, and the program should be judged accordingly.

That pair of results — T− written down, or one honest TM3 instance — is the definitive answer this gate has been asking for since Round 1.
