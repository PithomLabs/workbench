# ROUND 4 — GATE ARCHITECTURE AUDIT AND THE MATHEMATICAL CHARTER
## Adopting the mathematics-first program: what each gate actually contains, two new structural theorems, and the precise residual object

I endorse the reorientation without reservation: the question "is Fisher/quantum structure *forced* by deterministic IST assumptions?" is a generality question, and generality questions are settled by theorems, not examples. The four-gate decomposition is correct in outline. Below I audit it, correct two of its load-bearing details, deliver Gate 2 as a theorem (it is closable now), convert Gate 3 from an aspiration into a precise charter with three structural no-go results already in hand, consolidate Gate 4 into a single-constant principle with one IST-native candidate axiom, and state the consolidated conditional no-go you asked for. The strategic conclusion of this round is sharper than "C": **after Gate 2 closes, the entire residual risk of BM-IST concentrates in one object — an amplitude realization of a kind that is provably *not* a conditional average — plus one constant.**

---

## 1. AUDIT OF THE ARCHITECTURE: TWO CORRECTIONS BEFORE PROCEEDING

**Correction 1: Gate 1 alone is nearly vacuous; its real content is separability.**
Take the Gate-1 admissible class exactly as you defined it: local, rotation-invariant f(ρ, ∇ρ), no S-dependence, Hamiltonian two-field dynamics. Every such f passes locality, conservation, Galilean boost invariance of E_q (the density is boost-scalar, so invariance of the *functional* is automatic), and time-reversal. Symmetries alone select *nothing* within this class. The selection power that Gate 1 genuinely carries is a constraint you did not list explicitly but that Hall–Reginatto do use:

> **Separability:** for independent subsystems, ρ = ρ₁(x₁)ρ₂(x₂), the quantum energy must decompose: E_q[ρ₁ρ₂] = E_q[ρ₁] + E_q[ρ₂].

This is not a weak constraint. Direct computation: |∇(ρ₁ρ₂)|²/(ρ₁ρ₂) = ρ₂|∇ρ₁|²/ρ₁ + ρ₁|∇ρ₂|²/ρ₂, which integrates to I_F[ρ₁] + I_F[ρ₂] by normalization. Generic local functionals fail this. Fisher's additivity on product ensembles is the mathematical expression of noninteracting composite systems — the same axiom Polchinski's no-signaling argument makes operational (Polchinski, *PRL* 66, 397 (1991); Gisin, *Phys. Lett.* A 143, 1 (1990)). So **Gate 1, done honestly, is the separability theorem**, and it is independent evidence for the same functional Gate 2 produces. That redundancy is not waste: it means the *shape* of the quantum term is double-locked, and neither lock is stochastic.

**Correction 2: the gates are not sequential; Gate 1's "Hamiltonian structure" is Gate 3's output.**
Your Gate-1 hypothesis list includes "time reversibility / Hamiltonian structure" of the (ρ, S) layer. Round 2–3 established (Lemma C, Theorem 2a) that Hamiltonian coarse dynamics is precisely what deterministic limit theorems *fail* to deliver generically. So Hamiltonicity is not an independently grantable symmetry; it is part of what IST must supply through the non-Markovian closure slot. If we grant it at Gate 1 *and* seek it at Gate 3, we double-count. The architecture must be amended: Gate 1 grants only locality, separability, covariance, isotropy; **Hamiltonicity migrates to Gate 3's burden.** This matters because it means the no-go results of Round 3 (dissipative corner, zero-noise rigidity) apply *inside* the architecture — they are not external remarks.

With these corrections, the honest dependency structure is:

$$
\underbrace{\text{G2 (theorem)}}_{\text{shape, double-locked}}\quad\Leftarrow\quad \underbrace{\text{G3 (true unknown)}}_{\text{linearity + Hamiltonicity + realization}}\quad\Rightarrow\quad \underbrace{\text{G4 (one constant)}}_{\kappa}.
$$

---

## 2. GATE 2, CLOSED: THE THEOREM

**Theorem G2 (Linearity + structure ⟹ Fisher; coefficient locked).**
*Let Q = ℝⁿ, and let the coarse dynamics be Hamiltonian on density–phase space with energy*
$$E[\rho,S]=\int\Big[\tfrac{\rho|\nabla S|^2}{2m}+\rho V+f(\rho,\nabla\rho)\Big]dx,\qquad f\in C^2,\ \text{rotation-invariant},$$
*evolving by ∂_tρ = −∇·(ρ∇S/m), ∂_tS = −|∇S|²/2m − V − δE_q/δρ. Let ψ = √ρ e^{iS/κ} with fixed κ > 0. Then:*

