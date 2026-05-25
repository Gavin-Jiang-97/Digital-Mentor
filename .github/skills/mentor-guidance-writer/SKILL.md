---
name: mentor-guidance-writer
description: 'Package and apply a mentor-style wireless-paper writing workflow using a curated knowledge base. Use when the user says 写作指引, 导师风格写作, 无线通信短文, WCL introduction, refine wireless letter, update style_profile/outline_template/hard_memory/soft_memory, or wants a reusable mentoring skill for junior students.'
argument-hint: 'Describe the target file or section, target venue, whether this is zero-to-one drafting or local revision, the reference papers or source notes, and whether the packaged knowledge base itself should be updated.'
user-invocable: true
---

# Mentor Guidance Writer

This skill packages a mentor-style writing workflow for wireless short papers. It keeps the disciplined structure of the existing paper-polish workflow, but narrows the knowledge base to a portable subset that can be published and reused by junior students. The default target is an IEEE Wireless Communications Letters style short paper unless the user explicitly overrides the venue.

## When To Use

- Draft a wireless short paper from zero using a small set of curated reference papers.
- Revise an existing introduction, system model, method section, experiment section, or conclusion.
- Convert Chinese notes into idiomatic academic English instead of literal translation.
- Ask the agent to follow a mentor-like writing discipline rather than generic smoothing.
- Maintain the packaged knowledge base by refining `style_profile.md`, `outline_template.md`, `hard_memory.json`, or `soft_memory.json`.
- Coach junior students who need both writing structure and sentence-level guidance.

## Packaged Knowledge Base

Always read these files before making substantive writing changes:

- `knowledge_base/style_profile.md`
- `knowledge_base/outline_template.md`
- `knowledge_base/hard_memory.json`
- `knowledge_base/soft_memory.json`

Read this file when the task includes human review, recurring mistake diagnosis, or knowledge-base maintenance:

- `knowledge_base/error_log.md`

## Non-Negotiable Rules

- Treat `style_profile.md`, `outline_template.md`, `hard_memory.json`, and `soft_memory.json` as mandatory constraints, not optional inspiration.
- Default the structure and tone to IEEE Wireless Communications Letters style only when the user has not named another target venue.
- Separate two working modes: `Zero-to-one drafting` and `Local revision`. Do not blur them.
- If the task requires a large rewrite, a new section plan, or a knowledge-base update, show `<Writing_Plan>` before editing.
- Do not literally translate Chinese source material. Rewrite into natural academic English with explicit logic.
- Keep terminology, abbreviations, and unit reporting consistent with `hard_memory.json`.
- Keep sentence rhythm, paragraph handoff, and reviewer-facing tone consistent with `style_profile.md` and `soft_memory.json`.
- Do not mutate the packaged knowledge base during routine drafting unless the user explicitly asks for a knowledge-base update.
- Use `error_log.md` as a human-facing refresher and diagnostic aid. Do not blindly force every logged correction into unrelated tasks.

## Decision Logic

### 1. Classify The Task

- `Zero-to-one drafting`: the user has a topic, notes, or reference papers, but no finished prose.
- `Local revision`: the user already has text and wants targeted improvement.
- `Knowledge-base maintenance`: the user wants to update the package itself.

### 2. Decide Whether Approval Is Required

- If the task is a narrow local revision, proceed after reading the required context.
- If the task changes section structure, contribution framing, or experiment logic, summarize the intended change before editing.
- If the task is zero-to-one drafting of multiple sections or a package update, output `<Writing_Plan>` first and wait for approval.

### 3. Decide Which Knowledge Source Drives The Work

- Use `outline_template.md` to control section order, paragraph budgets, and page discipline.
- Use `style_profile.md` to control rhetoric, paragraph logic, and anti-AI writing habits.
- Use `hard_memory.json` to keep terminology, abbreviations, units, and fixed venue facts stable.
- Use `soft_memory.json` to tune phrasing, tone, and sentence-level readability.
- Use `error_log.md` when you need a human review lens for recurring mistakes.

## Procedure

### Step 1. Intake And Mode Selection

1. Identify the target task, target section, and target venue.
2. Read the four AI-facing knowledge-base files.
3. Decide whether the job is zero-to-one drafting, local revision, or package maintenance.
4. Extract explicit user constraints, implied stylistic preferences, and any reference papers or source notes.

### Step 2. Build A Writing Brief

Create a compact brief covering:

- task mode
- target section or deliverable
- venue and length constraints
- expected references or evidence
- structural expectations from `outline_template.md`
- style constraints from `style_profile.md`
- terminology and notation constraints from `hard_memory.json`
- tone and phrasing constraints from `soft_memory.json`

If the task is large, convert the brief into `<Writing_Plan>` with:

- objective
- affected sections
- planned structure
- expected evidence or figures
- whether the packaged knowledge base will be updated
- one-line approval request

### Step 3. Execute The Drafting Or Revision Pass

1. Draft or revise only the requested scope.
2. Keep one visible logic chain per paragraph: claim -> reason -> mechanism or evidence -> implication.
3. Use the sentence-by-sentence handoff rule to keep local flow explicit.
4. Make the introduction, system model, method, and results sections serve different rhetorical jobs instead of repeating the same framing.
5. When discussing figures, explain the question, the dominant trend, and the engineering implication.
6. If the source material is in Chinese, rewrite the logic rather than translating the shell.

### Step 4. Run Self-Review

Review the output against these checks:

- structure matches the intended short-paper format
- paragraph openings and endings hand off cleanly
- terminology and abbreviations are consistent
- contribution claims are specific and evidence-bound
- figures and results are interpreted, not just reported
- sentence rhythm is readable and not mechanically AI-like
- no obvious violations from the relevant parts of `error_log.md`

### Step 5. Maintain The Knowledge Base Only When Asked

If the user explicitly wants to improve the package:

- update `style_profile.md` for stable, high-level style preferences
- update `outline_template.md` for structural rules and venue-aware section budgets
- update `hard_memory.json` for exact terms, units, abbreviations, and fixed conventions
- update `soft_memory.json` for sentence-level preferences, phrasing, tone, and avoid-rules
- update `error_log.md` for recurring mistakes that are useful to humans during later review

When updating the package, preserve the separation between AI-facing files and the human-facing error notebook.

### Step 6. Return A Work-Oriented Result

Report:

1. current task mode
2. files drafted or revised
3. whether the packaged knowledge base was consulted only or also updated
4. what changed in the prose or workflow
5. any unresolved issue, approval gate, or missing evidence

## Quality Bar

- The output should read like disciplined wireless-paper writing, not generic academic smoothing.
- The introduction should move quickly from motivation to gap to contribution.
- The system model should be concise and should only define what later sections need.
- The method section should foreground intuition before detail.
- The results section should tie trends back to mechanism and practical implication.
- The knowledge base should remain stable, portable, and internally consistent after any maintenance pass.

## Examples

- `/mentor-guidance-writer Draft a WCL-style introduction for wireless channel estimation from these five reference papers and show me a Writing_Plan first.`
- `/mentor-guidance-writer Revise my System Model and Results sections using the packaged knowledge base, but do not update the package itself.`
- `/mentor-guidance-writer 根据这个段落和两篇参考文献，帮我重写 Introduction 的第二段与第三段，并检查是否符合短文结构。`
- `/mentor-guidance-writer Update the packaged soft_memory.json and style_profile.md based on the writing preferences we confirmed today.`