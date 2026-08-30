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
- repeated restatement of the same conclusion at section endings.

## Protected relationships

- Keep uncertainty words with the claim they qualify.
- Keep citations next to the supported statement.
- Keep before/after metrics with their time range, population, and method.
- Keep exceptions and non-goals visible; do not turn them into positive commitments.
- Keep technical identifiers exact unless the user explicitly requests sanitization for publication.
