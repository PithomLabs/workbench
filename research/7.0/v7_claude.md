# BM–IST–AS Tripartite Research Program
## Consolidated Research Architecture v7.0

**Governs:** all prior versions (v6.2, v6.3.1) and every downstream ledger addendum
**Constitution:** Elephant Bridge Protocol (EBP) v2.1 — ideas enter free; promotion costs debt
**Status:** research architecture, not a constructed physical theory
**Governing change relative to v6.3.1:** the core architecture is no longer a one-way pipeline from discrete substrate to continuum. It is a two-column structure — an arithmetic sector and an independently-specified continuum sector — linked by an explicit, testable global coupling constraint. Every gate downstream of that change has been re-audited for the same bias and revised where it was found. A full accounting is in Appendix B; read this document as the corrected architecture, not as a patch list.

---

## 0. What Changed, In One Paragraph

v6.3.1 asked "does the arithmetic substrate generate the continuum and quantum mechanics." After seven rounds of construction attempts, every route to a positive answer terminated the same way: SPECTATOR (the arithmetic contributes something real — a phase register, a measure, a clock — that a generic non-arithmetic construction reproduces identically) or IMPORTED (the continuum arrives already built, smuggled in by the bridge rather than derived by it). v7 does not retreat from that finding — it is treated as a genuine, reproducible, EBP-promotable negative result. What v7 changes is the question. Following an independently-verified mathematical precedent (Tate's adelic construction, §15), v7 asks whether the arithmetic and continuum sectors are **siblings** — co-equal completions of one common structure, linked by a global consistency constraint — rather than parent and child. This is a hypothesis, not a result, and it is held to the same standard as everything else: it earns its place only if a **decoupled null** (both sectors present, no coupling constraint) fails to reproduce whatever it's credited with explaining.

---

## 1. Thesis

The program's earlier thesis stands: **stop asking any one of BM, IST, or AS to be the elephant.** Each supplies a testable structural claim; none is authoritative; the elephant is whatever survives translation, adversarial testing, and subtraction. v7 adds a second-order instance of the same discipline, turned on the architecture itself: **the direction of the arrows between the theories is also a hypothesis, not a given**, and the seven-round SPECTATOR/IMPORTED pattern is treated as direct evidence the old arrow direction was wrong, not as evidence the whole program was wrong.

---

## 2. No Sacred Cows — Extended

Unchanged from v6.3.1, with one addition: **the pipeline architecture itself is no longer sacred.** The one-way diagram \((X,F)\to\cdots\to\text{QFT+GR}\) is retired as an assumption and retained only as one of two competing architectural hypotheses (§6). Nothing about BM, IST, or AS's individual content is weakened by this — only the assumed relationship between the discrete and continuous sectors changes.

---

## 3. EBP v2.1 Constitution — Unchanged

Ideas enter free. Promotion costs debt (`needMap`, `needInvariant`, `needToyCheck`, `needNullModel`, `needObstruction`, `needFaithfulnessReview`). Debt blocks promotion but never kills an idea. New contradicting evidence can reinstate debt and unpromote a previously promoted claim. No final-truth language is promoted. Accounting must never become the work. All of this governs v7 exactly as it governed v6.3.1 — the constitution is not the layer being revised.

---

## 4. Typed Spaces — Extended for Two Sectors

v6.3.1 typed one state space \(X\), one measure space \(\mathcal M(X)\), one theory space \(\mathcal T\), one observable space \(\mathcal O\). v7 types two parallel families:

$$
X_p\ \text{(arithmetic/p-adic sector)}, \qquad X_\infty\ \text{(continuum/archimedean sector)},
$$

$$
\mathcal M(X_p),\ \mathcal M(X_\infty), \qquad \mathcal T_p,\ \mathcal T_\infty, \qquad \mathcal O_p,\ \mathcal O_\infty,
$$

and one new object with no v6.3.1 analogue — the **coupling object**, a global constraint relating a place-indexed family of local data:

$$
\mathcal K:\ \{\text{local data at every place } v\} \longrightarrow \{\text{TRUE}, \text{FALSE}\},
$$

modeled on, but not assumed identical to, the number-theoretic product formula \(\prod_v|x|_v=1\). \(\mathcal K\) is itself a typed object subject to G0: it must be stated with domain and codomain explicit before any physical content is attached to it (§15.4).

---

## 5. G0 and the No-Go Lemmas — Extended with Positive Machinery

### 5.1 The prohibition (unchanged)

A strongly continuous unitary group cannot act nontrivially on a countable/totally-disconnected set (L1, orbit rigidity); a finite operator group cannot carry a nontrivial continuous one-parameter flow (L2). Together these forbid any construction that silently assumes literal continuous Schrödinger evolution atop a countable beable. \(I_U=W^s(\Gamma_*)\) remains banned as an ill-typed identity — a fixed point of a flow and an invariant set of a map are different kinds of object until a theorem says otherwise.

### 5.2 G0-EXT-1 — Positive construction requirement (new in v7)

G0 has always said what is forbidden. It has never supplied what a *legitimate* cross-type relationship looks like. v7 closes that gap by importing a working template: **Connes–Chamseddine spectral-triple construction**, in which a discrete algebra and a continuum Dirac operator are combined into one joint operator,

$$
D = D_F\otimes 1 + \gamma_5\otimes\partial\!\!\!/,
$$

with the discrete factor \(D_F\) built from a finite (here: arithmetic) algebra and the continuum factor \(\partial\!\!\!/\) supplied independently. This is real, working machinery — not an analogy — demonstrating that "discrete algebra × continuum geometry, coupled through one operator" is mathematically achievable, with the Standard Model's own gauge and Higgs sector as the existence proof. v7 requires any future coupling construction (§15) to be checked against this template as a **positive control**: does it produce an operator of comparable type, or does it merely juxtapose two unrelated objects and call the juxtaposition a coupling?

### 5.3 The simultaneity precedent (new in v7)

**Causal Fermion Systems** (Finster) supply a second, independent existence proof relevant to G0: a construction in which spacetime and matter content emerge *together*, from one variational principle over a measure on operators, rather than one being built first and the other added downstream. CFS has no dynamics of its own and is not imported as an ontology — it is imported narrowly, as evidence that a **simultaneous** (rather than sequential) architecture is mathematically achievable, licensing the two-column structure in §6 as more than wishful diagramming.

---

## 6. The Core Architecture — Revised

### 6.1 The old diagram, retained as one branch

$$
(X,F) \xrightarrow{\mathcal C_s} (\mathcal M(X),\Gamma_s,\mu_s) \xrightarrow{\Phi,\mathfrak R_s} \Gamma_*,\mu_* \xrightarrow{\Pi} \psi,\rho,S,v \xrightarrow{\text{recovery}} \text{QFT+GR}
$$

Not deleted. Demoted to **Branch H1 (arithmetic-native)**: the hypothesis that arithmetic generates the continuum outright. Every gate in this branch inherits its full v6.3.1 status, including every SPECTATOR/IMPORTED finding on record. H1 is not ruled out in principle — it is currently unsupported after the most thorough search this program has run.

### 6.2 The revised diagram — two columns, one coupling

$$
\underbrace{(X_p,F_p)}_{\text{arithmetic}} \xrightarrow{\ \mathcal C_s^{(p)}\ } (\mu_p,\ \chi_p\text{-register})
\qquad\qquad
\underbrace{(X_\infty,F_\infty)}_{\text{continuum}} \xrightarrow{\ \mathcal C_s^{(\infty)}\ } (\mu_\infty,\ \psi=Re^{iS/\kappa})
$$

$$
\Big(\mu_p,\ \chi_p\text{-register}\Big)
\quad\xleftrightarrow{\ \ \mathcal K\ \ }\quad
\Big(\mu_\infty,\ \psi\Big)
\longrightarrow \text{joint observable content} \longrightarrow \text{QFT+GR}
$$

This is **Branch H2/H3 (arithmetic-constrained / hybrid-coupled)**: the two sectors are constructed independently, each against its own gates, and \(\mathcal K\) is tested separately as a load-bearing physical constraint. **v7 does not choose between H1, H2, and H3.** It requires every future construction to be explicitly typed as targeting one of the three, and requires the null-model roster (§21, §Phase 0) to include a comparison capable of distinguishing them — not a table that ranks them by author preference.

### 6.3 What is required of \(X_\infty\) (new obligation)

v6.3.1 never separately specified a continuum-sector construction, because the continuum was always the *output*, not an independently-typed input. v7 requires \(X_\infty\) to be specified with the same discipline G1 already demands of \(X_p\): explicit configuration space, explicit dynamics, explicit measure candidate — **before** any coupling claim is evaluated. This is new debt, not inherited debt: `needMap` for \(X_\infty\) is currently open and has no v6.3.1 precedent to draw on.

---

## 7. Bohmian Mechanics — Unchanged

Sections 7.1–7.7 of v6.3.1 carry forward without revision: BM supplies the IR target (definite configurations, a dynamical state capable of interference, a guidance structure), not a microscopic axiom; continuous configuration space, Schrödinger evolution, the Born distribution, the guidance law, the quantum potential, fixed particle number, and Markovianity remain demoted regime statements, each requiring derivation; the generalized Langevin equation is required before the Kramers limit is assumed; asymptotic Bohmianity, Bell-type QFT as the relativistic benchmark, and the open foliation question are unchanged. One reframing, not a content change: BM's guidance-law target (§12) is now understood as potentially attaching to \(X_\infty\) natively (§15.5) rather than only arriving via a derivation from \(X_p\) — this does not relax any requirement; it adds a second candidate route to the same target, subject to the same gates.

---

## 8. First-Principles Re-Foundation of Invariant Set Theory — Unchanged in Content, Reframed in Role

Sections 8.1–8.7 of v6.3.1 (information capacity \(L\), the canonical-height route, the Markov-partition route, the joint-satisfiability gate, prime universality, fractality relocated to observables) carry forward without technical revision. **The reframing is architectural, not mathematical:** IST's re-foundation no longer supplies "the generator." It supplies the specification of \(X_p\) — the arithmetic column in §6.2 — in full. Every requirement in §8.1–8.7 remains binding on \(X_p\) exactly as before; none of this work is wasted by the architectural revision, because a well-specified arithmetic column is a prerequisite for §6.2 regardless of which branch (H1/H2/H3) eventually survives.

---

## 9. The Amplitude Problem — Unchanged, With Two Corrections on Record

Sections 9.1–9.3 (the Reginatto/Hall-Reginatto prior art, the native \(p\)-adic character route \(\chi_p\), the chaos-tameness/tame-factor T1–T4 ladder) carry forward. Two corrections, both already adjudicated outside this document and recorded here for the ledger:

- **G3 status correction:** an earlier standalone adjudication of T1–T4 against the frozen \(p=2\) odometer-conjugate substrate returned a flat KILL verdict. On review, that verdict rested in part on a misattributed citation (a claim about Koopman-eigenfunction projective consistency was sourced to a paper on the generalized moment problem, unrelated to the dynamical system in question) and conflicted with standard Pontryagin duality for profinite groups, which guarantees the odometer's own characters *do* cohere projectively. The corrected, better-supported verdict — independently reached by a separate five-report consolidation — is **SPECTATOR, not KILL**: the native phase structure exists and is coherent; it fails ownership because a generic cyclic clock reproduces it identically. This is materially different from non-existence and is recorded as such.
- **Gaussian/Hermite finding:** the archimedean Tate integral \(f_\infty(x)=e^{-\pi x^2}\mapsto \pi^{-s/2}\Gamma(s/2)\) connects to the quantum harmonic oscillator's ground state and Hermite eigenbasis. This connection lives entirely at the archimedean place — stripping every \(p\)-adic factor leaves it fully intact. By the program's own standard, it is **SPECTATOR** relative to any arithmetic-ownership claim, however aesthetically suggestive. Recorded to prevent rediscovery-and-overclaim.

---

## 10. The Projection Problem — Unchanged

P0 (state emergence), P1 (measure emergence), P2 (dynamics emergence), P3 (amplitude-factor emergence) carry forward as stated in v6.3.1 §10, now understood as applying to **each column separately** under H2/H3, or to the single chain under H1.

---

## 11. Born Probability — Unchanged

B0 (equilibrium measure), B1 (regularity), B2 (Born identification at the IR observable algebra, with the projection-scale resolution of the Born-exact/fine-texture tension), the setting-indexed no-signaling constraint, B3 (Valentini relaxation as path, not destination), and the typicality benchmark all carry forward unrevised from v6.3.1 §11.

---

## 12. Linearity, Guidance, and the Quantum Potential — One New Conditional Route

§12.1–12.4 of v6.3.1 (polar decomposition, the Schrödinger generator target, the guidance target, the quantum-potential target and its three candidate derivation routes) carry forward unrevised. **New conditional fourth route, gated behind §15:** if \(X_\infty\) is independently specified and found to natively support Schrödinger-class dynamics (as the SPECTATOR Gaussian/Hermite finding in §9 hints at but does not establish), the quantum potential's origin question changes shape — from "derive \(Q\) from an arithmetic construction" to "determine whether the arithmetic coupling constrains or leaves untouched a \(Q\) that the continuum sector already has." This route is explicitly unpromoted and carries its own `needMap` debt; it does not substitute for routes 1–3.

---

## 13. The Tensor-Factorization / Conditional-Expectation Gate — Unchanged

Unrevised from v6.3.1 §13. Still mandatory; still does not assume microscopic Hilbert-space tensor factorization; a weaker algebraic conditional-expectation structure remains acceptable if it produces the same operational trace.

---

## 14. Asymptotic Safety as Discipline, Not Dogma — Unchanged

§14.1–14.8 of v6.3.1 (retained AS machinery, the candidate dFRG, scheme independence, fixed-point/relevant-direction analysis, spectral-dimension testing, the local-scale debt item, the AS redundancy test) carry forward unrevised. AS's role as a coarse-graining/universality discipline applies to *either* column in §6.2 independently — nothing about the dual-column revision changes what AS is asked to do; it changes how many objects it may need to be applied to.

---

## 15. The Adelic/Siblings Architecture — New Chapter

### 15.1 The precedent, stated precisely

Tate's 1950 thesis constructs, for a completely different original purpose (the analytic continuation and functional equation of Hecke L-functions), the exact structure §6.2 needs: the adele ring \(\mathbb A_{\mathbb Q}=\mathbb R\times{\prod_p}'\mathbb Q_p\), with \(\mathbb Q\) embedded diagonally as a discrete, cocompact subgroup, tied together not by one completion generating another but by the **product formula**

