## Planck's Quanta under EBP v2.1

---

## Historical Backstory: Why the 19th Century Was Nervous

By 1890, classical physics looked finished. Newton's mechanics handled motion. Maxwell's electromagnetism handled light and fields. Thermodynamics handled heat. The mood among physicists was essentially: fill in the decimal places, we have the framework.

Two problems refused to cooperate.

**The blackbody problem.** Any hot object glows — iron heated in a forge goes red, then orange, then white. The question: what is the precise spectrum of that glow at a given temperature? Classical physics gave a formula (Rayleigh-Jeans) that worked at low frequencies but predicted that any hot object should emit *infinite energy* at high frequencies — the ultraviolet catastrophe. An infinite answer from a finite object is not a rounding error. It is a structural failure.

**The photoelectric effect.** Shine light on certain metals and electrons are ejected. Classical wave theory predicts: brighter light = more energetic electrons. Observed: brighter light = *more* electrons, same energy. Only higher *frequency* increases electron energy. Classical physics has no account for this whatsoever.

These were not engineering puzzles. They were cracks in the foundation.

---

## Planck 1900: The Door — An Unwilling Entry

Planck was a committed classicist. He did not want to break classical physics. He was tasked with fitting the blackbody spectrum experimentally measured by his colleagues in Berlin, and he found, through a mix of mathematical interpolation and desperation, that assuming energy is emitted in discrete chunks:

**E = nhν** (n = integer, h = new constant, ν = frequency)

reproduced the data perfectly across all frequencies.

He called it *"an act of desperation."* He explicitly did not believe it was physically real. He thought it was a mathematical fitting device that a better theory would eventually explain away.

**Under EBP: Planck enters the Door.** Owner: Planck. Claim: oscillator energies are quantized in units of hν. Planck himself would have *refused* to promote it as physics — he filed his own faithfulness objection at the moment of entry. This is EBP-correct behavior: the door is open, no promotion yet, and the author himself is the first to raise the debt.

---

## Planck on the Workbench: Debt Assessment

**needMap.** Domain = electromagnetic oscillator modes in cavity walls, codomain = energy distribution across frequencies, translation rule = E = nhν, Boltzmann-weighted sum over integer n. Map written explicitly. Planck distribution formula derived.

**needToyCheck.** Three finite tests:
- High-frequency limit: recovers Wien's law, which was known to work there.
- Low-frequency limit: recovers Rayleigh-Jeans, which was known to work there.
- Full intermediate regime: fits all Berlin experimental measurements precisely.

Both existing null models — Wien and Rayleigh-Jeans — are contained as limiting cases. needToyCheck retired.

**needNullModel.** The null models are explicit: Wien fails at low frequency, Rayleigh-Jeans fails catastrophically at high frequency (infinite energy). Planck beats both simultaneously on the same dataset. needNullModel retired.

**needInvariant.** What survives classical physics? In the limit hν << kT (low frequency, high temperature), Planck's formula collapses to Rayleigh-Jeans exactly — the classical regime is contained. The invariant: the classical limit is recovered where it should be. Partially retired — stated clearly enough to check, though the formal correspondence principle is not articulated until later.

**needObstruction.** Filed immediately and honestly: Maxwell's equations predict continuous energy exchange. Discrete quantization contradicts classical electromagnetism at the microscopic level. Planck has no mechanism for *why* energy is quantized. He states this, accepts the downgrade — "I describe the data; I do not explain the physics" — and parks the obstruction.

**needFaithfulnessReview.** Does "energy quantization of oscillators" faithfully describe what is physically happening? Planck's answer: **no** — he explicitly treats it as a calculational device. The faithfulness objection is raised by the author against his own claim. This blocks promotion. The formula is promoted. The physical interpretation is not.

**Ledger state after Planck:**
```
Idea: Energy quantization (E = nhν)
debt: [needObstruction (no mechanism), needFaithfulnessReview (physical reality contested)]
containsFinalTruthClaim: false
```
Promoted as a fitting formula. Not promoted as physics.

---

## Einstein 1905: New Idea at the Door — Quanta Are Real

Planck quantized the *oscillators* as a device. Einstein made a stronger claim: **light itself is quantized.** It travels in discrete packets — quanta — each carrying energy E = hν. These are not just a computational convenience. They are physical objects.

Historical note: this was considered the most radical of Einstein's 1905 papers — more radical than special relativity. Planck, on the Nobel committee, later wrote that Einstein's light quanta hypothesis was a step too far, evidence that "he may sometimes have missed the target." Einstein received the Nobel Prize in 1921 — for the photoelectric effect, not relativity.

