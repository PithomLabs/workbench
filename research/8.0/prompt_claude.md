## The core problem, stated once before the fix

Section 2 of v7.2.1 already lists everything wrong with v6.3.1's "arithmetic must generate the continuum" bias. But look at what actually got *built* since that diagnosis: sections 4A, 5, 5A, 5B, 5C, 9, most of 24, and Appendices C, D, E, F, G, H are almost entirely Tate/adelic scaffolding — benchmarks, operator ladders, Green-function precedents, a frozen minimal-bridge test protocol. The document correctly *says* arithmetic is a constraint, not a generator (Section 6), and correctly demotes IST's ontology — but it never applied the same demotion to its own newest, largest investment. The Reality-First checklist you've built independently confirms, in exhaustive and specific detail, that this investment was premature: arithmetic's *only* confirmed native role, across fifteen branches of mathematics tested against real physics, is as the descriptive language for a narrow class of already-existing invariants. Not a generator. Not a stage-builder. Not even, per arithmetic.md's own dividing line, most integer-valued quantities in physics — those belong to topology or symmetry instead.

So the revision isn't "add a Reality-First gate to the existing architecture." It's: stop building the Tate apparatus forward until something in the program actually needs it, and reorganize around the four components you named, using the checklist's own verdicts as the assignment rule rather than inventing a new one.

### 1. The four components, reassigned per the checklist's own findings

| Component | What it is | Native mathematics (per checklist) | Explicitly dead or silent here |
|---|---|---|---|
| **Dancer** (matter/energy) | BM's actual configuration, particle content, states | Algebra (representation theory of states) is native; arithmetic is native *only* for the spectral fingerprint of already-built operators (Level 2+ algebraic eigenvalues) | Arithmetic does not select gauge group or particle content, generations, or Yukawa couplings — "menu of representations, not the chef" |
| **Dance** (mechanism) | The actual generator of time evolution — Schrödinger equation, guidance law | **Calculus, and only calculus** — the checklist is explicit that of all fifteen branches surveyed, calculus is "the engine the other three refused to be... the only structure in the series whose constitutional function is generation" | Arithmetic, algebra, topology, geometry, symmetry — all explicitly SILENT on dynamics. Not contested, not partial. Silent. |
| **Stage** (spacetime) | Geometry, causal structure | Geometry, with topology for defect/phase classification; AS is the RG-scale diagnostic sitting on top of geometry | Arithmetic explicitly does NOT determine dimensionality, topology, or metric signature — "the adele class space is totally disconnected (the opposite of spacetime)" |
| **Mathematics** (the language layer) | Not a fourth substance — the cross-cutting question of which language natively describes which of the other three | Fifteen candidate languages, each already scored against physics by your own checklist | The mistake the whole program made was treating this as "which one language is the substrate" instead of "which language is native to which joint" |

This table *is* the reorganization. Everything downstream follows from taking it seriously.

### 2. The Occam-minimal null model, stated as what it actually is

Not a strawman to be beaten for rhetorical effect — the current best candidate theory, full stop, until something outperforms it:

$$\text{BM (calculus: Schrödinger + guidance law)} \;+\; \text{AS (RG flow on geometry)} \;+\; \text{no arithmetic substrate at all}$$

Per your own checklist, this pairing already covers everything a physical theory needs from "dance" and "stage" — an actual engine (calculus) and an actual stage-builder-with-scale-diagnostics (geometry + AS). Arithmetic was never shown to add anything to *either* role. The honest question the whole program has been dancing around finally has a name: **does BM+AS, run on its own, ever produce something arithmetic is the only language that can describe?** If it never does, the program is just BM+AS, and that's not a failure — it's the Occam-correct outcome your own nine-plus rounds of testing keep pointing at.

### 3. What gets demoted, and the specific checklist verdict doing the demoting

