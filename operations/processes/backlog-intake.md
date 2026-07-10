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

## Clarification conversation

After preserving the initial idea, identify two to four tailored questions for
its source before treating intake as complete. Ask only one question at a time,
wait for the answer, and use that answer to select or adapt the next question.
Never present a batch of questions to the source. Do not repeat questions the
source has already answered. Prefer questions that clarify:

- the observed situation, affected consumer, and why it matters;
- what a better outcome would look like;
- whether the proposed change is the need itself, one possible response, or a
  constraint on acceptable responses; and
- relevant examples, evidence, boundaries, dependencies, or trade-offs.

Adapt the questions to the work type. For an issue, ask about expected and
observed behavior, impact, and reproducibility. For an insight or idea, ask
what prompted it, who would benefit, and how improvement could be observed.
For a question, decision, research direction, or experiment, clarify the
decision it should inform and what evidence would be sufficient.

Keep intake lightweight. Accept “unknown” as useful information, avoid leading
the source toward a preferred solution, and do not demand grooming-level
answers merely to preserve an idea. Stop when the item is understandable
enough for later grooming; do not ask every candidate question when earlier
answers make them unnecessary. If the source is unavailable, retain the item
with the next unanswered question and record why clarification is pending.

Update the item's idea, motivation, evidence, open questions, and grooming log
with the answers. Distinguish source reports, direct observations, assumptions,
and operator interpretations. Then show the updated record to the source for
correction before requesting approval to commit or publish it.

Apply this clarification step prospectively while capturing new items. Do not
reopen an already captured item solely because it predates this requirement;
clarify it later only when its source requests revision or grooming begins.

## Intake result

A successfully captured item has:

- a stable ID and source;
- enough wording for another operator to understand the idea later;
- a short, one-question-at-a-time clarification conversation with the source,
  with answers recorded or the reason the next answer remains pending;
- `status: captured`; and
- no promise that it will be prioritized or implemented.

Material discussion during intake belongs in the item's grooming log or a
linked retained source. The next possible action is the
[backlog grooming process](backlog-grooming.md).
