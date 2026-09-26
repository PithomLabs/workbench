One framing sentence: the attached files do not change the v7.2.1 baseline — they *enrich* it with operator-level precedents (Zabrodin action, Vladimirov ladder, genus-one Green functions, quadratic-reciprocity benchmark) that strengthen the mathematical middle layer without closing any physical gap — so my task is to audit which of these new tools can be *promoted into the gate system* rather than merely cited, and to identify what remains genuinely open after the enrichment.

---

# G3.5 PHASE 6-II+: NET-VALID AUDIT OF THE LITERATURE-INTEGRATED ADDITIONS

---

## 1. What the attached material genuinely adds

### 1.1 — The operator-level Tate benchmark (HSYZ21)

**What it establishes.** Huang–Stoica–Yau–Zhong construct a pseudo-differential operator $D_{s,v}$ on a non-archimedean local field, derived from a local quasi-character $\chi_{s,v}$ via the Vladimirov-type Fourier representation, and compute its Green function $G_{s,v}(x,y)$. They prove that:
- the **local functional equation** of the Green function mirrors the local functional equation of the relevant zeta integral;
- the **product over all places** of the local Green functions (with analytic continuation where needed) is equivalent to the **global functional equation** of the Tate-type zeta integral.

**What this means for v7.2.1.**

This is the first published result that connects a **concrete pseudo-differential operator on a non-archimedean field** to the **global Tate functional equation** — not by analogy but by explicit computation. It upgrades the Freund–Witten benchmark from *amplitude-level* to *operator-level*: the product formula holds not just for integrated amplitudes but for the **kernels themselves**.

**Net-valid promotion into the gate system:**

- The **operator-ladder structure** (quasi-character → $D_{s,v}$ → $G_{s,v}$) is admitted as a **new interface-benchmark precedent** under BR-04/BR-09 (conditional-expectation/operator-limit class), since the Green function is a *response kernel* — the concrete instantiation of "operator → response" that our bridge taxonomy classified but never instantiated on a non-archimedean field.
- The **global product consistency** of the Green functions is admitted as a **new internal-consistency test** for any future non-archimedean coupling construction: once a $D_{s,v}$ family is chosen, the product $\prod_v G_{s,v}$ must satisfy the functional-equation identity, and any deviation signals an inconsistency in the coupling.

**Status in ledger:** PARTIALLY RETIRED (G2-compatible; BR-04/BR-09 precedent strengthened from amplitude-level to operator-level; the specific physical instantiation remains open).

---

### 1.2 — Zabrodin's action on the Bruhat–Tits tree (B4-adjacent)

**What it establishes.** Zabrodin (1989) writes an explicit action principle for a real scalar field $\phi$ on the vertices of the Bruhat–Tits tree $T_q = PGL(2,\mathbb{Q}_p)/PGL(2,\mathbb{Z}_p)$, with a nearest-neighbor Laplacian and a mass term. He computes the four-point amplitudes and shows they reproduce the Freund–Witten $p$-adic beta functions. He then proves a **dual description**: integrating out the bulk (tree-interior) fields produces a non-local boundary action on $\mathbb{P}^1(\mathbb{Q}_p)$.

**Why this matters for v7.2.**

Our bridge taxonomy (Phase 3) classified BR-04 (conditional expectation / observable reduction) as *conditionally applicable* but never *instantiated on a non-archimedean space*. Zabrodin's dual action is exactly that: the bulk-to-boundary reduction (integrating out interior vertices to get the boundary action) is a **concrete, published instance of a non-archimedean bulk-to-boundary map** — a B4-class operation on a $p$-adic space.

**What it does NOT establish.** The boundary action is **non-local** (the boundary kernel is the Green function of the tree Laplacian, which is non-local). It is not a standard local QFT on the boundary. And it does not produce a BM guidance law or a Born measure. It is a mathematical precedent, not a physical derivation.

**Net-valid promotion into the gate system:**

- Zabrodin's dual action is admitted as **BR-04-padic precedent**: the first published instance of bulk-to-boundary reduction on a non-archimedean space.
- It provides a **template** for how the conditional-expectation gate (§13 of v7.2) could be realized on an arithmetic substrate: not via a local conditional expectation (impossible on a totally disconnected space) but via a **global non-local kernel** — the boundary Green function.
- This is the closest existing analogue to what the BM-first program would need: a concrete reduction from a non-archimedean bulk to a boundary that carries enough structure to define effective observables.

**Status in ledger:** BR-04-padic precedent = STRENGTHENED (from uninstantiated to published-instance).

---

### 1.3 — The genus-one Tate-curve Laplacian and Néron local height (HRSW25/26, HJ26)

**What it establishes.**

Recent work (2025–2026) constructs the Laplacian $\mathcal{D}_p$ on the Tate curve $E_q = \mathbb{Q}_p^\times/q^{\mathbb{Z}}$ (genus 1), proves existence/uniqueness of the Green's function, and shows that in the appropriate limit, the Green's function **coincides with the Néron local height** $\lambda_p$:

