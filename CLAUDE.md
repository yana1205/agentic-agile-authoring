# Claude Code — Project Instructions

This repo is a **Claude Code plugin** and **Roo Code mode collection** for agile content authoring workflows.

## Repo structure

```
.claude-plugin/
  plugin.json          Claude Code plugin manifest
agents/                Claude Code subagents (plugin-level)
commands/              Claude Code slash commands (plugin-level)
skills/                Platform-agnostic skill definitions (source of truth)
.roomodes              Roo Code custom mode list (JSON)
.roo/
  rules-<slug>/        Per-mode rule files for Roo Code
dist/                  Roo Code importable mode YAMLs
```

## Claude Code usage

Install as plugin (once published to a marketplace):
```
/plugin install <owner>/agentic-agile-authoring
```

After install, commands are namespaced:
- `/agentic-agile-authoring:outline`
- `/agentic-agile-authoring:draft`
- `/agentic-agile-authoring:review`
- `/agentic-agile-authoring:revise`

Local development testing:
```
claude --plugin-dir ./
```

## Roo Code usage

Import a mode via Roo's Settings → Modes → Import:
- `dist/planner.yaml`
- `dist/author.yaml`
- `dist/reviewer.yaml`

## Authoring conventions

- **Skills are prompt-first.** Core logic goes in `skills/<name>/prompt.md` before being adapted for each platform.
- Keep platform-specific files thin — they should reference intent from `skills/`, not duplicate it.
- Subagent files (`agents/`) need YAML frontmatter with `name` and `description`.
- Roo mode slugs must be lowercase kebab-case and match between `.roomodes` and `.roo/rules-<slug>/`.

## When developing skills

1. Draft in `skills/<name>/prompt.md` first
2. Propagate to `commands/<name>.md` (Claude) and relevant `.roo/rules-*/` files (Roo)
3. Test Claude plugin locally: `claude --plugin-dir ./`
4. Test Roo modes: import from `dist/` or copy `.roo/rules-*/` directly
5. Regenerate `dist/*.yaml` after editing `.roomodes` or `.roo/rules-*/`
