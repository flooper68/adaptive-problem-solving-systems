---
id: apss.review-task
type: review
status: closed
owner: APS framework maintainer
agent: Claude Code operator
created: 2026-07-11
closed: 2026-07-27
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the task concept

## Intended result

Give task the smallest clear definition, boundary, relationships, ownership,
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
[task-family review](../../streams/working-sessions/2026-07-27-task-family-review.md),
which took this task together with `apss.review-task-candidate` and
`apss.review-selected-task` because both dependents were defined in terms of
this concept.

Disposition: **retain, widened.** `Task` is the family's only concept. It
absorbs the selection rules the two removed entries carried — work may be
captured before its problem relationship is clear, selection is the authorized
act that resolves it, and small execution steps inherit the relationship from
their containing task — and states explicitly that APS names no task states.
