---
entity:
  identity:
    type: key
    value: APS-R-29
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T07:39:46.655Z
  dispositionNote: null
  groomed: false
  key: APS-R-29
  keyNumber: 29
  labels:
    - process-improvement
    - intake
    - agent-behaviour
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T07:39:46.655Z
---

Maintainer feedback (2026-08-21): input intake should never spawn a different session. Capturing an input (feedback, insight, task candidate, problem, verification evidence) is its own act, done by a different consumer / persona / context than the one that later grooms or acts on it. The agent handling intake should record the input and stop — not offer to, or actually, start a grooming, brainstorming, or other session, and not link the input to problems or open work on the reporter's behalf. Disposition belongs to the groomer, in a grooming session, under the grooming persona.

Context: given right after capturing APS-R-28, when the intake agent closed by offering to link the record to a problem or start a grooming session immediately.

Open question for grooming: whether processes/intake.md and the session-type guidance state this separation explicitly enough, and whether the intake process should spell out what the intake agent does and does not do after capture.
