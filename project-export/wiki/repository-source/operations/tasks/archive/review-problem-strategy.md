---
id: apss.review-problem-strategy
type: review
status: closed
owner: APS framework maintainer
agent: Claude Code operator
created: 2026-07-11
closed: 2026-07-26
delivery: 4c70ff9
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the problem strategy concept

## Intended result

Give problem strategy the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected on 2026-07-26. The
[open-problem review](../../streams/working-sessions/2026-07-26-open-problem-review.md)
cleared the problem-lifecycle gate that this and five sibling reviews waited
on. This is the sixth concept review and the first of the unblocked set.

The orientation pass found that the normative framework defines the concept
twice — `Strategy` and `Problem strategy` — in two vocabulary sections and in
two bullets of one README list.

Disposition: **merge**. The concept review found no defect in the concept
itself — ownership and lifecycle were already clean, and its dependents are
real and unambiguous — but found that nothing depended on there being two
definitions. The surviving `Strategy` entry absorbs what only the removed entry
stated and now carries ownership and change authority. `System strategy`
remains the root-scoped specialization; "problem strategy" survives as ordinary
wording, checked occurrence by occurrence.

Immediate validation passes: `git diff --check` clean; no cross-file link or
anchor pointed at the removed definition; declared strategy, loop,
verification, work-session, and stream process paths resolve;
`operations/SYSTEM.md` still matches `framework/SCHEMA.md`; P1 retains its
required state and this task references it; the framework definition,
vocabulary, and changelog agree on one strategy concept.

Eighteen pre-existing broken links in retained evidence are left as written and
deferred to problem grooming rather than settled by a concept review.

The maintainer accepted the disposition on 2026-07-26 and asked to ship the
session. Commit `4c70ff9` contains the accepted framework change. This task is
closed and archived.

Working session:
[problem-strategy review](../../streams/working-sessions/2026-07-26-problem-strategy-review.md).