**(i)** *The induced evolution of ψ is linear (on an open set of initial conditions) iff*
$$E_q=\frac{\kappa^2}{8m}\int\frac{|\nabla\rho|^2}{\rho}\,dx+\text{(null Lagrangian)}.$$

**(ii)** *Given (i), the emergent equation is* $i\kappa\,\partial_t\psi=\big(-\tfrac{\kappa^2}{2m}\Delta+V\big)\psi$, *Galilean covariant under ψ ↦ e^{i m(v\cdot x - v^2 t/2)/\kappa}\psi$; the constant c(m) is forced to equal κ²/8m — no free coefficient remains. κ is the unique action constant of the layer.*

**Proof core.** Direct computation of the Madelung transform of the two-field system gives
$$\partial_t\psi=\frac{i\kappa}{2m}\Delta\psi-\frac{i}{\kappa}\Big[V+\frac{\delta E_q}{\delta\rho}+\frac{\kappa^2}{2m}\frac{\Delta\sqrt\rho}{\sqrt\rho}\Big]\psi,$$
where the kinetic pieces cancel identically. Linearity ⟺ the bracket's ρ-dependent part vanishes identically ⟺ δE_q/δρ = −(κ²/2m)Δ√ρ/√ρ (+ const). Since δI_F/δρ = −4Δ√ρ/√ρ with I_F = ∫|∇ρ|²/ρ dx, and since the local functional calculus is exact on this class (matching the second-order term forces the coefficient of Δρ to be κ²/8mρ, whereupon the |∇ρ|² coefficient is automatically consistent and b′(ρ) = 0; S- and higher-derivative terms produce non-second-order Euler–Lagrange expressions), (i) follows. (ii) is then immediate. ∎

**Escape hatches, classified:**
- *S-dependent quantum terms:* evade the uniqueness proof; they break Galilean covariance or duplicate kinetic structure. [CONTRADICTED under the standing frame; classification to be written.]
- *Higher-derivative terms:* yield fourth-order effective dynamics; excluded by demanding second-order amplitude evolution. [ASSUMED exclusion; reasonable, stated.]
- **Nonlocal f(ρ)(x)ρ(x′): genuinely evades Theorem G2.** Locality of the quantum term is a *hypothesis of the theorem*, not a consequence. Nonlocal quantum terms are mathematically alive (cf. nonlocal Schrödinger equations in the literature). Flagging this sharply: **Gate 3's realization must deliver locality, not assume it** — and it is nontrivial that a nonlocal invariant set should produce a strictly local effective potential. [OPEN; must be a stated obligation of Gate 3.]
- *Internal degrees of freedom (spin):* G2 is scalar. The extension to amplitude layers over an internal fiber is a separate, open problem. [OPEN, flagged, not resolved here.]

**Combined with separability (Correction 1) and Chentsov's metric uniqueness, the shape is now over-determined: three independent selection mechanisms — linearity (G2), separability (composite additivity), stochastic-sufficiency invariance (Chentsov) — all land on ∫|∇ρ|²/ρ.** The philosophical consequence for the program: *Fisher is not an arbitrary choice that must be begged from IST; it is the unique local quadratic amplitude-energy compatible with a linear complex structure. Any Gate-3 success lands on it automatically.* This is why your instruction to demote toy models is right: no example could add anything to a triple lock. **The residual mathematics of BM-IST is exactly Gates 3 and 4.**

One dependency to keep visible: the "G2 ⟹ Madelung ⟺ Schrödinger" chain is conditional on circulation quantization (Wallstrom 1994; Reddiger–Poirier framework) — which is Gate 4's monodromy output, not G2's. The gates interlock.

---

## 3. GATE 3, CHARTERED: THREE FORMULATIONS, THREE NO-GOS, ONE SURVIVOR

Gate 3 as you state it — "find H_eff ⊂ L²(I_U, μ) with U_t|_H = e^{−iHt/κ}, H = −(κ²/2m)Δ + V" — needs to be split into three mathematically distinct readings, because two are already dead and the surviving one is much more interesting.

