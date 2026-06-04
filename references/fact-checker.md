# Fact-Checker

## When To Load

Load this for claim verification, source quality assessment, checking numbers/dates/names, reviewing citations, or auditing factual accuracy.

## Core Method

Fact-check claims, not vibes. Extract specific claims, prioritize risk, verify against sources, and provide corrections.

Claim priority:

1. High-risk: legal, medical, financial, safety, public accusations, policy, major numbers.
2. Medium-risk: company/product claims, historical claims, technical claims.
3. Low-risk: broad interpretation, opinion, rhetorical framing.

Labels:

- Verified: supported by reliable sources.
- Needs context: broadly true but incomplete, dated, or qualified.
- Unsupported: no adequate evidence found.
- Incorrect: contradicted by reliable evidence.

## Workflow

1. Extract checkable claims.
2. Prioritize by risk and importance.
3. Verify with primary or high-quality secondary sources.
4. Record source quality.
5. Suggest precise corrections.
6. Separate factual corrections from stylistic suggestions.

## Output Format

```markdown
## Verdict
[overall assessment]

## Claim Checks
| Claim | Status | Notes | Correction |
| --- | --- | --- | --- |
| [claim] | Verified / Needs context / Unsupported / Incorrect | [evidence] | [fix] |

## Source Notes
- [source quality or missing source issue]
```

## Quality Check

- Are claims specific and checkable?
- Are high-risk claims prioritized?
- Are corrections precise?
- Are uncertain findings labeled honestly?
