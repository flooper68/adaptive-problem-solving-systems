---
entity:
  identity:
    type: slug
    value: key-aps-s-26-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-06T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-26
---

# Archived folders for the feedback and insight streams

## Frame

The maintainer reported that the feedback and insight streams should have an
`archived/` folder that the processes feed after grooming, for easier
orientation in the project. The session ran intake, grooming, and execution
of the resulting task end to end.

## Intake

Captured as framework feedback
([`archived/2026-08-06-stream-archived-folders.md`](../framework-feedback/archived/2026-08-06-stream-archived-folders.md))
with one clarification: a record groomed with a **keep** disposition also
moves — in the maintainer's words, "archived means 'groomed'"; the stream
root shows only what still awaits processing. The executable response was
captured as the linked task
[`stream-archived-folders.md`](../../tasks/archive/stream-archived-folders.md).
Automatic intake delivery was blocked by a non-fast-forward push (four
concurrent-session commits had landed on `origin/main`); after the
maintainer's go-ahead the local commit was rebased onto the remote and
delivered as `b462827`.

## Decisions

1. **Archived means groomed.** Every disposition — including `keep` —
   archives the record once its grooming entry is recorded; archiving marks
   that processing happened and is not a new lifecycle state.
2. **The rule lives in the grooming process.** One sentence in
   [`grooming.md`](../../processes/sessions/grooming.md)'s status paragraph;
   the stream READMEs restate the convention for readers arriving at the
   directories.
3. **Historical statuses qualify by their grooming record, not their
   vocabulary.** Records with a recorded disposition moved (`actionable`,
   `supported`, `contested`, `provisional`, `groomed`, and one `received`
   record whose grooming entry showed it was acted on); the mid-grooming
   `problem-creation-grooming-and-storage` report stayed because its
   grooming explicitly continues.

## Changes

- `framework-feedback/archived/` and `insights/archived/` created; four
  feedback records and seven insight records moved, with internal relative
  links re-depthed and all inbound links across problems, tasks, and session
  records updated.
- [`grooming.md`](../../processes/sessions/grooming.md) — archiving rule
  added to the stream-status paragraph.
- Both stream READMEs — convention stated.
- Feedback record groomed (**act**) and archived; task updated with the
  execution record (close and move under `archive/` at delivery).
- Stale "Not yet groomed" boilerplate removed above the recorded grooming
  entry in the moved `framework-constraints-seem-redundant` insight.
- This working-session record.

## Stopping point

Intake delivered (`b462827`). Grooming and execution changes compiled and
reviewed; the maintainer accepted the remaining working-tree scope and asked
to finish and deliver it. By delivery time the concurrent
subsystem-and-relationships review (`ca6a082`) and grooming-cadence
(`04eb6bc`) sessions had delivered their scopes, so this session's scope was
the whole remaining tree. The task is closed and archived with the delivery.
Delivered as commit 99014d1; this delivery reference was recorded in a
follow-up commit per the established pattern.

## Lessons and friction

- Three sessions working the same checkout produced a rejected push, an
  autostash conflict across three shared files (`CHANGELOG.md`, `STATE.md`,
  P1), and mid-session edits appearing under this session's feet. The
  per-session exact-staging discipline held, but shared mutable summary
  files (`STATE.md`, P1 `Current state`) are the recurring collision
  surface.
- The intake process's non-fast-forward blocker worked as designed: it
  stopped an automatic push from silently entangling three sessions'
  uncommitted scopes, and the maintainer's explicit go-ahead resolved it.

---

Legacy participants: APS framework maintainer, Claude Code operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-08-06-stream-archived-folders.md","legacyId":"apss.session.stream-archived-folders"}

---

[repository-import:session:apss.session.stream-archived-folders@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-08-06-stream-archived-folders.md]