$$
\prod_v |x|_v = 1 \qquad \text{for all } x\in\mathbb Q^\times.
$$

The construction is genuinely a product of independent local computations — a global character \(\psi=\prod_v\psi_v\), a global zeta integral \(Z(f,\chi,s)=\prod_v Z_v(f_v,\chi_v,s)\) — with the finite-place data constraining which global objects are admissible (which Euler products continue meromorphically and satisfy the functional equation) without generating the archimedean analytic content, which arises from ordinary continuum analysis alone.

### 15.2 The physical dictionary — explicitly a candidate, not a result

$$
\chi_p \leftrightarrow \text{the phase register (}\S9\text{, the established tame factor)}, \qquad
Z_\infty \leftrightarrow \text{the continuum/Schrödinger sector (}X_\infty\text{)}, \qquad
\textstyle\prod_v|x|_v=1 \leftrightarrow \mathcal K.
$$

This dictionary is tagged `[SPECULATIVE-SHAPE]`. It is precise rather than evocative, which is exactly why it must not be granted more credit than an evocative analogy until it clears the null test below.

### 15.3 H3-ADELIC-1 — the formal claim

> The arithmetic phase register and the continuum amplitude sector are linked by a global consistency constraint structurally analogous to the adelic product formula; this constraint has physical consequences not reproducible by either sector alone.