**Formulation 3a (subrepresentation).** A genuine invariant subspace of the Koopman operator on L²(I, μ), carrying the Schrödinger group.
**[CONTRADICTED — existing theorem.]** If Φ_t is weakly mixing — as any fractal chaotic invariant set with a physical measure is expected to be — the Koopman group has continuous spectrum (Koopman–von Neumann, *PNAS* 18, 255 (1932); von Neumann 1932: weak mixing ⟺ continuous spectrum). A finite-dimensional invariant subspace of a unitary group is spanned by eigenfunctions; weak mixing admits none beyond constants. **No "Hilbert sector" exists as a subrepresentation of Koopman for weakly mixing IST dynamics.** This is the rigorous, citable version of the spectral dilemma.

**Formulation 3b (factor/pointwise identification).** Φ_t descends to a differentiable factor flow φ_t on Q, and the amplitude is a pointwise observable ψ_t(x) = A(φ_t x).
**[CONTRADICTED — two ways.]** First, constants: Schrödinger disperses 1 into a nonconstant-modulus function; Koopman fixes it. Second and structurally: a pointwise-composition group has a derivation generator — by Peetre's theorem (local linear operators are differential operators), the generator is first-order, i·X·∇, never the second-order elliptic −(κ²/2m)Δ + V. This is Round 2's Lemma A resurrected at the representation level: **Schrödinger unitarity is never a Koopman representation of a deterministic configuration flow.**

**Formulation 3c (marginal intertwiner). The survivor.**
- Amplitude observable A: I → ℂ (realized, not defined);
- induced field ψ_t(x) := ∫_{π⁻¹(x)} A∘Φ_t dν_{t,x}, the conditional/fiber average;
- demand: ∃ self-adjoint H (state-independent) with ψ_t = e^{−iHt/κ}ψ₀ on a class of initial conditions, and ρ_t = π_♯μ_t = |ψ_t|²;
- independence: A, H, κ constructed from (I, Φ_t, μ, π) without reference to any solution of the Schrödinger equation.

DGZ equivariance shows 3c is *consistent* when H is given — Bohmian flow is the existence witness with roles reversed. The IST task is the independent realization. But now the decisive new structural result of this round:

> **No-free-lunch Lemma (conditional amplitudes).** *For A realized as a fiberwise conditional functional, exact marginal unitarity forces exactly two regimes:* **(a)** *fibers preserved ⟹ the induced field evolves by the factor Koopman operator ⟹ Formulation 3b ⟹ first-order generator ⟹ dead;* **(b)** *fibers mixed ⟹ P_t = E[U_t | base σ-algebra] is a Markov/conditional-expectation operator: positive, L²-contractive, non-invertible ⟹ information loss ⟹ dissipative corner (Fisher strictly decreases, Round 3 Thm 2a) ⟹ not unitary ⟹ dead.* *Interpolating metastable regimes (partial fiber mixing) inherit leakage — approximate, never exact, unitarity; the transfer-operator literature (Dellnitz–Junge, SIAM J. Numer. Anal. 36, 491 (1999); Froyland, Physica D 200, 205 (2005) on almost-invariant sets) establishes precisely this lossiness. (Mapping the leakage quantitatively to Lindblad-type generators is PLAUSIBLE analogy, not yet a theorem.)*

**Corollary (the strongest structural finding of this round):** *if Gate 3 has a solution, the amplitude is not a conditional average of any observable. It must be a genuinely different functional of the invariant set.* The word "different" is now theorem-backed, not stylistic: the entire natural family — averages, expectations, conditional measures — provably lands in the factor corner (first-order) or the Markov corner (dissipative). This retroactively explains why Round 2's Vlasov slot, while honest, felt empty: mean-field ρ-dependence is available, but every way of *computing* the amplitude from the invariant set's conditional structure is excluded. Whatever the amplitude is, it is not an average over fibers.

**Environment and anchors for 3c** (all existing mathematics, nearly all in the inverted direction — this is the honest state of the field):

