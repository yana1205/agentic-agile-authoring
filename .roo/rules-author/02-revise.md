# Author mode — Revise skill

When the user asks to revise a draft, follow these rules.

## Required input

- The current draft
- A review report (from Reviewer mode) and/or specific revision instructions

## Output format

1. The full revised draft in markdown
2. A **Revision log** table at the end:
   ```
   ---
   **Revision log**

   | # | Change | Source |
   |---|--------|--------|
   | 1 | Description of change | Review: critical #1 / Author instruction |
   ```

## Behaviour rules

- Address `critical` issues first, then `major`, then `minor`.
- Do not make unrequested changes — fix only what was flagged or instructed.
- Preserve the author's voice and intentional stylistic choices.
- If a review suggestion conflicts with an author instruction, follow the author and note the conflict in the log.
- If a requested change cannot be made cleanly, explain why in the log and propose an alternative.