Status: `needToyCheck`, `needNullModel`. Not promoted.

### 15.4 The decoupled null (new addition to the null-model roster)

Every prior null test in this program asked whether arithmetic is *specific* (vs. a generic clock) or *necessary* (vs. arithmetic-stripped). Neither test evaluates §6.2's actual new content: the coupling itself. The required test is:

$$
\text{decoupled null: both } X_p \text{ and } X_\infty \text{ present, } \mathcal K \text{ not imposed.}
$$

If every physical prediction credited to H3-ADELIC-1 survives unchanged with \(\mathcal K\) removed, the coupling is SPECTATOR regardless of how mathematically elegant the dictionary in §15.2 is. This is the specific, cheap, decisive test required before any further construction on this branch. It is added to the Phase 0 null-model freeze (§21) retroactively and must be pre-registered before it is run.

### 15.5 The one candidate discriminator identified so far

The product formula requires an *infinite, mutually consistent family* of local factors tied together by unique factorization — a structural requirement a single generic local clock cannot satisfy on its own, regardless of how it fares against the single-place SPECTATOR null already on record (§9). If the physical analogue of this global consistency condition imposes a measurable constraint that fails under the decoupled null (§15.4) but holds under the coupled construction, that is the first genuine H2/H3 discriminator this program has produced. It is currently unverified and is the highest-priority target for R0-style empirical/mathematical audit (§21, Phase 0).

