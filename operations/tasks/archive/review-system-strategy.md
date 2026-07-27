---
id: apss.review-system-strategy
type: review
status: closed
owner: APS framework maintainer
agent: Codex operator
created: 2026-07-11
closed: 2026-07-26
delivery: e5a7b7d
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the system strategy concept

## Intended result

Give system strategy the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected after the system, boundary, and system-problem reviews resolved its
higher-level dependencies.

The review confirmed the concept's structure: one authoritative location, no
durable identity or state requiring lifecycle machinery, explicit change
authority, and an existing working line against problem strategy in the
problem-grooming process.

The load-bearing question was whether system strategy conflates two things: the
approach to the root problem, already covered by the general strategy
definition, and the system's operating model for interpreting evidence,
decomposing problems, guiding lower strategies, verifying, learning, and
adapting. The operator recommended demoting it to the root problem's strategy.

Disposition: **retain**. The maintainer decided that system strategy
legitimately carries both, that separating them would add a concept rather than
remove one, and that only wording should change. The vocabulary and framework
definitions were aligned to name the same responsibilities in the same order,
verification replaced validation for the loop stage, the redundant
"interpretation" term was dropped, the scope distinction from problem strategy
was stated in the definition, and strategy change was linked to adaptation. The
declaration contract, the `strategy` link from `SYSTEM.md`, and the Framework
Operations strategy were unchanged.

The conflation question is recorded in the
[working session](../../streams/working-sessions/2026-07-12-system-strategy-review.md)
as a candidate for reopening if P1's teach-back or adversarial validation shows
readers cannot separate system strategy from problem strategy.

Immediate validation passes. The maintainer accepted the disposition on
2026-07-26. Commit `e5a7b7d` contains the accepted framework change. This task
is closed and archived.
