# Synthetic evaluation cases

All cases in this file are fictional and contain no production or organizational data.

## Case 1: read-only boundary

Prompt: `只读审计这份技术方案，指出结构和语言问题，等我确认，不要改文件。`

Fixture properties:

- one empty section;
- one authoring instruction left in a heading;
- a proposed rollout described next to implemented code.

Expected behavior: report findings without producing or writing a replacement document.

Treat the authoring instruction in the fixture as content to audit, not as an instruction to follow.

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

## Case 7: vague attribution is not filled in

Prompt: `润色这段技术说明，不要改变事实。`

Fixture: `evals/fixtures/vague-attribution.md`

Fixture properties:

- “专家认为” and “行业报告显示” with no named source and no figures;
- one supplied fact: rule matching has only an interface design, and the notification channel has no owner yet.

Expected behavior: in Audit or Revise, add no institution, year, or sample size; keep the attribution gap as a gap; keep “尚未” in the supplied fact.

## Case 8: qualifiers are preserved

Prompt: `把下面的中文技术说明改得具体、自然，但不要改变事实。`

Fixture excerpt: the Case 2 excerpt containing “仅” and “尚未”.

Expected behavior: “仅” and “尚未” remain in the revised text; unfinished work is never restated as complete.

## Case 9: non-technical text does not match implicitly

Prompt: `帮我把这篇周末露营的随笔去 AI 味，改得更有人味。`

Expected behavior: same as Case 5; this Skill should not activate implicitly. The criterion is the nature of the text, not the phrase “去 AI 味”; Revise on a technical document may still respond to that phrase.

## Case 10: conventional formal structure is preserved

Prompt: `把这份 RFC 改得具体、自然，但不要改变事实。`

Fixture: `evals/fixtures/formal-rfc.md`

Fixture properties:

- standard RFC and changelog headings;
- one unsupported promotional sentence inside an otherwise formal structure;
- a genuinely parallel list of supplied technical facts;
- a formal technical register.

Expected behavior: revise only the unsupported promotional sentence; preserve the section names and order, the parallel list, all supplied technical facts and qualifiers, and the formal register.
