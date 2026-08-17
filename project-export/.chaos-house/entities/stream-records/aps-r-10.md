---
entity:
  identity:
    type: key
    value: APS-R-10
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:40:45.962Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-10
  keyNumber: 10
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-16T19:41:17.522Z
---

# Working sessions should not need declaring as an input stream — they are information streams automatically

## Report

### Context

The maintainer recorded this feedback directly. Repository state at the time
of capture: [`operations/SYSTEM.md`](../../../SYSTEM.md) declares
`working-sessions` as the first of five entries in its `streams:` section,
alongside the `work_sessions:` section that declares the session types
producing those records. The framework already treats working-session records
as an information stream by definition — the information-stream definition in
[`README.md`](../../../../framework/README.md) lists "working-session records"
as its first example — yet its work-session retention guidance says to retain
records "in a declared working-session stream or its native system of
record", and [`SCHEMA.md`](../../../../framework/SCHEMA.md) has systems declare
streams explicitly.

### Observed problem or outcome

Initial statement, verbatim: "working session should not be defined in input
streams - they are information streams automatically".

Working sessions are declared twice in a system declaration: once as
work-session types and again as an input-stream entry, even though a system
that runs work sessions inherently produces working-session records as an
information stream.

### Desired outcome

Clarified 2026-08-06 with the maintainer: the framework wording is fine as it
stands. The desired outcome is operational — Framework Operations'
[`SYSTEM.md`](../../../SYSTEM.md) no longer carries a redundant `working-sessions`
entry in its `streams:` section, because a system that declares work-session
types produces that information stream automatically.

### Suggested response

Remove the `working-sessions` entry from the `streams:` section of
[`operations/SYSTEM.md`](../../../SYSTEM.md). The maintainer chose not to capture
a task candidate at intake; whether and how to make the change is left to
grooming of this record.

### Evidence

Direct maintainer design feedback from the current session, plus the
repository observations in Context. Clarification was two questions: the
maintainer scoped the feedback to Framework Operations cleanup rather than a
framework-semantics change, and declined a linked task candidate. Report and
observation; the suggested response has not been validated. Operator note,
distinct from the source's words: the entry being removed carries retention
and consumption details (one file per material session under
`streams/working-sessions/`, consumed by `processes/process.md` and
`processes/sessions/grooming.md`); whether any of that needs relocating is a
grooming question.

## Grooming record

### 2026-08-07 — act: redundant stream entry removed

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Evidence consulted:** `operations/SYSTEM.md`, the working-sessions stream
  README, and the consolidated grooming process.
- **Assessment:** the operator note's relocation question resolves to
  nothing needing relocation — retention (one file per material session
  under `streams/working-sessions/`) already lives in the stream README, the
  grooming process already names the session records as its cadence counter,
  and the loop process consumes session records as evidence regardless of a
  declared stream entry, which is this record's own point. The edit is an
  Operations-declaration change, not a compiled-framework change.
- **Disposition:** **act** — the `working-sessions` entry was removed from
  the `streams:` section of `operations/SYSTEM.md`, executed with this
  entry per the maintainer's approval.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/framework-feedback/archived/2026-08-06-working-sessions-are-streams-automatically.md","legacyId":"apss.feedback.working-sessions-are-streams-automatically"}

---

[repository-import:stream-record:apss.feedback.working-sessions-are-streams-automatically@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/framework-feedback/archived/2026-08-06-working-sessions-are-streams-automatically.md]
