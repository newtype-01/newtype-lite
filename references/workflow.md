# Workflow

## When To Load

Load this for any publishable content task: article, newsletter, report, essay, script, long post, content series, or "介绍 X" style requests.

Workflow is the bottom layer of newtype Lite's content creation system. It defines the default creative path and decides which method packs can be skipped.

## Core Method

Default path:

```text
interviewer -> extractor if user supplied material -> researcher -> analyst if synthesis is needed -> writer -> editor -> fact-checker if factual claims matter -> archivist if reuse is requested
```

Do not start with Writer just because the user says "write". Writing starts only after the brief and source basis are good enough.

The workflow's job is to answer three questions:

1. What are we making?
2. What inputs are missing?
3. Which stage can be skipped without lowering quality?

Principles:

- Brief before draft.
- Source basis before claims.
- Structure before prose.
- Edit before final delivery.
- Verify factual risk before confidence.
- Skip stages only when their exit criteria are already satisfied.

## Workflow

### 1. Interview / Brief

Goal: define the content brief.

Use `interviewer.md` when the task is missing two or more of:

- audience
- goal
- angle
- format
- length or depth
- tone
- source material
- must-include / must-avoid

Skip only if the user already provides a complete brief or the task is intentionally quick and low-stakes.

Exit criteria:

- The audience is known or safely assumed.
- The content angle is clear.
- The output format is clear.
- The success standard is clear enough to draft against.

### 2. Extract / Organize Supplied Material

Goal: turn user-provided material into usable inputs.

Use `extractor.md` when the user provides notes, drafts, pasted text, transcripts, screenshots, links, PDFs, or raw research.

Skip only if there is no source material or the material is already organized into a usable brief/outline.

Exit criteria:

- Key points are extracted.
- Useful evidence/examples are separated.
- Claims that need checking are visible.
- The material can be handed to Writer or Analyst.

### 3. Research

Goal: build a factual source basis.

Use `researcher.md` when the subject depends on current information, external facts, company/product details, dates, statistics, technical claims, examples, or source credibility.

Skip only if:

- the user supplied sufficient source material,
- the piece is pure opinion or personal reflection,
- or the task explicitly says no research / use only provided material.

Exit criteria:

- Important factual claims have sources or are marked as assumptions.
- The main context is current enough for the task.
- Source gaps are known.

### 4. Analysis / Synthesis

Goal: decide the angle, structure, and interpretation.

Use `analyst.md` when the work requires comparison, argument, strategic framing, root-cause reasoning, market/technical judgment, or synthesis across sources.

Skip only if the piece is straightforward exposition or the user already provides the angle and argument.

Exit criteria:

- The central thesis or organizing idea is clear.
- The structure follows the logic of the argument, not the order of sources.
- Facts, inferences, and opinions are separated.

### 5. Writing

Goal: produce the draft.

Use `writer.md` only after the brief and source basis are sufficient.

Skip only if the user does not want prose output, or the requested output is only a plan, diagnosis, or extraction.

Exit criteria:

- The draft matches the brief.
- The opening creates a reason to keep reading.
- Sections answer likely reader questions.
- Claims that need checking are not hidden.

### 6. Editing

Goal: make the draft publishable.

Use `editor.md` for any user-facing draft longer than a short answer.

Skip only if the user explicitly wants rough notes, brainstorming, or raw output.

Exit criteria:

- Structure is coherent.
- Paragraphs each do one job.
- Sentences are clear and direct.
- Tone is consistent.
- Material changes are understood.

### 7. Fact Check

Goal: remove factual risk.

Use `fact-checker.md` when the draft contains numbers, dates, names, current claims, source-dependent assertions, causality claims, product/company descriptions, legal/medical/financial/safety claims, or anything that could damage credibility if wrong.

Skip only if the output is clearly fictional, purely subjective, or explicitly based only on user-provided unsourced opinion.

Exit criteria:

- High-risk claims are verified, qualified, corrected, or removed.
- Unsupported claims are labeled or rewritten.
- The final draft does not overstate certainty.

### 8. Archive / Reuse

Goal: preserve reusable knowledge.

Use `archivist.md` when the user asks to save, reuse, summarize, tag, turn into notes, or continue later.

Skip by default for one-off deliverables unless the user asks for reusable assets.

Exit criteria:

- There is a concise knowledge card, tags, source note, and follow-up list.

## Skip Logic

| Stage | Skip when |
| --- | --- |
| Interviewer | brief is complete enough to draft |
| Extractor | no user material, or material is already structured |
| Researcher | pure opinion/personal content, or user says use only supplied material |
| Analyst | no judgment, comparison, or synthesis needed |
| Writer | deliverable is not prose |
| Editor | rough output requested, or final answer is short/simple |
| Fact-checker | no factual claims or factual risk |
| Archivist | no reuse, save, or continuation need |

## Output Format

For planning:

```markdown
## Brief
[goal, audience, format, angle, constraints]

## Workflow
1. [stage] - [why needed or skipped]
2. [stage] - [why needed or skipped]

## Acceptance Criteria
- [criterion]
```

For execution:

```markdown
## Final
[deliverable]

## Notes
- [assumptions, source caveats, or verification notes]
```

## Quality Check

- Did the workflow start with brief quality, not drafting eagerness?
- Were skipped stages skipped because their exit criteria were already met?
- Did research happen before source-dependent claims?
- Did editing happen before final delivery when the output is publishable?
- Did factual-risk content get checked?
