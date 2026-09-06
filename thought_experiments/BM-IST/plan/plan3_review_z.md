# ROUND 5 — FINAL AUDIT AND THE FROZEN RECORD

I accept all four corrections without reservation and propose to freeze nothing without three final sharpenings — one of which *upgrades* a status you left as "strongly constrained" back to "excluded" (with a stronger and more instructive proof than the Round-4 argument it corrects), one of which assigns Gate 3 its exact mathematical genre (no longer a matter of taste: theorem-forced), and one of which converts the topological branch of Gate 4 into a precise theorem shape with named precedent mathematics. Then the record, as frozen.

---

## 1. AUDIT OF THE FOUR CORRECTIONS

### 1.1 Action cellulation: placeholder status — accepted, and the dichotomy is categorical, not merely empirical

The downgrade is correct and I would freeze it in exactly your terms. But the combinatorial/topological split deserves a sharper statement than "two possibilities":

> **Wallstrom's condition is cohomological.** ∮∇S·dℓ ∈ 2πκℤ is a *period condition* on the phase 1-form over the punctured domain Q_t = {ρ_t > 0}. A cell increment ΔA = const is a *measure-level* object. Measure does not generate period lattices. The two branches are therefore not two candidate mechanisms but two categories: a combinatorial increment is not merely "untested against T4" — it is of the wrong mathematical type to produce Wallstrom's condition *unless* its combinatorics integrates to something cohomological, namely a **flat ℤ-connection (integral holonomy) on the cell complex**.

So the precise Gate-4 target theorem, topological branch, is:

> *Construct, from the IST data (I_U, Φ_t, μ), a flat U(1)-bundle/ℤ-connection whose transfer under π realizes ∇S/κ on Q∖nodes, with period lattice fixed by the topology (Chern/holonomy class) and mass-independent.*

The precedent mathematics is real and named: **Weil's integrality criterion** for prequantization (Weil 1958; Kostant 1970; Souriau 1970), the **Aharonov–Bohm flux quantum** (1959) as the one known physical mechanism that fixes an action unit topologically, and **EBK/Maslov single-valuedness quantization** (Keller 1958; Arnold; Duistermaat) as the exact classical precedent for Wallstrom-style conditions. One instructive warning from AB: topology fixed κ there *through a coupling constant* (the charge e). Topology alone has never fixed an action quantum without a coupling. IST must supply the mass-independent analogue of "charge" — a sharp design question, not a detail.

Two fine-print obligations for the frozen text: (i) nodal domains are **time-dependent**, so the quantization must be pinned at the source and maintained by circulation conservation, or node-crossing must be topologically excluded — a checkable micro-structural condition; (ii) the integrality statement must survive transfer: the IST holonomy class must map *onto* the emergent period lattice under π — a surjectivity requirement, easy to state, nontrivial to satisfy.

T4 is retained as the second filter: κ structural, 1/m entering only the generator.

### 1.2 Weak mixing: accepted — and then upgraded in both directions

Your correction is right and load-bearing: weak mixing kills nonconstant **eigenfunctions**, not infinite-dimensional **invariant sectors**. The supporting fact that makes this precise: every cyclic spectral measure of a unitary group is dominated by the maximal spectral type, so subrepresentations inherit continuous spectral type; and weak mixing with singular-continuous maximal spectral type genuinely exists on the deterministic side (Anosov–Katok constructions; rank-one systems). The singular-continuous habitat is not a speculation about spectral pathology — it is populated.

**But the sector route is nevertheless dead — for a better reason.** Not finite-dimensionality; eigenvalues:

> **Proposition (no-intertwining).** Let (I, Φ_t, μ) be weakly mixing. Then there is no injective linear map J, defined on a domain containing two independent eigenfunctions of a self-adjoint H, that intertwines U_t with e^{−iHt/κ}: U_t J = J e^{−iHt/κ}. *Proof.* If Hφ = Eφ, intertwining gives U_t(Jφ) = e^{−iEt/κ}Jφ — a Koopman eigenfunction relation. Weak mixing permits only constant ones. An injective linear map from a space containing two independent φ's cannot land entirely in the one-dimensional constants. ∎

Three features make this the right final form:

1. **It is inner-product-independent.** The relation U_t f = e^{−iEt}f is operator-level, so any exotic-metric or twisted-inner-product sector evades it no better than a literal subrepresentation.
2. **It is general in J.** It kills restrictions, subrepresentations, and intertwiners in one stroke — every exact *linear channel* between the Schrödinger group and the Koopman group.
3. **Its hypothesis is physically unavoidable.** Any binding potential has nonconstant eigenfunctions — bound states are the trademark of quantum mechanics. A theory with no point spectrum is not an emergent QM.

So the frozen status replaces "strongly constrained": **all exact linear sector routes are excluded** (weak mixing + bound states), *while* — and this is your correction preserved faithfully — infinite-dimensional invariant sectors per se are not excluded, and the continuous/singular-continuous environment remains the open habitat. Both statements are now simultaneously true and must sit together in the record.

