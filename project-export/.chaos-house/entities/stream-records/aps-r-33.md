---
entity:
  identity:
    type: key
    value: APS-R-33
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T09:01:01.943Z
  dispositionNote: null
  groomed: false
  key: APS-R-33
  keyNumber: 33
  labels:
    - intake
    - process
  originSession: session:key:APS-S-45
  originTask: null
  problem: problem:slug:p1
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T09:01:01.943Z
---

Intake should identify the input kind and route it to a kind-specific process

Kind: framework feedback (about applying APS in Framework Operations).

## Context
On 2026-08-21 the maintainer asked whether APS has an intake process and whether one was defined before the migration to Chaos House (dogfooding).

## Observed problem or outcome
The wiki `processes/intake.md` as of 2026-08-17 was five generic steps with no input-kind identification. The pre-migration `operations/processes/intake.md` (first committed 2026-08-06, `673f546`) distinguished framework feedback, insight, and task candidate, each with its own capture template, announcement, clarification, and delivery rules. That distinction was dropped in the migration. Streams `framework-usage` and `external-foundations` had no intake process; task candidates had no intake path; no intake session type existed.

## Desired outcome (maintainer's words)
"I would like the intake process to identify which type of input it is and use the proper process for the given input."

## Suggested response
Not specified by the maintainer beyond "create the new session type and update the processes". Operator note: the legacy page was a recoverable starting point.

## Evidence
- Wiki `processes/intake.md` before change, sha `1a6ff60f20473df4f8a718c5cdf2312ca2598ef0dba84660045595f2613a1b5f`.
- Legacy `operations/processes/intake.md` in the repository backup.
- `list_streams` for `aps-framework-operations` on 2026-08-21: intake process set only on `framework-feedback` and `insights`.

## Disposition note
Acted on in the same sitting in session APS-S-45 (brainstorming): `processes/intake.md` rewritten, `processes/sessions/intake.md` created, session type `intake` registered, both remaining streams pointed at the intake process. Captured after the change on the maintainer's instruction; the record preserves the observation, not the fix.
