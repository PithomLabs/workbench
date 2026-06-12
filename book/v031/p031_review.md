## P031 synthesis: TC-1A v0.3.1 review

The reviews broadly agree:

> **TC-1A v0.3.1 is a real improvement, but it needs a small v0.3.2 cleanup before TC-1B.**

It successfully reduces overclaim, replaces vague `Prop` placeholders with auditable metadata, adds null-model criteria, and provides a Go report schema. But several reviewers caught the same remaining cracks: undefined `endpoint`, undefined `CoarseAlternatives`, self-reported boolean metadata, `allowedStarts` hand-selection risk, vague random/permutation thresholds, and incomplete canonical encoding.   

## Quality comparison of the reviews

| Reviewer            |     Quality | Best contribution                                                                                                                             | Caveat                                                                                                          |      Weight |
| ------------------- | ----------: | --------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ----------: |
| **Claude**          |   Very high | Best at identifying the **self-reporting Bool problem**, `allowedStarts` loophole, undefined thresholds, and missing Go sub-schemas.          | Conservative, but very useful for preventing cracks.                                                            |   Very high |
| **DeepSeek**        |        High | Clear actionable list: define `endpoint`, `CoarseAlternatives`, canonical encoding, and runtime aborts for invalid metadata.                  | Slightly more optimistic about proceeding.                                                                      |        High |
| **Gemini**          |        High | Strong practical focus on exact thresholds for random success and generic permutations.                                                       | Treats metadata as more enforceable than it actually is.                                                        |        High |
| **Kimi**            |   Very high | Best at EBP skepticism: catches self-reported metadata, undefined terms, `allowedStarts`, `maxLength`, and “witness” terminology risk.        | Very strict; some concerns are acceptable as named debts.                                                       |   Very high |
| **Poolside**        | Medium-high | Concise and useful: says proceed with acknowledged debt, but flags undefined terms and missing thresholds.                                    | Less detailed than Claude/Kimi.                                                                                 |      Medium |
| **Qwen**            |        High | Strong confidence in proceeding, with one good fix: align canonicalization between Lean and Go.                                               | Too generous about “hard firewall” from booleans.                                                               | Medium-high |
| **Z**               |        High | Good summary: v0.3.1 structurally repairs v0.3 and can proceed if remaining definitions are handled in TC-1B.                                 | Slightly too willing to defer `endpoint`/`CoarseAlternatives`.                                                  |        High |
| **Research report** |       Mixed | Useful long-form synthesis: emphasizes type-level Go guardrails, Lean semantic contracts, JSON audits, and parity/XOR as primary null model.  | It overstates some claims and includes external references unevenly; use as supporting material, not authority. |      Medium |

## Integrated verdict

TC-1A v0.3.1 should remain:

```text
alive / clarified / unpromoted / nearly ready for TC-1B
```

But before TC-1B, we should write a **very small patch**:

> **TC-1A v0.3.2 — Definition and Enforcement Patch**

Not a major rewrite. Just a cleanup patch to make sure nothing slips through.

## Required v0.3.2 fixes

* **Define `endpoint` explicitly**

  ```text
  endpoint(h) = U iterated h.length times from h.start
  ```

* **Define `CoarseAlternatives` explicitly**

  ```text
  h1 ≠ h2 and Π(endpoint(h1)) = Π(endpoint(h2))
  ```

* **Make canonical encoding exact**
  Specify the exact string format, sorting rules, separator rules, ordered/unordered argument handling, and escaping.

* **Handle self-reported metadata honestly**
  `handPainted = false` and `fixedBeforeWitness = true` are audit declarations, not proof. Go can enforce the declared fields, but cannot prove the historical fact unless the workflow records construction order.

* **Require runtime enforcement**
  Go must abort or mark invalid if:

  ```text
  handPainted = true
  fixedBeforeWitness = false
  usesTargetOutcome = true
  usesWitnessLabel = true
  deduplicate = false
  ```

* **Fix `allowedStarts` / `maxLength` loophole**
  Require either:

  ```text
  allowedStarts = all states
  ```

  or a declared, pre-registered start-selection rule with justification.

* **Add thresholds**
  Define how random-label and generic-permutation nulls downgrade results:

  ```text
  random success near expected baseline => downgrade_to_random_label_artifact
  generic permutation witness rate above threshold => downgrade_to_generic_permutation_artifact
  ```

* **Require `independentlyJustified` or explicitly mark it open**
  If `Π` is not independently justified, result should carry:

  ```text
  coarse_graining_selection_debt_open
  ```

* **Clarify parity/XOR result statuses**

  ```text
  replicated_by_parity_xor => downgrade_to_classical_parity_artifact
  arithmetic_only_match => survives_with_parity_debt_open
  parity_xor_fails => parity_null_survived
  ```

## Next move

The right next step is:

```text
TC-1A v0.3.2 — Definition and Enforcement Patch
```

Then:

```text
TC-1B — First Go-Executable Toy Check Specification
```

So the P031 batch did **not** send us backward. It tightened the final pre-Go boundary. This is exactly the EBP process working: the patch survived, but the reviewers found the cracks before implementation.

