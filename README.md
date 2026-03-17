# Agentic Agile Authoring

Agent skills and modes for agile document/content authoring workflows.

## Overview

This repo defines reusable **skills** (prompts + instructions) that run on two platforms:

| Platform | Agent definition | Skill/command entry |
|----------|-----------------|---------------------|
| **Claude Code** | `.claude/agents/*.md` | `.claude/commands/*.md` |
| **Roo Code** | `.roomodes` (mode list) | `.roo/rules-<slug>/` (per-mode rules) |

Shared platform-agnostic skill logic lives in `skills/`.

## Skills

| Skill | Description |
|-------|-------------|
| `outline` | Generate a structured outline from a topic or brief |
| `draft` | Write a first draft from an outline or brief |
| `review` | Critique content and produce actionable feedback |
| `revise` | Apply review feedback to improve a draft |

## Agents / Modes

| Name | Role |
|------|------|
| `planner` | Breaks down authoring goals into outlines and tasks |
| `author` | Writes and revises content |
| `reviewer` | Evaluates content quality and consistency |

## Usage

### Claude Code

Subagents are invoked via the `Agent` tool or referenced in prompts. Slash commands are available as `/outline`, `/draft`, `/review`, `/revise`.

### Roo Code

Switch to a custom mode (`planner`, `author`, `reviewer`) via the mode selector. Each mode has tailored rules and tool permissions.

## Adding a new skill

1. Write the core prompt in `skills/<skill-name>/prompt.md`
2. Add a Claude command at `.claude/commands/<skill-name>.md`
3. Add a Roo rule file at `.roo/rules-<mode-slug>/<skill-name>.md` for relevant modes
4. Document it in this README
