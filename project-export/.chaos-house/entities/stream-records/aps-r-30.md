---
entity:
  identity:
    type: key
    value: APS-R-30
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-21T07:59:15.625Z
  dispositionNote: null
  groomed: false
  key: APS-R-30
  keyNumber: 30
  labels:
    - feedback
    - agent-guidance
    - sessions
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-21T07:59:15.625Z
---

Maintainer feedback, 2026-08-21 (given in chat to the Claude Code agent working on aps-framework-operations).

Claim: An agent running a Chaos House work session should always say, in plain chat, what type of session it is running (e.g. "Starting a grooming session") — right after start_session and whenever it refers to the session later. Today the agent can run a session without naming its type, which hides which process is pinned and makes it hard to check that the agent follows the right loop.

Follow-up claim: the agent guidance (the repository CLAUDE.md / agents guidance, and any equivalent in the wiki processes) should be improved so that agents follow this by default, rather than relying on per-agent local memory. The maintainer also asked that agent feedback like this be recorded in APS (Chaos House), not in the agent's local memory store.

Context: raised while recording feedback after recent grooming/intake sessions. Scope: all typed sessions, all agents working this project. Uncertainty: none stated; the wording of the guidance change is left to grooming.

Source: maintainer, chat, 2026-08-21. Disposition left to grooming.
