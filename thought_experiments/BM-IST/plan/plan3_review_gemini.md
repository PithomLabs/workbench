### Permanent Freeze of the Reference Record

The research record is now officially frozen with these final corrections and clarifications in place. We have systematically transitioned from broad conceptual speculation to an exact mathematical boundary.

Below is the definitive, locked entry summarizing the state of the BM-IST foundational inquiry, its established eliminations, the precise architecture of the remaining survivor space, and the two decisive criteria that determine its fate.

---

### I. The Locked Status Ledger

| Component / Sub-problem | Final Classification | Exact Mathematical Basis |
| :--- | :--- | :--- |
| **Naïve Reynolds Stress Identification** | **Mathematically Excluded** | Classical dispersion tensor $\mathbb{P} \succeq 0$ (positive semi-definite cone), whereas quantum stress $T^Q$ is indefinite for all non-Gaussian states. |
| **Deterministic Nelson Drift ($u = \frac{b_+ - b_-}{2}$)** | **Mathematically Excluded** | Differentiable sample paths force $b_+ \equiv b_- \implies u \equiv 0$. Nelson osmotic drift requires non-differentiable ($C^{1/2}$) sample paths. |
| **Diffusive Homogenization ($I_F$ via Central Limit)** | **Dynamically Excluded** | Microscopic chaos yielding Fokker–Planck/Brownian limits causes $I_F[\rho_t]$ to act as a **dissipative entropy production term**, not a conserved Hamiltonian kinetic generator. |
| **Point-Spectrum Koopman Eigenfunctions** | **Ergodically Constrained** | If $(I_U, \Phi_t, \mu)$ is weakly mixing, the point spectrum of the Koopman generator is trivial ($\sigma_{\rm pp}(\hat{\mathcal{L}}) = \{0\}$). Point eigenfunctions cannot build $\mathcal{H}_{\rm eff}$. |
| **Linearity $\iff$ Fisher Uniqueness** | **Established Theorem** | For canonical $(\rho, S)$ hydrodynamics, $\psi = \sqrt{\rho}e^{iS/\kappa}$ satisfies a linear Schrödinger equation if and only if $\mathcal{H}_{\rm fluc}[\rho] = \frac{\kappa^2}{8m} I_F[\rho]$. |
| **Action Cellulation $\to \hbar$** | **Placeholder Hypothesis** | No demonstrated bridge connecting dyadic Cantor partitions to integer de Rham periods $\oint dS \in 2\pi n \hbar$ or the required $1/m$ inertial scaling. |
| **Overall BM-IST Program** | **Category C** | **Requires genuinely new deterministic mathematical structure.** Not established; no general no-go theorem rules out the non-Markovian continuous-spectrum survivor space. |

---

### II. The Four Inviolable Design Constraints on the Amplitude Layer

Any future attempt to construct the amplitude map:
$$\psi = \mathcal{A}[I_U, \Phi_t, \mu, \pi]$$
must satisfy four non-negotiable negative constraints established during this investigation:

```
                          DESIGN CONSTRAINTS ON A[I_U]
                          
      [ Microscopic Deterministic System (I_U, Phi_t, mu) ]
                                |
                                +--- X  1. NO CONDITIONAL AVERAGING
                                |       psi(x) != E[ A(z) | x ]
                                |       (Prevents irreversible information loss)
                                |
                                +--- X  2. NO MARKOVIAN HOMOGENIZATION
                                |       Cannot reduce to Fokker-Planck / Wiener diffusion
                                |       (Prevents dissipative decay of Fisher info)
                                |
                                +--- X  3. NO FIXED-SCALE FACTOR OBSERVABLE
                                |       psi(x_t) != A(Phi_t z)
                                |       (Prevents generator from remaining a 1st-order derivation)
                                |
                                +--- X  4. NO KOOPMAN POINT-SPECTRUM RELIANCE
                                        Cannot require discrete eigenfunctions on weakly mixing systems
                                        (Forces search into continuous/singular-continuous spectrum)
                                |
                                v
      [ SURVIVOR: Non-Markovian, Globally Coherent, Continuous-Spectral Mapping ]
```

