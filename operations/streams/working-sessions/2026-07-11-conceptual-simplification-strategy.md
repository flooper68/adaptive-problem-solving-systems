---
id: apss.session.conceptual-simplification-strategy
type: working-session
status: retained
recorded: 2026-07-11
closed: 2026-07-11
delivery: 6702230
participants: [APSS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_problems:
  - P1
related_tasks:
  - apss.review-system-concept
  - apss.review-system-problem
  - apss.review-vision
  - apss.review-system-boundary
  - apss.review-purpose
  - apss.review-authority
  - apss.review-subsystem-and-relationships
---

# Refine the MVP conceptual simplification strategy

## Frame

Refine P1's top-down strategy so it works from the framework's actual concepts,
defines and prunes them one at a time, and makes simplicity testable. Produce
uncommitted strategy and task changes for maintainer review in Git.

## Maintainer direction

- Start from the framework's current concepts rather than introducing an
  assumed conceptual chain.
- Move from top concepts to dependent lower-level concepts.
- Make every retained concept as clear and simple as possible.
- Define lifecycles where they are genuinely needed.
- Validate the result by running the complete loop, trying to explain or teach
  the system in a way that exposes complexity, and conducting adversarial
  review.

## Material decisions

- Use the current review to create one bounded task for every concept identified
  so far; continue discovering missing concepts as the review proceeds.
- Use conceptual dependency, purpose, state, and authority to establish a
  provisional top-to-bottom order.
- Review one concept per bounded pass and give it a retain, simplify, merge,
  demote, defer, or remove disposition.
- Keep P1 as the long-running unit of improvement. A selected task implements
  or tests one bounded part of its strategy and should produce one inspectable
  result in one working session.
- Define an independent lifecycle only for a concept with durable identity or
  state. Treat other concepts as properties, relationships, activities,
  outputs, assessments, or transitions.
- Propagate every accepted disposition through all affected normative and
  supporting surfaces.
- Permit downstream use to reopen upstream decisions.
- Require complete-loop use, fresh-context explanation and teach-back, and
  adversarial complexity review as distinct validation modes.

## Affected artifacts

- [P1](../../problems/p1-finish-mvp-and-run-loop.md)
- [System-concept review](../../tasks/archive/review-system-concept.md)
- [Concept-review tasks](../../tasks/)
- [Framework vocabulary](../../../framework/VOCABULARY.md)
- [Framework definition](../../../framework/README.md)
- [Task-grooming process](../../processes/task-grooming.md)
- [Problem-grooming process](../../processes/problem-grooming.md)
- [Agent guidance](../../../AGENTS.md)

## Current stopping point

P1's strategy now states the concept review method, disposition choices,
propagation rule, and validation approach. The system strategy remains at goal
scope. Problem grooming now requires an explicit scope check before promoting a
problem-specific method into the system strategy. The umbrella task was deleted
because it duplicated P1 and could not be completed in one session. This
session's review was sufficient to create bounded tasks for every concept
identified so far. The system concept review is selected; the remaining reviews
are ready and will be selected one at a time in dependency order.

The maintainer ended the session at this accepted stopping point. Its changes
were delivered to `origin/main` in commit `6702230`; the next concept session
starts with the selected system-concept review.
