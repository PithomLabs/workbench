### I. The Stage: Spacetime Geometry (Causal Dynamical Triangulations)

#### Original Assumptions & Frictions

* **Original CDT Assumption:** Spacetime is fundamentally composed of discrete, piecewise-flat 4-simplices (triangles) assembled via Regge calculus, where the universe exists as a non-perturbative quantum superposition of all possible triangulated geometries.
* **Friction with the Synthesis:** This creates a double structural failure:
1. *The "Lego Brick" Trap:* Claiming smooth spacetime is literally constructed out of discrete triangles violates the continuum principle—a continuum is ambient, not generated from discrete building blocks.
2. *Ontological Category Error:* Bohmian Mechanics requires a defined, non-superposed background geometry to navigate. Placing Bohmian trajectories directly on a superposed CDT spacetime creates an irreconcilable category clash.



#### Revised Assumptions for Synthesis

* **CDT as a Combinatorial Regulator:** CDT is demoted from being the "fundamental discrete substance" of space to acting as a **non-perturbative statistical partition engine** (a mathematical regulator analogous to lattice QCD). The physical content of CDT lies in its causal topology and scale-dependent spectral dimension flow ($d_s: 2 \to 4$), not in the boundaries of the simplices.
* **The Emergent Stage Protocol:** The actual physical Stage is not the quantum superposition of geometries, but the **scale-dependent, coarse-grained expectation value of the metric** $\langle g_{ab} \rangle_k$ derived from the CDT ensemble via the Asymptotic Safety flow. In the deep UV, geometry is a thermodynamic ensemble; in the IR, a smooth classical spacetime manifold cleanly emerges.

---

### II. The Dancer: Ontological Matter & Configurations (Bohmian Mechanics)

#### Original Assumptions & Frictions

* **Original BM Assumption:** Matter particles and field modes possess definite configurations $Q(t)$ that evolve deterministically along smooth trajectories, guided by a wave functional over an immutable, unshifting flat configuration space $\mathbb{R}^{3N}$ with an axiomatic Born rule distribution ($\rho = \vert{}\psi\vert{}^2$).
* **Friction with the Synthesis:** As identified in ledger item `BM-CS-DIM-01`, both CDT and Asymptotic Safety prove that spectral dimension flows ($d_s \to 2$ in the UV), causing spatial geometry to fracture. Postulating a fixed, rigid $\mathbb{R}^{3N}$ configuration space backdrop in the UV generates unphysical geometric drag ($Q_{\text{geom}} \to \infty$) and breaks probability conservation. Furthermore, assuming $\rho = \vert{}\psi\vert{}^2$ as a dogmatic axiom leaves the Born rule unexplained at fundamental scales.

#### Revised Assumptions for Synthesis

* **Dynamical Configuration Space:** The Dancer’s configuration space is **scale-dependent and emergent**. The measure on configuration space $\mathrm{d}\mu_k(\mathbf{q}) = \sqrt{\det G(\mathbf{q}; k)}\,\mathrm{d}^{3N}q$ runs dynamically with the RG scale parameter $k$. At the Planck scale, configurations interact with a fractal, 2D effective geometry; as the system coarse-grains to the IR ($k \to 0$), the configuration space stabilizes onto flat $\mathbb{R}^{3N}$.
* **Emergent Born Rule via Subquantum Relaxation:** The Born rule ($\rho = \vert{}\psi\vert{}^2$) is demoted from a fundamental axiom to an **IR thermodynamic attractor**. At the UV fixed point, the universe is in quantum non-equilibrium ($\rho \neq \vert{}\psi\vert{}^2$), but Planckian geometric chaos drives dynamic relaxation toward quantum equilibrium as scale flows toward the IR.

---

### III. The Dance: Scale Flow & Renormalization (Asymptotic Safety)

#### Original Assumptions & Frictions

