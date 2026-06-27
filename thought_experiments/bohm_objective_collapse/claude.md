## prompt

wear your imaginative theoretical physics hat as a thought experiment how to unify bohmian mechanics with Objective-collapse theory into a cohesive whole by recasting our standard notions of QM and GR, remove all your biases and think with beginner's mind, the goal is the thought experiement and how to make it both cohesive coherent


answer: 

This is a great problem to think through properly, because the standard story makes Bohmian mechanics (BM) and objective collapse (GRW/CSL/Penrose) sound like rival, mutually exclusive answers to "what is real." Beginner's mind suggests starting from a different question: what do these two theories already agree on, underneath their apparent opposition? That agreement turns out to be the seam where a real synthesis is possible — and it happens to be the same seam where general relativity can be stitched in.

Let me build this up properly rather than just asserting a punchline.

## The shared foundation neither theory advertises

Both BM and GRW make a move that ordinary textbook QM never makes: they insist on a **primitive ontology** — something that exists in actual 3-dimensional space, at definite locations, independent of anyone observing it. Bell called these "local beables."

- BM's local beables: particle positions, guided by ψ but never identical to it.
- GRW's local beables (in its mass-density or "flash" versions): a matter-density field or discrete point-events in spacetime, both derived from |ψ|².

The wavefunction itself, in *both* theories, lives on configuration space — an abstract, high-dimensional object that is not directly "what's there in the room." Standard QM blurs this distinction (ψ does double duty as both dynamical law and the thing itself); BM and GRW both refuse to blur it, just in different ways. That's the real kinship. The disagreement people usually fixate on — does ψ collapse or not? — is actually downstream of a deeper agreement: ψ is not the whole story; something local has to settle outcomes.

## The actual tension (stated honestly, not hand-waved)

You cannot literally keep both mechanisms as fundamental:

