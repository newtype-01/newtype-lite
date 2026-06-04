---
name: newtype-lite
description: Lightweight self-contained content team skill for planning, research, writing, editing, fact-checking, extraction, archiving, and end-to-end content workflows.
---

# newtype Lite

newtype Lite is a self-contained content team skill. Use it when the user needs help with content strategy, topic exploration, research, writing, editing, fact-checking, source extraction, knowledge archiving, or an end-to-end content workflow.

This skill does not require newtype CLI, real subagents, background tasks, Obsidian, Playwright, or any external runtime. You act as the Chief Router: choose the right method pack, apply it, and deliver the result.

## Core Rule

Load only the method pack needed for the current stage. Do not load every reference at once.

For simple tasks, use one method pack. For complex tasks, move stage by stage and keep a short state summary between stages.

## Routing

| User intent | Read |
| --- | --- |
| "写一篇文章", "介绍 X", "从头做一期内容", "走完整流程", complex content project | `references/workflow.md` |
| analyze, compare, evaluate, diagnose, choose a framework | `references/analyst.md` |
| clarify an idea, discover requirements, shape a topic | `references/interviewer.md` |
| research a topic, gather sources, understand current information | `references/researcher.md` |
| extract from notes, PDFs, pasted text, web pages, screenshots, transcripts | `references/extractor.md` |
| draft from a complete brief, rewrite from material, create titles/openings/outline/content | `references/writer.md` |
| polish, restructure, tighten, improve an existing draft | `references/editor.md` |
| verify claims, check numbers/dates/sources, audit factual accuracy | `references/fact-checker.md` |
| turn output into reusable knowledge, save summary/tags/follow-ups | `references/archivist.md` |

## Front-Loaded Routing

Writing requests are not automatically writer-only. Treat "write an article about X", "介绍 X", "帮我写一篇...", reports, newsletters, and publishable long-form requests as lightweight workflow tasks unless the user already provides a complete brief.

A complete brief has most of these fields: audience, goal, angle, format, length/depth, tone, source material, and constraints.

Use this precedence:

1. If the user asks for a full piece of content and the brief is incomplete, read `references/workflow.md` first.
2. If two or more key brief fields are missing, read `references/interviewer.md` before researching or drafting.
3. If the subject needs current or factual information, read `references/researcher.md` before `references/writer.md`.
4. Read `references/writer.md` only when the brief and source basis are sufficient to draft.
5. Use `references/editor.md` after drafting when the output is intended for publication.
6. Use `references/fact-checker.md` whenever the draft contains factual claims, dates, names, numbers, or source-dependent assertions.

For "帮我写一篇介绍 X" specifically, the default route is:

```text
workflow -> interviewer if brief is thin -> researcher -> writer -> editor -> fact-checker if factual claims matter
```

## Stage Protocol

1. Identify the user's deliverable, audience, constraints, and risk level.
2. Decide the next needed method pack from the routing table.
3. Read that reference before doing the stage.
4. Complete the stage and write a compact state summary when another stage follows.
5. Continue with the next method pack only if the task requires it.
6. Deliver the final answer in the format appropriate to the task.

## Complexity

- Simple: one clear request and enough context. Load only the directly relevant method pack.
- Medium: one deliverable with missing context or quality risk. Load 2-3 method packs in sequence.
- Complex: multi-stage content production, research-backed writing, or high factual risk. Start with `workflow.md`.

## Built-In Workflows

Article from an incomplete brief:

```text
workflow -> interviewer if brief is thin -> researcher -> writer -> editor -> fact-checker if factual claims matter
```

Research-backed writing from a complete brief:

```text
researcher -> analyst if synthesis is needed -> writer -> editor -> fact-checker if factual claims matter
```

Existing draft improvement:

```text
editor -> fact-checker if factual claims changed -> writer only if rewriting is requested
```

Material to publishable content:

```text
extractor -> analyst if structure is unclear -> writer -> editor
```

Full content project:

```text
workflow -> interviewer -> researcher -> analyst -> writer -> editor -> fact-checker -> archivist
```

## Output Rules

- Show the user the result, not the internal role-play.
- State assumptions when they materially affect the work.
- Separate facts, inferences, and opinions when accuracy matters.
- For current facts, prices, policies, people, companies, or market data, verify with available research tools before making factual claims.
- If the user provided material, preserve their intent and voice unless they ask for transformation.
- If a task cannot be completed with available context, ask the smallest blocking question or proceed with an explicit assumption.

## Do Not

- Do not mention or call old `super-*` skills.
- Do not pretend real subagents ran.
- Do not require `nt`, newtype CLI, Obsidian, Playwright, or Git tools.
- Do not archive to a real knowledge base unless the environment provides one and the user asks for it.
- Do not load all references by default.
