## P032 synthesis: TC-1A v0.3.2 review

The review batch says:

> **TC-1A v0.3.2 is good enough to draft TC-1B, but not yet to implement Go.**
> Do **not** write v0.3.3 unless we want bureaucratic cleanup. Fold the remaining small fixes directly into the opening section of **TC-1B**.

## Quality comparison

| Reviewer     |     Quality | Best contribution                                                                                                                                         |      Weight |
| ------------ | ----------: | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------: |
| **Claude**   |   Very high | Best gap audit. Caught the `independentlyJustified` inconsistency, missing schema fields, undefined “same effective information,” and exact Go blockers.  |   Very high |
| **DeepSeek** |        High | Confirms v0.3.2 closes the big gaps; flags exact escaping and `independentlyJustified` documentation.                                                     |        High |
| **Gemini**   |        High | Strongest optimistic engineering read: says definitions, thresholds, type guardrails, and audit schema are enough for spec drafting.                      | Medium-high |
| **Kimi**     |   Very high | Best physics/EBP refinement: asks for `JustificationKind`, multiple-comparison caution, witness strength, and debt log.                                   |   Very high |
| **MiniMax**  |        High | Strong practical review; flags boundary-audit runtime validation, exact escaping, schema completeness, and trial-threshold consistency.                   |        High |
| **Qwen**     | Medium-high | Confirms TC-1B spec can proceed; useful note to map canonical encoding errors to runtime validation.                                                      |      Medium |
| **Z**        |        High | Clean verdict: no critical undefined terms; proceed to TC-1B spec with concrete `MicroSpace`, `ReversibleUpdate`, and `CoarseGraining`.                   |        High |

## Integrated verdict

```text
TC-1A v0.3.2:
  status = accepted as pre-TC-1B semantic-enforcement patch
  promotion = forbidden
  Go implementation = not yet
  next artifact = TC-1B specification draft
```

The reviewers mostly agree that `endpoint`, `CoarseAlternatives`, metadata enforcement, history selection, thresholds, U(1) audit, type guardrails, and JSON reporting are now clear enough for a **specification**. The remaining concerns are implementation details that TC-1B must lock down before code.  

## Fixes to fold into TC-1B

The first section of TC-1B should be called:

> **0. Carry-Forward Definitions and Final Inline Fixes**

It should include:

* **Restate all required types**

  * `RelState`
  * `ArgOrder`
  * `MicroSpace`
  * `ReversibleUpdate`
  * `CoarseGraining`
  * `CoarseCell`
  * `History`
  * `LabelRuleSpec`
  * `CoarseGrainingSpec`
  * `HistoryEnumerationSpec`

* **Specify canonical encoding escape rule**

  ```text
  Use backslash escaping.
  Reserved chars: | ; / ( ) , \
  Backslash itself becomes \\.
  Example: a|b -> a\|b
  ```

* **Fix `independentlyJustified`**
  Best fix:

  ```text
  Do not make independentlyJustified an invalid-run condition.
  Treat it as a downgrade condition.
  ```

  Cleaner schema:

  ```text
  clean witness = independently justified
  witness with weak justification = witness_found_with_coarse_graining_selection_debt
  invalid witness = uses target outcome / uses witness label / selected after result
  ```

* **Add `JustificationKind`**

  ```text
  symmetryQuotient
  priorFixed
  externalReference
  declaredWithoutProof
  ```

  `declaredWithoutProof` should trigger open debt, not automatic failure.

* **Define allStates enforcement**

  ```text
  if mode = allStates:
      Go ignores allowedStarts and enumerates M.State directly
  ```

* **Define runtime failure behavior**

  ```text
  invalid metadata => abort witness evaluation
  emit minimal invalid report
  do not populate witness_result
  ```

* **Clarify parity/XOR terms**
  Define:

  ```text
  same effective information
  declared substrate mechanism
  arithmetic-only match
  ```

* **Reconcile null-model trial thresholds**
  Use:

  ```text
  below 100 = underpowered / weak
  100–999 = reported with low-power warning
  1000+ = preferred default
  ```

* **Add schema fields**

  ```text
  schema_version
  parity_null_status
  coarse_graining_independence_status
  boundary_audit_valid
  witness_strength
  debt_log
  metadataTruthDebt_remaining
  ```

* **Use typed Go constants**
  Not just:

  ```go
  type WitnessStatus string
  ```

  but also:

  ```go
  const WitnessInvalid WitnessStatus = "invalid_by_declared_metadata"
  ```

## Next action

Proceed to:

> **TC-1B — First Go-Executable Toy Check Specification**

But with this boundary:

```text
Next = draft TC-1B spec
Not yet = Go implementation
Never yet = promotion or physics claim
```

The first TC-1B draft should be a **paper specification** that instantiates concrete `S`, `U`, `Π`, label rule, history enumeration, null models, type guardrails, and JSON report schema — but still does not run code.

