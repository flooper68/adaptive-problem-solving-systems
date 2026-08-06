---
id: apss.session.current-state-concept
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: [apss.current-state-reporting]
---

# Promote current state to a first-class framework concept

## Frame

The maintainer opened the session with the direction: "current state should be
a first class concept in the framework, it is very useful." The intended
result is the concept compiled into the normative package, generalizing what
the [learning-loop application
session](2026-08-06-learning-loop-application.md) implemented in Operations
([`STATE.md`](../../STATE.md), per-problem `Current state` sections) when it
closed [current-state-reporting](../../tasks/archive/current-state-reporting.md).
The stopping point is maintainer acceptance of the compiled changes.

## Decisions

1. **Compile as a vocabulary concept, not machinery.** Current state is the
   present condition of the system's work, owned by the problem and task
   systems of record; a current-state view is an optional derived,
   date-stamped snapshot that loses to those records on conflict. No
   lifecycle, no required artifact, no prescribed format or cadence — per the
   concept-review test, a property/view earns no lifecycle machinery.
2. **Design generalized from the delivered Operations answers.** The closed
   task's open questions (durable artifact vs. view, colocation with the
   owning record, refresh at delivery, date-stamped staleness, subordination)
   were answered by the maintainer on 2026-08-06; the vocabulary entry states
   the general form and leaves format, location, and cadence to each system.
3. **Feedback captured, delivered with the session.** The framing direction is
   preserved as
   [framework feedback](../framework-feedback/2026-08-06-current-state-first-class.md);
   delivery rides with the session scope instead of intake's automatic path
   because the same session compiles the response.

## Challenge

The change serves P1's strategy point 4 (add complexity later only when
observed use, feedback, or validation demonstrates need) and the system
problem's evidence-connected-operations clause. Strongest case against:
P1 is a pruning problem, and this is the first concept *added* after seven
prunings — the model could grow again by accretion. Counter-evidence: the
term was already load-bearing and undefined in five framework surfaces
(recoverability, working-session record, archive, visualization), which is
the ownerless-state defect the adversarial checklist hunts; defining it
removes ambiguity rather than adding machinery, and the addition carries no
lifecycle, schema field, or required artifact. No compiled knowledge or
prior decision is contradicted; the 2026-08-06 current-state-reporting
closure anticipated exactly this behavioral validation path. Only the
proposing agent reviewed this reasoning.

## Changes

- [`framework/VOCABULARY.md`](../../../framework/VOCABULARY.md) — new
  `Current state` entry (owned state plus optional derived current-state
  view) under *Problems and tasks*; `Working-session record` and `Archive`
  now link to it.
- [`framework/README.md`](../../../framework/README.md) — orientation phase
  reads current state; the work-session and task-recoverability paragraphs
  reference the vocabulary entry; the recoverability paragraph names the
  optional derived view.
- [`framework/CHANGELOG.md`](../../../framework/CHANGELOG.md) — entry
  "current state defined as a first-class concept."
- [Feedback record](../framework-feedback/2026-08-06-current-state-first-class.md)
  — the maintainer's report captured with provenance.

## Open questions

- None load-bearing. Whether the view concept should ever appear in
  `SCHEMA.md` is deliberately not proposed — APS prescribes no view, so the
  declaration contract is unaffected.

## Lessons and friction

- The promotion path ran instance-first: Operations implemented and used the
  pattern before the framework defined it, so the vocabulary entry inherited
  ready-made answers to the design questions the closed task had left open.
  This is what strategy point 4 looks like when it works; worth repeating for
  future additions.
- A one-line grep of the term across `framework/` was enough to surface the
  five load-bearing undefined uses that justified the entry. Cheap term
  sweeps are effective ownerless-state detectors, complementing the earlier
  lesson that orientation questions are cheap duplication detectors.
- `origin/main` moved by two feedback-capture commits during the session;
  because they only added new stream files, a fast-forward before delivery
  resolved it without conflict. The snapshot refresh absorbed them as
  ungroomed in-flight items, which is exactly the staleness-visibility job
  the new concept describes.

## Acceptance and delivery

The maintainer reviewed the compiled changes and said "finish" on
2026-08-06; per the brainstorming process that is the bounded approval
signal for the reviewed session scope and authorizes delivery to
`origin/main`. Verification: repository checks pass (links resolve, the
vocabulary/README/changelog are consistent, no declaration change). P1's
signal reading: the maintainer's "very useful" report on the operating
current-state pattern is direct understand-and-operate outcome evidence —
an improvement reading, with the framework-level generalization's own
usefulness a delayed observation for later teach-back and use. The delivery
commit is referenced in this record's frontmatter follow-up.
