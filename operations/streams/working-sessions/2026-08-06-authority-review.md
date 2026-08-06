---
id: apss.session.authority-review
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: [apss.review-authority]
---

# Review system and adaptation authority

## Frame

Decide whether authority is an APS concept, apply the concept review test from
[P1](../../problems/p1-finish-mvp-and-run-loop.md), and propagate one
disposition. The responsible user is the APS framework maintainer. This is the
tenth concept review and the second-to-last Direction-level review before
`apss.review-subsystem-and-relationships`.

## Orientation

Four findings framed the decision:

**Authority was a load-bearing term the vocabulary never defined.** Five
entries leaned on it — problem grooming and adaptation were
"authority-governed," open and closed were "authorized decisions," and the
Strategy entry said "the system's declared authority changes it."

**The model existed once, as a principle.** The framework definition's
"Process participants and authority" section said each process defines who
participates and who approves its decisions, and that participation does not
imply authority. `SCHEMA.md` excluded authority from the declaration.

**The task-family review had already pruned the task half.** Its principle —
the framework keeps responsibilities, authorities, and boundaries, not state
names — removed selection and authority machinery from tasks on 2026-07-27.

**"Declared authority" was residue.** The Strategy entry and the loop diagram
said authority was declared, but nothing declared it anywhere: the declaration
model that once carried it was removed, and view 3 still drew a "Declared
approver" node.

## Exploration and decision

The operator asked whether authority should get a small vocabulary entry as a
property-concept or remain ordinary English with only the residue fixed. The
maintainer went further than either option: APS should not define authority as
a first-class citizen at all — it can be part of a specific implementation,
but not of the MVP.

Asked whether that removes only the qualifier wording or also the framework's
delegation requirement (that every process must state who decides), the
maintainer grounded the deeper cut in the model itself: **APS defines no
owners or personas, so there can be no concept of authority.** With no one for
authority to attach to, the framework cannot require or govern it.

Decision: **remove authority from the framework entirely.** The decisions it
qualified are untouched — problem grooming still opens and closes problems,
adaptation still accepts and applies changes — but the framework no longer
implies that it defines who may make them. Who participates and who decides
are choices each system's processes state for themselves. Instance-level
authority rules, such as Framework Operations naming its maintainer as
adaptation approver, are exactly where the ruling says such rules belong and
are unchanged.

This is the seventh pruning disposition, after goal removal, boundary
demotion, open problem, problem strategy, the two task-state entries, and task
collection. Like the open-problem removal, it was reached from the
maintainer's own reasoning rather than an operator recommendation — the
operator had recommended the shallower cut.

## Changes

- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — "authorized" and
  "authority-governed" qualifiers removed from the system, strategy, feedback,
  insight, task, problem-grooming, open, closed, and adaptation entries;
  adaptation now states that who decides it is each system's process choice.
- [`README.md`](../../../framework/README.md) — "Process participants and
  authority" became "Process participants" carrying the single boundary
  statement; the loop diagram adapts without "declared authority"; the
  closure-decision diagram node, problem-creation paragraph, decision-history
  paragraph, creating-a-system step 4, work-session process responsibilities,
  and assessment checklist dropped the term.
- [`SCHEMA.md`](../../../framework/SCHEMA.md) — authority removed from the
  list of concerns that belong outside the declaration.
- [`VISUALIZATION.md`](../../../framework/VISUALIZATION.md) — view 3's
  "Declared approver" node became "Adaptation decision."
- [`CHANGELOG.md`](../../../framework/CHANGELOG.md) — entry recorded.
- [`review-authority.md`](../../tasks/archive/review-authority.md) — closed
  with the remove disposition and moved under `tasks/archive/`.
- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — grooming history
  records the seventh pruning disposition.

## Observations this surfaced

**"Authoritative" survives with a different job.** The framework still calls
systems of record authoritative for current state. That is the
source-of-truth sense of the word, not decision power; the review left it
alone. Whether readers separate the two senses is a question for the
teach-back pass.

**The task named ownership too.** The framework's "owns" language — a problem
owns its signal, loop ownership — is concept-to-concept placement of
authoritative state, not a person owner, so the maintainer's no-owners ruling
does not disturb it. Operations task files carry an instance-level `owner`
field, which the ruling permits. Flagged during review rather than edited.

## Open questions

P1's own signal rewrite remains open from the problem-signal review,
unchanged here.

## Acceptance and delivery

The maintainer reviewed the compiled changes and asked to finish the session
on 2026-08-06; per the brainstorming process that acceptance approves
delivering this session's scope to `origin/main`. A separate, unfinished
prior session's changes to three intake process files remain in the working
tree and are deliberately excluded from this delivery. The delivery commit is
referenced in this record's frontmatter follow-up.
