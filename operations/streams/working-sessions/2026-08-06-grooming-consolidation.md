---
id: apss.session.grooming-consolidation
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
delivery: dd63166
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: []
---

# Consolidate the four grooming processes into one

## Frame

The maintainer asked whether the four per-kind grooming processes can be
simplified into a single grooming that handles all inputs — streams, tasks,
problems, and verification evidence — reasoning that the system can always add
more later. The intended result is one declared grooming process, the four
per-kind processes archived, and every live declaration and pointer updated.
The responsible user is the APS framework maintainer. A useful stopping point
is a reviewable working tree with the consolidation applied.

## Orientation

- The operations system declared four grooming processes:
  `problem-grooming.md`, `task-grooming.md`, `insight-grooming.md`, and
  `framework-feedback-grooming.md`. All four shared the same skeleton —
  orient, clarify one item at a time, assess evidence, decide one
  maintainer-approved disposition, propagate without conflating, append a
  dated record — and differed mainly in per-kind disposition vocabularies
  (nine problem results, four task dispositions plus closure reasons, eight
  insight statuses, eight feedback statuses).
- [`STRATEGY.md`](../../STRATEGY.md) points 2–4 already mandate this: keep
  only what one complete loop needs, prefer the smaller understandable model,
  and add complexity only when observed use demonstrates need. The
  consolidation implements the existing strategy rather than changing it.
- The framework permits it without normative change:
  [`VOCABULARY.md`](../../../framework/VOCABULARY.md) states that problem and
  task grooming are distinct responsibilities "even when a system combines
  them in one meeting, process, tool, or cadence," and the System entry
  defines grooming generally as the responsibility to process relevant
  information and make decisions from it.

## Decision

Consolidate: one [`grooming.md`](../../processes/grooming.md) process handles
all input kinds. The responsibilities remain distinguishable in the questions
asked and the propagation rules, not in separate procedures. The rich per-kind
disposition vocabularies collapse to four dispositions — act, revise, keep,
close — with the closure reason recorded in the file. Invariants preserved
from the four processes: the maintainer approves every disposition and alone
selects work; grooming never edits the compiled framework (framework-worthy
lessons become compilation tasks executed by brainstorming); source records
are appended to, never rewritten to fit conclusions; problems and tasks keep
the two-state open/closed lifecycle; strategy changes stay at the smallest
evidenced level.

The maintainer also stated the general lesson — always start simple, add only
when needed — captured separately as an insight through insight intake and
linked below.

On review the maintainer rejected archiving the removed processes: processes
are compiled knowledge that changes over time, and superseded versions can be
reconstructed from session records and git history. The four files were
deleted rather than moved, and links inside historical records were left
exactly as written — a record cites the processes of its time, and git
history recovers them.

## Changes

- [`grooming.md`](../../processes/grooming.md) — new single grooming process.
- `problem-grooming.md`, `task-grooming.md`, `insight-grooming.md`, and
  `framework-feedback-grooming.md` — deleted; recoverable from git history.
- [`SYSTEM.md`](../../SYSTEM.md) — the `problem-grooming` work session became
  `grooming`; the insights and framework-feedback streams' `access` and
  `consumed_by` now point at `processes/grooming.md`; the working-sessions
  purpose says "grooming invocations."
- [`process.md`](../../processes/process.md) — steps 2–4 route assessment of
  feedback, insights, work candidates, and problems through `grooming.md`.
- [`insight-intake.md`](../../processes/insight-intake.md),
  [`framework-feedback-intake.md`](../../processes/framework-feedback-intake.md),
  [`task-intake.md`](../../processes/task-intake.md) — next-action pointers
  and record templates link `grooming.md`.
- Stream READMEs (`streams/README.md`, `streams/insights/README.md`,
  `streams/framework-feedback/README.md`) — grooming links updated.
- Ungroomed stream records — "Not yet groomed" pointers now link
  `grooming.md`. Historical in-body links in retained records and sessions
  were left unchanged; they cite the deleted files as they existed and
  resolve through git history. No record content was rewritten.

## Related records

- Insight: [Always start simple, add only when
  needed](../insights/archived/2026-08-06-start-simple-add-only-when-needed.md).

## Open questions

- Whether the four-disposition set is expressive enough in practice; the first
  grooming invocations under the new process are the reconsideration trigger
  for adding per-kind procedure back.

## Acceptance and delivery

The maintainer reviewed the consolidation iteratively — correcting the
initial archive approach to deletion — and accepted the session scope on
2026-08-06 when asked explicitly before applying follow-up work; per the
brainstorming process that acceptance approves delivering this scope to
`origin/main`. The unrelated in-progress authority-review changes in the same
working tree are excluded from this delivery. The delivery commit is
referenced in this record's frontmatter follow-up.
