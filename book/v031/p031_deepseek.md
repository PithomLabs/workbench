**Overall verdict:**
Yes, v0.3.1 successfully repairs the named weaknesses of v0.3. The patch replaces ambiguous `Prop` promises with explicit metadata, boolean audit fields, and concrete generation rules. It renames terms to reduce overclaim, adds falsifiable null-model criteria, and imposes a structured Go output schema. It remains a debt-bearing semantic-boundary patch, not a physics promotion.

**Remaining undefined terms:**
- `CoarseAlternatives : CoarseGraining M → History M R → History M R → Prop` — used in `SignedTallyCancellationWitness` but not defined in this patch; presumably inherited from an earlier artifact but should be explicitly included or referenced.
- `endpoint : History M R → M.State` — used throughout but its definition (via iteration of `R`) is only hinted at; needs a concrete definition for Lean/Go.
- `nodeCount`, `relation records` sorting in canonical encoding — described in prose but not fully formalised; the rule is first‑implementation but needs to be spelled out as a deterministic algorithm before Go execution.

**Hidden imports still present:**
- All structures from the previous TC-1A framework (`MicroSpace`, `ReversibleUpdate`, `History`, etc.) are assumed. The patch does not re‑declare them, so their precise signatures remain a prerequisite. `CoarseAlternatives` and `endpoint` are the main gaps that are not obviously defined in this patch.

**Terminology assessment:**
The renamings (`UnlabeledCount`, `SignedTally`, `SignedTallyCancellationWitness`, `WitnessLabel`) are a clear improvement. They shed misleading physics connotations (`classical`, `signed count`, `non‑additive`) and anchor the language in finite bookkeeping. The forbidden-inference rule and mandatory disclaimer further guard against overclaim. The debt acknowledgment (why‑summation, origin‑of‑signs) keeps the terms honest. The terminology patch is therefore effective.

**Label‑rule and coarse‑graining metadata assessment:**
Both `LabelRuleSpec` and `CoarseGrainingSpec` replace mere promises with explicit boolean fields (`handPainted`, `fixedBeforeWitness`, `usesTargetOutcome`, etc.) and admissibility conditions. This makes hand‑painted labels and result‑driven coarse‑grainings auditable. The rule that `usesCoarseState = true` triggers stricter review is a good guard. The metadata is sufficient for a toy‑check, provided the Go implementation actually enforces the admissibility conditions at run time (e.g., rejecting a run if `handPainted = true`). The patch does not specify that runtime check, but the semantics are clear enough for a draft.

**History enumeration assessment:**
`HistoryEnumerationSpec` with `allowedStarts`, `maxLength`, and mandatory `deduplicate = true` prevents hand‑selected and duplicate histories. The requirement that the Go code generate histories from the spec, not from a manually chosen list, is explicitly stated. This repair is solid.

**Null‑model criteria assessment:**
The nine null models (constant label, endpoint‑only, random label, hand‑painted anti‑model, identity coarse‑graining, constant coarse‑graining, generic permutation, parity/XOR, cycle‑length) each come with a pass/fail criterion and a downgrade status. The random‑label null mandates reporting frequency, not just binary outcome, and correctly notes that a single two‑history cancellation is weak evidence. This is a pragmatic and sufficiently strong battery for a toy check. It does not guarantee physical relevance, but it catches the most obvious artifacts.

**Go output schema assessment:**
The schema is comprehensive: it captures instance specification, main witness result, detailed null‑model outcomes, distributional summary, debt ledger, and a forbidden‑inference audit. It ensures that no run can accidentally claim quantum behaviour. The schema is sufficient for a reproducible, auditable toy check.

**Should TC‑1B proceed?**
Yes. The patch fixes the terminology, metadata, enumeration, and null‑model gaps that blocked v0.3. TC‑1B now has unambiguous entry criteria and a concrete output contract. The remaining debts (origin‑of‑signs, why‑summation, etc.) are explicitly documented and do not block a toy‑level implementation.

**Required edits before TC‑1B:**
1. **Define `CoarseAlternatives` explicitly.** Without it, the witness condition is incomplete.
2. **Define `endpoint` concretely** (e.g., by iterating `R` on the start state for `length` steps) so that the count functions are well‑founded.
3. **Specify the canonical‑encoding algorithm precisely** enough to be coded (e.g., exact string format, handling of ordered/unordered argument lists, escaping). The prose is a good start but must become a deterministic function.
4. **Add a note in the admissibility conditions** stating that the Go implementation must read the metadata fields and abort if `handPainted = true`, `fixedBeforeWitness = false`, etc., are encountered. This turns metadata promises into runtime enforcements.

**Smallest useful next move:**
Draft the concrete instance for TC‑1B: fix a small `MicroSpace` (`S`), a bijective `U`, a specific `Π`, a specific label rule (e.g., transition‑parity or endpoint‑only), and a bounded `HistoryEnumerationSpec`, then implement the canonical encoding and null models, producing the Go output schema. This will immediately surface any remaining ambiguity in the repaired definitions.
