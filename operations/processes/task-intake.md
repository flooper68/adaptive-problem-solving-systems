# Task intake

## Purpose

Capture a potentially valuable executable response without requiring enough
analysis to select or prioritize it. Intake preserves the proposed action and
its source; grooming decides whether and how it should proceed.

## When to capture

Create a task file when a bounded research inquiry, experiment, review,
remediation, or other action may improve the framework, Framework Operations,
or a future application and is not already represented by a task.

A report, observation, insight, question, issue, or decision remains in its
source record. If it warrants a response, create a separate task candidate
that describes the executable action and links the source. Do not give a record
an execution lifecycle merely because it may influence future work.

Search `operations/tasks/`, compiled knowledge, and recent sessions first. Link
new source evidence to an existing candidate instead of creating a duplicate.

## Minimum capture

Create `operations/tasks/backlog/<short-slug>.md` with this structure:

```markdown
---
id: apss.<stable-id>
type: task
status: captured
owner: APS framework maintainer
created: YYYY-MM-DD
source: <person, observation, document, validation, or other origin>
source_records: []
---

# <Concise action-oriented title>

## Proposed action

<What could be done or investigated?>

## Intended result

<What observable result would make the action useful?>

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

Use the closest executable type, such as `task`, `research`, `experiment`,
`review`, or `remediation`. Capture may add fields, but it must not invent
evidence, imply approval, or rewrite the source record as a settled response.

## Clarification conversation

After preserving the initial idea, identify two to four tailored questions for
its source before treating intake as complete. Ask only one question at a time,
wait for the answer, and use that answer to select or adapt the next question.
Never present a batch of questions to the source. Do not repeat questions the
source has already answered. Prefer questions that clarify:

- the observed situation, affected consumer, and why it matters;
- what a better outcome would look like;
- whether the proposed action is one possible response or a requirement limiting
  acceptable responses; and
- relevant examples, evidence, boundaries, dependencies, or trade-offs.

Adapt the questions to the action. For remediation, ask about expected and
observed behavior, impact, and reproducibility in the linked issue or report.
For a task or review, clarify the intended consumer and observable result. For
research or an experiment, clarify the question or decision it should inform
and what evidence would be sufficient.

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

A successfully captured candidate has:

- a stable ID and source;
- an executable action and intended result another operator can understand;
- links or recoverable provenance for the records that motivated it;
- a short, one-question-at-a-time clarification conversation with the source,
  with answers recorded or the reason the next answer remains pending;
- `status: captured`; and
- no promise that it will be prioritized or implemented.

Material discussion during intake belongs in the item's grooming log or a
linked record retained through the
[brainstorming process](brainstorming.md). The next possible action is the
[task grooming process](task-grooming.md).
