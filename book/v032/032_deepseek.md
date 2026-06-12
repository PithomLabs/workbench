**Overall verdict:**  
TC‑1A v0.3.2 is a careful, focused patch that closes the final pre‑TC‑1B cracks. Every missing or underspecified element from v0.3.1 is now defined, enforced, or clearly bounded. The patch remains honest about its debts and does not overclaim. It is ready for TC‑1B drafting.

**Does v0.3.2 close the v0.3.1 gaps?**  
Yes. `endpoint` and `CoarseAlternatives` are defined. Canonical encoding is precise enough for implementation. Metadata is audited, not taken as proof. History‑selection loopholes are closed by `StartSelectionMode` and `maxLength` rules. Null‑model thresholds are quantified. Parity/XOR statuses are clearly differentiated. A U(1) boundary audit and Go type‑level guardrails are added. The report schema is extended to capture all enforcement results.

**Remaining undefined terms:**  
- The exact escaping scheme for canonical encoding (e.g., backslash‑escape or percent‑encoding) is not fully specified. It is sufficiently sketched but will need a precise rule during TC‑1B spec implementation.  
- `independentlyJustified` is a boolean; what constitutes “independent justification” is left to human documentation, but that is acceptable at this stage as long as the field is required and auditable.

**Remaining hidden imports:**  
None. The patch explicitly audits and denies any U(1), complex‑number, Hilbert‑space, or Born‑rule structures.

**Endpoint / CoarseAlternatives assessment:**  
Clear, executable definitions. `endpoint` is given as iteration, with Go pseudo‑code. `CoarseAlternatives` is a simple conjunction of inequality and coarse equality. No physics‑loaded interpretation is smuggled.

**Canonical encoding assessment:**  
Deterministic enough for Go implementation. The rules (sorting, escaping, ordering) are explicit. The only minor debt is the exact escaping specification, which can be resolved before coding without changing the contract.

**Metadata enforcement assessment:**  
Honest and practical. The patch separates declared discipline from proof, introduces runtime rejection of invalid metadata, and retains `metadataTruthDebt` for future audit. This is an appropriate lightweight enforcement.

**History selection assessment:**  
`StartSelectionMode` with `allStates` as the clean default, plus explicit invalidation of `invalidHandSelected`, effectively closes the selection loophole. The `maxLength` rule (fixed before witness, recommended to be `|S|`) adds a reasonable first‑pass coverage constraint.

**Null‑model threshold assessment:**  
Reasonable. Random‑label threshold (≥0.25) and generic‑permutation threshold (≥0.10) are conservative, pragmatic audit values, not physics constants. The requirement for at least 100 (or 1000) trials and under‑powered flags ensures basic statistical hygiene. The thresholds are acknowledged as revisable with `thresholdJustificationDebt`.

**Parity/XOR status assessment:**  
Well‑defined triage: equivalent replication → downgrade; arithmetic pattern only → `survives_with_parity_debt_open` with required extra evidence; failure → `parity_null_survived`. This prevents overclaiming and is EBP‑safe.

**U(1) / phase boundary assessment:**  
The boundary audit is sufficient for TC‑1B. It explicitly declares the label carrier is finite two‑label, with no continuous phase, no complex numbers, no U(1) structure claimed. The debt `u1ExtensionDebt` is correctly parked for later phases.

**Go type‑guardrail assessment:**  
Sufficient. Distinct types for `UnlabeledCount`, `SignedTally`, `WitnessLabel` and an explicit prohibition on probability/amplitude types prevent accidental promotion in Go code.

**JSON report schema assessment:**  
Complete enough. The schema includes runtime validation, boundary audit, null‑model power, and selection audit fields, ensuring that every enforcement result is captured in the output.

**Should TC‑1B be drafted next?**  
Yes, **draft the TC‑1B specification**. The patch has supplied all the required pieces. Implementation should follow after the spec is reviewed and the remaining tiny details (escaping scheme, `independentlyJustified` documentation guidelines) are nailed down.

**Required edits before TC‑1B:**  
- Specify the exact escaping rule for canonical encoding (e.g., backslash‑escape `|`, `;`, `/`, `(`, `)`, `,`, `\` itself) so that Go code can be deterministic.  
- Clarify what kind of documentation satisfies `independentlyJustified = true` (e.g., a textual justification that the coarse‑graining was chosen for independent reasons, not tuned to the witness). This can be a required field in the report.

**Smallest useful next move:**  
Draft the TC‑1B specification document, incorporating the above two minor clarifications, and then implement a minimal Go check for a tiny concrete system (e.g., 2–3 nodes) to validate the entire pipeline.