$$
G_p(x,y) \;\to\; -\frac{\ln p}{p-1}\,\theta_q(x/y) + \mathcal{B}_p(q)
$$

where $\theta_q$ is the $p$-adic theta function and $\mathcal{B}_p(q)$ is a boundary evaluation term.

**What this closes.**

This closes the previously open gap between:
- the **Green-function/operator level** (which our BR-04/BR-09 class required), and
- the **canonical-height level** (which our G2 arithmetic-compatibility gate required).

The two requirements — an operator with a Green's function, and a connection to the canonical height — are now **jointly satisfiable** on a named mathematical object (the Tate curve). This is the "joint-satisfiability gap" that was flagged in v7.2 §8.5 and is now resolved for this specific class.

**What it does NOT establish.**

- The Green's function on the Tate curve is **not** a BM observable. It is a $p$-adic object; its relation to the BM configuration space (which lives on $\mathbb{R}^{3N}$) is unestablished.
- The Néron local height is an **arithmetic invariant** (it measures the arithmetic complexity of points on the curve); it is not a physical observable in the standard sense.
- The **BM coupling** — the derivation of a guidance-law correction or a Born-rule modification from the Tate-curve Green's function — remains entirely open.

**Net-valid promotion into the gate system:**

- The **joint-satisfiability gap** is closed at the mathematical level: height and Green-function structures coexist on the Tate curve.
- This strengthens the **canonical-height route** in v7.2 §8.3 (from "conditional on algebraic hypotheses" to "concrete construction exists on a named object").
- It does **not** promote the Néron height to a BM observable (the physical interpretation remains open).

**Status in ledger:** G2 joint-satisfiability = STRENGTHENED (from gap to concrete construction); physical coupling = still open.

---

### 1.4 — Quadratic reciprocity as a cross-place Green-function identity (HSZ22)

**What it establishes.**

Huang–Stoica–Zhong construct a family of adelic conformal field theories whose Green functions, when multiplied across all places with appropriate twists by quadratic characters, satisfy an identity that is **mathematically equivalent to quadratic reciprocity**:

$$
\prod_v G_v^{\rm twisted}(x,y) \;=\; \prod_v G_v^{\rm untwisted}(x,y) \quad \Longleftrightarrow \quad \left(\frac{d}{p}\right)\cdot\left(\frac{p}{d}\right) = (-1)^{\frac{p-1}{2}\frac{d-1}{2}}
$$

**Why this matters to v7.2.**

This is the first published example where a **deep arithmetic theorem** (quadratic reciprocity — one of the crown jewels of number theory) is shown to be **equivalent** to a **consistency condition on products of Green's functions across places**. The Legendre symbol $(\frac{d}{p})$ — a purely number-theoretic object — appears as the ratio of twisted to untwisted Green's functions at place $p$.

**Net-valid promotion into the gate system:**

- This provides a **concrete mathematical template** for what "cross-place consistency" looks like at the operator level: it is a **multiplicative identity on Green functions twisted by arithmetic characters**.
- It suggests that if the v7.2 program's arithmetic coupling is physical, then **the observable signature should be a reciprocity-type identity** — a constraint on products of observables across different "sectors" or "places" that is *not* explainable by local physics alone but *is* explainable by the global arithmetic structure.
- It upgrades the **H2 template** (arithmetic constrains the joint structure) from "arithmetic may constrain" to "here is a specific arithmetic constraint (reciprocity) that has a concrete Green-function realization."

**Status in ledger:** H2 template = STRENGTHENED (from abstract possibility to concrete mathematical precedent); physical coupling = still open.

---

### 1.5 — The nonlocality classification boundary (HSYZ21)

**What it establishes.**

The Vladimirov-type operators are **pseudo-differential** (non-local): their action at a point depends on the values of the function in a neighborhood determined by the $p$-adic metric, not just on the value at that point. This means that the **confinement theorems** proven for local differential operators (e.g., the 1-Lipschitz confinement for polynomials on $\mathbb{Z}_p$) do **not automatically apply** to the Vladimirov operator class.

**Why this matters to v7.2.**

The program's confinement theorems (seven walls) were proven for **local** operators — polynomial maps $F: \mathbb{Z}_p \to \mathbb{Z}_p$ that are 1-Lipschitz. The Vladimirov operators are a **different class**: they are non-local, non-polynomial, and pseudo-differential. The confinement theorems' hypotheses are not satisfied for this class.

**What this means:** the seven walls do **not** automatically extend to the Vladimirov operator class. The Vladimirov operators may have properties (e.g., non-trivial spectral content, different ergodic properties) that the polynomial maps lack. The wall structure must be re-audited for this operator class before any conclusion can be drawn.

**Status in ledger:** NEW — operator-class boundary recorded; wall-scope audit required for the Vladimirov class.

