---
id: apss.review-information-stream
type: review
status: open
owner: APS framework maintainer
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the information stream concept

## Intended result

Give information stream the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected as the next concept review by the
[first cadenced grooming invocation](../streams/working-sessions/2026-08-06-first-cadenced-grooming.md)
(2026-08-07): the Direction-level reviews are closed, the order descends, and
this concept has the most accumulated direct evidence. Groomed input
evidence:

- [Stream declaration entries are too complex](../streams/framework-feedback/archived/2026-08-06-stream-declaration-complexity.md)
  — the maintainer's three-field shape (name, description, process link) is
  the concrete candidate disposition to propagate through
  `framework/SCHEMA.md` and `operations/SYSTEM.md`.
- [Every input stream needs grooming, declared propagation, and a check](../streams/framework-feedback/archived/2026-07-26-stream-grooming-and-declaration-doctor.md)
  — whether per-stream grooming is a framework responsibility or the
  vocabulary's current permission; the "doctor" proposal routes to the
  process review.
- [Working sessions are streams automatically](../streams/framework-feedback/archived/2026-08-06-working-sessions-are-streams-automatically.md)
  — delivered example: the redundant `working-sessions` entry is removed
  from `operations/SYSTEM.md`.
