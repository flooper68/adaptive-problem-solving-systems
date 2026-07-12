---
id: apss.session.task-collection-review
type: working-session
status: active
recorded: 2026-07-12
participants: [APS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_problems: [P1]
related_tasks: [apss.review-task-collection]
---

# Flatten the task collection

## Frame

Make the task collection easier for the maintainer to browse by keeping every
current task directly under `operations/tasks/`. A useful stopping point is one
reviewable disposition propagated through the normative framework, Operations
processes, current task files, and live references.

## Evidence and decision

The maintainer reported direct dislike of the `backlog/` structure and directed
that all tasks live at the task root. Current task files already declare an
explicit lifecycle status, while folder placement repeats that state and
requires files and links to move during ordinary transitions.

The maintainer then clarified that the archive remains useful. Revised
decision: remove only the backlog subdivision. Status carries candidate,
selection, and execution state for every current task at the task root;
`tasks/archive/` remains the inactive-material boundary, with final status,
reason, and delivery reference retained in each archived file.

The maintainer identified the broader boundary: task organization belongs to
the system's process, not the normative framework. APS systems may use Jira,
GitHub, Linear, repository files, or another system of record. The normative
proposal now retains only the task and traceability responsibilities and
delegates representation, organization, identifiers, views, and lifecycle
states. The root-plus-archive layout remains specific to Framework Operations.

The maintainer then clarified the positive task definition: a task is actual
work that iterates on a problem's solution, provides information processing to
the system, and serves as an information source for future learning. The
compiled wording distinguishes the roles: the task processes information into
an attempt or result, while its execution and results provide evidence to
verification and later learning.

## Current stopping point

The proposal is compiled and uncommitted. Framework Operations has 44 current
task files at the task root, eight inactive files in `tasks/archive/`, no backlog
directory, no duplicate task IDs, no invalid current/archived status placement,
and no broken task or current normative links. Normative scans find no
prescribed task folder, product, identifier format, or fixed lifecycle states.
The task definition and framework explanation consistently connect actual work,
information processing, verification evidence, and future learning.
`git diff --check` passes.

Current stopping point: awaiting maintainer review. If accepted, validate the
reviewed scope, deliver it through the brainstorming close process, retain this
session, and close and archive the task.

## Brainstorming source references

While returning to the system-problem concept, the maintainer requested that
brainstorming files cite sources when relating existing concepts is useful. The
brainstorming orientation step now requires direct references to authoritative
concept, decision, or evidence sources in affected task, session, problem, or
compiled files when those references materially help explain the work. It also
avoids citations that merely repeat obvious context.
