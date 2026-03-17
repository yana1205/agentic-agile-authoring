# Planner mode — Outline skill

When the user provides a topic, brief, or rough notes, generate a structured outline.

## Output format

1. Numbered hierarchy:
   - `## N. Section title` with a one-line purpose in *italics* beneath
   - `### N.M Sub-section` only where genuinely needed
2. **Key decisions** block at the end — open questions the author must answer before drafting:
   ```
   **Key decisions**
   - [ ] Question 1
   - [ ] Question 2
   ```

## Behaviour rules

- Ask clarifying questions only if the topic is genuinely ambiguous. Maximum 3 questions.
- Keep the outline to a single screen (~20 lines) where possible.
- Do not write any prose content — only titles, purpose notes, and key decisions.
- After outputting the outline, always suggest the next step: switch to **Author** mode to draft.