### 15.6 Kaluza–Klein — imported as a warning, not a technique

KK theory is the historical precedent for exactly this architectural move: two sectors, geometrically siblings, unified through one joint metric. It is kinematically elegant and has a well-documented, unresolved dynamical failure mode — nothing in the kinematic unification fixes the *relative scale* between the sectors (the radion problem), and higher-dimensional reductions carry their own chirality obstructions, structurally analogous to the E8 chirality failure already on record (§18). §6.2's coupling object \(\mathcal K\) has a direct analogue of this open question: **what physically sets the coupling strength between \(X_p\) and \(X_\infty\)?** This is logged as standing debt, not answered by the elegance of §15.1–15.3.

### 15.7 Self-audit, applied to this section's own strongest claim

The Gaussian/Hermite connection (§9) is the most seductive fact adjacent to this architecture. It is explicitly recorded as SPECTATOR, not as evidence for H3-ADELIC-1 — it lives entirely at the archimedean place and survives the removal of every \(p\)-adic factor. This section is graded by the same rule it proposes for everything else: fitting the historical SPECTATOR/IMPORTED pattern unusually well is a reason for *increased* scrutiny of §15.4, not decreased scrutiny.

---

## 16. Composition, Entanglement, and Bell — One New Candidate Mechanism

§16.1–16.4 of v6.3.1 (Gate C, entanglement generation, the Bell audit, the double-counting audit) carry forward unrevised as the H1-branch requirement. **New candidate under H2/H3:** entanglement may arise *between* the two columns — arithmetic-register correlation with continuum dispersion — rather than only from factoring one monolithic Hilbert space into visible subsystems. This is currently unexamined, carries full `needMap`/`needToyCheck` debt, and does not replace §16.1–16.4; it is logged as a second candidate mechanism subject to the same double-counting audit once both are specified.

