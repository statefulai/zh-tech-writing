# Synthetic evaluation cases

All cases in this file are fictional and contain no production or organizational data.

## Case 1: read-only boundary

Prompt: `只读审计这份技术方案，指出结构和语言问题，等我确认，不要改文件。`

Fixture properties:

- one empty section;
- one authoring instruction left in a heading;
- a proposed rollout described next to implemented code.

Expected behavior: report findings without producing or writing a replacement document.

## Case 2: unsupported value language

Prompt: `把下面的中文技术说明改得具体、自然，但不要改变事实。`

Fixture excerpt:

> 示例平台通过智能化能力全面打通告警闭环，显著提升研发质量。当前仅完成事件解析模块，尚未接入生产告警通道。

Expected behavior: replace unsupported value claims with the implemented fact and keep the deployment gap explicit.

## Case 3: protected technical content

Prompt: `润色这份接口设计，代码、表格、链接、数字和字段名不要动。`

Fixture properties:

- a JSON example object;
- a Markdown table;
- `https://api.example.invalid/v1/events`;
- a measured latency of `120 ms` under a stated load.

Expected behavior: revise surrounding prose while preserving every protected item and its qualifier.

## Case 4: structure without invention

Prompt: `根据这些会议结论整理技术方案结构，缺的地方标出来。`

Fixture: `evals/fixtures/structure-notes.md`

Fixture properties:

- known goal and two constraints;
- no rollback decision;
- no acceptance criteria;
- two competing implementation options with no final choice.

Expected behavior: produce an outline and explicit gaps without choosing an option.

## Case 5: trigger boundary

Prompt: `给新品发布写一段更有感染力的中文营销文案。`

Expected behavior: this Skill should not activate implicitly.

## Case 6: draft from supplied facts

Prompt: `根据这份会议纪要起草一版技术方案，未知项保留待确认。`

Fixture: `evals/fixtures/draft-notes.md`

Fixture properties:

- a synthetic component running in a test environment;
- one approved design decision;
- one proposed rollout sequence;
- missing notification owner, rollback switch, production acceptance metrics, and production evidence.

Expected behavior: produce readable technical prose for known facts, keep the rollout labeled as proposed, and mark the missing ownership and evidence without inventing them.
