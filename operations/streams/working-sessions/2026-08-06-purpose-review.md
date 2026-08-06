---
id: apss.session.purpose-review
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: [apss.review-purpose]
---

# Review the purpose concept

## Frame

Decide whether purpose is an independently useful APS concept or should be
merged with or demoted beneath the system problem or another concept. The
responsible user and decision authority is the APS framework maintainer.

This session follows the
[task-family review](2026-07-27-task-family-review.md). The maintainer selected
`apss.review-purpose` as the next task: it is the oldest ready review, first
among the three Direction-level tasks the earlier sessions skipped when they
moved down into problems and tasks.

## Orientation

Orientation answered the review test before any exploration was needed. Three
findings:

**The vocabulary never defined the concept.** A git history search for a
`Purpose` entry in `VOCABULARY.md` returns nothing across all sixty commits.
Unlike goal and vision, purpose was never compiled as a framework concept — it
existed only as a system declaration field.

**That field was already removed, with its fate explicitly ruled on.** The
[system-concept review](2026-07-11-system-concept-review.md)'s 2026-07-12
declaration field audit listed `purpose` first among the strong pruning
candidates — "restates the problem, vision, name, and prose purpose" — and the
minimal declaration compiled that day excludes it. Vision, purpose's sibling in
the same ruling, had its review task superseded and archived within that
session. This task was missed by the same sweep. The loop has operated without
a purpose concept since 2026-07-12.

**Every surviving occurrence is a property or ordinary wording.** A full survey
of current normative and Operations surfaces found three kinds of residue:

- the stream `purpose` field ("why the system reads this stream") in
  `SCHEMA.md`, the framework definition's example, and the Operations
  declaration — a property of a stream, whose representation belongs to the
  open `apss.review-information-stream` task;
- `Purpose:` view headers in `VISUALIZATION.md` and `## Purpose` sections in
  Operations process files — descriptive convention, not concept use; and
- ordinary prose ("support that purpose", "fit-for-purpose").

Against the concept review test: no independent meaning in the loop — a
system's purpose is its problem; nothing depends on it; no durable identity or
state; and the first complete loop demonstrably operates without it.

## Decision

**Close as superseded by `apss.review-system-concept`,** mirroring
`apss.review-vision`. The substance was decided in the system-concept review's
field audit; this session's contribution is the verification above that no
conceptual residue remains, and the bookkeeping the earlier sweep missed.

The maintainer chose supersession over recording a fresh remove disposition:
the earlier session's ruling is the authoritative decision, and a second
disposition for an already-absent concept would be ceremony.

This closure is task grooming, not a concept pruning. The pruning count under
P1 stays at six.

## Changes

- [`review-purpose.md`](../../tasks/archive/review-purpose.md) — closed with
  `superseded_by: apss.review-system-concept` and the verification result, and
  moved under `tasks/archive/`.
- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — grooming history notes
  the closure and the remaining Direction-level queue.

No normative surface changes. The framework is untouched.

## Observations this surfaced

**The vision sweep missed its sibling.** The system-concept session superseded
`review-vision` when its decision made that task moot, but not
`review-purpose`, whose field the same audit pruned. A session that closes
tasks as side effects of a broader decision has no checklist forcing it to ask
which other open tasks the decision moots. Same shape as the stale
`Selected task` entry the task-family review found: an edit pass that touches
some affected surfaces and misses one. Recorded for the adversarial pass of the
validation strategy.

**The remaining Direction-level queue is two tasks** — `review-authority` and
`review-subsystem-and-relationships` — before the review order descends into
evidence, grooming, and results concepts. The task-family review's removal of
selection and authority machinery from tasks materially advanced
`review-authority` already.

## Open questions

None opened by this session. P1's own signal rewrite remains open from the
[problem-signal review](2026-07-26-problem-signal-review.md), unchanged here.

## Validation

`git diff --check` is clean. The archived task's links resolve at archive
depth — the defect the task-family review found in five earlier archived
records is not reproduced. No current surface links to the task at its old
path. Every occurrence of "purpose" in current framework and Operations
surfaces is one of the three residue kinds listed above; none is concept use.

Problem-signal evidence: no reading was taken. This session changes no
normative surface, so the maintainer's review of the closure is the only
evidence relevant to P1.

## Acceptance and delivery

The maintainer accepted the session on 2026-08-06 and directed delivery of
this session's scope alone. The parallel plain-language grooming session's
uncommitted changes — its strategy revision and grooming entry in P1, its
session record, and the captured backfill task — are deliberately excluded
from this delivery and remain in the working tree with their own session.
The delivery commit is referenced in this record's frontmatter follow-up.