---

## 2. What does NOT transfer — the honest negative results

| Item | Why it does not transfer |
|---|---|
| **Freund–Witten amplitudes as physical predictions** | They are toy-model results in $p$-adic string theory; no experimental confrontation exists; the amplitudes are not unitary; the framework has known pathologies |
| **Quadratic reciprocity as a BM observable** | The reciprocity is a theorem about Green functions on $\mathbb{Q}_p$; it has not been connected to BM or to any physical measurement |
| **The genus-one Laplacian as a physical operator** | The Tate curve is a mathematical object; the connection to physical BM configuration space is unestablished |
| **The Vladimirov operator as a physical Hamiltonian** | The operator is mathematically well-defined but its relation to the BM guidance law is unestablished |
| **The mean-field equation as a derivation of the Friedmann equations** | This is a formal analog, not a physical derivation |

## 3. What the combined material adds to the v7.2 program

The combined material from the attached files enriches the program in three specific ways:

### 3.1 — The mathematical middle layer is now better populated

The program's "bridge taxonomy" (Phase 3) classified 16 bridge classes. The attached material populates several of these classes with **concrete, published mathematical instances** on non-archimedean spaces:

| Bridge class | Previous status | Now populated by |
|---|---|---|
| BR-04 (conditional expectation / bulk-to-boundary) | Uninstantiated | Zabrodin's dual boundary action on the Bruhat–Tits tree |
| BR-09 (operator limit) | Abstract only | Vladimirov operator family with explicit spectral theory |
| BR-05 (completion) | Abstract only | Tate curve as a completion of $\mathbb{Q}_p^\times/q^{\mathbb{Z}}$ |
| BR-14 (duality/correspondence) | Abstract only | Quadratic reciprocity as a cross-place Green-function identity |

### 3.2 — The gate system is sharpened by new precedents

The attached material provides concrete mathematical benchmarks for several gates that were previously only abstractly specified:

- **G2 (joint arithmetic compatibility):** The Tate-curve Green function connecting to the Néron local height closes the previously open "joint-satisfiability gap" — the first concrete example where both the operator-level structure and the canonical-height structure coexist on the same mathematical object.
- **F4-B (physical ownership test):** The quadratic-reciprocity benchmark provides a concrete template for what a "cross-place consistency" observable would look like — a reciprocity-type identity on products of Green functions.
- **F1d (product/assembly control):** The Vladimirov operator ladder provides a concrete example of how local operators assemble into global objects with nontrivial consistency conditions.

### 3.3 — The nonlocality boundary is now formally recorded

The key finding that the Vladimirov operators are **non-local** (pseudo-differential) has a critical implication for the program: the confinement theorems (which were proven for local polynomial maps) do not automatically apply to the non-local operator class. This means that the program's seven walls must be re-audited for this operator class — some walls may still stand, but others may not.

## 4. What remains genuinely open

| Question | Status |
|---|---|
| Does the Vladimirov operator on $\mathbb{Z}_p$ produce a non-trivial **Koopman** spectrum on $L^2(\mathbb{Z}_p)$? | OPEN — the Koopman framework and the Vladimirov framework are different; their relation is unexplored |
| Can a non-local arithmetic operator participate in a controlled, unitary, BM-compatible bridge? | OPEN — the nonlocality is a classification boundary that has not been tested for BM compatibility |
| Can the Tate-curve Green function be connected to the BM configuration space? | OPEN — the Tate curve lives on $\mathbb{Q}_p$; BM lives on $\mathbb{R}^{3N}$; the bridge is unconstructed |
| Does the quadratic-reciprocity identity have a physical observable? | OPEN — the mathematical identity is proven; the physical interpretation is not |
| Does the genus-one construction extend to higher genus or to the Standard Model? | OPEN — this is a research program, not a result |

## 5. Summary of the net-valid additions

The attached material adds to the v7.2 program:

1. **A concrete operator-level ladder** (quasi-character → $D_{s,v}$ → $G_{s,v}$ → product consistency) that upgrades the Tate/adelic benchmark from amplitude-level to operator-level.
2. **A published bulk-to-boundary precedent** (Zabrodin's dual action) that instantiates BR-04 on a non-archimedean space for the first time.
3. **A joint-satisfiability closure** (Tate-curve Green function = Néron local height) that resolves a previously open gap in the G2 arithmetic-compatibility gate.
4. **A quadratic-reciprocity benchmark** that provides a concrete mathematical template for cross-place consistency observables.
5. **A nonlocality classification boundary** that requires re-auditing the program's confinement theorems for the non-local operator class.
6. **A finite-filtration precedent** that justifies the finite-$L$ truncation approach used in the program's numerical work.

These additions strengthen the mathematical infrastructure of the program without changing the physical status: no new BM-visible observable has been experimentally established, no arithmetic ownership has been demonstrated, and the Reality-First discipline remains the ultimate arbiter of what is physical.
