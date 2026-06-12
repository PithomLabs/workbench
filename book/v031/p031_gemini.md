Here is the Workbench evaluation of the terminology, rule, and boundary patch under EBP v2.1 discipline.

### **Overall verdict:**

Strong structural improvement. The patch successfully converts vague Lean `Prop` promises into auditable data structures and executable schemas. It holds the line against physics overclaims and shifts the project from methodological promises to enforceable engineering constraints. This remains a debt-bearing semantic boundary patch; Phase 0 is not solved, but the boundary is now defensible.

### **Does v0.3.1 repair the v0.3 weaknesses?:**

Yes, substantially. It forces executable constraints (Go schemas) and explicit metadata (`Spec` structures) over unprovable conceptual promises. The vulnerabilities regarding history curation, result-driven labeling, and post-hoc coarse-graining have been closed via formal preconditions.

### **Remaining undefined terms:**

* `CoarseAlternatives` (Section 9): Referenced in the Lean-shaped contract but not explicitly defined. It is implied to mean two histories with the same coarse endpoint but different properties, but this needs formalization.
* **"Frequent" random success:** Section 10.3 dictates a downgrade if random success is "frequent," but no statistical threshold or $p$-value equivalent is defined.
* **"Generic bijective permutations":** Section 10.7 requires testing generic permutations, but no sample size or distribution boundary is provided.

### **Hidden imports still present:**

* The mapping of `WitnessLabel.plus` to 1 and `minus` to -1 accompanied by integer summation is still an imported algebraic assumption (the `whySummationDebt`).
* The assumption of uniform history generation over `allowedStarts` without a defined metric or physical justification for uniform weighting.

### **Terminology assessment:**

Highly effective. The renames aggressively strip away unwarranted physics prestige:

* `ClassicalCount` $\rightarrow$ `UnlabeledCount`: Removes the smuggling of "classical theory" and correctly identifies it as a positive tally.
* `SignedCount` $\rightarrow$ `SignedTally`: Removes the "measure" implication. It is simply finite signed bookkeeping.
* `NonAdditiveWitness` $\rightarrow$ `SignedTallyCancellationWitness`: Strips the misleading "non-additive" label (which was ironic given the mechanism uses addition) and strictly describes the toy-level outcome.

### **Label-rule and coarse-graining metadata assessment:**

Replacing `Prop` flags with `LabelRuleSpec` and `CoarseGrainingSpec` structures makes the discipline machine-readable. It prevents hand-painted labels by demanding `handPainted = false` and `fixedBeforeWitness = true` for admissibility. This ensures $\Pi$ and labels cannot be reverse-engineered to fit a desired cancellation.

### **History enumeration assessment:**

Generating histories via `HistoryEnumerationSpec` explicitly bans manual curation. The strict requirement `deduplicate = true` effectively closes the vulnerability where duplicate list entries could manufacture a false cancellation.

### **Null-model criteria assessment:**

Excellent. The nine null models provide a gauntlet that shifts the burden of proof. The consequence statuses (e.g., `downgrade_to_endpoint_artifact`, `downgrade_to_classical_parity_artifact`) establish clear falsifiability conditions. If the toy mechanism fails these, it fails auditably.

### **Go output schema assessment:**

The `tc-1b-go-report-v0.1` schema is a massive improvement. It enforces a structural audit of forbidden inferences (`claims_quantum_interference`, etc.) directly in the artifact metadata. It also forces null-model results and the history enumeration spec to be published alongside the main witness.

### **Should TC-1B proceed?:**

Yes. The semantic boundaries are sufficiently patched to allow a safe toy-model execution. The risk of accidentally promoting classical parity bookkeeping to quantum interference has been mitigated by the schema and null models.

### **Required edits before TC-1B:**

1. Explicitly define `CoarseAlternatives` in the Lean/Go contract.
2. Define the exact sorting and concatenation rules for the `CanonicalEncoding` string to prevent Go implementation drift.
3. Establish strict integer bounds/thresholds for "frequent" random success and the number of "generic permutations" to test.

### **Smallest useful next move:**

Draft **TC-1B** by instantiating a minimal, concrete state space $S$, an update rule $U$, and a coarse-graining $\Pi$, strictly conforming to the new JSON schema and `Spec` constraints. Execute the null models.