1. **Koopman–von Neumann mechanics gives linearity for free — and that is exactly its failure mode.** The KVN representation (Mauro, arXiv:math-ph/0202058 (2002); operational unification in Bondar–Cabrera–Lompay–Ivanov–Rabitz, *PRL* 109, 190403 (2012)) linearizes deterministic dynamics into a unitary group with a *first-order* self-adjoint generator. Lesson, stated once: **Gate 3 ≠ linearity. Koopman already owns linearity; it owns the wrong generator.** The Gate-3 question is precisely: can the Koopman generator's *marginal action* be unitarily equivalent to a second-order elliptic operator — not on L²(μ), but across the conditional structure.
2. **The cat-map datum.** The only explicit unitary groups attached to deterministic maps — quantized torus maps (Hannay–Berry, Physica D 1, 267 (1980); Balasz–Voros, Ann. Phys. 190, 1 (1989)) — are semiclassical bridges (N ↔ 1/ħ, N → ∞ recovers the map), and the quantized cat map has **finite order**: its spectrum is discrete/pure-point even though its classical limit is mixing. In every existing deterministic⟷unitary bridge, *unitarity and spectral poverty go together; mixing and sector-unitarity never do.* This is a pattern, not a theorem — but it is the single most instructive regularity in the neighborhood of Gate 3.
3. **The singular-continuous branch** (integrating the observation you attribute to Claude, which I endorse and sharpen): the spectral regime the program actually needs is neither pure point (3a-dead but trivial) nor Lebesgue (3a-dead by weak mixing) but **singular continuous** — continuous enough to forbid the factor trap, concentrated enough to support quasi-local "spectral packets." Such spectra exist concretely on both sides of the divide: Koopman operators of substitution/rank-one systems (Thue–Morse subshift: singular continuous maximal spectral type, Riesz-product structure; Chacon-type weakly mixing constructions) and Schrödinger operators with aperiodic potentials (Fibonacci Hamiltonian: singular continuous spectrum with anomalous quantum transport — Sütō, *J. Phys.* A 20 (1987); Bellissard–Iochum–Scoppola–Testard 1989; the Damanik–Gorodetski program). **Notably, these are also the structures nearest Palmer's own dyadic/p-adic constructions of the invariant set** — his Bloch-sphere dyadic discretization papers live in exactly this substitution/Riesz-product neighborhood. That is the first time in four rounds that the program's missing object and its published raw material occupy the same mathematical region. It is suggestive, not established: all known results run in the *reverse* direction (fractal structure produces singular-continuous quantum dynamics; nobody has exhibited singular-continuous deterministic dynamics producing a Schrödinger-marginal).
4. **Groenewold–van Hove rigidity** (Groenewold, *Physica* 12, 405 (1946); van Hove 1951; Gotay, *J. Math. Phys.* 40, 2107 (1999)): the classical observable algebra cannot embed exactly into the quantum one. Design consequence for 3c: the independence/realization demand cannot also require exact preservation of classical observables through the amplitude layer; *something classical must be sacrificed.* The charter must say what. This is a constraint on candidate constructions, not a blocker.
5. **Fractal analysis supports second-order operators on fractal supports** — Kigami's Dirichlet forms on p.c.f. fractals, Fukushima–Shima's spectral decimation on the gasket (explicit pure-point spectra), Jonsson–Wallin trace theory for smooth layers over d-sets. Existence of "Laplacians on fractals" is established mathematics; what is absent — and is precisely the Gate-3 burden — is *identification of such an operator with the marginal transport of a deterministic flow*, with the Euclidean Fisher functional as continuum limit and a universal coefficient.

**Gate-3 charter, final form.** Define the *Independent Realization Problem*: exhibit (or prove nonexistent) a triple (A, H, κ) for a deterministic (I, Φ_t, μ, π) satisfying Formulation 3c with H = −(κ²/2m)Δ + V, κ mass-independent, A not a conditional average (per the no-free-lunch lemma), locality of the effective quantum potential *proved* (not assumed), and Groenewold–van Hove sacrifice explicitly declared. The hunting ground, per items 2–3, is the singular-continuous/substitution neighborhood — the only corner all three lines of evidence converge on.

---

## 4. GATE 4, CONSOLIDATED: ONE CONSTANT, ONE AXIOM

Theorem G2(ii) has already performed the crucial unification: **the phase unit κ is one constant with three jobs** — (i) the unit of the phase in ψ = √ρ e^{iS/κ}; (ii) the energy coefficient, c = κ²/8m, forced; (iii) the circulation quantum, ∮∇S·dl ∈ 2πκℤ/m (Wallstrom's condition, which Reddiger–Poirier's framework accommodates but does not derive). Gate 4 therefore does not ask "where does ħ²/8m come from" — G2 answered that — it asks:

