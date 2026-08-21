---
entity:
  identity:
    type: key
    value: APS-R-32
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T08:10:41.240Z
  dispositionNote: null
  groomed: false
  key: APS-R-32
  keyNumber: 32
  labels:
    - feedback
    - intake
    - sessions
    - agent-guidance
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T08:10:41.240Z
---

Maintainer feedback, 2026-08-21 (given in chat to the Claude Code agent working on aps-framework-operations).

Claim: every intake — capturing feedback, an insight, a task candidate, a problem, or verification evidence — should begin by starting an APS session (start_session) as its first step, so the capture happens inside a typed, recorded session rather than as a loose tool call from chat.

Observation at capture time: the project currently declares only four session types (brainstorming, grooming, automated-brainstorming, automated-grooming) and no intake type. APS-R-29 forbids intake from spawning a grooming or brainstorming session, so an agent cannot follow this rule today. This record was therefore captured without a session. Grooming will need to decide whether to add an intake session type (and a process under processes/sessions/ pinning what intake does and does not do — see APS-R-29), or to satisfy the rule another way.

Context: raised right after APS-R-30 and APS-R-31, both about agent feedback handling; today's three feedback captures (APS-R-29, -30, -31) were all done outside any session. Scope: all intake by all agents on this project. Uncertainty: none stated about the rule; the session-type design is left to grooming.

Source: maintainer, chat, 2026-08-21. Disposition left to grooming.
