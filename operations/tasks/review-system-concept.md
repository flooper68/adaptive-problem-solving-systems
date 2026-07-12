---
id: apss.review-system-concept
type: review
status: in-progress
owner: APS framework maintainer
agent: Codex operator
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the adaptive problem-solving system concept

## Intended result

Give the APS system concept the smallest clear definition and boundary needed
by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition, and
propagate accepted changes through normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Awaiting maintainer review.

Proposed disposition: **simplify**. Adaptive Problem Solving (APS) is the general
method. An adaptive problem-solving system is one concrete instantiation that
owns a problem statement and an iterative loop. Verification is the loop's
value function. The system owns closure of its loop while its processes define
implementation, participation, authority, lifecycle behavior, and contextual
artifacts. Problem decomposition links to another named system from the problem,
strategy, or process that performs the decomposition.

The human-readable declaration contract and template are consolidated in
`framework/SCHEMA.md`. A system declares, in order:

1. `name`;
2. `problem`;
3. `verification` as a direct process link;
4. `strategy`;
5. the main `process`;
6. its system-specific `work_sessions` catalog, which may be empty; and
7. `streams`.

Framework Operations is the first and only current APS application. Its main
loop is `operations/processes/process.md`; its value function is
`operations/processes/verification.md`. The machine-readable schema, separate
template, provisional example directory, fixed system identity and lifecycle
fields, universal roles, generic limits concept, aspirational-future field,
fixed validation split, and universal relation registry were removed or
superseded. The root README now contains only repository purpose and high-level
structure.

Detailed discussion and intermediate decisions are retained in
`operations/streams/working-sessions/2026-07-11-system-concept-review.md`.

Validation passes for the declaration contract and field order, declared
process paths, active task-to-problem references, current Markdown links,
removed-file references, terminology scans, and diff whitespace. Historical
records retain old terminology and filenames where they describe prior state.

Downstream concept reviews remain available for the system problem, strategy,
processes, streams, grooming, tasks, learning, adaptation, and other lower-level
concepts. The richer stream-entry shape is explicitly deferred to its own
review.

The maintainer accepted the reviewed session and explicitly requested delivery
on 2026-07-12. Final verification passes. Next: commit and push the reviewed
scope, then close and archive this task with its delivery reference.

Commit `a636d22` contains the accepted scope. The push to the external GitHub
remote was blocked because its trust could not be established and it would
transmit private workspace contents. The maintainer explicitly approved the
push after the risk notice and requested a process clarification eliminating
redundant delivery confirmation. Next: commit that clarification, push the
accepted session, then close and archive this task.
