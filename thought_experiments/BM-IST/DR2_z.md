# ADVERSARIAL DEEP-RESEARCH REPORT
## Gate II: Can deterministic invariant-set dynamics generate the osmotic / Fisher-information structure of Bohmian mechanics?

---

## EXECUTIVE VERDICT

After adversarial scrutiny, the bridge survives only as an aspiration, not as mathematics. Existing rigorous results establish three facts that jointly reshape — and largely gut — the program as currently formulated. **First**, the "osmotic velocity" is not a neutral bookkeeping device but the *fingerprint of noise*: for any deterministic flow (Markov or not), the forward and backward conditional drifts coincide, so the osmotic pair is identically zero; u = (ħ/2m)∇ln ρ exists *only* as the reversion asymmetry of a genuinely random semimartingale (Haussmann–Pardoux 1986). A deterministic program must therefore abandon the osmotic velocity as a dynamical object and target the Fisher functional directly as the *Hamiltonian potential of a reversible transport* — a strictly different and harder requirement. **Second**, the Fisher information is exactly the Dirichlet energy of √ρ, i.e., the target functional is literally (ħ²/2m)∫|∇ψ|²: "deriving Fisher" is not a softened version of "deriving quantum mechanics" — it *is* deriving the quantum kinetic term, and every published selection principle that picks Fisher out of the space of local density functionals (exact uncertainty, minimum Fisher, entropic metric, Chentsov sufficiency-invariance, Cramér–Rao) imports stochastic or explicitly quantum-motivated structure. **Third**, the rigorous deterministic chaotic-limit theorems that exist (Melbourne–Stuart, Kelly–Melbourne) deliver dissipative Fokker–Planck limits with Green–Kubo, model-dependent coefficients — structurally orthogonal to the Hamiltonian, universal, self-consistent structure Bohmian mechanics requires — and genuinely fractal metric-measure structure actively *destroys* smooth Fisher calculus (anomalous walk dimension; singular energy measures, Hino 2005). No existing theorem rules out a specially structured deterministic invariant set whose coarse transport is Madelung (Bohmian flow itself is the trivial witness), but published IST contains no mechanism — no invariant measure, no closure, no selection principle, no coefficient, no monodromy — that would deliver it. The verdict is **C**: new mathematical structure is required; most of the missing pieces are new theorems within existing mathematics, but the Fisher-selection principle and the universality of ħ have no known deterministic route of any kind.

---

## A. BOTTOM-LINE VERDICT

**C. REQUIRES NEW MATHEMATICAL STRUCTURE** — with a sharpened internal decomposition:

- *Category (1)–(2) items* (existing theorems, straightforward applications): equivalence theorems (Guerra–Morato), Fisher→Q (Madelung/Takabayasi), equivariance (Dürr–Goldstein–Zanghì), deterministic diffusion limits (Kelly–Melbourne), Chentsov uniqueness, Wallstrom's inequivalence, Reddiger–Poirier framework.
- *Category (3) items* (new theorems within existing mathematics): fibration + smooth-marginal theorem; autonomous closure theorem; reversibility/conjugacy of the coarse limit; circulation quantization from invariant-set topology.
- *Category (4) items* (genuinely new structure): a **deterministic selection principle** that fixes the amplitude-Dirichlet/Fisher functional among local density functionals; and a **universality mechanism** fixing the coefficient ħ/2m identically across all systems and masses.

No current result, and no route currently visible, belongs to categories (1)–(3) for these last two items.

---

## PRELIMINARY: TWO STRUCTURAL CLARIFICATIONS THAT RESHAPE THE PROBLEM

These two observations govern everything below.

**(O1) The osmotic velocity is a noise fingerprint.**
For a continuous-path process, the Nelson backward drift conditioned on the *terminal* point,
b₋(x,t) = lim_{δ↓0} E[(X_t − X_{t−δ})/δ | X_t = x],
equals the forward conditional drift whenever sample paths are differentiable — i.e., whenever the process is deterministic. u = (b₊ − b₋)/2 ≠ 0 requires a nontrivial martingale component. For a diffusion with forward drift b and diffusion matrix νI, the time-reversal identity (Haussmann & Pardoux, *Ann. Probab.* 14, 1188 (1986)) gives b₋ = b − ν∇ln ρ, whence u = (ν/2)∇ln ρ. Consequence for BM-IST: **no deterministic microscopic dynamics can produce an osmotic pair by conditional-mean algebra; the two-stream/forward–backward mechanism (Investigation §5) is dead as a derivation, and the honest deterministic target is the Fisher functional in the Hamiltonian, not the osmotic velocity.**

**(O2) The Fisher functional is the quantum kinetic term.**
I_F[ρ] = ∫ρ|∇ln ρ|² dx = 4∫|∇√ρ|² dx. Hence

  (ħ²/8m) I_F = (ħ²/2m) ∫ |∇ψ|²,  ψ = √ρ.

