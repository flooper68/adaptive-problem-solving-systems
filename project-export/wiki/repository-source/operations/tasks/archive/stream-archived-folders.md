---
id: apss.stream-archived-folders
type: task
status: closed
owner: APS framework maintainer
created: 2026-08-06
closed: 2026-08-06
source: Maintainer feedback in the current Claude Code session
source_records:
  - apss.feedback.stream-archived-folders
---

# Add archived folders to feedback and insight streams fed by grooming

## Proposed action

- Create `archived/` subdirectories in
  `operations/streams/framework-feedback/` and
  `operations/streams/insights/`.
- Extend [`grooming.md`](../../processes/sessions/grooming.md) so that once a
  stream record's grooming disposition is recorded, the record moves into its
  stream's `archived/` folder — for every disposition, including `keep`,
  because archived means "groomed", not "closed".
- Move the existing already-groomed records in both streams into the new
  folders, preserving relative links.
- Update both stream READMEs to state the convention: the stream root holds
  records awaiting grooming; `archived/` holds processed ones.

## Intended result

Looking at a feedback or insight stream directory immediately shows which
records still need grooming, mirroring the existing `archive/` pattern for
closed problems and tasks.

## Motivation

Maintainer feedback
[`2026-08-06-stream-archived-folders.md`](../../streams/framework-feedback/archived/2026-08-06-stream-archived-folders.md):
flat stream folders mix processed and unprocessed records, making orientation
in the project harder as the streams grow.

## Evidence

- 6 feedback and 14 insight records currently share flat directories with
  mixed lifecycle statuses (`received`, `captured`, `grooming`, `actionable`,
  `supported`, `contested`, `provisional`, `groomed`).
- `operations/tasks/archive/` already receives closed tasks, so the pattern
  is established in the operations layout.

## Open questions

- Which historical statuses count as "groomed" when moving existing records —
  the pre-consolidation vocabularies (`actionable`, `supported`, `contested`,
  `provisional`) presumably qualify, but each file's grooming record should
  confirm a disposition was actually recorded.
- Whether the working-sessions stream needs the same treatment is out of
  scope; the maintainer named only the feedback and insight streams.

## Grooming log

### 2026-08-06 — captured

Captured during the same intake as its source feedback record; not yet
groomed.

### 2026-08-06 — act: selected and executed

The maintainer approved the source feedback's **act** disposition in session
and selected this task for immediate execution. Executed by the Claude Code
operator: `archived/` folders created in both streams, the move rule declared
in [`grooming.md`](../../processes/sessions/grooming.md), eleven already-groomed
records relocated with their inbound and internal links updated, and both
stream READMEs updated. The open question about historical statuses was
resolved by reading each candidate's grooming record: records with a recorded
disposition moved (including historical statuses `actionable`, `supported`,
`contested`, `provisional`); the mid-grooming
`problem-creation-grooming-and-storage` report stayed in the stream root
because its grooming explicitly continues. Closed and moved under `archive/`
at session delivery; details in the
[working-session record](../../streams/working-sessions/2026-08-06-stream-archived-folders.md).
