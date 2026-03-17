# Skill: outline

Generate a structured, hierarchical outline from a topic, brief, or rough notes.

## Input

The user provides one of:
- A topic or title
- A brief / set of requirements
- Rough bullet notes to organize

## Output

A numbered hierarchical outline with:
- Top-level sections (H2)
- Sub-sections where appropriate (H3)
- One-line purpose note per section in *italics*

## Instructions

1. Identify the core argument or narrative arc.
2. Group related ideas into coherent sections.
3. Order sections for logical flow (general → specific, problem → solution, etc.).
4. Keep section titles concise and action-oriented.
5. After the outline, add a **Key decisions** block listing open questions the author must resolve before drafting.

## Example output shape

```
## 1. Introduction
*Establish context and state the central claim.*

### 1.1 Background
### 1.2 Problem statement

## 2. ...

---
**Key decisions**
- [ ] Target audience: practitioner or executive?
- [ ] Include case studies? If so, how many?
```
