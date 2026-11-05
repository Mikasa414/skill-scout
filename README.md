# Skill Scout

### Describe your task. Get relevant AI skill recommendations automatically.

[中文说明](README.zh-CN.md) · [Example conversation](examples/interview-to-report.md) · [Make it yours](CUSTOMIZING.md) · [Contribute](CONTRIBUTING.md)

**Skill Scout recommends AI skills based on what you want to do.** Describe your task in plain language: it clarifies the essentials, checks your installed skills and tools, and searches for additional candidates when needed. You get numbered recommendations with reasons and sources.

When skill selection is needed, choose the skills you want, review the workflow, then approve execution. If the requirements are clear and available capabilities already cover the task, Scout completes it directly. Existing selections, plans, and authorization are reused.

**One complex task can use several skills at each step.** Simple tasks stay simple.

```mermaid
flowchart LR
    A[Your task] --> B[Clarify the essentials]
    B --> C[Numbered skill options]
    C --> D[Your selection]
    D --> E[Workflow and skill handoffs]
    E --> F[Your confirmation]
    F --> G[Execute and verify]
```

## A 30-second example

> **You:** Turn ten interview transcripts into a product insights report and a presentation.
>
> **Scout:** Who is the audience? Which files do you need? Should findings link back to quotes?
>
> **You:** Product team. A report, slides, and charts. Keep the evidence.
>
> **Scout:** 1. Spreadsheet skill for an evidence table and charts. 2. Document skill for the report. 3. Presentation skill for the slides. These are illustrative roles; actual recommendations depend on installed and verified candidates.
>
> **You:** 1, 2, and 3.
>
> **Scout:** Extract evidence → build the analysis table with 1 → write the report with 2 → create slides with 3 → verify quotes, counts, and consistency. Each step specifies its inputs and outputs. Proceed?
>
> **You:** Yes.

[Read the full walkthrough →](examples/interview-to-report.md)

## Why use it?

| What you need | What Scout does |
|---|---|
| Skills matched to your task | Automatically identifies relevant capability areas and recommends candidates |
| A clearer task | Asks up to three questions that affect the recommendation |
| Skills you can choose | Numbers candidates and explains the fit, source, and installation status |
| Fewer duplicate installations | Checks available skills, plugin skills, and tools first |
| Help with a complex step | Combines complementary skills; reuses the same skill across steps |
| A plan you can understand | Shows actions, skill use, inputs, outputs, and acceptance checks |
| Honest recommendations | Separates description screening, source inspection, and actual testing |

## Three exceptions that keep it practical

1. **Simple, clear task:** do it directly, without a forced selection ritual.
2. **Task with meaningful skill tradeoffs:** use the necessary selection stages; ask only useful questions and normally offer two or three relevant options per capability area. One valid option is enough. Multiple outputs or steps alone do not require the full workflow.
3. **“You choose, go ahead”:** skip selection and workflow confirmation within the user's authorization. This does not grant unrelated permissions.

Clear requirements and known capabilities take the direct path, even for several related text outputs. Missing essential input calls for clarification; reversible style choices can use stated assumptions. An explicit request to see options or a plan still takes precedence. After a workflow, its impacts, and acceptance checks have been shown, “choose 1 and execute this plan” can combine selection and execution confirmation. Choosing a number alone does not authorize execution or installation.

## Install in Codex

Ask the built-in installer:

```text
$skill-installer Install the skill from https://github.com/Mikasa414/skill-scout (skill directory: repository root).
```

Or clone into a supported local skill directory. First check that the destination does not already contain a different copy.

**macOS / Linux**

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/Mikasa414/skill-scout.git ~/.agents/skills/skill-scout
```

**Windows PowerShell**

```powershell
$skillParent = Join-Path $HOME '.agents/skills'
New-Item -ItemType Directory -Path $skillParent -Force | Out-Null
git clone https://github.com/Mikasa414/skill-scout.git (Join-Path $skillParent 'skill-scout')
```

Current [official skill documentation](https://learn.chatgpt.com/docs/build-skills) lists `.agents/skills` locations. The original local setup used `~/.codex/skills`; use your host's discovered location and avoid installing duplicate copies. If the skill does not appear, restart Codex.

Then try:

```text
$skill-scout Help me turn customer interviews into an evidence-backed report and slides. Ask the key questions, recommend numbered skills, and show the workflow before execution.
```

For an explicit fast path:

```text
$skill-scout Find the best available skills for this task. You choose, go ahead. Use installed skills only.
```

## What ships

- `SKILL.md`: the workflow and its boundaries.
- `references/`: question gates, discovery, candidate evaluation, and output guidance.
- No bundled executable scripts, API keys, or required third-party packages.

Skill Scout is an instruction-based Codex skill. Search and execution depend on the tools and other skills available in your environment. It does not include transcription, document production, or a hosted skill search service. Existing connector access remains necessary where applicable.

The skill instructions are currently written in Chinese; this README and the walkthrough include English. Other hosts and English-output behavior have not been independently validated. Start with an explicit invocation and tell the agent your preferred response language.

## Fork it for your workflow

Build a version for research, product discovery, teaching, or development. Start with [the customization guide](CUSTOMIZING.md): change the questions, candidate criteria, and handoffs while preserving clear authorization boundaries.

Useful contributions include reproducible examples, better discovery paths, English instruction variants, and reports of recommendations that missed the task. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Validation status

The updated skill passed the bundled format validator and local reference checks. In a small text-only comparison, two independent evaluation agents each answered the same eight scenarios, one using the previous version and one using the updated version. Routing matched the review criteria in 6/8 previous-version cases and 8/8 updated-version cases. The observed improvement was direct delivery on two fully specified, multi-part text tasks. Each version had one batch of eight scenarios, without repeated trials or a fresh session per scenario; these counts are not overall success rates. External skill discovery, third-party installations, cross-host behavior, and complete multi-turn production workflows were not tested. The walkthrough remains a simulated conversation.

## License

[MIT](LICENSE) · Copyright 2026 Mikasa414.
