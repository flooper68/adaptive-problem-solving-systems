---
id: apss.session.session-close-delivery
type: working-session
status: retained
recorded: 2026-07-11
accepted: 2026-07-11
closed: 2026-07-11
delivery: 6702230
participants: [APSS framework maintainer, Codex operator]
source: Maintainer feedback after ending the prior session
related_problems:
  - P1
related_tasks:
  - apss.review-work-session
---

# Deliver accepted changes when a session finishes

## Frame

Correct the session lifecycle so an accepted repository-backed session includes
delivery rather than ending with reviewed changes only in the working tree.

## Material decision

An unresolved stopping point leaves a handoff and uncommitted work. Maintainer
acceptance or an explicit request to finish or end the reviewed session is a
bounded approval signal to validate, commit the session-scoped changes, and push
them to `origin/main`. The session becomes retained and closed only after that
delivery succeeds; otherwise it remains awaiting delivery with the blocker
recorded.

## Affected artifacts

- [Brainstorming process](../../processes/brainstorming.md)
- [AI-agent task process](../../processes/ai-agent-tasks.md)
- [Work-session review task](../../tasks/review-work-session.md)
- [Agent guidance](../../../AGENTS.md)

## Current stopping point

The maintainer accepted the process improvement and explicitly asked to finish
the session. Commit `6702230` delivered the complete reviewed scope to
`origin/main`, exercising the new close rule successfully.