**Door.** Owner: Einstein. Claim: light quanta are real; E = hν applies to the light field, not just oscillator walls. Full debt load.

**needMap.** Domain = incident light (frequency ν), codomain = ejected electron kinetic energy, translation rule = E_kinetic = hν - φ (where φ = work function of the metal, the energy cost to free an electron). Map explicit and testable.

**needToyCheck.** Millikan (1916) spends a decade trying to disprove Einstein's equation. Every measurement confirms it exactly — threshold frequency, kinetic energy scaling with ν, independence from intensity. needToyCheck retired against an adversarial experimenter. This is the strongest possible toy check outcome.

**needNullModel.** Classical wave theory predicts: electron energy scales with light *intensity*. No threshold frequency. Both predictions fail experimentally. Null model explicitly beaten.

**needObstruction.** Wave-particle duality filed immediately. Young's double-slit shows light produces interference — a wave phenomenon. How do discrete particles produce interference fringes? If light is particles, what interferes? Filed. Not retired. This obstruction will not be meaningfully addressed until the full quantum formalism.

**needFaithfulnessReview.** Does "discrete light quantum with energy hν" faithfully capture what travels from source to detector? Contested. What is the spatial extent of a photon? How does one photon know about both slits? The formalization is faithful to the photoelectric predictions. It is not faithful to a complete physical picture. Promotion holds for the photoelectric domain. Ontology is explicitly out of scope.

---

## Bohr 1913: Quantization Invades the Atom

**Historical context.** Rutherford (1911) showed the atom has a tiny dense nucleus with electrons orbiting it. Classical electromagnetism predicts orbiting electrons radiate continuously, losing energy and spiraling into the nucleus in roughly 10⁻¹¹ seconds. Observed: atoms are stable and emit only specific discrete spectral lines — hydrogen emits four visible frequencies, no more, no less.

Bohr's claim: electrons occupy quantized orbits with specific allowed energies. Transitions between levels emit or absorb photons with E = hν = ΔE. The allowed orbit condition: angular momentum is quantized in units of ℏ.

**Door.** Owner: Bohr. Claim: atomic orbits are quantized; spectral lines are transition energies. Full debt load.

**needMap.** Domain = electron transitions (initial and final quantum number n), codomain = emitted photon frequency, translation rule = ΔE = E_n₁ - E_n₂ = hν, where E_n = -13.6 eV/n². Map explicit.

**needToyCheck.** Rydberg formula for hydrogen — all known spectral lines predicted to high precision. Paschen series, Balmer series, Lyman series: all accounted for. needToyCheck retired for hydrogen.

**needNullModel.** Classical model predicts spiral collapse and continuous spectrum. Beaten on both counts.

**needObstruction.** Bohr files three honestly:
1. No physical mechanism for why these orbits are quantized — the quantization condition is imposed, not derived.
2. Model fails for helium — two electrons produce a multi-body problem the semi-classical framework cannot handle.
3. Model predicts spectral line positions, not intensities.

Consequence stated: Bohr's model is explicitly scoped to hydrogen-like atoms (one electron systems). Downgrade accepted. Not killed — scoped.

**needFaithfulnessReview.** Does "quantized circular orbit" faithfully capture electron behavior? Contested — electrons don't actually travel in circles; the orbital picture is a fiction that gives correct energies. Faithfulness gap noted. Promotion holds for spectral predictions; spatial picture is flagged as unfaithful.

---

## de Broglie 1924: Matter Has Waves

Einstein showed waves (light) have particle properties. de Broglie inverts: particles (matter) have wave properties. λ = h/p.

**Door.** Claim: any particle with momentum p has an associated wavelength λ = h/p. Symmetry argument — not a derivation from deeper principles.

**needMap.** Domain = particle momentum p, codomain = wavelength λ, translation rule = λ = h/p. Map explicit.

**needToyCheck.** Davisson and Germer (1927) fire electrons at a nickel crystal and observe diffraction rings — interference patterns. The measured wavelengths match de Broglie's formula exactly. needToyCheck retired by a result that was initially an accident (their crystal oxidized, was cleaned, and accidentally recrystallized into a diffraction grating).

**needObstruction.** What is waving? What physical medium carries the matter wave? Filed. No answer. This obstruction waits for Born's probability interpretation (1926).

---

