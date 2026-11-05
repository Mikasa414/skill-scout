# Make Skill Scout yours

[README](README.md) · [中文说明](README.zh-CN.md)

Fork this repository and customize the instructions for a repeatable workflow. Keep the skill name and folder consistent if you rename it, and avoid installing two copies with the same name.

| Variant | Questions to change | Candidate criteria | Handoff to define |
|---|---|---|---|
| Research | Research question, source access, evidence standard | Citation support, extraction limits, reproducibility | Sources → evidence table → synthesis |
| Product discovery | Audience, interview format, decision to support | Traceability, qualitative analysis, charting | Transcripts → themes → report → slides |
| Teaching | Learner level, objectives, lesson length | Curriculum fit, answer verification, editable outputs | Materials → lesson → exercises → answer key |
| Development | Repository, desired behavior, verification | Existing tooling, dependency cost, test coverage | Requirements → implementation → meaningful checks |

## Files to edit

1. `SKILL.md`: trigger scope, questions, workflow, and exception behavior.
2. `references/question-gates.md`: domain-specific questions.
3. `references/scoring.md`: criteria for choosing candidates.
4. `references/output-format.md`: the numbered choices and workflow presentation.
5. `examples/`: a realistic conversation showing your variant.

The installed skill is instruction-based. A fork changes agent guidance, not its available tools. Check integrations and dependencies in the target environment.

## Keep these boundaries clear

Recommendations must use real sources. Choosing a skill is distinct from authorizing installation. Confirmation should describe the actual plan and its impacts. Existing user authorization should not be requested repeatedly. Explain whether a recommendation was screened, inspected, or tested.

## Try your variant

Use a clear small task, an ambiguous complex task, a task requiring several skills in one step, and a “you choose, go ahead” request. Observe whether the agent takes the expected path. Check a missing-tool case too. Record the host, prompt, tool access, and observed result rather than just a success claim.

## 中文提示

优先改领域问题、候选标准和步骤衔接。每个复杂步骤可有多个互补技能；没有合适技能时不要编造。保留编号、来源和验证程度，检查“简单任务直接做”和“明确授权跳过确认”是否正常生效。
