Overall verdict:
The TC-1A v0.3.1 patch is a highly successful and rigorous refinement. It successfully transforms vague methodological promises into auditable, enforceable metadata structures. The artifact now provides a tight semantic boundary that is ready to support an executable Go specification without ambiguity or physics-smuggling.

Does v0.3.1 repair the v0.3 weaknesses?
Yes. It directly and effectively addresses the core weaknesses of v0.3 by replacing unexecutable `Prop` placeholders with concrete metadata records (`LabelRuleSpec`, `CoarseGrainingSpec`, `HistoryEnumerationSpec`) and tightening the semantics of history selection and label generation.

Remaining undefined terms:
- `encoding_is_canonical : Prop` in `CanonicalRelState` remains a `Prop` in the Lean sketch. While the text correctly notes that Go must compute `CanonicalEncoding(RelState) -> string`, the Lean contract should ideally reflect this as a computable function equality or a boolean flag to prevent a disconnect between the Lean contract and the Go implementation.

Hidden imports still present:
- **Sign-Smuggling Risk**: The use of `+1` and `-1` in `WitnessLabel` and `SignedTally` walks a very fine line. While explicitly disclaimed as "bookkeeping" and flagged as `whySummationDebt` and `originOfSignsDebt`, the arithmetic of integer addition is isomorphic to the real part of complex amplitude addition. The framework must rigorously ensure this is treated as a finite label (e.g., `ZMod 2` or a custom finite enum) rather than imported real-number arithmetic, to prevent accidental smuggling of interference math.

Terminology assessment:
Excellent. The shift from `ClassicalCount`/`SignedCount`/`NonAdditiveWitness` to `UnlabeledCount`/`SignedTally`/`SignedTallyCancellationWitness` is a major improvement. It accurately describes the operation as finite, additive integer bookkeeping over histories, actively preventing the reader (or the author) from conflating it with probability measures, quantum amplitudes, or norm-squared quantities.

Label-rule and coarse-graining metadata assessment:
Strong and robust. The explicit boolean flags (`handPainted`, `usesTargetOutcome`, `fixedBeforeWitness`, `independentlyJustified`) create a hard, auditable firewall against result-driven tuning. The `LabelRuleAdmissible` and `CoarseGrainingAdmissible` definitions provide clear, machine-checkable validity conditions for a witness.

History enumeration assessment:
The `HistoryEnumerationSpec` successfully closes the duplicate-history and hand-selection loopholes. Mandating `deduplicate = true` and generating histories strictly from `allowedStarts` and `maxLength` ensures the history collection is a deterministic, auditable product of the rules, not a curated list.

Null-model criteria assessment:
Highly robust. The explicit downgrade statuses (e.g., `downgrade_to_classical_parity_artifact`, `downgrade_to_endpoint_artifact`) prevent ambiguous "partial passes" and force a clear epistemic consequence for every null-model outcome.

Go output schema assessment:
Comprehensive and well-designed. The inclusion of the `forbidden_inference_audit` object is a masterful EBP safeguard, ensuring that the automated tool cannot accidentally generate overclaimed text (e.g., claiming "quantum interference") even if the numerical tally happens to be zero.

Should TC-1B proceed?
Yes. The semantic contract is now sufficiently precise, bounded, and auditable to draft the first executable Go specification.

Required edits before TC-1B:
1. **Canonicalization Alignment**: Change `encoding_is_canonical : Prop` in `CanonicalRelState` to a computable check (e.g., `encoding = canonicalEncodingFunction raw`) or a boolean flag to ensure the Lean contract perfectly mirrors the stated Go execution rule.
2. **Coarse-State Label Dependency**: In `LabelRuleSpec`, explicitly note that if `usesCoarseState = true`, the witness must undergo stricter review, to ensure the label is not merely mirroring the coarse outcome it is supposed to explain.

Smallest useful next move:
Draft **TC-1B — First Go-Executable Toy Check Specification**. This artifact should instantiate a concrete, minimal example (e.g., 4-to-8 state `MicroSpace`), a specific nontrivial bijective `ReversibleUpdate` `U`, a fixed `CoarseGraining` map `Π`, and a declared `LabelRuleSpec` (e.g., `transitionParity` or `cycleParity`). It must strictly adhere to the `HistoryEnumerationSpec` and produce output that perfectly matches the v0.1 Go report schema, without introducing any new physics-facing language.