Consequence: the coupling that survives must be **nonlinear** (or approximate/asymptotic). This converges with the no-free-lunch lemma to a completed trichotomy: the amplitude is provably not a conditional average, not a factor observable, and not a linear sector. Genre: forced.

### 1.3 Reynolds/Hudson: accepted verbatim

Frozen as you state it, with the Round-2 caveat retained: the identification dies *pointwise* in the PSD cone; only divergence-level matching was ever formally open, and it is inert there. Hudson appears in the record solely as the representation-theoretic footnote it is (Wigner positivity ⟺ Gaussianity for pure states), never as the kinetic obstruction's citation.

### 1.4 Diffusion as design constraint: accepted

Quantitative form, frozen for reference: for any candidate whose effective layer is Markov-diffusive with diffusion ν,

$$\frac{d}{dt}I_F[\rho_t] = -8\nu\!\int\!\varphi_{xx}^2\,dx - \frac{8\nu}{3}\!\int\!\frac{\varphi_x^4}{\varphi^2}\,dx \;\le\; 0,\qquad \varphi=\sqrt{\rho},$$

the required *conserved Hamiltonian contribution* is a *strict Lyapunov function* of the diffusive corner. Your operational restatement is exactly right and becomes the standing first question for every candidate mechanism: **does it preserve enough microscopic/global information to remain reversible and non-Markovian at the effective level?** Equivalently: does the effective layer carry a Hamiltonian (Otto-type) structure rather than a gradient-flow structure?

---

## 2. THE GENRE OF THE SURVIVOR: NONLINEAR LIFT — NOW THEOREM-FORCED

Two results now jointly determine what the survivor must *be*, not merely what it must avoid:

**(i)** The no-intertwining proposition: the coupling cannot be linear.