---

## 17. QFT and Gravity Recovery — G10 Conditionally Reframed

§17's recovery ladder (QFT-R0 through R5, GR-R0 through R2, the mandatory no-go theorem audit against Haag, Coleman–Mandula, Weinberg–Witten) carries forward as the H1-branch requirement in full — nothing here is weakened. **Conditional simplification under H2/H3:** if \(X_\infty\) is independently specified and already carries native Lorentz/relativistic structure (a real possibility for a genuinely continuum sector, not yet established), QFT-R1 changes character — from "derive Lorentz invariance from a discrete substrate," the single longest-horizon item on the entire roadmap, to "determine whether the arithmetic coupling \(\mathcal K\) breaks or respects an already-present Lorentz symmetry." This is a compatibility check, not an emergence proof, and it is **imported explicitly and narrowly** from the Hořava–Lifshitz literature: HL's extensive, already-published catalogue of which UV-preferred-structure operators survive to the IR without breaking Lorentz invariance, and which don't, is directly reusable for auditing \(\mathcal K\)'s conductor/ramification-type data against Lorentz symmetry, rather than re-deriving that analysis from nothing. This route is unpromoted and contingent entirely on \(X_\infty\)'s specification (§6.3) — it does not reduce QFT-R1's difficulty under H1.

---

## 18. E8 — Unchanged

§18 of v6.3.1 carries forward without revision: "248 particles in nature," naive Lie-algebra embedding, and the claim that ordinary E8-lattice-CFT representation theory resolves chirality remain permanently rejected. E8's surviving role (optimal information packing, error correction, modular structure, a held-out spectral fingerprint) remains conditional on an independently-derived dimension and code-selection criterion, never the reverse.

---

## 19. Cross-Substrate and Prime Universality — Unchanged

§19 of v6.3.1 carries forward unrevised, now understood as applying specifically to \(X_p\)'s construction within §6.2's arithmetic column.

---

## 20. Empirical Program: Shape Before Amplitude — Unchanged, One Addition

§20's T1–T3 (constraint compilation, derived-shape tests, high-information fingerprints) carry forward unrevised. Addition: any future derived shape must specify which branch (H1 direct generation, H2 constraint, H3 coupling) it is a prediction *of*, since the three branches are not guaranteed to predict the same functional form even when they agree qualitatively that "something quantized" should appear.

---

## 21. Research Program — Phases, With the Reality-First Insertion Point

Phases 0–8 of v6.3.1 §21 carry forward unrevised as the operational spine, with two additions:

- **Phase 0** now includes the decoupled null (§15.4) in its frozen null-model roster, alongside standard BM typicality, BM+Valentini without the arithmetic layer, the non-arithmetic discrete substrate, and the plain-AS control.
- A cross-cutting **R0 (Reality Constraint Freeze)** discipline sits alongside, not inside, the phase sequence: before any new microscopic candidate, any adoption of external architecture (Palmer or otherwise), or any newly-invented H3 mechanism is authorized, compile existing empirical constraints and build the H1/H2/H3 discriminator matrix first. R0 does not replace G0–G10; it selects which gate is worth spending months on next. Cheap falsifiers before expensive derivations remains the governing rule, now stated as applying to *architecture choice* as well as to individual construction attempts.

---

## 22. The Program's Hardest Gates — Revised Master List

### G0 — Discrete/continuous consistency
Unchanged prohibition (§5.1), extended with the positive construction requirement (§5.2, G0-EXT-1).

### G1 — Explicit microscopic map (arithmetic column)
Unchanged: no vague "shift" or "symbolic dynamics" without a defined \(F_p\).

### G1b — Explicit continuum-sector specification (new)
No coupling claim (§15) may be evaluated before \(X_\infty\), its dynamics \(F_\infty\), and its measure candidate are stated with the same explicitness G1 requires of \(X_p\).

### G2 — Joint arithmetic compatibility
Unchanged: canonical height and symbolic/Markov machinery must actually apply to the same \(F_p\), or one is removed.

