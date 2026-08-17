---
id: apss.review-system-boundary
type: review
status: closed
owner: APS framework maintainer
agent: Codex operator
created: 2026-07-11
closed: 2026-07-12
delivery: 731f6ae
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the system boundary concept

## Intended result

Give the system boundary concept the smallest clear definition, relationships,
ownership, and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected by the maintainer on 2026-07-12 after the system and system-problem
reviews resolved its higher-level dependencies.

In progress. Current framework language uses boundary in at least three
different senses that this review must distinguish: the root problem defines
what problem the system owns; an independent boundary helps distinguish a
child system from an internal problem; and a concrete application may explain
which operations and artifacts it includes. The next step is to decide whether
"system boundary" needs an independent normative concept or is sufficiently
expressed by the system problem, loop ownership, and application-specific
scope.

The maintainer's current interpretation is that system boundary is not a
first-class APS concept. It is contextual description derived from retained
concepts rather than something with independent identity or lifecycle. The
maintainer reviewed the child-system wording and decided it remains clear as
contextual shorthand; no replacement is needed.

Proposed disposition: **demote**. The normative framework keeps no independent
system-boundary definition, field, identity, state, or lifecycle. The root
problem and complete-loop ownership carry system identity, while boundary may
remain ordinary contextual language. The declaration guidance no longer
invites a boundary explanation, and the duplicated Framework Operations
boundary section is removed. The root repository README remains the
authoritative orientation to the repository's `framework/` and `operations/`
parts.

Immediate validation passes: `SYSTEM.md` retains every required declaration
field; all declared strategy, loop, verification, work-session, and stream
process paths resolve; the active task still references P1; the removed prose
remains available without duplication in the root README; terminology scans
show no required boundary field or standalone vocabulary concept; and
`git diff --check` passes.

The maintainer accepted the reviewed disposition and asked to finish the
session on 2026-07-12. Commit `731f6ae` contains the accepted framework change.
This task is closed and archived.
