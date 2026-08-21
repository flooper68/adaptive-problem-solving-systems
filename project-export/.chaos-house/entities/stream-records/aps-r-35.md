---
entity:
  identity:
    type: key
    value: APS-R-35
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T09:31:23.806Z
  dispositionNote: null
  groomed: false
  key: APS-R-35
  keyNumber: 35
  labels: []
  originSession: session:key:APS-S-48
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T09:31:23.806Z
---

# A linting/review concept is needed so docs, processes and outputs stay consistent and coherent as they grow

## Context

Maintainer feedback, 2026-08-21, intake session APS-S-48. Not prompted by a specific incident: "just a long term concern as wiki and processes grow."

## Observed problem or outcome

Source words: "there should be some concept of linting/reviewing the docs/processes/outputs so they are consistent and coherent."

Operator note: the concern is about drift over time — as the wiki (framework pages, processes) and the outputs produced under them (records, sessions, tasks) accumulate, nothing systematically checks that they remain consistent with each other and internally coherent. No current inconsistency was named.

## Desired outcome

Documents, processes and outputs stay consistent and coherent as their number grows, caught by a repeatable mechanism rather than by someone noticing.

## Suggested response

A concept of "linting/reviewing". The maintainer did not specify whether as a normative APS responsibility, an Operations process or session type, or tooling. Unknown.

## Evidence

- Direct maintainer statement.
- Recurrence of the "doctor/linting" proposal in APS-R-6 (2026-07-26, routed to the `review-process` task on 2026-08-07, still unowned), now widened from declarations to docs, processes and outputs.
- Operator note, not source claim: APS-R-11's grooming distinguished mechanical consistency checks (a "doctor") from judgment-level adversarial review; this feedback falls on the mechanical side.
