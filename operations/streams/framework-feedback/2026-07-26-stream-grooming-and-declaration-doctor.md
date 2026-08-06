---
id: apss.feedback.stream-grooming-and-declaration-doctor
type: framework-feedback
status: received
received: 2026-07-26
reporter: APS framework maintainer
source: Maintainer-agent discussion in the current Claude Code session, recorded in streams/working-sessions/2026-07-26-problem-strategy-review.md
related_feedback:
  - apss.feedback.problem-creation-grooming-and-storage
  - apss.feedback.unbounded-stream-indexes
related_work:
  - apss.review-information-stream
  - apss.review-process
---

# Every input stream needs grooming, declared propagation, and a check that catches the gap

## Report

### Context

During the problem-strategy concept review the maintainer asked whether a
process exists for grooming insights and feedback. Orientation found two
grooming processes ([`insight-grooming.md`](../../processes/insight-grooming.md),
[`framework-feedback-grooming.md`](../../processes/framework-feedback-grooming.md))
and an asymmetry around them: `problem-grooming` is a declared work-session type
in [`operations/SYSTEM.md`](../../SYSTEM.md) while insight and feedback grooming
are not, and the `working-sessions` stream purpose still describes itself as
preserving brainstorming and problem-grooming invocations only.

Reading the five declared streams together, three of them — `working-sessions`,
`framework-usage`, and `external-foundations` — name `processes/process.md` as
`consumed_by` and have no grooming responsibility at all.

### Observed problem or outcome

- Grooming is uneven across input streams and nothing in APS makes it
  otherwise. [`VOCABULARY.md`](../../../framework/VOCABULARY.md) states that a
  system "may implement different grooming for each problem or input stream" —
  permission, not a responsibility. A system can therefore declare a stream,
  capture into it, and never process what it captured.
- Where grooming does exist, the framework states only one propagation target.
  [`README.md`](../../../framework/README.md) problem-lifecycle says
  source-specific grooming "may propose a higher-level problem to solve" and
  says nothing about grooming's other legitimate outputs.
- Nothing catches this class of inconsistency. It surfaced from an ad-hoc
  question during an unrelated concept review. The declaration review list in
  [`SCHEMA.md`](../../../framework/SCHEMA.md) checks reference resolution and ID
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
[`operations/SYSTEM.md`](../../SYSTEM.md); the permissive grooming sentence in
[`VOCABULARY.md`](../../../framework/VOCABULARY.md); the single stated
propagation target in [`README.md`](../../../framework/README.md); and the
declaration review list in [`SCHEMA.md`](../../../framework/SCHEMA.md), which
also records that the stream shape "is retained pending the separate
stream-concept review". Report and repository observation; the proposed
responses are not independently validated.

## Grooming record

Not yet groomed. See
[`grooming.md`](../../processes/sessions/grooming.md).