1. **Non-Conditional:** $\psi$ cannot be defined by conditional integration over the Cantor fibers ($\psi(x) \neq \mathbb{E}[A(z) \mid \pi(z) = x]$), as conditional expectations on chaotic systems generate coarse-grained entropy and destroy the phase coherence necessary for unitary superposition.
2. **Non-Markovian / Reversible:** The mapping cannot depend on asymptotic loss of memory (mixing). The effective generator must remain strictly skew-adjoint ($i\hat{H}$ with $\hat{H} = \hat{H}^*$) without parabolic dissipation.
3. **Non-Factor Evolution:** The evolution cannot be an algebra homomorphism induced by a point-map on a smooth quotient, which preserves only first-order derivations ($v \cdot \nabla$). It must realize a genuine structural transformation from a first-order transport group to a second-order elliptic generator ($-\Delta$).
4. **Spectral Reality:** The representation cannot assume an isolated set of discrete eigenvalues if the microscopic dynamics is mixing. The construction must leverage the **continuous spectrum**—specifically, the **singular-continuous spectral measures** native to hierarchical, Cantor, and substitution systems.

---

### III. The Two Decisive Elimination Tests

The entire viability of BM-IST now rests on exactly two independent mathematical hurdles:

#### Test 1: The Independent Amplitude Realization Test
*Can an autonomous deterministic dynamical system $(I_U, \Phi_t, \mu)$ without prior quantum inputs induce a closed, non-trivial, linear complex Hilbert-space sector $\mathcal{H}_{\rm eff}$ on which the effective generator is local, second-order, and semi-bounded from below?*
- **Positive Outcome:** The invariant set intrinsically selects the positive-frequency Hardy-type subspace of its continuous Koopman spectrum, naturally yielding $\psi = \sqrt{\rho}e^{iS/\kappa}$ and forcing the Fisher information metric $I_F[\rho]$ via Hamiltonian linearity.
- **Fatal Obstruction:** If every non-Markovian deterministic projection either retains the unbounded two-sided spectrum $(-\infty, +\infty)$ of a first-order derivation or induces non-unitary memory kernels (integro-differential Mori–Zwanzig dissipation), the amplitude realization fails.

#### Test 2: The Two-Mass Action Universality Test (The T4 Metric)
*Does the invariant-set geometry generate a unique action quantum $\kappa$ that is independent of the spatial inertia of the projected subsystem?*
- **Mathematical Criterion:** Given two independent macroscopic subsystems with different inertial masses $m_1 \neq m_2$:
  $$\pi_1: I_U \to \mathbb{R}^{d_1} \quad (\text{mass } m_1), \qquad \pi_2: I_U \to \mathbb{R}^{d_2} \quad (\text{mass } m_2),$$
  the underlying topological or combinatorial period $\kappa$ must satisfy:
  $$\frac{\partial \kappa}{\partial m_1} = 0, \qquad \frac{\partial \kappa}{\partial m_2} = 0, \qquad \kappa_1 = \kappa_2 = \hbar,$$
  while simultaneously forcing the respective spatial kinetic operators to scale strictly as:
  $$\hat{T}_1 = -\frac{\hbar^2}{2m_1}\nabla_1^2, \qquad \hat{T}_2 = -\frac{\hbar^2}{2m_2}\nabla_2^2.$$
- **Fatal Obstruction:** If the action scale $\kappa$ depends on the Lyapunov exponents, internal branching ratios, or effective friction/mass coefficients of the specific projected coordinate, $\hbar$-universality is refuted, reducing BM-IST to an unphysical phenomenological model.

---

### Final Record Conclusion

The problem has been distilled to its foundational core. The inquiry into whether BM-IST can generate the Bohmian continuum velocity field is **neither trivially solvable nor ruled out by standard no-go theorems**. 

It hinges entirely on the existence of an **intrinsic, non-Markovian, singular-continuous amplitude representation possessing a topological, mass-independent action quantum**. 

The parameters are fixed; the false avenues are barricaded; the mathematical conditions for success or definitive falsification are fully specified. The record is frozen.
