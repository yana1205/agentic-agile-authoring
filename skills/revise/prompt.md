# Skill: revise

Apply review feedback and/or author direction to improve a draft.

## Input

- The current draft
- Review feedback (from `review` skill) and/or specific revision instructions

## Output

- The revised draft (full document)
- A **Revision log** at the end listing every significant change made

## Instructions

1. Address all `critical` and `major` issues from the review first.
2. Apply `minor` issues unless they conflict with author instructions.
3. Do not make unrequested changes beyond fixing the stated issues.
4. Preserve the author's voice and intentional stylistic choices.
5. If a review suggestion conflicts with explicit author direction, follow the author — note the conflict in the revision log.
6. If a requested change cannot be made cleanly, explain why in the revision log and propose an alternative.

## Revision log format

```
## Revision log

| # | Change | Source |
|---|--------|--------|
| 1 | Rewrote introduction to front-load the central claim | Review: critical issue #1 |
| 2 | Added concrete example in §3.2 | Review: major issue #2 |
| 3 | ... | Author instruction |
```
