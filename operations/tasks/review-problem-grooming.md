---
id: apss.review-problem-grooming
type: review
status: ready
owner: APS framework maintainer
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the problem grooming concept

## Intended result

Give problem grooming the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Ready. The
[system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
established that source-specific grooming may propose higher-level problems but
problem grooming alone opens, merges, revises, defers, or rejects them. The
[follow-up feedback](../streams/framework-feedback/2026-07-12-problem-creation-grooming-and-storage.md)
also established that cadence is system-specific and may be event-driven,
scheduled, continuous, or mixed. Problem grooming maintains the hierarchy while
task grooming separately shapes bounded work and readiness; systems may combine
their implementation only when distinct decisions remain inspectable.
APS now delegates all problem-storage and cadence details to each system's
process. Framework Operations retains its current file-based implementation.
