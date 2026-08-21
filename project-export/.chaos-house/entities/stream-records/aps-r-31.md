---
entity:
  identity:
    type: key
    value: APS-R-31
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T07:59:36.848Z
  dispositionNote: null
  groomed: false
  key: APS-R-31
  keyNumber: 31
  labels:
    - feedback
    - agent-guidance
    - agent-behaviour
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T07:59:36.848Z
---

Maintainer feedback, 2026-08-21 (given in chat to the Claude Code agent working on aps-framework-operations).

Claim: when an agent refers to a task, problem, session, record, wiki file, or repository file in chat, it should give a link to that item (instance URL when the tool result provides one, otherwise the clickable wiki/repo path) next to the key or title, so the maintainer can open it for a quick look instead of searching for it.

Follow-up observation: the agent first stored this feedback in its local memory store; the maintainer corrected it, pointing at APS-R-30, which already asks that agent feedback be recorded in APS rather than local memory. The local memory entry was removed and this record created instead. This is a second instance of the pattern APS-R-30 describes, which strengthens the case for putting the "record feedback in APS" rule into the agent guidance itself.

Scope: all agents working this project, all chat references to project items. Uncertainty: none stated; whether Chaos House tool results expose item URLs in a form agents can link is for grooming to check.

Source: maintainer, chat, 2026-08-21. Disposition left to grooming.