There is no mathematically weaker target hiding inside "Fisher emergence." A successful derivation of the Fisher term *is* a derivation of the Schrödinger kinetic energy, with all that implies (linearity, superposition, ħ). The program's decisive content is therefore concentrated in: *what deterministic fact forces the Dirichlet energy of the amplitude, universally and reversibly?*

---

## B. WHAT THE LITERATURE PROVES

### B1. Nelson / Guerra–Morato: exact assumption inventory

| Ingredient | Content | Status |
|---|---|---|
| State space | Q = ℝⁿ (or manifold); configurations | postulate |
| Process class | Markov diffusions, continuous paths, **non-differentiable** paths | postulate — *essential* (O1) |
| Diffusion coefficient | ν = ħ/m, universal, scalar, isotropic | **postulate; ħ enters here** |
| Osmotic velocity | u = (ν/2)∇ln ρ | *theorem given the diffusion* (reversion identity; Haussmann–Pardoux 1986) |
| Current velocity | v, generating ρ: ∂_tρ = −∇·(ρv) | definitional |
| Time reversal | two diffusions (forward/backward) sharing ρ_t | postulate (bridge reversion) |
| Variational principle | Guerra–Morato: criticality of Ā = E∫(m/2)v² − V dt within the diffusion class at fixed ν | theorem: criticality ⇔ Schrödinger (Guerra & Morato, *Phys. Rev.* D **27**, 1774 (1983); Guerra, *Phys. Rep.* 77 (1981)) |
| Quantum potential | Q = −(ħ²/2m)Δ√ρ/√ρ, from the u-term (m/2)u² = (ħ²/8m)I_F | **derived within the stochastic structure**; the structure itself encodes QM |
| Regularity | ρ ∈ C^{1,2}, ρ > 0; v, u ∈ C¹; finite energy | assumption |
| References | Nelson, *Phys. Rev.* 150, 1079 (1966); *Quantum Fluctuations* (Princeton 1985) | |

**Assessment:** every stochastic ingredient is load-bearing. Replacing diffusions by deterministic flows: (i) u ≡ 0 by (O1); (ii) the Guerra–Morato action degenerates to classical Hamilton's principle (no Q); (iii) ν = ħ/m has no analogue anywhere. **The quantum term is derived only relative to assumptions that already contain the quantum physics (fixed universal ν). Nelson's own position is that ν = ħ/m is the quantization postulate, not a result.**

### B2. Exact-uncertainty / information-theoretic routes

