---
id: apss.session.plain-language-constraint-grooming
type: working-session
status: retained
recorded: 2026-08-06
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: [apss.plain-language-backfill]
---

# Add a plain-language constraint to P1's strategy

## Frame

The maintainer asked whether the current strategy involves making the system
simple, "also using simple language, terms etc... so 'normal' person can
easily understand," and asked to run the change session right away. The
maintainer's request is a valid problem-grooming trigger. Scope: P1, which
owns the understandability signal. Stopping point: one approved decision in
P1's grooming history and any captured task.

## Discussion

Orientation found the strategy explicit about structural simplicity — keep
only what one complete loop needs, prefer the smaller model, prune concept by
concept — and about understandability as a validation bar, but scoped to the
maintainer and a teach-back reviewer, with no commitment to plain wording. The
prose itself remained dense: "normative package," "lifecycle machinery,"
"disposition," "adversarial review."

The first load-bearing question was the audience: is the "normal person" a
real consumer the system serves, or a quality bar for the existing readers?
The maintainer chose the latter — same audience, plainer wording. That answer
also settled the strategy-scope rule: the change guides only P1, so it belongs
in P1's strategy, not the system strategy.

The second question was whether surfaces already written under the old wording
get a rewording pass. The maintainer chose to capture a backfill task rather
than fix them only opportunistically. The intake clarification then asked
which surfaces the backfill covers; the maintainer chose everything —
framework package, Operations processes, problem files, and stream
documentation — accepting that the task will need splitting, which is left to
task grooming.

## Decision

**Revise P1**, approved by the maintainer:

- P1's strategy now requires every retained surface to be written in plain
  language, treating wording a reader stumbles over as avoidable complexity to
  remove like any other, applied while propagating each concept decision.
- The teach-back validation pass now asks the reviewer to flag wording they
  had to reread or could not restate in their own words.
- One task captured: [`apss.plain-language-backfill`](../../tasks/plain-language-backfill.md)
  for the surfaces already written.

## Affected files

- `operations/problems/p1-finish-mvp-and-run-loop.md` — strategy paragraph
  added, teach-back pass sharpened, grooming history entry appended.
- `operations/tasks/plain-language-backfill.md` — captured.
- This record.

## Verification

Immediate checks pass: the links among the problem file, task file, and this
record resolve; the task follows the intake structure; no `framework/` surface
changed, so the changelog and declaration contract are unaffected. P1's signal
was not read — it remains unreadable, as the 2026-07-26 problem-signal review
recorded, and rewriting it is already an open grooming trigger. Whether the
plain-language constraint improves understandability is delayed evidence for
the teach-back pass.

## Stopping point

Grooming for this question is complete; the session stops without selecting
the backfill task. Next trigger: task grooming shapes the backfill's split and
sequencing, and the first teach-back can seed its list of stumbling points.
