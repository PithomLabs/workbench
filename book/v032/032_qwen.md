Overall verdict:
TC-1A v0.3.2 successfully functions as a debt-bearing semantic-enforcement patch. It systematically replaces vague prose from v0.3.1 with explicit, Lean-shaped definitions, Go-enforceable runtime rules, and honest debt declarations. It rigorously protects the workbench from overclaiming while preparing a clean, auditable foundation for the next phase.

Does v0.3.2 close the v0.3.1 gaps?
Yes. Every identified gap (undefined predicates, vague enforcement, self-reported metadata, history-selection loopholes, null-model thresholds, and encoding drift) is addressed with explicit rules, status downgrades, or retained debt markers.

Remaining undefined terms:
None at the TC-1B entry level. `RelState` internal structure is assumed from prior context, but its encoding is now strictly bounded.

Remaining hidden imports:
None introduced. The patch relies only on standard mathematical operations (Nat iteration, List filtering, lexicographical sorting) and the explicitly declared `MicroSpace` and `ReversibleUpdate` structures.

Endpoint / CoarseAlternatives assessment:
Mathematically precise and explicitly bounded. `endpoint` is cleanly defined as `Nat.iterate`. `CoarseAlternatives` is strictly defined as distinct histories yielding the same coarse endpoint. The explicit "Forbidden inference" block correctly prevents smuggling quantum superposition or physical path interference claims.

Canonical encoding assessment:
Deterministic and Go-ready. The rules for escaping reserved characters, lexicographical sorting, and argument ordering (ordered vs. unordered) eliminate ambiguity. The retention of `fullGraphIsomorphismDebt` is an honest and EBP-compliant acknowledgment of practical limits.

Metadata enforcement assessment:
Handled with EBP-appropriate honesty. The patch correctly reclassifies Bool metadata as "audit declarations, not proof." The runtime enforcement rules (e.g., rejecting runs where `handPainted = true` or `fixedBeforeWitness = false`) are strong, and the explicit retention of `metadataTruthDebt` ensures the protocol does not pretend Go can verify real-world human history.

History selection assessment:
The introduction of `StartSelectionMode` and the strict `maxLength` rules effectively close hand-selection loopholes. Mandating `allStates` for the cleanest check, while allowing subsets only with an explicit `history_selection_debt_open` tag, perfectly aligns with EBP v2.1's "promotion costs debt" doctrine.

Null-model threshold assessment:
The thresholds (random >= 0.25, generic permutation >= 0.10) are conservative, pragmatic, and explicitly flagged as Workbench defaults (`thresholdJustificationDebt`), not physical constants. The addition of `random_null_underpowered` and `permutation_null_underpowered` flags is a strong, anti-bureaucratic safeguard against weak statistical claims.

Parity/XOR status assessment:
The three-tier status system (`downgrade_to_classical_parity_artifact`, `survives_with_parity_debt_open`, `parity_null_survived`) is clear, auditable, and EBP-safe. The explicit "Forbidden claim" rules prevent the illicit leap from "toy signed-tally pattern" to "interference-like structure."

U(1) / phase boundary assessment:
The explicit JSON boundary audit block is sufficient for TC-1B. By hardcoding `continuous_phase_used: false`, `complex_numbers_used: false`, and `born_rule_used: false`, it erects a firm firewall. Retaining `u1ExtensionDebt` correctly defers this to a later phase without blocking current progress.

Go type-guardrail assessment:
Strong and necessary. Defining distinct types (`UnlabeledCount`, `SignedTally`, `WitnessLabel`) and explicitly forbidding aliases like `Probability` or `Amplitude` prevents semantic drift and conceptual smuggling at the compiler level.

JSON report schema assessment:
Complete enough for TC-1B execution. The additions (`runtime_validation`, `boundary_audit`, `null_model_power`, `selection_audit`) provide all necessary hooks for automated, auditable reporting without demanding excessive bureaucratic overhead.

Should TC-1B be drafted next?
Yes. Specifically: **draft TC-1B spec**. (Promotion is strictly forbidden at this stage, and implementation should only follow a locked specification).

Required edits before TC-1B:
Minor alignment check: Ensure the Go `CanonicalEncoding` error conditions (e.g., "unknown ArgOrder") are explicitly mapped to the `runtime_validation.invalid_reason` string in the JSON schema, so encoding failures are captured uniformly with metadata failures.

Smallest useful next move:
Draft the TC-1B specification document, instantiating concrete `S`, `U`, `Π`, `LabelRuleSpec`, and `HistoryEnumerationSpec`, along with the required Go types and JSON schemas, without attempting to execute the toy check or claim any physical result.