- **Reginatto (1998), *Phys. Rev.* A 58, 1775:** minimum-Fisher-information principle with canonical-momentum constraints reproduces the Schrödinger equation exactly. The *minimum-Fisher principle itself* is the quantum input.
- **Hall & Reginatto (2002), *Phys. Rev.* A 65, 052109; *J. Phys.* A 35, 3289:** ensemble Hamiltonian H = ∫ρ[|∇S|²/2m + V]dx plus a quantum term built from the "quantum momentum field" P = ∇ln ρ. Assumptions: locality in (ρ, ∇ρ), Euclidean covariance, and **exact uncertainty** (fluctuation strength ∝ |P|², saturating the Cramér–Rao-type bound with constant ħ²). Result: H_Q = (ħ²/8m)I_F. **Uniqueness is conditional on quadratic homogeneity in ∇ln ρ; relaxing it yields nonlinear Schrödinger families** (log-nonlinear: Bialynicki-Birula & Mycielski, *Ann. Phys.* 100, 62 (1976); Doebner–Goldin 1992; Weinberg's nonlinear QM, *Ann. Phys.* 194, 336 (1989); Polchinski, *PRL* 66, 397 (1991) shows linearity is separately required for no-signaling). ħ is inserted; only its *factorization* ħ²/2m is constrained a posteriori by Galilean covariance of the lifted ψ-dynamics.
- **Caticha's entropic dynamics** (AIP Conf. Proc. 2010; *Entropy* 17, 6110 (2015); 2019 lectures): Fisher is chosen as the canonical metric of the probability manifold; ħ enters as the constant fixing the scale of entropic fluctuations relative to mass. Fully epistemic/stochastic; no determinism anywhere; Fisher and ħ are both inputs.

**Uniqueness results that genuinely exist:** **Chentsov's theorem** (*Statistical Decision Rules and Optimal Inference*, AMS 1982; cf. Campbell, *Proc. AMS* (1986)): the Fisher metric is, up to scale, the unique Riemannian metric on the probability simplex invariant (as equality) under sufficient statistics. Caveats that matter here: (i) sufficiency is a *stochastic-map* notion; monotonicity under coarse-graining alone leaves a whole family of Morozova–Chentsov metrics (Petz, *Lin. Alg. Appl.* 244, 287 (1996) for the quantum analogue), so the uniqueness is only as strong as the acceptance of stochastic-sufficiency invariance; (ii) the theorem is about the *state space of probability distributions*, i.e., an epistemic geometry — it does not say any deterministic dynamics must respect it. **Conclusion: the only genuine uniqueness theorem for Fisher is stochastic-statistical in its hypothesis. No deterministic selection principle for Fisher exists in the literature.**

### B3. Deterministic systems with rigorous stochastic limits

- **Melbourne & Stuart, *Nonlinearity* 24, 1361 (2011); Kelly & Melbourne, *J. Funct. Anal.* 272 (2017):** fast–slow deterministic systems Ẋ = F(X,Y), Ẏ = (1/ε)G(Y), with Y uniformly hyperbolic/mixing and Hölder observables, converge (weakly, in C^α) to solutions of dX = b̄ dt + σ dW, with b̄(x) = ∫F(x,y)dμ(y) and σσᵀ given by a **Green–Kubo integral of fast fluctuations over the invariant measure**.
- **Deterministic diffusion:** Lorentz gas / dispersive billiards (Bunimovich–Sinai; Chernov–Markarian, *Chaotic Billiards*, AMS 2006): diffusion constants D again from Green–Kubo data of the invariant measure.
- **Functional CLTs for chaotic systems:** Gordin's martingale–coboundary decomposition (1969) and its hyperbolic extensions (Denker–Philipp): yes, deterministic chaos rigorously *generates Brownian motion* for suitable observables.
- **Averaging with measure-valued/Young-measure limits** (Tartar's compensated compactness framework; Dolgopyat's deterministic averaging): limits retain fast-variable invariant data through averaged coefficients; no noise, but also no ρ-self-consistency.
- **Homogenized Hamilton–Jacobi** (Lions–Papanicolaou–Varadhan): single-field HJ homogenizes to effective HJ — relevant only as the *classical* (Q-free) endpoint of transport-type limits.

**The decisive structural facts** (see Lemma C below): (i) these theorems produce *dissipative* Fokker–Planck limits — coarse entropy increases, coarse Fisher information decreases (de Bruijn identity: dI/dt < 0 under pure diffusion); (ii) the coefficients are **invariants of the fast dynamics**, identical across slow observables and initial conditions; (iii) no theorem in this literature produces a coarse drift that depends on the coarse density itself (ρ-self-consistency). Self-consistent, ρ-dependent drifts *do* have a rigorous deterministic theory — **Vlasov/mean-field limits** (Braun & Hepp, *CMP* 56, 101 (1977); Neunzert) — but there the ρ-dependence is inserted in the microscopic force law, which is exactly the "engineering" the gate excludes.

### B4. Fisher information from fractal / singular measures

- **Singular marginals kill Fisher.** If the configuration marginal has a singular component, smoothing gives I_F[ρ_ε] ≥ C(K)/ε² → ∞ (rigorous for atoms; standard for positive-dimensional fractal components with local lower mass bounds). A finite continuum Fisher requires an **absolutely continuous marginal with controlled gradient at a fixed physical scale ε₀** — the coarse-graining cannot be removed.
- **Genuinely fractal metric-measure structure has the wrong calculus.** On p.c.f. fractals, self-similar Dirichlet forms exist (Kigami, *Analysis on Fractals*, CUP 2001; Barlow–Bass 1989) but the walk dimension is anomalous (d_w = log5/log2 ≈ 2.32 on the Sierpiński gasket): the intrinsic energy of a ball of radius ε scales as ε^{−d_w}, not ε^{−2}. Moreover Hino (*Probab. Theory Relat. Fields*, 2005) proved the intrinsic **energy measures are singular** with respect to the natural self-similar measures on standard p.c.f. fractals. Consequence: any "Fisher-like" energy generated by genuinely fractal geometry carries scale anomalies that **break the universality of the coefficient** ħ²/8m. Fractality is not merely insufficient for Fisher — it is *counterproductive*; Fisher structure is the signature of a smooth metric-measure layer.
- **p-adic spaces:** Vladimirov-operator Dirichlet forms exist rigorously (Vladimirov–Volovich–Zelenov 1994; Albeverio et al.), so a p-adic layer could host a nonlocal energy form; but nothing in that literature selects the Euclidean Fisher functional or fixes its coefficient. Palmer's dyadic/p-adic structures (Bloch-sphere sparse sampling) are number-theoretic bookkeeping, not a metric-measure calculus.
- **Γ-convergence:** I know of **no published Γ-limit theorem** deriving exactly ∫ρ|∇ln ρ|² from discrete/fractal deterministic dynamics. What exists: homogenization of quadratic Dirichlet forms (Dal Maso, *Γ-Convergence*, Birkhäuser 1993) — note Fisher *is* such a quadratic form in the field φ = √ρ, so "a Dirichlet energy emerges" is generic; nothing forces it to be *the* energy of √ρ, in the Hamiltonian role, with universal coefficient.
- **No-go flavor:** there is no theorem in this literature *phrased* as "deterministic homogenization cannot generate osmotic structure"; the impossibility is a corollary-level synthesis (Lemmas A, C, E below).

### B5. Equivariance, Wallstrom, Reddiger–Poirier

- **Dürr–Goldstein–Zanghì, *J. Stat. Phys.* 67, 843 (1992):** if ψ solves Schrödinger and v^ψ = (ħ/m)Im(∇ψ/ψ), then ρ_t = |ψ_t|² is transported by v^ψ (equivariance). This is the *model* of what an emergence theorem must prove — with the roles reversed: DGZ take V from ψ; IST must produce V and ψ's constituents from invariant-set geometry. Bohmian mechanics itself is therefore a deterministic system with exactly the target marginals: **no absolute no-go exists**; the entire question is *identification with independent microscopic structure*.
- **Wallstrom, *Phys. Rev.* A 49, 1613 (1994):** the Madelung equations admit solutions with arbitrary circulation ∮∇S·dl that correspond to no wavefunction; exact equivalence to Schrödinger requires ∮∇S·dl ∈ 2πħℤ/m. **Reddiger–Poirier (J. Phys. A 50, 2017; with Zarrouati 2022–23)** give a rigorous geometric framework (loop spaces, monodromy of the phase) in which the quantization of circulation remains an *additional postulate*. The node structure (ρ = 0) is where multi-valuedness enters.
- **Relevance to IST:** the one place where a deterministic number-theoretic structure could plausibly contribute a *theorem* is here: if IST's phase restrictions (dyadic/prime structure of the world-lattice) force integer winding, Wallstrom is solved by topology. **This is plausible and IST-motivated, but no theorem exists.**

### B6. Hudson's theorem: precise content

**Hudson, *J. Appl. Prob.* 11, 311 (1974):** a pure quantum state has everywhere-nonnegative Wigner function iff it is Gaussian. That is the entire theorem. See also Mari & Eisert, *PRL* 109, 230503 (2012) for the operational corollary (Wigner-positive states are efficiently classically simulable in that representation).

---

## C. WHAT THE LITERATURE RULES OUT

Formal statements, each with classification per Investigation §10.

**Lemma A (Zero-osmotic lemma). [CONTRADICTED — for deterministic microdynamics]**
Let Φ_t be a C¹ deterministic flow on Ω, X_t = π(Φ_t) any coarse process with marginal density ρ_t. Then the Nelson forward and backward conditional drifts satisfy b₊ = b₋, hence u ≡ 0. *Proof:* both limits equal E[∇π·F | π(x_t) = x]; differentiability of paths makes the left and right difference quotients converge to the same conditional mean. Nonzero u exists iff a nontrivial martingale component is present (reversion identity, Haussmann–Pardoux 1986). ∎
*Consequence:* the two-stream mechanisms of Investigation §5 — time-reversal involutions, stable/unstable pairings, symbolic branch pairings, bidirectional coarse-graining — all reduce to conditional-mean decompositions and are killed. Escape only by *defining* u := (ħ/2m)∇ln ρ as a bookkeeping field and demanding the dynamics close through it — which is the closure problem, not a derivation.

**Lemma B (PSD cone obstruction). [CONTRADICTED — pointwise, at stress level]**
For classical ensembles with nonnegative density on velocity space, the Reynolds stress R_ij = ∫w_i w_j f dw ⪰ 0. The Takabayasi stress of the Madelung representation, τ_ij = (ħ²/4m)∂_i∂_j ln ρ (Takabayasi, *Prog. Theor. Phys.* 8, 143 (1952)), is generically indefinite. PSD matrices form a closed convex cone; no pointwise match. This is elementary linear algebra — Hudson is not needed. At the level of the *force density* −∇·τ the statement weakens (divergence of a PSD field family vs. a prescribed field is not a clean pointwise no-go).

**Lemma C (Dissipation and model-dependence of deterministic stochastic limits). [CONTRADICTED — generically; theorem over the hyperbolic class]**
For every deterministic fast–slow system covered by Melbourne–Stuart / Kelly–Melbourne, the limit is an Itô diffusion with coefficients given by invariant-data functionals; hence (i) the coarse dynamics is dissipative with positive entropy production and *no* conserved Hamiltonian or conjugate phase on the coarse space; (ii) I_F[ρ_t] strictly decreases (de Bruijn); (iii) the diffusion constant is model-dependent, not universal; (iv) no ρ-self-consistency of the drift. Madelung dynamics requires exactly the opposite: Hamiltonian *transport* (∂_tρ = −∇·(ρ∇S/m), zero diffusion) conserving an energy functional containing I_F. Landing on pure transport requires the zero-noise corner of the same theorems — where only potential/drift renormalization survives and no Fisher term appears. **Either way, the deterministic-limit theorems cannot deliver the target; this is a theorem over the entire class for which rigorous deterministic stochastic-limit theory exists.**

**Lemma D (Fisher divergence of singular marginals). [CONTRADICTED — ε→0 limits]**
Singular marginals (any fractal marginal of positive codimension) give I_F[ρ_ε] → ∞ (atoms: ≥ C/ε² rigorously; fractal components: standard via local lower mass bounds). Finite Fisher requires a fixed physical scale ε₀ and a smooth marginal there — new structure, absent from published IST.

**Lemma E (Universality rigidity). [NO ROUTE — not a theorem, a precise obligation]**
In all published deterministic homogenization theorems, effective coefficients are Green–Kubo integrals against the fast invariant measure. If IST's flow is in this class, the osmotic/Fisher coefficient must be such an invariant, **identical for all slow masses**: D(m) = ħ/2m for every m. No universal Green–Kubo functional is known, conjectured, or even defined in the IST literature; in known model classes such coefficients vary with parameters. Demanding this universality is falsifiable and currently unsupported.

**What the literature does NOT rule out:** existence of *some* deterministic dynamics with Madelung marginals (Bohmian flow, Lemma-free); specially structured invariant sets with non-Markovian, globally geometric closures; number-theoretic circulation quantization. There is no published absolute no-go theorem against deterministic BM-IST — the obstructions are structural and class-specific.

---

## D. WHAT THE GEMINI FLASH REVIEW GOT RIGHT

1. **The pivot is correct.** The naive route "positive velocity dispersion → quantum stress" is untenable: the PSD cone (Lemma B) cannot reproduce the indefinite Takabayasi stress pointwise. This is the right conclusion, even though (see E) it does not need Hudson.
2. **The bifurcation is correct:** whatever survives must be mean-field/informational — a functional of ρ alone — not a local fluctuation effect. This is genuinely the right diagnosis: Q is a *mean-field* object, and mean-field dependence is the one kind of nonlinearity deterministic dynamics demonstrably can carry rigorously (Vlasov limits).
3. Recognizing that the surviving question is whether *specifically* Fisher — not generic information functionals — can emerge, and demanding uniqueness results, is correct and was honored here.

---

## E. WHAT GEMINI FLASH OVERSTATED OR GOT WRONG

1. **Hudson misattribution.** Hudson's theorem is a statement about *Wigner functions of quantum states*: Wigner-nonnegative pure states are Gaussian. It is **not** a no-go theorem for deterministic hidden-variable ensembles, local quantum stress, hydrodynamic representations, or effective coarse-grained currents. Bohmian mechanics — deterministic, with measure |ψ|² — is trivially consistent with Hudson, because it never proposes a positive phase-space distribution reproducing all quantum moments. Using Hudson as "the" blocker conflates a *representation* statement with an *ontological* one. The correct blocker for the naive route is Lemma B (elementary PSD-cone algebra); Hudson adds only the distinct fact that positive-Wigner representations cover a measure-zero sliver of state space (with the Mari–Eisert simulation corollary).
2. **"The viable route must be osmotic."** Overstated in the light of Lemma A: *the osmotic velocity is precisely the ingredient a deterministic ontology cannot have* — it is the signature of noise. The viable deterministic route, if any, must drop the osmotic framing entirely and target Fisher-as-Hamiltonian-potential. Flash's proposed safe harbor is, strictly analyzed, unavailable.
3. **Scope of the PSD argument.** It is a pointwise statement about stress tensors; it does not by itself preclude matching coarse-grained force balances through nonlocal averaging. Correct conclusion, imprecise theorem.

---

## F. THE STRONGEST CONSTRUCTIVE ROUTE CURRENTLY AVAILABLE

**The program: "smooth fibration + Hamiltonian closure + amplitude-Dirichlet selection."**

The one existing-mathematics anchor that genuinely fits deterministic self-consistent drifts is **Vlasov-type mean-field theory** (Braun–Hepp 1977): deterministic dynamics *can* rigorously generate ρ-dependent transport — when the ρ-dependence is present in the microscopic force law or in the invariant structure that generates it. Palmer's invariant set is precisely a *global, nonlocal geometric object*; if its coarse transport closes at all, it will close nonlocally, Vlasov-style. This is the only structurally honest slot for "invariant-set geometry → Q." The constructive skeleton (each hypothesis classified):

- **(H1) [new theorem, category 3]** *Fibration:* the invariant set I fibers over configuration space with Lipschitz fibers; the SRB-type invariant measure disintegrates with an absolutely continuous marginal ρ_t ∈ C¹, ρ_t > 0, **at a fixed physical scale ε₀** (Lemma D). Published IST contains no such statement; "fractal geometry" per se produces singular marginals, i.e., the opposite.
- **(H2) [new theorem, category 3]** *Closure:* the pushforward density obeys an autonomous continuity equation ∂_tρ = −∇·(ρV), with V a functional of the invariant-set geometry — Vlasov-like if nonlocal. No general closure theorem exists for chaotic transport at fixed scale; this is a real research problem, not a formality.
- **(H3) [new theorem, category 3; fails generically per Lemma C]** *Reversibility/conjugacy:* V = ∇S/m with an energy functional E[ρ,S] conserved — a Hamiltonian structure on density space (rigorous framework exists: Otto calculus / Wasserstein Hamiltonian flows; von Renesse, *Canad. Math. Bull.* 55 (2012) treats Schrödinger evolution as Hamiltonian flow in Wasserstein space; Ambrosio–Gigli–Savaré 2008; the Fisher–Ricci connection via Lott–Villani 2009 and Otto–Villani 2000 shows I_F is a natural geometric object on density space). The demand is that the *emergent* dynamics land on this Hamiltonian corner rather than the dissipative corner that deterministic-limit theorems actually produce.
- **(H4) [category 4 — genuinely new structure]** *Selection:* E contains exactly 4(ħ²/8m)∫|∇√ρ|². **No deterministic selection principle is known.** All existing selectors are stochastic or quantum-motivated: exact-uncertainty quadratic homogeneity (assumption); minimum Fisher (assumption); entropic metric (choice); Chentsov sufficiency-invariance (stochastic); Cramér–Rao sampling (statistical); linearity of the emergent dynamics (quantum assumption, needed for no-signaling per Polchinski 1991). Note the reframing forced by (O2): this is selecting *the quantum kinetic term*.
- **(H5) [category 4]** *Universality:* the coefficient is ħ/2m, scalar and isotropic, identical for all systems and masses (Lemma E). Dimensional analysis fixes only the form (const)·∇ln ρ and is explicitly not a derivation.
- **(H6) [plausible, category 3, IST-specific]** *Monodromy:* invariant-set topology (number-theoretic phase restrictions) forces ∮∇S·dl ∈ 2πħℤ/m, discharging Wallstrom. Framework: Reddiger–Poirier. **This is the best IST-specific leverage point; it currently exists only as a suggestion.**

**Toy model verdict (Investigation §13).**
- *Positive control (uninformative):* transport by v^ψ on Q — deterministic, equivariant, exact Fisher structure — but engineered; excluded by the gate's own criterion.
- *Negative test (informative):* Melbourne–Stuart fast–slow system with explicit hyperbolic fast dynamics. Emergent equation is Fokker–Planck; b̄, D computed from invariant data; I_F[ρ_t] strictly decreases; no conjugate phase. Negative for the *whole hyperbolic class*, because the obstruction (Lemma C) is structural, not tuned.
- *Fibration toy (revealing):* skew product with invariant set Q × Cantor, invariant measure ρ(x)dx ⊗ μ_C. Smooth marginal and closure for free — but the transport V is whatever was chosen. Demonstrates that smooth fibration trivially buys (H1)–(H2) and that *all remaining content* sits in (H3)–(H6).
- **No toy model exists, or is currently constructible, in which the Fisher term emerges unengineered.** Given (O2), an unengineered emergence of I_F would amount to deriving the Schrödinger kinetic energy — the hardest thing in the program — so this absence is not an accident of effort.

---

## G. THE STRONGEST NO-GO ARGUMENT CURRENTLY AVAILABLE

**Synthesis no-go (corollary-level over existing theorems; not a single published theorem):**

> *Let the microscopic dynamics be deterministic, with positive invariant measure, and let its coarse configuration marginal have a density ρ_t. Then:* (i) *any osmotic velocity obtained by forward/backward conditional-mean decomposition vanishes identically* (Lemma A); (ii) *any coarse limit covered by existing deterministic homogenization theory is a Markov Fokker–Planck limit with Green–Kubo, model-dependent, time-invariant-structure coefficients — dissipative, without conjugate phase, and without ρ-self-consistency* (Lemma C); (iii) *any pointwise fluctuation-stress mechanism fails by the PSD cone* (Lemma B); (iv) *a singular (fractal) marginal admits no finite Fisher limit without a fixed physical scale and smooth disintegration* (Lemma D); (v) *no mechanism fixes a universal coefficient* (Lemma E). *Therefore, within every class of deterministic systems for which rigorous coarse-limit theorems exist, neither u = (ħ/2m)∇ln ρ nor the exact Fisher functional can arise without being inserted — via the drift law, the invariant-set structure, or the closure ansatz itself.*

**Scope limits — stated honestly:** this is not an absolute no-go. It does not cover: non-Markovian, memory-bearing closures generated by genuinely global invariant-set geometry (the Vlasov-analogue slot); invariant sets *designed* so that their global structure encodes a Madelung functional; systems outside the hyperbolic/mixing classes where no limit theorems exist. Bohmian flow itself proves logical consistency. The no-go is a theorem about *mechanisms we can currently analyze*, and it is strong precisely because those are the mechanisms IST has available in print.

---

## H. THE DECISIVE BM-IST-SPECIFIC MISSING THEOREM

**IST Closure–Identification Theorem (formulation of what must be proved):**

> *Let (I, Φ_t, μ) be the Palmer invariant set with its flow and natural measure, and π: I → Q a coarse map. Suppose (H1)–(H6) hold. Then the π-marginal transport of Φ_t converges to (ρ_t, S_t) satisfying the Madelung system*
> ∂_tρ = −∇·(ρ∇S/m),  ∂_tS + |∇S|²/2m + V − (ħ²/2m) Δ√ρ/√ρ = 0,
> *with ħ/2m universal (independent of m and of the fast dynamics) and with circulation classes restricted to 2πħℤ/m.*

Even the *existence* of one nontrivial, independently specified instance (not the Bohm flow re-imported) is open. Conversely, the decisive negative result would be:

> *Rigidity extension of Lemma C:* prove that for any deterministic system whose coarse limit is Markov with coefficients from invariant data (the entire Kelly–Melbourne class and its foreseeable extensions), the emergent energy functional is a gradient-quadratic form with Green–Kubo coefficient, hence cannot equal (ħ²/8m)I_F universally without engineering. The expected failure mode of this no-go — non-Markovian, globally geometric closures — **is exactly the slot in which BM-IST's hope lives.** That is the honest map of the battlefield.

---

## I. MINIMAL ADDITIONAL STRUCTURE REQUIRED (IF THE THEOREM CANNOT FOLLOW FROM CURRENT IST)

Each item is an explicit deterministic addition, none present in published IST:

1. **A smooth layer:** a fibration of I over Q with a fixed physical scale ε₀ and smooth marginal (fights Lemma D; makes Fisher even definable).
2. **A closure principle:** the coarse transport at scale ε₀ is autonomous (currently no theorem even for chaotic transport at fixed scale).
3. **A reversibility principle:** the emergent transport is Hamiltonian with conjugate phase, landing in the Wasserstein-Hamiltonian corner rather than the dissipative corner (contradicts the generic behavior established by Lemma C; must be forced by invariant-set structure).
4. **A Fisher-selection principle:** a purely deterministic-geometric axiom forcing the amplitude-Dirichlet energy. **No candidate exists** in any literature surveyed; every known selector is stochastic/statistical/quantum-motivated. This is the sharpest single gap.
5. **A universality mechanism:** invariant-set data whose Green–Kubo-type functional equals ħ/2m for all masses and systems (Lemma E).
6. **A monodromy restriction:** number-theoretic phase quantization enforcing Wallstrom's condition (plausible, IST-native in spirit, unproved).

Item 4 — and to a lesser degree 5 — is where "new mathematics" in the strict sense (category 4) enters, not merely unproved theorems.

---

## J. PROOF OBLIGATION LEDGER

| # | Claim | Status | Existing theorem / source | Key assumptions | BM-IST applicability | What remains |
|---|---|---|---|---|---|---|
| 1 | Fisher functional ⇒ Q | Existing theorem | Madelung 1926; Takabayasi 1952 | ρ smooth, ρ>0 | Applies trivially once ρ exists | Nothing (given ρ) |
| 2 | u = (ν/2)∇ln ρ from process structure | Existing theorem | Nelson 1966; reversion: Haussmann–Pardoux 1986 | Non-differentiable (Markov diffusion) paths; ν = ħ/m postulated | **Inapplicable**: determinism ⇒ u ≡ 0 (Lemma A) | Deterministic replacement: none exists; target must be reformulated |
| 3 | Schrödinger ⇔ stochastic critical points | Existing theorem | Guerra–Morato 1983; Guerra 1981 | Fixed ν = ħ/m; diffusion class; regularity | Inapplicable without replacing kernels | Deterministic analogue degenerates to classical HJ |
| 4 | Fisher uniquely selects Q | Conditional | Hall–Reginatto 2002 | Quadratic homogeneity ("exact uncertainty"); ħ inserted | Imports the quantum answer as an assumption | A non-quantum selection principle |
| 5 | Fisher uniquely selected among metrics | Existing theorem | Chentsov 1982; Campbell 1986 (cf. Petz 1996) | Invariance under stochastic sufficiency maps | Hypothesis is stochastic; not a determinism principle | Deterministic invariance class (uniqueness fails there) |
| 6 | Deterministic chaos → diffusion | Existing theorem | Melbourne–Stuart 2011; Kelly–Melbourne 2017; Gordin 1969; Bunimovich–Sinai/Chernov–Markarian | Hyperbolicity; Hölder data | Gives wrong structure: dissipative, model-dependent D, no phase | Escape from the class without losing rigor |
| 7 | Deterministic osmotic pair | **Contradicted** | Lemma A (elementary, standard) | Determinism of paths | Blocks all two-stream mechanisms | Reformulate target (drop "osmotic") |
| 8 | PSD dispersion → indefinite quantum stress | **Contradicted** | Lemma B (elementary; Takabayasi 1952) | Pointwise stress matching | Correct; does not need Hudson | — |
| 9 | Hudson as no-go for deterministic HV ensembles | **Misattributed** | Hudson 1974 (states Gaussianity of Wigner-positive states) | — | Not applicable to configuration-space ensembles | — |
| 10 | Finite Fisher from fractal marginal, ε→0 | **Contradicted** | Lemma D; Dirac bound rigorous; fractal rate standard | Singularity of marginal | IST marginals are singular as published | Fixed scale ε₀ + smooth disintegration (new structure) |
| 11 | Smooth positive marginal at fixed scale from invariant set | New theorem needed | (none; fibration toy trivial) | Fibration hypothesis H1 | Central; absent from published IST | Existence + scale identification |
| 12 | Autonomous coarse closure | New theorem needed | (none for chaotic transport at fixed scale) | H2 | Central | Closure theorem |
| 13 | Reversible/Hamiltonian coarse limit | New theorem needed; **fails generically** | Lemma C (corollary of 6) | H3 | Central; contradicts generic behavior | Structural mechanism for the Hamiltonian corner |
| 14 | Deterministic ρ-dependent drift | Existing (non-Bohm) theorem | Vlasov/mean-field: Braun–Hepp 1977; Neunzert | ρ-dependence in micro force law / structure | **Best existing anchor** for IST nonlocality | Prove IST geometry induces Madelung functional, not engineered one |
| 15 | Universality of ħ/2m | **No route** | Lemma E (rigidity corollary) | Green–Kubo class | Unaddressed in all of IST | Category-4 structure |
| 16 | Circulation quantization from IST topology | Plausible | Wallstrom 1994 (problem); Reddiger–Poirier 2017+ (framework; quantization postulated) | Number-theoretic phase restrictions | Best IST-native opportunity | A theorem from p-adic/dyadic structure |
| 17 | Equivariance given v^ψ | Existing theorem | Dürr–Goldstein–Zanghì 1992 | ψ given; regularity | Existence witness only; roles reversed in IST | Identification theorem (H) |

---

## K. DECISION TREE

**IF deterministic IST structure naturally yields the osmotic/Fisher term:**
No. Published IST contains no invariant measure with smooth marginal, no closure, no conjugate structure, no selection principle, no coefficient. → *not this branch.*

**ELSE IF it can arise only after adding a clearly motivated deterministic structure:**
Partially — items 1, 2, 3, 6 of Section I are "additional deterministic structure" of a conventional kind (new theorems, category 3). But items 4–5 (Fisher selection, ħ universality) are not conventional missing theorems: every known selection mechanism for Fisher is stochastic or quantum-assumption-laden (Chentsov sufficiency, exact uncertainty, min-Fisher, entropic metric, Cramér–Rao, linearity/no-signaling), and no deterministic mechanism of any kind is on the table for the coefficient. → *partially this branch; insufficient alone.*

**ELSE IF stochasticity is mathematically indispensable:**
Precisely scoped: stochasticity is provably indispensable *for the osmotic velocity as such* (Lemma A) — it is the noise fingerprint. It is *not* provably indispensable for the Fisher functional (Dirichlet energies emerge from deterministic homogenization generically), but it is currently the **only known selection mechanism** for Fisher *as the specific functional* and for a *universal* coefficient. This is a genuine, sharply localized conflict with the BM-IST ontology: not "stochasticity is needed for the structure," but "stochasticity is needed for the *selection*." → *this branch, with the scoping above.*

**ELSE (precise no-go):**
For published IST as it stands: the chain *deterministic invariant-set dynamics → osmotic structure → Fisher → quantum potential* contains, at its second link, an object (the osmotic pair) that is **identically zero for deterministic dynamics**, and at its third link a functional whose deterministic selection is **unmotivated by any existing mathematics**; the fourth link then merely re-encodes the Schrödinger kinetic energy (O2). Under the stated commitments — deterministic ontology, no stochastic insertion, no quantum assumptions — this chain **cannot currently be traversed**, and no extension of known theorems traverses it. What prevents upgrading this from C to D is equally precise: no theorem forbids a non-Markovian, globally geometric closure (the Vlasov-analogue slot), Bohmian flow witnesses logical consistency, and IST's number-theoretic structure is a plausible (unproved) source of Wallstrom's quantization.

---

## FINAL: THE SHORTEST CREDIBLE PATH TO A DEFINITIVE ANSWER

One theorem in either direction settles the gate:

**T+ (constructive):** Exhibit one deterministic flow on a closed invariant set — whose structure is specified *independently of any ψ* — with an invariant measure whose configuration marginal has smooth density ρ_t at a fixed scale, such that the induced transport closes as ∂_tρ = −∇·(ρ∇S/m) with S satisfying the HJ equation containing −(ħ²/2m)Δ√ρ/√ρ, the coefficient identical for two different masses m. Even a two-mass toy model with a fibred invariant set and a *derived* (not inserted) drift would force the field to take the program seriously; anything less is engineering.

**T− (rigidity no-go):** Prove that for every deterministic system in the Kelly–Melbourne class (and its nonlocal Vlasov-type extensions), the emergent coarse energy functional is a gradient-quadratic form whose coefficient is a Green–Kubo invariant of the fast dynamics — hence cannot equal (ħ²/8m)I_F universally without the drift law being engineered. T− is *nearly provable today* for the Markov class (it is the formalization of Lemmas C + E); its honest limit of validity — memory-bearing, globally geometric closures — is exactly where BM-IST's residual hope must either produce T+ or die.

Given the current state of the literature, the expected outcome of attempting T− is success for the Markov class and a precise identification of the non-Markovian gap; the expected outcome of attempting T+ is failure at the Fisher-selection and coefficient steps, confirming verdict **C**. The gate closes only when one of T+, T− is written down.
