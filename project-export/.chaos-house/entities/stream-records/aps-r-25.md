---
entity:
  identity:
    type: key
    value: APS-R-25
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-17T16:50:02.393Z
  dispositionNote: 'Closed — accepted as-is by the maintainer (APS-S-38). The legacy typing of the 33 imported sessions as "brainstorming" and their missing task/problem links are a recorded migration limitation; provenance stays recoverable in the session bodies and source commit 43b9f69. LICENSE was verified still tracked at the repository root on main outside project-export, so the wiki projection never dropped it and no import is needed. No work created. Reconsideration: if teach-back or adversarial verification actually needs session→task traceability, recover it from the source commit then.'
  groomed: true
  key: APS-R-25
  keyNumber: 25
  labels:
    - migration-follow-up
    - repository-import
  originSession: session:key:APS-S-34
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-17T16:56:21.159Z
---

Import-fidelity residuals from the 2026-08-17 migration audit (APS-S-34), not remediated during cutover:

1. All 33 legacy working-session records were imported with type "brainstorming" and none are linked to their source tasks or problems. This includes one expected-output fixture that is not a working session at all. If the legacy typing is accepted as-is, that acceptance should be recorded; otherwise the sessions need re-linking or an explicit note that Chaos House sessions cannot be retyped/relinked after close.

2. LICENSE is the sole tracked source file (of 143) not imported from repository commit 43b9f69. Decide whether it belongs in the wiki projection or is intentionally left to the Git repository only.
