---
id: apss.review-problem-signal
type: review
status: awaiting-review
owner: APS framework maintainer
agent: Claude Code operator
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
session: streams/working-sessions/2026-07-26-problem-signal-review.md
---

# Review the problem signal concept

## Intended result

Give problem signal the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

In progress as the seventh concept review under P1, following the
[problem-strategy review](../streams/working-sessions/2026-07-26-problem-strategy-review.md),
which named problem signal as the highest remaining concept in the dependency
chain. The gate it was waiting on has cleared: the
[system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
established that verification evaluates task attempts against the problem
signal and that satisfying the signal may support a solved assessment without
automatically closing the problem, and the problem lifecycle is now accepted.

This task implements P1's strategy by applying the concept review test to one
concept and propagating a single reviewed disposition. It is accepted when the
concept has one maintainer-authorized disposition, the affected normative and
Operations surfaces agree, and downstream questions are captured rather than
decided here.

Awaiting review. The disposition is **retain, sharpened, renamed**: a signal
must be readable while the problem is open, and the entry is now `Signal`.
`Outcome` absorbed the target the signal was being confused with. Changes are
compiled and uncommitted; validation passes. Next step is maintainer acceptance,
then delivery. Two questions are recorded rather than decided: whether P1's own
signal is rewritten, which belongs to problem grooming, and whether `Outcome`
should move next to `Signal` in the vocabulary.

This file keeps its `apss.review-problem-signal` id and name, as
`review-problem-strategy` did through the equivalent rename.
