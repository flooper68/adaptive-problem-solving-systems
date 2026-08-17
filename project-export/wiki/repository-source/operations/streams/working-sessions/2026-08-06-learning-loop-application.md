---
id: apss.session.learning-loop-application
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
delivery: 673f546
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session, continuing from the grooming-consolidation session
related_problems: [P1]
related_tasks: [apss.current-state-reporting]
---

# Apply the learning-loop package: intake consolidation, snapshots, adversarial beat

## Frame

After delivering the grooming consolidation, the maintainer raised a series
of gaps in one discussion — current-state visibility, retrospectives, a
"heartbeat" cadence, adversarial review, and process-directory
comprehensibility — then asked for a summary, a review of the conclusions,
and final questions before applying. The intended result is the
evidence-backed subset of that package applied as reviewable changes.

## Decisions

Recorded from the maintainer's explicit answers to the pre-application
questions:

1. **Deliver the grooming consolidation** — done first (`dd63166`).
2. **Evidence-backed subset only.** The alignment/adversarial beat, applied
   to the package itself, sorted it into evidence-backed (intake
   consolidation, snapshots, adversarial beat, session lessons,
   working-sessions as grooming input) and anticipation-heavy (declaring a
   heartbeat work session that has never run). The maintainer chose the
   subset; heartbeat runs as ordinary grooming invocations first.
3. **Keep under P1** rather than opening a second problem; recorded in P1's
   grooming history with a reconsideration trigger.
4. **Root snapshot in a separate `STATE.md`** (different change cadence than
   the declaration), and the archiving ruling captured as a second insight.

Discussion decisions carried into the design: grooming keeps its
framework-aligned name — "heartbeat" was assessed as a cadence name, not an
activity name; grouping the processes stays a presentation-layer view
(README), not folders; priority remains problem-anchored rather than
kind-based.

## Changes

- [`intake.md`](../../processes/intake.md) — the three intake processes
  consolidated into one shared skeleton (announce, capture with per-kind
  templates, clarify one question at a time, automatic delivery for insight
  and feedback records); `insight-intake.md`, `framework-feedback-intake.md`,
  and `task-intake.md` deleted per the compiled-knowledge ruling. Live
  references updated in `SYSTEM.md`, `process.md`, `grooming.md`,
  `brainstorming.md`, `knowledge-compilation.md`, `ai-agent-tasks.md`, and
  stream READMEs.
- [`processes/README.md`](../../processes/README.md) — derived loop-stage
  index; grouping as a view instead of folders.
- [`grooming.md`](../../processes/grooming.md) — alignment and adversarial
  beat in the decide step (which problem/strategy the disposition serves,
  contradictions with compiled knowledge, strongest objection, P1's promoted
  defect checklist); lessons-and-friction and snapshot-refresh duties in
  evidence and retention.
- [`brainstorming.md`](../../processes/brainstorming.md) — new "Challenge"
  step before compilation with the same beat and the self-review limit
  stated; delivery step refreshes snapshots; session records carry a
  lessons-and-friction note.
- [`SYSTEM.md`](../../SYSTEM.md) — working-sessions stream consumed by
  grooming as well as the loop process; purpose mentions lessons notes;
  intake references updated.
- [`STATE.md`](../../STATE.md) — new thin root snapshot: open problems,
  recent deliveries, next work; date-stamped, refreshed at delivery,
  explicitly subordinate to authoritative files.
- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — new `Current state`
  section; grooming-history entry recording the keep-under-P1 decision and
  heartbeat deferral.
- Groomed under the new process (first real invocations):
  [roadmap insight](../insights/archived/2026-07-26-roadmap-concept-may-be-useful.md)
  — **act**, merged into current-state-reporting and executed;
  [current-state-reporting](../../tasks/archive/current-state-reporting.md)
  — **act** then **close: delivered**, moved to `tasks/archive/`;
  [adversarial-review insight](../insights/archived/2026-07-26-adversarial-review-absent-from-deliberation.md)
  — recurrence appended, **act**, beat implemented.
- New insight captured:
  [processes are compiled knowledge](../insights/archived/2026-08-06-processes-are-compiled-knowledge.md).

## Open questions

- Whether the unified `intake.md` reads clearly enough with three embedded
  templates, or should shed them into per-stream README examples.
- Whether heartbeat earns declaration after one or two manual grooming
  invocations; STATE.md's "Next" section carries the trial.
- The compiled-knowledge insight's release question: does the delete-not-
  archive rule hold for published framework versions consumed by others?

## Lessons and friction

- The consolidation argument applied twice in one day (groomings, then
  intakes); the duplication was visible for weeks but only became actionable
  when the maintainer asked a naive question ("do we have a concept of
  grooming?"). Orientation questions are cheap duplication detectors.
- The adversarial beat's first target was the package proposing it, and it
  changed the outcome (heartbeat deferred). Self-review caught the
  structural issue; it would not have caught a blind spot — the limit is
  real and now stated in the process text.
- Working-tree hygiene mattered constantly: three concurrent scopes (this
  session, the authority session delivered mid-way by another agent, and
  foreign files appearing in the tree) required exact staging throughout.
  A `Foreign changes` check before staging may deserve a process sentence
  if it recurs.
- A real staging error occurred and was corrected: `git rm`/`git mv` stage
  immediately, so a later narrow intake-delivery commit (`c4cdb1f`) swept
  three deletions and a rename belonging to this still-under-review session
  onto `origin/main`; restored by `git checkout` from the parent commit and
  a follow-up commit before continuing. Candidate process lesson for
  `ai-agent-tasks.md`: verify `git diff --cached --stat` matches the
  intended bounded scope immediately before any intake-delivery commit.

## Acceptance and delivery

The maintainer reviewed the applied package and said "finish" on 2026-08-06;
per the brainstorming process that is the bounded approval signal for the
reviewed session scope and authorizes delivery to `origin/main`. Two foreign
working-tree items from a concurrent session are excluded (a modification to
`operations/tasks/archive/review-authority.md` and the untracked
`2026-08-06-automated-session-type.md` record). The compiled-knowledge
insight was delivered separately (`c4cdb1f`) per `intake.md`. The delivery
commit is referenced in this record's frontmatter follow-up.
