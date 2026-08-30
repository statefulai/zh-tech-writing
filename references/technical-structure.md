# Technical document structure

Choose sections according to the decision the document must support. Do not force every document into one template.

## Common information jobs

- **Purpose and audience:** what decision or action the document enables.
- **Context and current state:** relevant constraints and verified existing behavior.
- **Goals and non-goals:** what changes and what remains outside scope.
- **Decision and alternatives:** selected approach, rejected options, and trade-offs.
- **System impact:** affected components, data flow, ownership, and compatibility.
- **Contracts:** inputs, outputs, schemas, permissions, ordering, and invariants.
- **Failure and recovery:** partial failure, fallback, rollback, and data safety.
- **Delivery:** dependencies, rollout sequence, migration, and release gates.
- **Verification:** tests, observability, runtime evidence, and acceptance criteria.
- **Open decisions:** unresolved items, owners, and consequences.

Include only the jobs relevant to the document. A short decision note may need four sections; a cross-system implementation plan may need most of them.

## Structural review signals

- multiple top-level titles without a clear hierarchy;
- empty, duplicate, or placeholder sections;
- authoring instructions or chat residue inside the deliverable;
- conclusions before the evidence they depend on;
- API details without their role in the end-to-end flow;
- implementation details mixed with unresolved product decisions;
- rollout steps without rollback or acceptance gates;
- diagrams that repeat prose without adding relationships.

## Reorganization rule

Move a claim together with its qualifier, evidence, citation, and exception. Do not separate a number from its measurement scope or a decision from the trade-off that explains it.