$$\boxed{\text{Does IST contain a mathematically unavoidable, universal, mass-independent action unit }\kappa\text{?}}$$

with the explicit requirements: state-independence, universality across systems, mass-independence, isotropy/scalar character, topological protection (immunity to coarse-graining details), and empirical value to be measured — exactly as c and G are measured. Note what does *not* count as an answer: any normalization of a derived S (conventional unless anchored), and dimensional analysis (explicitly rejected by your §8 discipline).

**The one IST-native candidate worth stating as an axiom:** Palmer's invariant-set construction partitions state space dyadically — information cells. The minimal extension is to upgrade the partition from *information cellulation* (bits) to **action cellulation**: cells of equal symplectic volume 2πκ. This is one axiom with three consequences: (a) circulation quantization becomes automatic (winding through cells — the Wallstrom constant is the cell volume); (b) universality is automatic (cell volume is a structural invariant, not a model parameter); (c) a sharp empirical hook — mass-dependence enters through spatial cell size, ℓ* = κ/(m v*): the invariant set must resolve **Compton-scale cells for each mass**. That last consequence is strongly falsifiable in structure: it ties the fractal geometry to Compton scales, which is either a feature or a fatal rigidity. [Category 4; PLAUSIBLE; one axiom, two tests; nothing in published Palmer asserts action-labeling — flagged per your attribution discipline.]

**Status assessment of Gate 4:** no route exists today in any literature to a derived universal action quantum; the action-cellulation axiom is the first candidate with a mechanism rather than a fiat. If it fails, κ-universality has no candidate mechanism at all, and the program's C-verdict hardens accordingly.

---

## 5. THE CONSOLIDATED CONDITIONAL NO-GO (your requested form)

> **CN.** *Let (I, Φ_t, μ, π) be deterministic with positive invariant measure, π: I → Q the configuration projection, and no stochastic ontology. Then the marginal dynamics cannot realize the Fisher–Madelung structure with universal coefficient unless the model contains structure outside every currently analyzable mechanism class, specifically:* **(i)** *fixed-scale differentiable dynamics (u ≡ 0; first-order generators — Lemma A, Peetre);* **(ii)** *hyperbolic fast–slow / homogenization limits (dissipative Fokker–Planck corner with Fisher as strict Lyapunov function; zero-noise corner drift-rigidity — Round 3 Thm 2);* **(iii)** *Koopman subrepresentations (weak-mixing spectral obstruction — §3, 3a);* **(iv)** *factor flows and pointwise amplitude identification (derivation obstruction — §3, 3b);* **(v)** *conditional-averaging amplitudes (no-free-lunch lemma — §3);* **(vi)** *PSD fluctuation-stress matching (Lemma B).* *The minimal structure not excluded is: a non-conditional-averaging amplitude realization (Formulation 3c) with a universal topological action unit (Gate 4).*

Every clause of CN is either an existing theorem, an immediate corollary, or a to-be-written lemma with a clear proof path (the no-free-lunch lemma for (v) is the only genuinely new write-up, and it is elementary). CN is therefore **defensible now** in a way the Round-2 synthesis no-go was not: it is no longer a literature-level corollary but an assembled chain of statements, each with a proof obligation of bounded difficulty.

Scope limits, stated with equal precision: CN is not absolute. Bohmian flow witnesses logical consistency. The excluded classes are those *with existing limit theorems or representation theorems*; a singular-continuous, non-conditional, globally geometric amplitude layer sits outside all of them — which is exactly where the evidence (§3, items 2–3) independently points, and exactly where nothing has been proved.

---

## 6. PROOF OBLIGATION LEDGER (DELTA ONLY)