- BM: ψ evolves unitarily, *forever*, no exceptions. Apparent collapse is just bookkeeping (the "conditional wavefunction" of a subsystem effectively stops caring about branches the particle isn't in).
- GRW/CSL: ψ undergoes a genuine, physical, irreversible stochastic jump. There is no separate particle to "carry" the outcome — the collapse *is* the outcome.

Something has to give. A real synthesis has to say explicitly which piece is doing fundamental work and which piece becomes *derived* or *re-purposed* — otherwise it's just two incompatible postulates glued together with hope.

## The synthesis move: let gravity decide when "empty branches" die

Here's the move I'd make, and I'll flag it clearly as a postulate rather than smuggle it in as if it were forced:

Keep a **single primitive ontology** — say, the GRW mass-density field m(x,t), with Bohmian-style trajectories defined as its *streamlines* (this is the Madelung-fluid reading of BM: ψ = √ρ e^{iS/ℏ}, velocity field v = ∇S/m). You don't need two separate ontological commitments (particles *and* a collapsing field); you need one field with two regimes of motion — smooth deterministic flow (Bohmian) punctuated by sharp localization events (GRW).

Then borrow Penrose and Diósi's idea and give it a bigger job than they originally assigned it: the trigger for a collapse event isn't a free-floating stochastic rate constant (GRW's λ, fitted by hand to taste). It's the **gravitational self-energy difference between branches** — how distinguishable two possible mass distributions are, geometrically, in the spacetime they'd each generate. Roughly, collapse time τ ~ ℏ/E_G, where E_G is that self-energy difference.That's the core loop. A few things worth unpacking about why it actually closes rather than just gesturing at a compromise.

**Why the left branch (spacetime) never has to deal with superposition.** The chronic headache in semiclassical gravity is: if a 1-kg mass is in a superposition of "here" and "there," what sources the metric — both locations at once, weighted by ⟨ψ|T_μν|ψ⟩? A statistical mixture? Does spacetime itself branch? Every answer has been unsatisfying. In this picture the question doesn't arise, because the primitive ontology — the Bohmian streamlines, or equivalently the GRWm mass-density field — is *defined* to be single-valued in physical space at every instant. There's exactly one mass distribution sourcing G_μν = 8πG T_μν, full stop. The "other branches" are real in the sense that ψ still assigns them amplitude on configuration space, but they have never been candidates for sourcing curvature. Superposition lives upstairs in configuration space; geometry lives downstairs in physical space; and the primitive ontology is the floor between them that only one branch gets to touch at a time.

**Why the right branch (the coral box) is the actual new physics, not just imported GRW.** Standard GRW/CSL treats its collapse rate λ as a free constant of nature, tuned by hand so microscopic systems stay coherent and macroscopic ones don't. Here, the collapse rate isn't free — it's tied to something physically meaningful: how much the candidate branches *disagree* about the gravitational field they'd produce. Diósi and Penrose independently noticed that this gives roughly τ ~ ℏ/E_G, where E_G is the self-energy of the difference between two mass distributions. A single electron in two slightly displaced locations has a minuscule E_G — coherence survives a long time, which is why electrons interfere. A cat in two macroscopically different configurations has enormous E_G — coherence dies almost instantly, which is why cats don't. The classical/quantum boundary and the "why does collapse happen at all" question turn out to be the *same fact*, both set by gravitational self-energy. That's a real unification, not a verbal one — it's deriving something GRW has to postulate.

**Why the loop has to close back into node 1, not just terminate.** If collapse just picked a branch and stopped, you'd have GRW with extra Bohmian decoration. The thing that makes it a *genuine synthesis* rather than two theories taped together is that the selected branch isn't a fresh random draw (as in vanilla GRW) — it's anchored to wherever the Bohmian streamlines/mass-density already were, which were themselves set by initial conditions at the start of the universe (quantum equilibrium, |ψ|² typicality). So the "randomness" you see in outcomes isn't a new ontological ingredient injected at each collapse event — it's the same old epistemic randomness BM already has, now given a physical mechanism (gravity) that prevents the discarded branches from lingering forever as equally-real ghosts. That's BM's most-criticized feature — eternally surviving empty branches — actually getting fixed, rather than just reasserted.

Now let me be honest about the structure of this claim, the way I would if this were going through the same kind of audit you've been running on the EBP work — what's actually forced, what I chose, and what's still owed:

**Derived / genuinely explained, not just accommodated:**
- The macro-classical / micro-quantum split and "why does anything ever collapse" become one explanation instead of two separate postulates.
- The semiclassical-gravity superposition-of-sources problem dissolves rather than getting patched.
- GRW's free rate constant λ gets replaced by something with independent physical motivation (G, ℏ, c) instead of being fit to taste.

**Accommodated — a real choice I made, not a forced one:**
- Whether the primitive ontology is separate point particles guided by a collapsing field, or a single mass-density field whose own flow lines play the Bohmian role. I leaned toward the single-field version because it's more economical (one ontological commitment instead of two) and because it directly imports BM's typicality machinery to solve GRW's notorious "tails problem" (the bit of the wavefunction that never quite reaches zero after a collapse hit) — almost every streamline still ends up in the dominant lobe, for the same |ψ|²-typicality reason BM already uses to explain why we never see macroscopic interference. But the particle-plus-collapsing-field version is equally coherent if you prefer keeping particles as a separate, more conservative commitment.

**Postulated — flagged honestly as new, not derived:**
- That gravitational self-energy difference is the *sole* trigger for branch selection. This is essentially adopting the Diósi–Penrose hypothesis and handing it a bigger job than its authors gave it.
- Even Diósi–Penrose itself needs a coarse-graining length scale to tame the divergent self-energy of point masses — so this synthesis doesn't eliminate free parameters, it relocates one. You go from GRW's two essentially arbitrary constants (λ, the localization width) to one constant with a physical job description (regularizing a known divergence) rather than a dial chosen purely to match observation. That's progress, not a free lunch.

**Inherited debt, not resolved here:**
- Relativistic covariance. Both BM and flash-ontology GRW need something like a preferred foliation to say where a particle is or where a collapse event happens "at a given time" — sitting uneasily with general covariance, which refuses to privilege a foliation. This synthesis doesn't fix that; if anything it raises the stakes, because now you'd want the foliation to be *dynamically* picked out by the matter distribution itself rather than imposed externally. That's a real research program, not a paragraph.
- Backreaction stability and no-signaling. The loop is self-referential (matter sets curvature, curvature differences set collapse rate, collapse picks matter) — that needs an actual proof that it doesn't blow up or violate the no-superluminal-signaling theorems CSL satisfies only after careful work, not just narrative plausibility.
- It's a weak-field, semiclassical-regime theory by construction. Near the Planck scale there's no fixed background to even define "gravitational self-energy of a branch" against, so the whole mechanism is silent exactly where quantum gravity proper would need to speak.

One thing worth sitting with: most interpretations of QM are constructed to be permanently empirically indistinguishable from standard QM — that's almost a design goal. This one isn't. Tying collapse to gravitational self-energy makes falsifiable, numerically specific predictions (decoherence rates for mesoscopic superpositions) that are in the range current optomechanics and matter-wave interferometry experiments are starting to probe. A unification that can be wrong is a better unification than one that can't be — and this one can be wrong.

If you want, I can take the relativistic-covariance debt as the next target and see how far "matter-determined foliation" can actually be pushed before it breaks — that's the obstruction I'd want resolved first if this were going into a formal ledger.


## prompt

Good — let's actually push on this rather than wave at it. To do it honestly I need to be precise about what "covariant" has to mean here, because there's a real distinction hiding in the phrase "preferred foliation" that most popular accounts blur.

**What we actually need, stated precisely**

A theory isn't ruined just because evolving it forward requires picking a time-slicing. Ordinary GR in the ADM/Hamiltonian formulation does that too — you slice spacetime into spacelike surfaces and evolve the 3-metric forward, and the theory is still generally covariant because *which* slicing you pick doesn't matter; any slicing gives the same physical spacetime. The thing that would actually violate the spirit of relativity is a foliation that's *externally imposed* — fixed by fiat, not derivable from the dynamical content of the theory itself, and (worse) detectable in principle.

So the real target isn't "no foliation." It's: a foliation whose *defining rule* references only the theory's own dynamical matter content, stated in a way that doesn't presuppose a frame, such that no experiment could ever recover which slicing "really" happened. That's the bar. Let's see how far matter — specifically, the always-single-valued primitive ontology from the loop above — can actually clear it.

**The win: Bohmian flow is structurally the right kind of object**

This is the part that isn't a postulate — it falls out of the guidance equation's own form. Write ψ = √ρ e^{iS/ℏ}. The Bohmian velocity field is v = ∇S/m — a gradient. Gradients are curl-free. In relativistic language, a congruence of worldlines is hypersurface-orthogonal — meaning you can slice spacetime into simultaneity surfaces orthogonal to it — exactly when its vorticity tensor vanishes (this is standard timelike-congruence kinematics, the Ehlers decomposition into expansion/shear/vorticity). A curl-free flow has zero vorticity by construction. So wherever ψ ≠ 0, the actual matter flow in this theory is *automatically* the kind of object Frobenius's theorem lets you build a foliation out of — not because we postulated it, but because "guided by the phase of a wavefunction" already has the right mathematical shape.

This isn't just a curiosity — it's already a working technique elsewhere in GR. Brown and Kuchař showed you can solve the "problem of time" in canonical quantum gravity by introducing a pressureless, irrotational dust field and using its proper time as the physical clock. That's the identical move, just imported from cosmology instead of invented here. In a dust-dominated regime, the GRWm mass density essentially *is* Brown–Kuchař dust, and the foliation comes for free.

**Crack 1 — wavefunction nodes**

But "wherever ψ ≠ 0" is doing real work in that sentence. At the zeros of ψ, the phase S isn't single-valued — it can wind around a nodal point or line with quantized circulation, exactly like a vortex in a superfluid. This is well documented in the Bohmian-trajectory literature: nodal regions are where the flow genuinely picks up vorticity. That's not a gap in our knowledge that more computation fixes — it's the Frobenius condition failing as a matter of mathematical fact. A foliation built from "orthogonal to the matter's rest frames" cannot be smoothly continued through these loci. They're generically a thin set (nodal surfaces are codimension-1 or higher), so you can probably argue the foliation is well-defined *almost everywhere* — but "almost everywhere" is a different, weaker claim than "everywhere," and it's the kind of weakening you should be honest about rather than bury.**Crack 2 — entanglement forces a chicken-and-egg problem**

The deeper issue isn't nodes, it's that BM's guidance equation was never really a *local* law to begin with. Particle 1's velocity depends on the wavefunction evaluated at the *simultaneous* positions of particles 2 through N — that's what entanglement means here. So to evolve particle 1 forward you already need a notion of "what everyone else is doing at the same time," which is precisely the thing a foliation is supposed to supply. You can't bootstrap the foliation from positions that themselves presuppose the foliation.

There's a real, if partial, answer to this on a *fixed* background: Dürr, Goldstein, Norsen, Struyve, and Zanghì showed (if I'm recalling the construction correctly — worth double-checking the original if you want to build on it) that for two entangled particles in flat spacetime, you can define the foliation using past light cones built from the particles' own actual worldlines, in a way that's covariant as a *rule* even though it singles out a specific slicing for any given history. It reproduces ordinary BM in the right limit and respects no-signaling. What I don't think exists — and I want to flag this as a genuine extrapolation past what I can confidently attribute to the literature rather than something I've verified — is a clean generalization to many entangled bodies, and certainly not to a setting where the light cones themselves are dynamically warped by the same matter you're trying to track, which is exactly our situation: gravity here is sourced by the configuration whose simultaneity you're trying to pin down. The flat-background trick doesn't obviously survive that self-reference. This is real open territory, not a solved problem dressed up as one.

**Crack 3 — the sharpest one, and specific to this hybrid theory**

Here's the finding I think is actually new to this particular synthesis rather than inherited wholesale from the existing relativistic-BM literature. Bohmian positions are always continuous — even through a collapse event, the particle doesn't teleport. But its *velocity* doesn't have that protection. A Diósi–Penrose collapse event sharply reshapes the guiding wave, and v = ∇S/m can change almost discontinuously across it — a kink in the worldline's tangent vector, not in its position.

A kink in the tangent vector is exactly the kind of irregularity that breaks the "extend the local rest frame into a smooth orthogonal foliation" construction. You need the congruence to be at least differentiable to extend it; right at the kink, "before" and "after" rest frames disagree about what's simultaneous, and there's no principled way to average them. So the foliation construction is least well-behaved at *exactly* the moment — a collapse event — where you most need a clean simultaneity, because that's the moment whose effects are supposed to propagate (without superluminal signaling) to the rest of the system. The mechanism we built to make collapse physically well-motivated (gravity) and the mechanism we hoped would rescue covariance (matter-determined time) turn out to lean on the same matter at the exact instant it's least kinematically cooperative. That's not an oversight to patch — it's a structural tension between the theory's two main ideas.

**Is there a way past this, or does it just stop here?**

A few real options, none of which I'd call solved:

- **Fall back to geometry where matter fails you.** Constant-mean-curvature (CMC) foliations are defined from the trace of the extrinsic curvature of the slice itself — a property of the geometry near the Einstein constraint equations, not of any matter congruence. Bartnik and Moncrief's existence results show CMC slicings exist quite generally for physically reasonable spacetimes. You could imagine a hybrid rule: matter-determined (dust-time) wherever the matter is calm and irrotational, CMC-determined as the global completion through nodes and collapse kinks. This patches the breakdown rather than dissolving it — you'd be trading "foliation from matter" for "foliation from matter, except exactly where the theory's own dynamics gets interesting, where you switch to a geometric proxy." Honest, but a retreat.
- **Shape Dynamics** (Barbour, Gomes, Koslowski and collaborators) already reformulates GR around CMC-type slicing as canonically preferred, trading foliation-dependence for a different gauge symmetry (local conformal invariance) instead of hiding it. It's a structurally relevant scaffold for exactly this kind of question, but whether it actually absorbs the vorticity/kink problem above is something I haven't seen examined and shouldn't claim — that's me pointing at a tool, not reporting a result.

**Verdict**

The matter-determined foliation gets pushed considerably further than I expected going in — it's not decoration, it's forced by the same gradient structure that makes Bohmian mechanics what it is, and it has a genuine, independently-motivated precedent in Brown–Kuchař dust time. But it doesn't resolve the relativistic-covariance debt; it relocates it to two sharply identifiable places — nodal vortices and collapse-event kinks — instead of leaving it as a vague, theory-wide worry about "needing a preferred frame somewhere." That's progress in the EBP sense: an undiagnosed obstruction became a diagnosed one, with a specific mathematical mechanism (failed Frobenius integrability) rather than a hand-wave. It's not closed. If you want to take it further, the CMC/Shape-Dynamics fallback at collapse events looks like the most promising next thread to pull.
