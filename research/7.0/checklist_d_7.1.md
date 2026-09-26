# The v7 Dashboard: A Human-Scale View of the BM–IST–AS Program

## How to use this document

This is a companion to the technical documents, not a replacement. It has one job: let you see, in under five minutes, where the program stands and what matters next.

For humans: read top to bottom once. Then use the checklist as a status board.
For AI agents: treat each task as a checkpoint with an explicit acceptance criterion. Do not skip the kill conditions.

Update this document at the end of every major work session. If a task is in progress, mark it. If a task is blocked, say why.

---

## The Mission (one paragraph)

We are trying to explain why quantum mechanics is the way it is. Our bet: the quantum world lives on a mathematical structure called the *adeles*, in which the continuous and the discrete are co-equal siblings rather than one deriving from the other. The continuous supplies geometry and statistics. The discrete supplies phase and exact quantization. Arithmetic acts as a constraint — it selects which states are physical — not as a generator of the physics. If this bet is right, we can derive the Born rule, the exact quantization conditions, and the recovery of standard physics from a single framework.

---

## The Current Picture

**Where we are:** One hypothesis (v7.0). One mathematical framework (Tate's thesis — mature, seventy-five years old). One bridge candidate (the adelic scaling flow). One missing object (a Dirac-type operator). Zero empirical tests passed. Zero empirical tests failed.

**What changed recently:** We dismantled the earlier assumption that physics has a "bottom layer" from which everything else derives. This assumption had driven every failed attempt. Removing it forced a full paradigm revision.

**What is not yet known:** Whether the framework is mathematically realizable. Whether it has any empirical consequences. Whether the p-adic sector is doing any physical work.

**What we are honest about:** We have not yet earned the right to say the framework is correct. We have earned the right to ask whether it is coherent.

---

## The Critical Path

Everything hinges on one question. Answer it, and the rest cascades. Ignore it, and everything else is decoration.

1. **Does the central operator exist?** — The framework requires a specific kind of operator (a Dirac operator) acting on the space of adelic states. Its existence, and the properties it must have, is the first gate. If it does not exist, the framework is dead in its current form.

2. **Does its spectrum match reality?** — If it exists, its spectrum should encode the exact discrete structure of quantum mechanics: the phases, the quantization conditions, the topological invariants. If it doesn't, the framework is falsified.

3. **Does it produce probabilities?** — The Born rule is the deepest unexplained fact in quantum mechanics. If the framework cannot derive it, it has not explained the phenomenon it set out to explain.

4. **Does it match the renormalization group?** — Physics is known to change with scale. The framework proposes a natural flow between sectors. Does it match the observed scale dependence?

5. **Can it recover known physics?** — From nonrelativistic quantum mechanics through the Standard Model and General Relativity.

Everything else — the empirical tests, the imports from other theories, the technical refinements — serves these five questions.

---

## The Full Checklist

Status markers: `✓` done · `✗` failed · `?` open · `~` in progress · `!` blocked · `—` deferred

### Part A — Foundation

- `?` **A1. State the adelic framework precisely.** — The ambient state space, the arithmetic constraint, the bridge. *Acceptance:* a single-page specification any mathematician can read.
- `?` **A2. Specify the Dirac operator's required properties.** — Five conditions the operator must satisfy. *Acceptance:* a mathematical statement of what "correct operator" means.
- `?` **A3. Confirm the mathematical framework is standard.** — Verify that Tate's thesis and Connes' work provide the needed tools. *Acceptance:* a short document listing which theorems are being used and where they are published.

### Part B — Mathematical Realizability

- `?` **B1. Does the operator exist?** — The first decisive gate. *Acceptance:* either an explicit construction or a proof that no such operator exists.
- `?` **B2. What is its spectrum?** — Compute the spectrum on the physical subspace. *Acceptance:* a numerical or analytic result.
- `?` **B3. Does the spectrum encode quantum mechanics?** — Compare against known quantization data. *Acceptance:* a match or a discrepancy, stated precisely.
- `?` **B4. Is the framework replaceable?** — Could a simpler non-adelic structure do the same work? *Acceptance:* a null model and a comparison.

### Part C — Physical Consistency

- `?` **C1. Born rule derivation.** — Can the framework derive the Born rule from its own measure? *Acceptance:* a derivation or a proof that it cannot.
- `?` **C2. Scaling flow vs. renormalization.** — Does the proposed flow match observed scale dependence? *Acceptance:* a match in the relevant limit, or a discrepancy.
- `?` **C3. Bell channel.** — Does the framework predict any new Bell observable? *Acceptance:* we already have a partial answer: no, at accessible precision. Record this as `✓` with scope.
- `?` **C4. Standard physics recovery.** — Can the framework reproduce continuum quantum mechanics in the appropriate limit? *Acceptance:* a derivation, not an assumption.

### Part D — Empirical Tests

- `?` **D1. AS critical exponents.** — Do the exponents of the Asymptotic Safety fixed point satisfy the adelic product formula? *Acceptance:* a finite computation, PASS/FAIL/INAPPLICABLE.
- `?` **D2. Quantum dimensions of anyons.** — Do the dimensions of anyon theories satisfy adelic consistency? *Acceptance:* a finite computation over known theories.
- `?` **D3. Corner census.** — Is any exact quantization phenomenon p-power-specific in a way a generic clock cannot reproduce? *Acceptance:* a literature census with a verdict.
- `?` **D4. Freund–Witten compatibility.** — Does the framework reproduce the Freund–Witten formula for 4-point amplitudes? *Acceptance:* a mathematical derivation or a disproof.

### Part E — Structural Integrity

- `?` **E1. Product formula check.** — Is the adelic product formula doing genuine physical work, or is it decoration? *Acceptance:* a null model where the formula is removed and the difference is quantified.
- `?` **E2. Prime universality.** — Are all primes treated equally, or does a specific prime dominate? *Acceptance:* a structural answer.
- `?` **E3. Cross-checks between sectors.** — Do independent derivations of the same quantity agree? *Acceptance:* at least two independent paths to the same prediction.
- `?` **E4. Kill conditions audit.** — Have any of the framework's kill conditions been triggered? *Acceptance:* a periodic audit report.

### Part F — Program Hygiene

- `?` **F1. External review.** — Has an independent reviewer examined the framework? *Acceptance:* a written review, versioned.
- `?` **F2. Reproducibility.** — Are all computations scripted and archived? *Acceptance:* a reproducibility manifest.
- `?` **F3. Debt ledger.** — Is the debt ledger current? *Acceptance:* every open claim has an owner and a status.
- `?` **F4. Removal record.** — Have rejected ideas been recorded? *Acceptance:* an append-only record with reasons.

---

## The Kill Conditions

If any of these is true, the framework is dead in its current form. They are the program's honesty guarantee.

- **K1.** The central operator does not exist.
- **K2.** Its spectrum does not encode quantum mechanics.
- **K3.** The Born rule cannot be derived from the framework's measure.
- **K4.** The scaling flow does not match the renormalization group.
- **K5.** The framework makes a prediction that contradicts observation.
- **K6.** A simpler non-adelic structure reproduces all predictions.
- **K7.** The framework makes no prediction distinguishable from standard quantum mechanics.

None has been triggered. None has been ruled out. The program is in the phase of asking whether any of them is true.

---

## What Success and Failure Look Like

**Success** — even partial — looks like this:
- One of the five critical-path questions answered with a rigorous construction.
- One empirical test passing with an independent null failing.
- One previously assumed postulate being derived from the framework.

**Failure** looks like this:
- A kill condition triggered.
- A critical-path question answered with a rigorous disproof.
- A previously claimed derivation revealed to be circular.

Both are progress. The program is designed so that failure is informative.

---

## How to Read the Deeper Documents

- **v7.0** — the current research charter. Read the executive thesis first, then skip to the gates section.
- **R0 Reality Constraint Ledger** — the empirical envelope. Read the first table only.
- **R1-A Bell Audit** — a completed test. Read the executive finding only.
- **Tate's thesis and Connes' work** — the mathematical foundation. Do not read the primary sources unless you are checking a specific claim; use secondary expositions.

For AI agents: every claim in the deeper documents must trace back to an entry in this dashboard, and every task in this dashboard must have a corresponding detailed specification in the deeper documents.

---

## A Standing Invitation

The program is not asking for believers. It is asking for critics.

If you know number theory, check whether the adelic framework is being used correctly.
If you know physics, check whether the empirical constraints are being applied honestly.
If you know mathematics, check whether the operator exists.
If you know philosophy of science, check whether the framework is a theory or an interpretation.

The most useful thing you can do is find a kill condition.

---

## Update Log

Keep a running log at the bottom of this document. Each entry:

```
Date | Task ID | Status change | Reason | Owner
```

The log is how anyone — human or AI — reconstructs the trajectory of the program without reading every technical document.

---

*This document is a living artifact. It is meant to be updated, not preserved. If it becomes stale, the program has lost track of itself. If it becomes cluttered, it has lost its purpose. Keep it small. Keep it honest. Keep it current.*
