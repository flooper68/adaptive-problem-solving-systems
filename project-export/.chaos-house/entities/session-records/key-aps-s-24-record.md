---
entity:
  identity:
    type: slug
    value: key-aps-s-24-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-07-11T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-24
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

---

Legacy participants: APSS framework maintainer, Codex operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-07-11-session-close-delivery.md","legacyId":"apss.session.session-close-delivery"}

---

[repository-import:session:apss.session.session-close-delivery@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-07-11-session-close-delivery.md]