* **Original AS Assumption:** Quantum gravity is a non-perturbatively renormalizable quantum field theory where coupling parameters flow continuously along an effective average action $\Gamma_k$ governed by a Non-Gaussian Fixed Point (NGFP).
* **Friction with the Synthesis:** Continuum Functional Renormalization Group (FRG) calculations rely on artificial truncations of the action and treat scale transformations abstractly, often lacking an explicit physical time parameter or non-perturbative lattice proof.

#### Revised Assumptions for Synthesis

* **Calculus Engine on Causal Foliation:** Asymptotic Safety acts as the **continuous calculus engine** ($\dot{g} = \beta(g)$) governing how couplings, metrics, and quantum potentials transform across scales along an explicit, physical **Causal Time** axis $t$.
* **Lattice-Validated Scale Flow:** Rather than relying purely on field-theoretic truncations, AS assumes CDT's non-perturbative lattice path integral as its physical realization. CDT’s phase transition boundary supplies the non-perturbative proof of the NGFP, while AS supplies the smooth differential calculus describing the RG flow.

---

### IV. The Structural Joints: Synthesis Integrations

The revised assumptions connect these three frameworks through two primary structural joints:

```
                     [ THE STAGE ]
             Emergent Metric <g_ab>_k
           (CDT Statistical Regulator)
                       / \
                      /   \
  [ Causal Synchronization ] [ Scale-Dependent Measure ]
                    /       \
                   /         \
          [ THE DANCE ] <---> [ THE DANCER ]
      Asymptotic Safety       Bohmian Trajectories Q(t)
     (Continuous RG Flow)    (Emergent Born Rule via H-Theorem)

```

1. **Causal Synchronization (Solving the Problem of Time):** CDT's discrete global time-slicing ($t \in \mathbb{Z}$) and BM's preferred temporal parameter ($t \in \mathbb{R}$) are aligned into a single fundamental **Causal Time** axis. This eliminates the static time frozen-state issue ($\hat{H}\Psi = 0$) and allows the Bohmian guidance equation to run continuously across spatial slices generated by the CDT/AS engine.
2. **Scale-Dependent Subquantum $H$-Theorem:** In the UV ($k \sim M_{\text{Planck}}$), the anomalous dimension $\eta = 2$ at the AS fixed point generates a scale-dependent subquantum diffusion tensor:

$$\mathcal{D}^{IJ}(k) = \mathcal{D}_0 \left( \frac{k}{M_{\text{Planck}}} \right)^2 G^{IJ}(\mathbf{q}; k)$$



This diffusion tensor induces turbulent geometric mixing ($\frac{\mathrm{d}\bar{H}}{\mathrm{d}t} \le 0$), rapidly driving arbitrary UV non-equilibrium states ($\rho \neq \vert{}\psi\vert{}^2$) into standard quantum equilibrium ($\rho = \vert{}\psi\vert{}^2$) by the time geometry reaches the macroscopic IR scale.

---

### Comparative Summary of Revisions

| Framework | Original Assumption | Revised Synthesis Assumption | Ontological Role |
| --- | --- | --- | --- |
| **CDT** | Fundamental discrete 4-simplices in quantum superposition. | Non-perturbative combinatorial regulator generating an emergent statistical metric $\langle g_{ab} \rangle_k$. | **The Stage** (Spacetime Arena) |
| **BM** | Static $\mathbb{R}^{3N}$ configuration space with axiomatic Born rule $\rho = \vert{}\psi\vert{}^2$. | Scale-dependent measure $\mathrm{d}\mu_k(q)$ with Born rule as an emergent thermodynamic attractor via subquantum $H$-theorem. | **The Dancer** (Matter/Configurations) |
| **AS** | Truncated continuous FRG flows over abstract metric spaces. | Non-perturbative calculus engine ($\dot{g}=\beta(g)$) operating along CDT's explicit Causal Time foliation. | **The Dance** (Dynamics across Scales) |