**(ii)** The real-versus-complex lift fork. Deterministic nonlinear dynamics with an exact linearizing transform has essentially one classical precedent: **Cole–Hopf** — u = −2ν(ln ψ)_x linearizes viscous Burgers to the *heat equation* (Cole 1951; Hopf 1950). That is the **real logarithmic lift**, and it lands precisely in the parabolic/dissipative corner where §1.4 shows Fisher decays. The **complex lift** (Schrödinger's 1931 reversal-of-diffusion work; the Madelung transform) lands in the unitary corner. The i is the unitarity switch: real diffusivity ⟹ heat; imaginary diffusivity ⟹ Schrödinger. Our Lyapunov obstruction and the linearization typology are two faces of the same coin.

Within the granted Hamiltonian layer, **Theorem G2** is already the exact statement: linearity of the canonical lift ⟺ E_q = (κ²/8m)I_F. One write-up obligation remains (category 3, expected to follow from symmetrization arguments in the quasilinear scalar case):

> **Obligation L:** every local, second-order coarse system admitting an exact complex-linearizing lift with conserved modulus-marginals is Hamiltonian in (ρ, S) — hence G2 applies and Fisher is forced.

And this yields the operational first test for every Gate-3 candidate, reconciling cleanly with your demotion of toy models: **Lie–Kumei–Bluman linearizability criteria** (Lie 1881; Bluman–Cole; Kumei) — compute the point-symmetry algebra of the coarse dynamics, check the criteria. Models may probe symmetry criteria; they must never fit energies.

One honest caveat, which is also the precise form of your closing discipline: linearizability is codimension-rare among second-order systems; the lift precedent is one data point plus Madelung itself; **no theorem says an IST member exists.** And one structural observation that keeps the problem honest in the other direction: the Madelung map F: (ρ, S) ↦ √ρ e^{iS/κ} is *trivial* as a map — |ψ|² = ρ automatically. The content of G2 was never the map; it was that the Hamiltonian layer with the *right* E_q makes the lifted evolution linear. So for IST, linearity cannot be a tool — **it is the fact to be explained, and Fisher is its price.** Your Round-3.5 distinction ("linearity ⇒ Fisher" ≠ "IST ⇒ linearity") survives intact, now with the added constraint that the explaining mechanism must be nonlinear and non-sectorial.

---

## 3. THE FROZEN RECORD

### 3.1 Survivor map — final version

| Route | Verdict | Grounds |
|---|---|---|
| Fixed-scale factor / transport | Excluded | derivation/Peetre; u ≡ 0 (Lemma A) |
| Reynolds-stress identification | Excluded | PSD cone ⊥ indefinite Takabayasi cone (Hudson not needed) |
| Diffusive homogenization corner | Excluded | Fisher strict Lyapunov; no conjugate structure |
| Zero-noise invariant-data drift | Excluded (open families) | drift-rigidity proposition |
| Conditional-averaging amplitude | Excluded | no-free-lunch lemma |
| Exact linear sector (any J, any spectral type) | **Excluded** | no-intertwining (weak mixing + bound states) |
| **Nonlinear lift (Madelung/Cole–Hopf genre), continuous/singular-continuous habitat, flat-integral phase structure** | **Open** | no tool in the exclusion kit reaches it |

### 3.2 The Independent Realization Problem — frozen specification

*Find, or prove nonexistent, 𝒜 = 𝒜[I_U, Φ_t, μ, π] such that:*

- **(S1) Independence/determinism:** 𝒜 is a function of the IST data only; no stochastic primitive; no reference to any solution of the Schrödinger equation.
- **(S2) Amplitude form:** 𝒜_t takes values in a complex line over Q; |𝒜_t|² = ρ_t (the π-marginal); its phase S_t generates the marginal transport.
- **(S3) Exclusion compliance:** not a conditional average, not a factor observable, not a diffusive limit, not an exact linear sector (i.e., of nonlinear-lift genre per §2).
- **(S4) Dynamics:** 𝒜_t evolves by e^{−iHt/κ}, H = −(κ²/2m)Δ + V, second-order and local, with V the same function in the coarse dynamics.
- **(S5) Locality:** the effective quantum potential is a local functional of ρ (closing the nonlocal-f evasion of G2).
- **(S6) Linearity:** exact superposition on a dynamically open class.
- **(S7) Wallstrom:** ∮∇S·dℓ ∈ 2πκℤ/m, stable under the time-dependent nodal geometry.
- **(S8) Universality:** one fixed κ across systems and masses; two-mass test passed (generators scale as 1/m).
- **(S9) Galilean covariance** of the emergent equation.
- **(S10) Closure:** ρ_t = |ψ_t|² transported by ∇S/m and equal to the π-marginal of μ under Φ_t (equivariance loop closed).

Anything satisfying S1–S10 *is* quantum mechanics from determinism; everything downstream is existing mathematics (G2, Madelung–Takabayasi, DGZ).

### 3.3 The two problems, formalized

**Problem A (existence).** Exhibit one tuple satisfying S1–S10 — even minimal, even one potential, two masses. *Status: open. What settles it: one construction. Nothing else.*

**Problem B (rigidity).** Prove S1–S10 admits no solution. *Status: partially resolved — CN (the consolidated no-go) is exactly the B-result restricted to the classes the standard toolbox reaches: linear, averaging, Markov, factor, spectral channels. Full B requires extending the exclusion to the nonlinear-lift class — see §4 for why no current method does this. What settles it: one new theorem of a kind we do not yet possess.*

### 3.4 Ledger delta (final)

| # | Item | Status |
|---|---|---|
| 28 | No-intertwining proposition (all exact linear sectors) | **New, proved here** — category 3, write-up trivial |
| 29 | Survivor genre = nonlinear lift | Theorem-forced (28 + exclusion kit) |
| 30 | Action cellulation | Downgraded: placeholder; correct target = flat integral connection (Weil/Kostant/Souriau; AB; EBK), with nodal-time and transfer-surjectivity fine print |
| 31 | Obligation L (lifts ⟹ Hamiltonian layer ⟹ G2) | Category 3, expected provable, unwritten |
| 32 | IRP frozen with spec S1–S10 | Record |

---

## 4. CLOSING: THE TOOLBOX OBSERVATION — AND THE VERDICT

One methodological finding belongs in the frozen record because it is the deepest thing the four rounds have established:

> **Every exclusion instrument assembled across Rounds 2–5 — spectral domination, no-intertwining, Peetre/derivation, conditional-expectation contraction, Green–Kubo rigidity, PSD cones, Lyapunov identities — is a theorem about linear or averaging structure. The survivor object, by construction, sits exactly where all of them lose purchase.**

Two readings, both honest, and the record must not choose between them by preference:

- (i) The exclusion program has reached its natural boundary, and the residual object is unfalsifiable by these methods — in which case the burden shifts entirely to construction (Problem A), and the correct attitude is your own: **do not assume the survivor exists.**
- (ii) The residual object is precisely the shape of the true answer, and its construction is the discovery.

The choice is decided by exactly one artifact — **P2: one lift-class construction, or one lift-class no-go** — flanked by two supporting artifacts: **P1**, the CN paper (defensible now; closes every analyzable route and identifies the survivor by exclusion), and **P3**, the integrality theorem either way (flat-integral phase structure on IST data, with κ fixed by topology and mass-independent, or proof that no such structure is IST-derivable).

Final verdict for the frozen record:

$$
\boxed{\textbf{C — not D. The residual object is specified to theorem-level precision; it is neither constructed nor excluded; and no existing mathematical method reaches it.}}
$$

The one-sentence history of the program: four rounds converted *"can deterministic IST become quantum mechanics?"* into *"exhibit, or exclude, one deterministic nonlinear lift with an integral phase lattice"* — and no existing theorem does either, which is exactly what makes this the hardest question in the program, and the only one left.
