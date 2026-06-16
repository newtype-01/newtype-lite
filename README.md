# newtype Lite

Lightweight content-team workflows for agent environments, packaged as Skills.

[简体中文](README.zh.md)

## What Is newtype Lite?

newtype Lite is a self-contained Skills package that brings part of the newtype content workflow into agent environments without requiring the full newtype OS runtime.

It turns a compatible agent into a lightweight content team router for:

- planning and shaping content briefs
- research and source organization
- analysis and synthesis
- writing articles, reports, posts, scripts, and newsletters
- editing and restructuring drafts
- fact-checking claims
- extracting useful information from supplied material
- archiving reusable knowledge summaries

newtype Lite is designed for users who want the method layer of newtype in a portable Skills format. It can be used with Codex and other agent systems that support Skill-style instructions.

## newtype Lite vs. newtype OS

newtype Lite is not a replacement for newtype OS.

| Capability | newtype Lite | newtype OS |
| --- | --- | --- |
| Delivery model | Skills package | Full CLI product |
| Runtime | Uses the current agent session | Dedicated newtype runtime |
| Agents | Simulated through method packs | Full multi-agent workflow |
| Background tasks | Not included | Included where supported |
| Knowledge workflow | Lightweight summaries | Full project workflow |
| Best for | Quick content workflows inside compatible agents | Complete newtype experience |

If you want the full experience, including the integrated CLI, richer workflow orchestration, and full product behavior, deploy or install newtype OS instead.

## How It Works

The Skill uses `SKILL.md` as the router. Depending on the task, it loads only the relevant method pack from `references/`:

- `workflow.md` for end-to-end publishable content
- `interviewer.md` for clarifying ideas and briefs
- `researcher.md` for source-backed research
- `analyst.md` for comparison, diagnosis, and synthesis
- `writer.md` for drafting
- `editor.md` for polishing and restructuring
- `fact-checker.md` for verification
- `extractor.md` for turning raw material into usable notes
- `archivist.md` for reusable knowledge cards

This keeps the workflow lightweight while still preserving the core newtype approach: brief before draft, source basis before claims, structure before prose, and verification before confidence.

## Installation

Install it into a Skills-compatible agent environment. For Codex, you can use:

```bash
mkdir -p ~/.codex/skills/newtype-lite
cp -R SKILL.md references ~/.codex/skills/newtype-lite/
```

Then restart Codex or reload your Skill environment. For other agents, place `SKILL.md` and `references/` wherever that agent expects Skills.

## Usage

Ask your agent for a content task and mention newtype Lite when useful:

```text
Use newtype Lite to help me turn these notes into a publishable article.
```

```text
用 newtype Lite 帮我研究这个选题，并写一篇公众号文章。
```

For simple tasks, the Skill loads one method pack. For more complex work, it moves through the needed stages step by step.

## Repository Structure

```text
.
├── SKILL.md
└── references/
    ├── analyst.md
    ├── archivist.md
    ├── editor.md
    ├── extractor.md
    ├── fact-checker.md
    ├── interviewer.md
    ├── researcher.md
    ├── workflow.md
    └── writer.md
```

## Relationship To newtype OS

newtype Lite carries the lightweight workflow ideas from newtype OS into a Skill-only package. It is useful when you want a portable, no-runtime version of the content team methods.

For production use, full orchestration, and the complete newtype product experience, use newtype OS.

## Links

YouTube: [youtube.com/@huanyihe777](https://www.youtube.com/@huanyihe777)
Twitter: [x.com/huangyihe](https://x.com/huangyihe)
Substack: [newtype.pro](https://newtype.pro/)
