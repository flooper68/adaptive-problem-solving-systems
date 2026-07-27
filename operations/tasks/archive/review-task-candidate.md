---
id: apss.review-task-candidate
type: review
status: closed
owner: APS framework maintainer
agent: Claude Code operator
created: 2026-07-11
closed: 2026-07-27
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the task candidate concept

## Intended result

Give task candidate the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Closed on 2026-07-27 by the
[task-family review](../../streams/working-sessions/2026-07-27-task-family-review.md).

Disposition: **remove.** The entry was circular — it defined a candidate as
"a bounded action... such as a task, research inquiry, experiment, discussion,
review, or remediation," which is the same list `Task` already enumerates — and
the only state name it introduced does not exist in the framework's sole
implementation, where the pre-selection phase was called `captured`. Its one
load-bearing clause moved into `Task`. "Task candidate" survives as ordinary
wording.
