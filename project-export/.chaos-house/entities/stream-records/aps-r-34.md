---
entity:
  identity:
    type: key
    value: APS-R-34
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T09:30:37.221Z
  dispositionNote: null
  groomed: false
  key: APS-R-34
  keyNumber: 34
  labels: []
  originSession: session:key:APS-S-47
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T09:30:37.221Z
---

# process.md lacks a flow diagram of inputs, session types and their connections

## Context

The maintainer reading `processes/process.md` (the operating loop every piece of work follows) on 2026-08-21. The page is prose: a nine-step numbered loop. The input kinds live in `processes/intake.md` and the session types (brainstorming, grooming, aps-intake, aps-dogfooding, retrospective) in `processes/README.md` and `processes/sessions/*`; process.md names only some of them in passing.

## Observed problem or outcome

The process file does not show, in one place, all inputs and all session types, nor how they connect — which input feeds which session, which session hands off to which, and where the loop returns to itself.

## Desired outcome

A reader of process.md can see the whole flow at a glance: every input kind, every session type, and the connections between them, as a flow diagram.

"Inputs" means the kinds defined in `processes/intake.md` — framework feedback, insight, usage observation, external foundation, task candidate — not the orienting inputs of loop step 1 (clarified by the maintainer, 2026-08-21).

## Suggested response

Add a flow diagram to process.md covering all inputs and session types and how they connect. (Maintainer's words; form of the diagram not specified.)

## Evidence

- Maintainer statement in session APS-S-47, 2026-08-21: "the process file should include all inputs/ session types and how they connect in a flow diagram."
- process.md as read in that session (sha 706d7e92…): prose loop, no diagram; step 2 mentions grooming, step 4 session types generically, step 7 the retrospective and brainstorming; intake, dogfooding, streams and the input kinds are not named in the loop.
- Operator note: a process page changes only through a retrospective or a brainstorming session (process.md step 7); that constrains any response but is not part of the report.
