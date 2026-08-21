---
entity:
  identity:
    type: slug
    value: key-aps-s-43-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-21T08:27:11.164Z
  outcome: completed
  session: session:key:APS-S-43
---

# Working-session record — APS-S-43 (brainstorming, P1)

## Topic and result

Add a `retrospective` session type: a process that checks whether one declared process works as written and as run, and changes the process page from evidence. Approved by the maintainer in full ("go") and applied. Operations only; no `framework/` page changed.

## Participants

Maintainer (decisions and approval); Claude Code operator (orientation, drafting, writes).

## Decisions (maintainer)

1. Retrospective is a separate session type, not a grooming scope. Reason: different inputs (session records), questions (adherence, cost, effect), and write target (process pages); grooming.md already too large (APS-63).
2. Grooming step 8 schedules a retrospective for process lessons instead of editing processes directly; grooming keeps authority over problem, task, and stream state.
3. Triggers: grooming schedules it; five runs of the process since its last retrospective; maintainer request; last signal unreadable. One process per session.
4. The retrospective opens by asking the maintainer what didn't work (four plain questions) before reading any session record; records then confirm, contradict, or are silent on each answer.
5. Strict prioritization: collapse findings to causes; rank by repeated → cost of being wrong → checkable fix; work at most three; park the rest with a trigger.
6. Maintainer corrections of procedure are recorded in the moment as `process:` session notes (process.md step 4). Missing data reads as "unreadable", never estimated.
7. Every process edit records its expected effect, checked at the next retrospective (process.md step 7).
8. Records: one append-only `records/process-state-log.md` with a fixed entry shape. Verified learnings go into the process pages themselves; cross-process rules collect in `processes/design-rules.md`.
9. Moving rules into `framework/` is undecided; a three-part graduation test (domain-independent, held twice, a new system would get it wrong without it) sits at the top of design-rules.md. Reconsider after the third retrospective or the first rule that passes.

## Changed canonical state

- New: `processes/sessions/retrospective.md`, `processes/design-rules.md`, `records/process-state-log.md`.
- Edited: `processes/sessions/grooming.md` (step 8 last two sentences; Signal section) → sha d5f14461; `processes/process.md` (step 4 `process:` note rule; step 7 retrospective path and expected-effect rule) → e65f89d3; `processes/README.md` (two list lines) → e80a6bd9; Signal sections appended to `sessions/brainstorming.md` (214b9759), `sessions/automated-grooming.md` (0570fad8), `sessions/automated-brainstorming.md` (3f7cf7fc).
- Session type `retrospective` created (manual) → `processes/sessions/retrospective.md`.
- Comment on APS-63: it is in substance the first grooming retrospective; consider running it as a `retrospective` session; keep the step-8 and Signal changes when revising grooming.md.
- P1 verification reading appended to `records/problem-state-log.md`.

## Verification

All written pages read back; session type resolves with no warnings; no declaration warnings; no contradiction with `framework/` (no prescribed session types; processes are compiled knowledge). P1 signal: inventory restated as 7 clusters, loop responsibilities unchanged in what has run plus one newly declared process, understandability carried from S-41 (not re-asked). Delayed evidence: retrospective effectiveness is unreadable until it has run twice on one process. Repository backup convergence not checked in-session; pending, not authority.

## Strongest case against (recorded)

Framework prefers merging over elaborating; a fourth grooming scope would have avoided a new type. Rejected for the reasons in decision 1. Reopen if the first two retrospectives show the page duplicating grooming's work.

## Handoffs and next trigger

- APS-63 (todo): run as a `retrospective` on grooming.md, or keep as brainstorming — maintainer's call.
- First retrospective on any process: when APS-63 runs, or after five grooming sessions.
- Design-rules graduation test: reconsider after the third retrospective.

## Lessons / friction

- `session_note` is capped at 1000 characters; one note had to be split.
- The draft was reviewed from a rendered scratchpad file plus inline summary; that worked for an 11-write change.
