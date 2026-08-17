---
entity:
  identity:
    type: key
    value: APS-R-5
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:39.227Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-5
  keyNumber: 5
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:41:12.948Z
---

# Stream declaration entries are too complex; an entry should be name, description, and a process link

## Report

### Context

The maintainer was reading the `streams` declarations in
[`operations/SYSTEM.md`](../../../SYSTEM.md) and quoted the `external-foundations`
entry, which carries five fields per the template in
[`framework/SCHEMA.md`](../../../../framework/SCHEMA.md): `purpose`, `source`,
`access`, `consumed_by`, and `grill`. SCHEMA.md itself notes the entries'
"richer shape is retained pending the separate stream-concept review"
([`apss.review-information-stream`](../../../tasks/review-information-stream.md),
still open).

### Observed problem or outcome

The maintainer's words: "this structure is too complex, the input stream
should have just name, description and link to a process file, that's it."

### Desired outcome

A stream declaration entry consists of a name, a description, and a link to a
process file — nothing more. The dedicated fields carry unnecessary
information, and keeping several per-stream fields aligned with the processes
they describe is a maintenance burden that invites drift.

### Suggested response

Reduce the stream entry shape in the SCHEMA.md template (and the entries in
`operations/SYSTEM.md`) to name, description, and process link. This mirrors
the shape already used for `work_sessions` entries (id, description, process).
When clarified, the maintainer chose that the description absorbs the jobs of
the removed fields: a single free-text description can mention source or
consumers when relevant, without dedicated `source`, `access`, `consumed_by`,
or `grill` fields.

### Evidence

Direct maintainer feedback from the current session. Supporting repository
state at the time of capture: the five-field stream entries in
[`operations/SYSTEM.md`](../../../SYSTEM.md); the matching template and the
"richer shape is retained pending the separate stream-concept review" note in
[`framework/SCHEMA.md`](../../../../framework/SCHEMA.md); the three-field
`work_sessions` entry shape in the same files. The suggested response is not
independently validated.

## Intake and clarification record

### 2026-08-06 — captured and clarified

Initial statement preserved verbatim in the Observed problem section. Two
clarification questions were asked and answered:

- Where do the removed fields' jobs go? — The description absorbs them: a
  single free-text description can mention source or consumers when relevant,
  without dedicated fields.
- What effect does the five-field shape have? — It is unnecessary
  information, and a maintenance burden (per-stream fields must be kept
  aligned as processes change).

Clarification reached a useful stopping point; no questions remain open.
Whether the change lands in the `framework/SCHEMA.md` contract, in
`operations/SYSTEM.md`, or both is left to grooming, likely alongside
[`apss.review-information-stream`](../../../tasks/review-information-stream.md).

## Grooming record

### 2026-08-07 — act: candidate disposition for the information-stream review

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Evidence consulted:** the five-field entries in `operations/SYSTEM.md`,
  the SCHEMA.md template and its "richer shape is retained pending the
  separate stream-concept review" note, and the three-field `work_sessions`
  precedent.
- **Assessment:** the maintainer's proposed shape — name, description, and a
  process link — mirrors the work-session entry shape and serves P1 strategy
  point 3 (prefer the smaller model the maintainer can understand). The
  change lands in the compiled framework (`SCHEMA.md`), which grooming never
  edits, and SCHEMA.md itself defers the shape to the stream-concept review.
- **Disposition:** **act** — this record becomes input evidence to
  [`apss.review-information-stream`](../../../tasks/review-information-stream.md),
  now the next selected work; the three-field shape is the concrete
  candidate disposition for that review to adopt and propagate through
  `framework/SCHEMA.md` and `operations/SYSTEM.md`.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-08-06-stream-declaration-complexity.md","legacyId":"apss.feedback.stream-declaration-complexity"}

---

[repository-import:stream-record:apss.feedback.stream-declaration-complexity@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-08-06-stream-declaration-complexity.md]