| # | Claim | Status | Theorem/source | Assumptions | BM-IST applicability | What remains |
|---|---|---|---|---|---|---|
| 18 | Symmetries alone (locality, boosts, reversibility, conservation) do not select any f(ρ,∇ρ) | New lemma (elementary) | direct | Gate-1 class | **Correction 1 adopted** | — |
| 19 | Separability/additivity selects Fisher up to scale within local class | Existing computation + H–R axiomatization | product-density computation; Hall–Reginatto 1998/2002 axioms | locality; separability | Double-locks Gate 2 | Write as lemma |
| 20 | Linearity + structure ⟹ E_q = (κ²/8m)I_F; coefficient locked | **Theorem G2 — provable now** | Round 3 Thm 1, tightened | Hamiltonian two-field layer; local f; fixed κ | Yes, conditional on layer existence | Rigorous write-up; classify S-dependent/higher-derivative escapes |
| 21 | Nonlocal quantum terms evade G2 | Open loophole | — | — | Gate 3 must *prove* locality | Locality theorem from realization |
| 22 | No Hilbert sector for weakly mixing Φ_t | Existing theorem | Koopman–von Neumann 1932; von Neumann 1932 | weak mixing | Kills Formulation 3a | — |
| 23 | No pointwise/factor amplitude with second-order generator | Existing theorem (core) | Peetre; derivation property | factor flow; differentiability | Kills Formulation 3b | Write cleanly |
| 24 | No conditional-averaging amplitude (no-free-lunch) | **New lemma, provable now** | §3 trichotomy; Dellnitz–Junge/Froyland for leakage | A conditional functional | Kills the entire natural amplitude family | Rigorous write-up; quantify leakage |
| 25 | Amplitude layer must be non-conditional, singular-continuous-neighborhood object | Corollary of 24 + cat-map datum | §3 items 2–3 (pattern, not theorem) | — | Directs the search | Convert pattern to theorem or find counterexample |
| 26 | κ = ħ via action cellulation | PLAUSIBLE, one axiom | — | Palmer dyadic structure + action labeling | Only candidate mechanism for Gate 4 | Axiomatize; derive Compton-scaling consequence; test |
| 27 | CN (consolidated no-go) | Defensible now | items 18–24 + Round 2–3 | as stated | Yes | Write the chain as one paper |

---

## 7. DECISION TREE (UPDATED)

**IF deterministic IST naturally yields the osmotic/Fisher term:** No — established across Rounds 2–4, now at theorem level (CN).

**ELSE IF it arises after adding clearly motivated deterministic structure:** Precisely this — but the structure is now specified to type: *not* "any new axiom," but (a) a non-conditional amplitude realization (Formulation 3c, outside the provably dead families), and (b) one universal action unit (action-cellulation axiom, single candidate). Both are stated axioms with consequences, not vague appeals.

**ELSE IF stochasticity is mathematically indispensable:** Scoped as in Round 2/3 and unchanged: indispensable for the *osmotic object* (noise fingerprint), not for the Fisher *shape* (triple-locked: linearity, separability, Chentsov), currently the only known selector for the *constant* — and Gate 4's cellulation axiom is the first deterministic candidate to challenge that.

**ELSE (no-go):** CN is the precise no-go; it excludes all analyzable mechanism classes, and its only uncovered corner is the singular-continuous, non-conditional amplitude layer — where the program lives or dies.

---

## 8. SHORTEST PATH, FINAL FORM

The definitive answer to this gate is now a pair of papers, not a survey:

**Paper A (negative, weeks not years): "Conditional rigidity of deterministic coarse limits."** Contents: T− (Round 3 Thms 2a/2b with TM1 instances), the no-free-lunch lemma, the 3a/3b obstructions, assembled as CN. This permanently closes every analyzable route and, crucially, *identifies the only surviving structural type* by exclusion. Its falsification test: one counterexample — any deterministic system with a conditional-averaging amplitude evolving by exactly e^{−iHt/κ}. The lemma says there is none; finding one would be a major event.

**Paper B (the real question): "The Independent Realization Problem."** Formalize Formulation 3c, state CN's uncovered corner, and attack the singular-continuous neighborhood: substitution/scale-invariant dynamics (Thue–Morse- and Fibonacci-type structures; Palmer's dyadic sets as raw material) with the express goals — an amplitude functional that is not a conditional average, a *proved* locality theorem for the effective potential, and a topological action unit with the Compton-scaling consequence. The cat-map datum and the weak-mixing obstruction jointly predict that the solution, if it exists, must show **unitarity with a non-Lebesgue, non-pure-point spectrum** — a regime with named exemplars on both sides of the divide and no bridge in the forward direction. That inverted bridge is the program's true frontier.

Your architecture stands, with the two corrections (separability is Gate 1's real content; Hamiltonicity migrates to Gate 3) and the new constraint (no-free-lunch: the amplitude cannot be an average). Gate 2 is closed as a theorem. Gate 4 is one axiom from closure in principle. Everything else — the entire remaining scientific content of BM-IST — is Gate 3: one object, one constant, one spectral neighborhood, and two papers between us and a definitive answer.
