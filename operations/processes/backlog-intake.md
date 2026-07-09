# Backlog intake

## Purpose

Capture a potentially valuable idea without requiring enough analysis to plan
or prioritize it. Intake preserves the idea and its source; grooming decides
whether and how it should proceed.

## When to capture

Create a backlog item when an observation, issue, question, research direction,
experiment, decision need, or proposed change may improve the framework,
examples, or stewardship operation and is not already committed in the current
plan.

Search `operations/work/backlog/`, `operations/work/PLAN.md`, compiled
knowledge, and recent logs first. Add new evidence to an existing item instead
of creating a duplicate.

## Minimum capture

Create `operations/work/backlog/<short-slug>.md` with this structure:

```markdown
---
id: apss.<stable-id>
type: insight
status: captured
owner: APSS framework maintainer
created: YYYY-MM-DD
source: <person, observation, document, validation, or other origin>
---

# <Concise idea title>

## Idea

<What might change or become possible?>

## Motivation

<Why might this matter, and to whom?>

## Evidence

<Known observations or references; say “none yet” when appropriate.>

## Open questions

- <What must grooming clarify?>

## Grooming log

### YYYY-MM-DD — captured

<Who captured it and any essential provenance.>
```

Use the closest APSS work type: `task`, `issue`, `insight`, `question`,
`decision`, `research`, or `experiment`. Capture may add fields, but it must not
invent evidence or imply approval.

## Intake result

A successfully captured item has:

- a stable ID and source;
- enough wording for another operator to understand the idea later;
- `status: captured`; and
- no promise that it will be prioritized or implemented.

Material discussion during intake belongs in the item's grooming log or a
linked retained source. The next possible action is the
[backlog grooming process](backlog-grooming.md).
