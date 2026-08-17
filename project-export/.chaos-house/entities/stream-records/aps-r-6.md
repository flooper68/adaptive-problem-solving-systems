---
entity:
  identity:
    type: key
    value: APS-R-6
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:43.258Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-6
  keyNumber: 6
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:41:14.957Z
---

# Every input stream needs grooming, declared propagation, and a check that catches the gap

## Report

### Context

During the problem-strategy concept review the maintainer asked whether a
process exists for grooming insights and feedback. Orientation found two
grooming processes ([`insight-grooming.md`](../../../processes/insight-grooming.md),
[`framework-feedback-grooming.md`](../../../processes/framework-feedback-grooming.md))
and an asymmetry around them: `problem-grooming` is a declared work-session type
in [`operations/SYSTEM.md`](../../../SYSTEM.md) while insight and feedback grooming
are not, and the `working-sessions` stream purpose still describes itself as
preserving brainstorming and problem-grooming invocations only.

Reading the five declared streams together, three of them — `working-sessions`,
`framework-usage`, and `external-foundations` — name `processes/process.md` as
`consumed_by` and have no grooming responsibility at all.

### Observed problem or outcome

- Grooming is uneven across input streams and nothing in APS makes it
  otherwise. [`VOCABULARY.md`](../../../../framework/VOCABULARY.md) states that a
  system "may implement different grooming for each problem or input stream" —
  permission, not a responsibility. A system can therefore declare a stream,
  capture into it, and never process what it captured.
- Where grooming does exist, the framework states only one propagation target.
  [`README.md`](../../../../framework/README.md) problem-lifecycle says
  source-specific grooming "may propose a higher-level problem to solve" and
  says nothing about grooming's other legitimate outputs.
- Nothing catches this class of inconsistency. It surfaced from an ad-hoc
  question during an unrelated concept review. The declaration review list in
  [`SCHEMA.md`](../../../../framework/SCHEMA.md) checks reference resolution and ID
  uniqueness but not whether each declared stream is actually consumed, and the
  stale `working-sessions` purpose line went unnoticed through the
  work-session declaration being added.

### Desired outcome

- Grooming is part of the process for every type of input stream, not an option
  exercised per stream.
- The propagation from stream grooming is stated: it can influence problem
  grooming and change problems, add to compiled knowledge, or create tasks.
- A repeatable check exists that catches process and declaration issues of this
  kind instead of relying on someone noticing.

### Suggested response

The maintainer proposed:

1. make grooming a general part of the loop process, covering every declared
   input stream;
2. state that stream grooming's results may reach problem grooming, the
   problems themselves, compiled knowledge, or task creation;
3. add a "linting" or "doctor" capability that catches these process issues.

These are proposals. Whether each belongs to normative APS semantics or to a
system's own implementation is a grooming question — in particular the doctor,
which could be a normative review responsibility, a Framework Operations
process, or supporting tooling.

### Evidence

Direct maintainer design feedback from the current session. Supporting
repository state at the time of capture: the five stream entries in
[`operations/SYSTEM.md`](../../../SYSTEM.md); the permissive grooming sentence in
[`VOCABULARY.md`](../../../../framework/VOCABULARY.md); the single stated
propagation target in [`README.md`](../../../../framework/README.md); and the
declaration review list in [`SCHEMA.md`](../../../../framework/SCHEMA.md), which
also records that the stream shape "is retained pending the separate
stream-concept review". Report and repository observation; the proposed
responses are not independently validated.

## Grooming record

### 2026-08-07 — act: route to the information-stream and process reviews

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Evidence consulted:** the consolidated
  [`grooming.md`](../../../processes/sessions/grooming.md), the vocabulary's
  system entry, and the two linked review tasks.
- **Assessment:** at Operations level, two of the three proposals have been
  overtaken since capture — the consolidated grooming process grooms every
  input kind and states its propagation targets (problems, tasks, compiled
  knowledge) in its propagation step. What remains open is framework-level:
  the vocabulary still says a system "may implement different grooming for
  each problem or input stream" — permission, not a responsibility — and the
  proposed "doctor"/declaration-linting check has no owner.
- **Disposition:** **act** — this record becomes input evidence to
  [`apss.review-information-stream`](../../../tasks/review-information-stream.md)
  (grooming as per-stream responsibility versus permission, stated
  propagation) and to
  [`apss.review-process`](../../../tasks/review-process.md) (the doctor
  proposal, which is process/declaration linting). Both tasks link back
  here. The information-stream review is the next selected work.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-07-26-stream-grooming-and-declaration-doctor.md","legacyId":"apss.feedback.stream-grooming-and-declaration-doctor"}

---

[repository-import:stream-record:apss.feedback.stream-grooming-and-declaration-doctor@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-07-26-stream-grooming-and-declaration-doctor.md]
