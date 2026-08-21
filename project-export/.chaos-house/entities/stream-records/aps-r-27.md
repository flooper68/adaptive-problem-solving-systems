---
entity:
  identity:
    type: key
    value: APS-R-27
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-17T17:00:04.281Z
  dispositionNote: "Act — maintainer decided to fix the process first: produced APS-60 to make in-session signal readings, explicit strategy application, and enumerated adaptation decisions mandatory phases of processes/sessions/grooming.md, with chaos-house-development's problem-grooming.md as the reference. The next grooming re-runs with the revised process; the maintainer judges whether the experience matches CHouse. The APS-S-38 selection of APS-21 stands until that re-run confirms or revises it."
  groomed: true
  key: APS-R-27
  keyNumber: 27
  labels:
    - process-improvement
    - grooming
  originSession: null
  originTask: null
  problem: problem:slug:p1
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-17T17:07:50.060Z
---

Maintainer feedback on the first root grooming invocation (APS-S-38, 2026-08-17), given immediately after it closed: the grooming was unsatisfying compared to how grooming works in chaos-house-development. Specifically:

1. Verification was not run for the core problem — no fresh P1 signal reading was taken; the session leaned on the same-day APS-S-36 reading instead of reading the signal in the grooming itself.
2. The strategy was not applied — the strategy's own grooming guidance (every open problem identifies its parent and states evidence, a desired outcome, a strategy, and an observable signal) was not checked against P1, whose problem declaration is in fact a bare title.
3. New learning was not considered for adaptation — the process's adapt-before-selecting-work step was passed with "none needed" without genuinely testing whether the migration and recent completions warrant tweaking the problem composition, statement, or strategy.

The maintainer points to chaos-house-development's grooming as the model that feels right. Open question for grooming: whether these are execution failures against the existing processes/sessions/grooming.md (which does contain orientation, problem-picture review, and adaptation steps) or gaps in the process text itself that a comparison with chaos-house-development's groom-* processes would expose.