| Section | Current status | Demoted to | Checklist verdict that forces this |
|---|---|---|---|
| 4A (BM–Tate interface, A1–A3) | Foundation gate, near top of document | Reserve Library — dormant until trigger (§4 below) fires | "Arithmetic does NOT drive local dynamics... DEAD" |
| 5, 5A, 5B, 5C (Adelic Principle, Freund–Witten, Vladimirov operators, Tate curve) | Load-bearing benchmarks | Reserve Library | "Arithmetic does NOT regularize UV divergences better than standard methods... Occam's Razor cuts the adelic regulator. The math is elegant; the physics is unnecessary." |
| 9 (Arithmetic Phase Register) | Active reclassified gate | Reserve Library, re-opened only for the specific invariant-matching use case in §4 | "Measurement basis... UNRESOLVED — the program's sharpest remaining theoretical gap" — an unresolved foundational problem is not load-bearing scaffolding |
| F1 (Local-to-Global/Adelic Consistency) in the F0–F11 gate list | Early gate | Moved to conditional status, gated behind the trigger | Same as above — this gate currently has no confirmed target to be consistent *about* |
| Appendices C, D, E, F, G, H | Active protocol/test records | Reserve Library, frozen as-is (nothing here is wrong, it's just premature) | The checklist's own standing rule, stated in nearly every file: "It is silent when physics asks..." — dynamics, spacetime, Born rule, gauge content are the actual open problems, and none of this apparatus touches them |
| The operational diagram at line 164 ("Tate/local-global structure → candidate bridge → BM-compatible physical sector → ...") | Governs the whole program's read order | Replaced (§5 below) | Starting the diagram with Tate is the exact bias Section 2 already diagnosed and never actually fixed |

Nothing here is deleted — EBP's own constitution (ideas enter free) says it shouldn't be. It's relabeled from "under active construction" to "reserved," which is an honest description of what it actually is right now.

### 4. The arithmetic re-entry condition — the concrete, checkable form of "not until necessary"

Lifted directly from arithmetic.md's own dividing line, not invented new:

> Arithmetic re-enters the active architecture only when BM+AS's own construction (run with zero arithmetic assumed) produces an invariant — a spectrum, a partition function, a symmetry classification — whose **values are algebraic numbers with Galois structure** (Level 2 or higher on the checklist's own spectral ladder), not merely integer-valued from topology or from an ordinary symmetry group. Integer-valued is not sufficient. Modular-form-valued, root-of-unity-valued, or Galois-orbit-valued is the actual bar.

Concretely, three checkable questions, asked of whatever BM+AS actually produces:
1. Is the quantity discrete because of topology (winding, Chern number) or symmetry (SU(2) quantization)? → **stays with topology/symmetry, arithmetic does not re-enter.**
2. Is the quantity a generic real number, continuously varying? → **arithmetic is inapplicable, full stop.**
3. Does the quantity's value require an algebraic number field, a modular form, or a Galois action to state precisely? → **only here does the Reserve Library open**, and only the specific piece matching that invariant (e.g., if a modular partition function shows up, Bost–Connes-type material is the right reserve item to promote — not the whole adelic apparatus at once).

### 5. The corrected operational diagram

Replacing the Tate-first diagram at line 164:

$$
\text{BM configuration + guidance (calculus)} \;\longrightarrow\; \text{AS/RG closure on geometry (stage)} \;\longrightarrow\; \text{invariant check (§4 above)} \xrightarrow{\text{Level 2+ only}} \text{targeted Reserve-Library entry}
$$

Arithmetic is now a *conditional branch at the end*, not the opening premise. This single change is the actual reorganization; everything else in this delta just works out its consequences.

### 6. What was already correct and should be promoted, not demoted

Section 6 ("Arithmetic: Constraint, Not Generator"), Section 18 (Ownership Taxonomy, which already has a SPECTATOR category doing real work), and Section 32B (the Top-Down Reality/Physics Constraint Track) were already Reality-First-compliant before this checklist existed — they just weren't given priority over the Tate-building work happening in parallel. Under this revision, 32B becomes the *primary* driver of the roadmap, with the bottom-up BM+AS construction feeding it, rather than the two streams being treated as co-equal per the current "Bidirectional Convergence Architecture" (32A). Reality-First isn't one of two streams anymore. It's the gate everything else has to clear.

### 7. Occam's razor applied to the specific gates that were about to reach for arithmetic

- **G3 / amplitude gate:** before any Tate-based phase register, ask whether ordinary Berry phase or geometric phase (already-established, calculus-and-geometry-native machinery) already supplies whatever phase structure BM needs. Per the checklist, Berry phase is explicitly cited as a case where "the phase sector of QM behaves like a register" without any arithmetic content — check that cheaper explanation first.
- **G9 / composition:** before reaching for adelic tensor structure, check whether ordinary Hilbert-space composition (algebra's native role, per the checklist) already suffices — it almost certainly does, since nothing in nine-plus rounds of testing found composition to be an arithmetic-owned phenomenon anywhere.
- **G10 / relativistic recovery:** the checklist is unambiguous that spacetime dimension, topology, and signature are geometry's domain exclusively — arithmetic re-entry here should be considered closed, not conditional, barring an extraordinary future finding.

### 8. Subtraction record entry this revision requires

Per Section 37's own convention: log that sections 4A/5/5A/5B/5C/9 and Appendices C–H are **demoted, not removed**, with this delta as the citation, so a future pass doesn't rebuild the same premature scaffolding without first checking whether §4's trigger has actually fired.

---

Want this written up as the actual `v7.3` document — replacing the operational diagram, formally demoting the listed sections into a labeled Reserve Library appendix, and adding the arithmetic re-entry condition as a new numbered gate — in the same file format and style as v7.2.1 itself?