## Heisenberg / Schrödinger 1925-26: Full Quantum Mechanics

Two independent frameworks arrive within one year:
- Heisenberg (with Born and Jordan): **matrix mechanics** — physical quantities are matrices, not numbers; position and momentum are non-commuting operators.
- Schrödinger: **wave mechanics** — a partial differential equation (the Schrödinger equation) governs the evolution of a wavefunction ψ.

They look completely different. Dirac and von Neumann prove they are the same theory in different mathematical languages — different representations of the same abstract Hilbert space structure.

**needInvariant across the two formulations.** What must be preserved under the map Heisenberg ↔ Schrödinger? Observable predictions — eigenvalue spectra of operators. Dirac proves the map is a unitary transformation on Hilbert space. Invariant stated precisely and proven. needInvariant retired.

**needMap (QM as a whole).** Domain = quantum state ψ (vector in Hilbert space), codomain = probability distribution over measurement outcomes, translation rule = Born rule: P(outcome) = |⟨outcome|ψ⟩|². Map explicit.

**needToyCheck.** Hydrogen spectrum recovered exactly from Schrödinger's equation — with correct line intensities now, which Bohr's model couldn't provide. Helium handled perturbatively. Molecular bonding explained. Solid-state band structure derived. The scope of successful toy checks is large enough that QM reaches Promoted status within a decade.

**needNullModel.** Classical mechanics is the null model. Correspondence principle (Bohr, formalized by Dirac): in the limit of large quantum numbers, QM predictions must converge to classical predictions. Verified across multiple domains.

---

## Open Debt on Promoted QM

**needObstruction — three items, all open:**

1. **Measurement problem.** QM predicts superpositions evolve unitarily. Measurements produce definite outcomes. What causes the transition? Wavefunction collapse is postulated (Copenhagen), not derived. Every interpretation of QM — Copenhagen, many-worlds, Bohmian mechanics, QBism — is a different attempt to retire this obstruction. All remain contested. QM is promoted for operational predictions. The ontological question is explicitly out of scope.

2. **Relativistic extension.** Schrödinger's equation is not Lorentz covariant. Dirac equation (1928) fixes this for spin-1/2 particles but predicts negative energy states — which forces the prediction of antimatter. Antiparticle obstruction filed → retired by Dirac's prediction → confirmed by Anderson's positron discovery (1932). This is a clean EBP retirement: obstruction filed, consequence stated (either the theory is wrong or antimatter exists), experiment closes it.

3. **Gravity.** QM and GR remain structurally incompatible. Quantum field theory on curved spacetime is a patch, not a solution. This is the same open obstruction noted on GR's ledger — the two theories file it against each other. Neither has retired it.

**needFaithfulnessReview — the Born rule.**
Does "P = |ψ|²" faithfully capture what's happening during measurement? The formalism predicts all measurement statistics correctly. What it does not explain is *why* a definite outcome occurs at all, or what ψ represents physically. Contested since 1926. No resolution. Promotion holds for predictive content. Ontological faithfulness: open.

---

## The Full Ledger

| Idea | Status | Scope | Open Debt |
|---|---|---|---|
| Planck's distribution formula | Promoted | Blackbody spectrum | None — it's a formula |
| Energy quantization as physics | Promoted | Sub-relativistic quantum phenomena | Measurement problem |
| Einstein's photons | Promoted | Photoelectric, Compton scattering | Wave-particle ontology |
| Bohr's atomic model | Dormant, scoped | Hydrogen-like atoms | Multi-electron, intensities |
| de Broglie matter waves | Promoted | Non-relativistic matter | Absorbed into QM |
| Full QM | Promoted | Sub-Planck, non-gravitational | Measurement problem, gravity |

---

## The Through-Line

Planck's quanta is the cleanest case in the history of physics of a **Door entry that the author refused to promote himself.** He had the formula. He had the toy check. He had the null models beaten. He filed his own faithfulness objection and parked the idea as a device.

Einstein took the same idea — same formula, no new mathematics — and promoted it to a physical claim by retiring needMap, needToyCheck, and needNullModel against the photoelectric effect. Millikan tried to kill it and instead closed the debt.

The remaining open items — measurement problem, gravity — have sat on the ledger for a century. No shame. No expiration. The ledger makes the target visible. Whoever closes the measurement problem or quantum gravity will do to QM what Einstein did to Newton: not destroy it, but honestly scope it, contain it as a limit, and carry its open debt into a larger promoted framework.
