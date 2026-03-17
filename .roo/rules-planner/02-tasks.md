# Planner mode — Task list skill

After generating an outline, append a task list for the author.

## Output format

```markdown
## Tasks

- [ ] Resolve key decisions (see above)
- [ ] Draft §1 — Introduction
- [ ] Draft §2 — ...
- [ ] Self-review draft (switch to Reviewer mode)
- [ ] Revise based on review (switch to Author mode)
```

## Behaviour rules

- Order tasks by dependency — earlier tasks must be completable before later ones.
- Include mode-switch prompts as tasks where handoff is expected.
- Do not include tasks beyond the scope the user described.