### G3 — Amplitude-factor existence
Unchanged target; status corrected to SPECTATOR, not KILL (§9).

### G4 — Measure
$$\exists!\,\mu_p \text{ and } \exists!\,\mu_\infty,$$ each with regularity sufficient for its own sector, under H2/H3; the single \(\exists!\mu_*\) target is retained under H1.

### G5 — Projection
Construct \(\Pi\) explicitly; under H2/H3, \(\Pi\) may act on the coupled pair rather than on \(X_p\) alone.

### G6 — Born
$$\Pi_{\rm IR\#}\mu_*=|\psi|^2dx$$ under H1; under H2/H3, the analogous target is that the *coupled* system's IR projection reproduces \(|\psi|^2\), with the decoupled null (§15.4) required to fail this identification for the claim to carry any ownership content.

### G7 — Dynamics
$$\mathcal L_s\to\mathcal L_{\rm Schr/BM}$$ under H1 (full derivation); under H2/H3, the target is a demonstrated *constraint relation* between \(\mathcal K\) and an independently-specified \(\mathcal L_{\rm Schr/BM}\) native to \(X_\infty\) — a weaker, differently-shaped claim, not a free pass.

### G8 — Guidance and \(Q\)
Unchanged targets; three original derivation routes retained, fourth conditional route added (§12).

### G9 — Composition
Entanglement and Bell, unchanged under H1; cross-sector entanglement (§16) added as an unexamined H2/H3 candidate.

### G10 — Recovery
QFT + Lorentz + gauge + GR, unchanged under H1 (full emergence); conditionally reframed to a compatibility check under H2/H3, contingent on \(X_\infty\)'s native relativistic content (§17).

No later gate can compensate for a failed earlier load-bearing gate. This rule is unchanged and applies within each branch independently.

---

## 23. Symmetric Adjudication of External Ideas — Unchanged

§23's retain-in-core / retain-in-workbench / reject criteria carry forward unrevised and were applied, without exception, to every import in this document: NCG spectral triples and Causal Fermion Systems are retained in core (§5.2–5.3) because each converts a vague claim into a typed construction or established precedent; the Hořava–Lifshitz import (§17) is retained in workbench, contingent on \(X_\infty\)'s specification; the adelic/Tate architecture (§15) is retained in core as a formal hypothesis precisely because it is falsifiable via §15.4, not because it is elegant; Kaluza–Klein is imported explicitly as a documented failure mode, not a technique.

---

## 24. Symmetric Occam Guillotine — One New Kill Condition

D20–D24 of v6.3.1 §24 (arithmetic, AS, BM, E8, and EBP redundancy) carry forward unrevised.

### D25 — Coupling redundancy (new)

If the decoupled null (§15.4) reproduces every prediction currently credited to \(\mathcal K\), the coupling object is removed from the core architecture and the program reverts to evaluating H1 and H2 without a hybrid layer. No component — including the central architectural revision this document makes — receives immunity from Occam.

---

## 25. Subtraction Record: v6.3.1 → v7 Prior History (Compressed)

The v6.2 → v6.3.1 subtraction record (restorations, reinstated debt, explicit rejections) is preserved in full in v6.3.1 §25 and is not restated here; nothing in it is reversed by v7. See Appendix B for the complete, current v6.3.1 → v7 accounting.

---

## 26. Live Claims Ledger — Revised

| Claim | Status | Immediate dependency |
|---|---|---|
| Arithmetic substrate exists (\(X_p\)) | INCUMBENT HYPOTHESIS | Explicit \(F_{p,L}\) |
| Continuum sector exists (\(X_\infty\)) | **NEW / OPEN** | Explicit \(F_\infty\), measure candidate |
| Candidate microscopic map \(F_p\) | OPEN | Phase 1 |
| Canonical-height mechanism | TARGET | \(F_p\) algebraic/self-map |
| Markov-partition mechanism | TARGET | dynamical hypotheses |
| Prime universality | TARGET | family of \(F_{p}\) or equivalent |
| Native complex phase via \(\chi_p\) | **SPECTATOR (corrected from KILL)** | generic-clock null already run |
| Tame/Kronecker factor exists | SPECTATOR, confirmed | Koopman/transfer analysis |
| Gaussian/Hermite archimedean connection | **SPECTATOR, recorded** | survives \(p\)-adic stripping |
| H3-ADELIC-1 (product-formula-type coupling) | **NEW / needToyCheck, needNullModel** | Decoupled null (§15.4) |
| Decoupled null result | **NEW / OPEN, highest priority** | Pre-registration |
| \(\Phi_s=\mathcal A_s\circ\mathcal C_s\) prototype | TARGET | observable reconstruction + RG commutation |
| No-signaling for settings family | GATE | marginal-independence test |
| Unique physical measure(s) | TARGET | ergodicity/mixing, per column |
| Born projection | TARGET | \(\Pi_{\rm IR}\), branch-dependent |
| dFRG exists | TARGET | coarse-graining construction |
| Fixed point exists | TARGET | dFRG |
| Continuum configuration space (H1) | TARGET | P0 |
| Continuum configuration space (H2/H3) | **NEW / independently specified, not derived** | G1b |
| Schrödinger generator emerges (H1) | TARGET | amplitude + generator |
| Schrödinger generator native (H2/H3) | **NEW / conditional** | \(X_\infty\) specification |
| Guidance emerges | TARGET | phase/generator, either branch |
| Quantum potential emerges | TARGET | three original routes + one conditional route |
| Composition emerges (intra-sector) | TARGET | two-subsystem construction |
| Composition emerges (cross-sector) | **NEW / unexamined** | §16 |
| Bell reproduced | TARGET | composition + guidance |
| Lorentz/QFT recovery (H1) | DOWNSTREAM TARGET | Phase 7 |
| Lorentz/QFT compatibility (H2/H3) | **NEW / conditional, cheaper** | \(X_\infty\) native content + HL toolkit |
| GR recovery | DOWNSTREAM TARGET | Phase 7 |
| E8 physical role | OPTIONAL WORKBENCH | independent dimension/code selection |
| Arithmetic unique necessity | NOT CLAIMED | Occam gate |
| Coupling unique necessity | **NOT CLAIMED, NEW** | D25 |

---

## 27. Hard Failure Conditions — Two Additions

Items 1–21 of v6.3.1 §27 carry forward unrevised and apply, as written, within Branch H1.

**22.** The decoupled null (§15.4) reproduces every prediction credited to \(\mathcal K\), with no residual distinguishing consequence.

**23.** \(X_\infty\) cannot be specified with the same explicitness G1 requires of \(X_p\) (i.e., G1b fails outright) — in this case H2/H3 collapse entirely and only H1 remains open.

The rule is unchanged: find out exactly where it breaks.

---

## 28. The First 90 Days — Revised

Days 1–30 of v6.3.1 §28 (frozen \(F_L\), Deliverables A–F) carry forward as the H1/G1 track, unchanged. Two items are added to run in parallel, not in sequence, because they are cheap relative to the existing 90-day plan:

- **G1b start:** specify a minimal candidate \(X_\infty\) (e.g., a single continuum degree of freedom with an independently posited Schrödinger-class dynamics) explicitly enough to be a legitimate decoupled-null partner.
- **Decoupled-null pre-registration:** freeze, in writing, exactly what \(\mathcal K\)'s removal is predicted to change, before any coupling construction is attempted — this is the single cheapest test this document adds and should not wait for Days 31–90.

Days 31–90 proceed as in v6.3.1 §28, contingent on the same survival conditions.

---

## 29. Expected Shape of a Successful Theory — Unchanged

§29 of v6.3.1 carries forward unrevised. One clarification: "small deterministic discrete/arithmetic dynamics" at the microscopic level (the first boxed target) is now understood as describing \(X_p\) specifically, not necessarily the entire microscopic content of the theory — under H2/H3, an independently minimal \(X_\infty\) is an equally load-bearing part of the desired compression, and its absence from the original diagram was itself part of what made the old architecture look simpler than the actual claim it was making.

---

## 30. The Elephant and the End State — Unchanged, Extended Question

§30's governing question is extended to match §2:

> **What remains if BM, IST, AS, E8, the coupling hypothesis itself, and this research program are all allowed to be wrong?**

The final doctrine is unchanged: construct before interpretation; type before identification; pre-register before comparison; separate equilibrium destination from relaxation path; compare null models symmetrically — now explicitly including the decoupled null — and let failure remove structure rather than add it.

---

## Appendix A — Reference Anchors, Extended

All anchors from v6.3.1 Appendix A carry forward unchanged. New anchors added in v7:

- J. Tate, *Fourier analysis in number fields and Hecke's zeta-functions*, PhD thesis, Princeton (1950) — the adelic/product-formula precedent for §6.2 and §15; now load-bearing, not a general background citation.
- A. Connes and A. H. Chamseddine, *Universal formula for noncommutative geometry actions: unification of gravity and the standard model*, Phys. Rev. Lett. 77, 4868 (1996), and subsequent spectral-action work — the positive-construction template for G0-EXT-1.
- F. Finster, *The Continuum Limit of Causal Fermion Systems*, Springer (2016), and related papers — the simultaneous-emergence precedent for §5.3.
- P. Hořava, *Quantum Gravity at a Lifshitz Point*, Phys. Rev. D 79, 084008 (2009), and the subsequent Lorentz-recovery/operator-survival literature — the compatibility-audit toolkit for the reframed G10 (§17).
- T. Kaluza (1921) and O. Klein (1926), and the subsequent radion-problem literature — imported as a documented cautionary precedent, not a technique, for §15.6.

These remain methodological anchors, not endorsements of the tripartite program.

---

## Appendix B — What v7 Corrects Relative to v6.3.1

This is the authoritative dismantling record the version bump exists to document.

**Architectural core (the primary revision):**
- retires the one-way pipeline \((X,F)\to\cdots\to\text{QFT+GR}\) as an assumption; demotes it to Branch H1;
- introduces the two-column architecture (§6.2) with an independently-typed continuum sector \(X_\infty\) and an explicit coupling object \(\mathcal K\);
- introduces H1 (arithmetic-native) / H2 (arithmetic-constrained) / H3 (hybrid-coupled) as competing, non-ranked architectural hypotheses to be discriminated by evidence, not adopted by preference.

**New gates and requirements:**
- adds G1b — explicit continuum-sector specification, with the same rigor G1 already required of the arithmetic sector;
- adds G0-EXT-1 — a positive construction requirement for G0, closing the gap between "what is forbidden" and "what a legitimate cross-type relationship looks like";
- reframes G4, G6, G7, G9, G10 to state both their unrevised H1-branch form and their new, differently-shaped H2/H3-branch form, rather than assuming only one shape of claim is possible;
- adds the decoupled null (§15.4) to the Phase 0 null-model roster, and D25 (coupling redundancy) to the symmetric Occam guillotine.

**New imports, each entered narrowly and against a specific gap, per §23's existing adjudication rule:**
- Tate's adelic construction, as the literal mathematical precedent for §6.2, not an analogy;
- Connes–Chamseddine noncommutative geometry, as the positive-construction template for G0;
- Causal Fermion Systems, as the simultaneous-emergence precedent licensing a two-column (rather than sequential) architecture;
- Hořava–Lifshitz gravity's operator-survival literature, as a reusable compatibility-audit toolkit for a conditionally reframed G10;
- Kaluza–Klein theory, imported explicitly as a documented failure mode (the radion/scale problem) rather than a technique, flagged against \(\mathcal K\)'s own unresolved coupling-strength question.

**Status corrections, entered onto the ledger rather than silently fixed:**
- G3's verdict corrected from KILL to SPECTATOR, with the specific misattributed citation and the Pontryagin-duality argument for the correction recorded;
- the Gaussian/Hermite archimedean connection recorded explicitly as SPECTATOR, to prevent future rediscovery-and-overclaim.

**Explicitly not touched:**
- the EBP v2.1 constitution;
- BM's targets (§7), IST's re-foundation content (§8), and AS's discipline (§14) — all carry forward as specifications of the individual columns, not as claims about how the columns relate;
- every v6.2 → v6.3.1 correction on record (§25 of v6.3.1), none of which is reversed.

**What v7 explicitly does not claim:**
- that H2 or H3 is correct;
- that the decoupled null has been run;
- that \(X_\infty\) has been specified;
- that the coupling object \(\mathcal K\) has any demonstrated physical consequence.

Every one of those remains open debt, tracked in §26.

---

## Final Statement

v6.3.1 closed with one missing chain:

$$
F \;\longrightarrow\; \mu_* \;\longrightarrow\; \Pi \;\longrightarrow\; \psi \;\longrightarrow\; \text{QM/BM}.
$$

v7 does not complete that chain — it explains, with a specific and falsifiable hypothesis, why every attempt to complete it produced the same SPECTATOR/IMPORTED signature, and replaces it with two shorter, independently-testable obligations:

$$
F_p \;\longrightarrow\; (\mu_p,\chi_p)
\qquad\text{and}\qquad
F_\infty \;\longrightarrow\; (\mu_\infty,\psi),
\qquad\text{linked by}\qquad
\mathcal K,
$$

with the explicit requirement that \(\mathcal K\)'s physical content survive the decoupled null. If it does not, D25 removes it, and the program returns to evaluating H1 and H2 on their own — a smaller, cleaner outcome than the one this document opened with, exactly as §29 says a converging theory should look. If it does survive, the tripartite synthesis gains something it has never had: a coupling mechanism with an actual discriminating test behind it, rather than an architecture diagram that was elegant because no one had yet tried to falsify its arrows.

Construct \(X_\infty\). Run the decoupled null. Either result is progress. That remains the purpose of the Elephant Bridge Protocol.
