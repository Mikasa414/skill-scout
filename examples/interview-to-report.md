# Example: interviews → evidence table → report → slides

[Back to README](../README.md) · [中文首页](../README.zh-CN.md)

This is a simulated conversation. Skill labels below describe capability roles, not verified downloadable packages. They must be replaced by candidates actually available in the user's environment.

**User:** Turn ten customer interviews into a report and a presentation.

**Scout:** Three details will shape the workflow:
1. Are the interviews text or audio? I suggest using transcripts when available; audio adds a transcription step.
2. Who will read the output? I will assume a product team unless you say otherwise.
3. Which deliverables do you need? I suggest an evidence table, a report, and about ten slides.

**User:** Text transcripts. Product team. All three, with charts and traceable quotes.

**Scout:** Here is the proposed skill combination:

| # | Capability role | Contribution |
|---|---|---|
| 1 | Spreadsheet skill | Evidence table, participant-level counts, charts |
| 2 | Document skill | Findings, supporting quotes, limitations |
| 3 | Presentation skill | Concise slides using the same findings and charts |

In a real recommendation, each row also includes a verified skill name, source, installation status, and inspection level. Choose numbers or ask me to select.

**User:** 1, 2, 3.

**Scout:** Proposed workflow:

| Step | Action and capability | Input → output |
|---|---|---|
| 1 | Read transcripts with general analysis | Transcripts → quotes and candidate needs with references |
| 2 | Use 1 to structure evidence and count participants | Evidence → workbook and charts |
| 3 | Assess needs and uncertainty with general analysis | Workbook and source text → supported findings |
| 4 | Use 2 to produce the report | Findings, quotes, charts → report |
| 5 | Use 3 to build the presentation | Report and charts → about ten slides |
| 6 | Verify evidence and consistency | All files → checked deliverables |

Count participants mentioning an issue rather than repeated mentions by one person. Separate evidence from interpretation. Deliver a workbook, report, and slide deck; confirm formats against the selected skills. If any selected skill requires installation, disclose source, destination, and dependencies here before approval. Proceed?

**User:** Proceed.

The agent then carries out the authorized plan and reports actual checks and limitations. It does not claim completion without producing the artifacts.

## If a step becomes more complex

A specialized qualitative-analysis skill can complement the spreadsheet skill in steps 1–3. Add a new unique number, explain the evidence handoff, and include it in the reviewable plan. The whole task is not restricted to three skills.

## 中文简版

你：十份访谈做成报告和 PPT。

Scout：先确认文字或录音、汇报对象、交付物。

你：文字，产品团队，要表格、报告和图表 PPT。

Scout：编号推荐表格、文档和演示技能，说明真实来源和可用状态，等你选择。

你：选 1、2、3。

Scout：解释提取证据、统计制图、分析需求、编写报告、制作 PPT 和验证的一整套流程，标出每步技能的输入输出，然后问是否执行。

你确认后再执行。复杂步骤可组合多个技能；简单步骤不强行配技能。
