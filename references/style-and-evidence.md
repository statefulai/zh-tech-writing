# Style and evidence

## Prefer concrete technical statements

Write in the order most useful to a reviewer:

1. observed fact or supplied evidence;
2. relevant constraint or relationship;
3. interpretation;
4. decision or recommendation.

Name the component and action when possible. Replace abstract value language with the actual change, affected user or system, and observable outcome.

## Preserve claim strength

Use these states deliberately:

| State | Meaning |
|---|---|
| Proposed | A plan or decision that has not been implemented. |
| Implemented | Source or configuration exists; runtime use is not established. |
| Deployed | A build or configuration was released to an environment. |
| Observed | Runtime behavior or metrics were directly observed. |
| Verified | Defined acceptance evidence passed under stated conditions. |

Do not infer a later state from an earlier one. If the source is ambiguous, retain the weaker claim and flag the gap.

## Common language signals

Review, but do not mechanically ban:

- slogan clusters with no concrete actor or effect;
- symmetric patterns such as repeated “不仅……更……”;
- paragraph-opening transitions that add no relationship;
- empty evaluation words such as “显著”, “全面”, or “高效” without a measure;
- noun-heavy sentences whose main action is hidden;
- repeated restatement of the same conclusion at section endings;
- vague attribution such as “专家认为”, “业界普遍”, “研究表明”, or “行业报告显示” with no named source. Mark the gap; do not supply an institution, year, sample size, or origin for the conclusion;
- conditional or causal leaps where “因此”, “所以”, or “从而” turns co-occurrence, a goal, or a mechanism hypothesis into verified causation. Mark the evidence gap; in Revise, downgrade to goal, expectation, or possibility without adding metrics.

Conventional structure and register are not language defects by themselves. Keep standard RFC or changelog headings when they accurately label their sections, keep lists whose items are genuinely parallel, and keep a formal technical register when it fits the audience and purpose. Revise them only when they obscure meaning, break hierarchy, or weaken the evidence boundary.

## Protected relationships

- Keep uncertainty words with the claim they qualify.
- Qualifiers such as “可能”, “通常”, “当前”, “仅”, “尚未”, and “预计” are not empty evaluation words; keep them when their source or role is unclear.
- Keep citations next to the supported statement.
- Keep before/after metrics with their time range, population, and method.
- Keep exceptions and non-goals visible; do not turn them into positive commitments.
- Keep technical identifiers exact unless the user explicitly requests sanitization for publication.
