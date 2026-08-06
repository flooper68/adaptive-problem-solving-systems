---
id: apss.session.grooming-cadence-declaration
type: working-session
status: retained
recorded: 2026-08-06
accepted: 2026-08-06
closed: 2026-08-06
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: []
---

# Declare the grooming cadence: every third working session

## Frame

The maintainer proposed tweaking the operations processes so grooming runs
every three sessions to take in accumulated feedback and insights and
reprioritize or groom the next steps. The intended result is the smallest
process change that makes that cadence a declared invocation rule.

## Orientation

- The same-day [learning-loop application
  session](2026-08-06-learning-loop-application.md) had groomed the
  "heartbeat" idea and deferred declaring it as anticipation-heavy:
  heartbeat runs as ordinary grooming invocations first and may be declared
  after observed use ([P1 grooming
  history](../../problems/p1-finish-mvp-and-run-loop.md)). That session
  also assessed "heartbeat" as a cadence name, not an activity name.
- [`grooming.md`](../../processes/sessions/grooming.md) already lists
  event-driven invocation triggers; a cadence is one more trigger, not a
  new session type.
- STATE.md carried the trial ("run 1–2 invocations before deciding") and
  listed the pending ungroomed backlog: remaining insights and feedback,
  and stale task review.
- Three working sessions have run since the last grooming invocations
  (automated-session-type, automated-session-precondition-stop,
  subsystem-and-relationships-review).

## Decisions

1. **Declare the cadence now, revising the same-day deferral.** The
   objection was presented per the Challenge step: the deferral's stated
   reconsideration evidence (observed use of the consolidated grooming
   process) does not yet exist. The maintainer decided the accumulated
   ungroomed backlog across back-to-back sessions is itself the evidence —
   an unforced cadence does not happen on its own — and chose "declare it
   now" over "trial first" with both cases in view.
2. **Cadence lives in one place.** The rule is recorded only as an
   invocation trigger in `grooming.md` (one grooming per three working
   sessions, counted from the working-session records, reset by any
   grooming invocation, a floor rather than a gate). `SYSTEM.md`'s
   work-session declaration is unchanged to avoid a second source of
   truth, and no new session type or artifact is created, honoring the
   cadence-not-activity finding.
3. **Reconsideration trigger.** After two cadenced invocations, grooming
   assesses whether the three-session interval fits observed cost and
   backlog size. Recorded in P1's grooming history.

## Changes

- [`processes/sessions/grooming.md`](../../processes/sessions/grooming.md)
  — cadence paragraph added to "Invocation and roles".
- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — `Current state`
  refreshed; grooming-history entry recording the revised deferral.
- [`STATE.md`](../../STATE.md) — snapshot refreshed; the first cadenced
  grooming invocation recorded as immediately due.
- This working-session record.

## Acceptance and delivery

The maintainer reviewed the compiled scope and asked to finish the session;
per the brainstorming process that acceptance approves delivery to
`origin/main`. The working tree concurrently held the uncommitted
stream-archived-folders execution scope, which also edits `grooming.md` and
`STATE.md`, so delivery staged this session's hunks exactly and left that
scope in the tree awaiting its own review. The delivery commit is recorded
in this record's `delivery` field per the established pattern.

## Lessons and friction

- A deferral can be legitimately revised the same day it was made when the
  awaited evidence arrives as an absence — the backlog the cadence was
  meant to prevent accumulated before any trial invocation ran. The
  adversarial beat still earned its place: the decision was made with the
  contradiction explicitly on the table.
- Two open sessions sharing P1's `Current state` section make exact
  staging fragile; a per-session diff check before delivery remains
  necessary.
