---
entity:
  identity:
    type: key
    value: APS-R-4
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:38.136Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-4
  keyNumber: 4
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:41:10.745Z
---

# Feedback and insight streams need archived folders fed by grooming

## Report

### Context

The maintainer reviewed how the local Framework Operations processes handle
the feedback and insight streams. Both stream directories are flat: records
awaiting grooming sit alongside records whose grooming is already recorded
(current statuses in the two folders include `received`, `captured`,
`grooming`, `actionable`, `supported`, `contested`, `provisional`, and
`groomed`). The insight stream README intentionally keeps no exhaustive
index, so the directory listing itself is the primary navigation.

### Observed problem or outcome

The maintainer's words: "the feedback + insights streams should have archived
folder + processes should move the files there after grooming for easier
orientation in the project." The stated friction is orientation: the flat
folders do not show which records still need attention.

### Desired outcome

Easier orientation in the project: looking at a stream directory should
distinguish records that still await processing from records already handled.

### Suggested response

Add an `archived/` folder to the `framework-feedback/` and `insights/`
streams, and have the declared processes — grooming in particular — move a
record there after it is groomed. (Operator note: this mirrors the existing
pattern where closed problems and tasks move under their `archive/`
directories per [`grooming.md`](../../../processes/sessions/grooming.md).)

### Evidence

- Direct maintainer report in the current session.
- Repository state at capture: 6 feedback records and 14 insight records in
  flat directories with mixed lifecycle statuses; `operations/tasks/archive/`
  already exists and receives closed tasks.
- Related report
  [`2026-07-10-unbounded-stream-indexes.md`](../2026-07-10-unbounded-stream-indexes.md)
  raised the adjacent concern that unbounded stream collections degrade
  navigation.

### Clarification (2026-08-06)

Asked whether a record groomed with a **keep** disposition (retain and
monitor) should also move to `archived/`, or whether only records needing no
further attention should move. The maintainer answered: "it was processed, so
we don't want to groom it again - archived means 'groomed'." Operator
restatement: `archived/` marks that grooming happened, independent of the
disposition chosen; every record moves there once its grooming disposition is
recorded, and the stream root then holds only records still awaiting
grooming.

The suggested response is captured as the linked task candidate
[`stream-archived-folders.md`](../../../tasks/archive/stream-archived-folders.md)
(`apss.stream-archived-folders`); capture carries no approval of priority or
adoption.

## Grooming record

### 2026-08-06 — act: executed in the capturing session

- **Participants:** APS framework maintainer and Claude Code operator.
- **Evidence consulted:** this report with its clarification, the statuses
  across both stream directories, the established `archive/` pattern for
  closed problems and tasks, and
  [`grooming.md`](../../../processes/sessions/grooming.md).
- **Alignment:** serves the same orientation concern recorded in
  [unbounded-stream-indexes](../2026-07-10-unbounded-stream-indexes.md) and
  extends an existing operations pattern rather than adding new lifecycle
  machinery; archived marks that grooming happened, it is not a new state.
- **Strongest case against:** every move breaks inbound relative links and
  adds a mechanical step to each grooming. Accepted: link fixes are one-time
  per record while the navigation benefit recurs with every visit to the
  stream.
- **Disposition:** **act** — approved by the maintainer in session; executed
  immediately through the linked task
  [`stream-archived-folders.md`](../../../tasks/archive/stream-archived-folders.md),
  which created the `archived/` folders, declared the move in the grooming
  process, and relocated the already-groomed records.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-08-06-stream-archived-folders.md","legacyId":"apss.feedback.stream-archived-folders"}

---

[repository-import:stream-record:apss.feedback.stream-archived-folders@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-08-06-stream-archived-folders.md]
