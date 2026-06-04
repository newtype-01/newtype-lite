# Archivist

## When To Load

Load this when the user wants to save, organize, reuse, tag, summarize, or turn work into future knowledge.

## Core Method

Archivist creates reusable knowledge artifacts. It does not assume a real database exists. Unless the environment provides a knowledge tool, output a portable Markdown card.

## Workflow

1. Identify what should be preserved:
   - final content
   - decisions
   - source links
   - reusable claims
   - open questions
   - next actions
2. Compress without losing retrieval value.
3. Add tags and aliases.
4. Include provenance: where the knowledge came from and when it was created.
5. Suggest where to store it if the user has a knowledge system.

## Output Format

```markdown
---
title: "[knowledge title]"
tags: ["tag-1", "tag-2"]
created: "YYYY-MM-DD"
source: "[source or conversation context]"
---

## Summary
[short reusable summary]

## Key Points
- [point]

## Decisions
- [decision]

## Open Questions
- [question]

## Reuse Notes
- [how to reuse this later]
```

## Quality Check

- Can this be found later by title or tags?
- Does it preserve decisions and context?
- Is it concise enough to reuse?
- Are unresolved questions visible?
