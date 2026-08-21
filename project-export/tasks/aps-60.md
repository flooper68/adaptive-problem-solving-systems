---
entity:
  identity:
    type: key
    value: APS-60
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-17T17:07:42.524Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-21T06:59:38.372Z
  key: APS-60
  keyNumber: 60
  labels:
    - process-improvement
    - grooming
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 2
  problem: problem:slug:p1
  queuePosition: null
  startedAt: 2026-08-17T17:08:25.283Z
  status: done
  summary: "Maintainer approved and the revision is applied to processes/sessions/grooming.md (new step 3 Read the signal; step 5 strategy test with failure dispositions; step 8 enumerated adaptation decisions; completion criteria enforce all three). Verified: session type resolves to the revised page, no warnings, P1 reading appended to the problem state log, current state refreshed. Validation continues in the next grooming invocation, run as the experiment the maintainer requested."
  title: Make verification, strategy application, and adaptation mandatory phases of the grooming process
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T06:59:38.373Z
---

## Intent

The first root grooming (APS-S-38) satisfied processes/sessions/grooming.md nominally while skipping its substance: no fresh signal reading was taken for P1, the strategy's grooming guidance was not tested against the open problems (P1's declaration is a bare title and fails it), and the adapt-before-selecting-work step was passed with an unexamined "none needed". Maintainer feedback is APS-R-27; the reference experience is chaos-house-development's problem-grooming.md, whose phase structure makes these responsibilities unskippable.

## Work

Compare processes/sessions/grooming.md with chaos-house-development's problem-grooming.md (and its pre-grooming handoff boundary) and revise the APS process so that a conforming invocation must:

1. **Read the signal in-session** — for each in-scope problem, take the declared signal reading per Verification during the invocation, append it to records/problem-state-log.md, and compare with the prior entry; inheriting a recent reading requires an explicit maintainer acceptance, not a default. State the root health judgement or record why it stays unset.
2. **Apply the strategy explicitly** — test every in-scope problem against the strategy's grooming guidance (identifies parent; states evidence, desired outcome, strategy, and a readable signal; work selected only when it implements or tests the problem strategy) and record a disposition for each failure.
3. **Treat adaptation as work** — enumerate material learnings since the boundary and record an explicit decision for each on whether it tweaks the problem statement, composition, strategy, verification, or process; "no change" is a recorded decision with reasons, not a skipped step.

Keep the single-process, proportional-scope model from APS-59; do not introduce new session types. Adopt CHouse's decision discipline (challenge pass, revisit triggers) in APS plain language where it strengthens the above without importing ceremony.

## Validation

The revised page makes APS-S-38's shortcuts impossible to record as a complete invocation; the next grooming runs with the revised process and the maintainer judges whether it produces the CHouse-quality experience. Completion criteria in the process must require the appended reading (or recorded unreadability), the per-problem strategy check, and the enumerated adaptation decision.

## Context

Follows APS-59 (which added scope proportionality) and the 2026-08-17 migration. Related: APS-R-27 (maintainer feedback), CHouse processes problem-grooming.md / pre-grooming.md at chaos-house-development.
