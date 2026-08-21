---
entity:
  identity:
    type: slug
    value: key-aps-s-45-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-21T09:04:21.307Z
  outcome: completed
  session: session:key:APS-S-45
---

Brainstorming APS-S-45 — intake identifies the input kind and routes it; intake session type. Problem P1.

Participants: maintainer, Claude Code agent. Context: dogfooding; maintainer asked whether APS has an intake process and whether one existed pre-migration, then asked for a session type and process update.

Evidence: wiki processes/intake.md (2026-08-17, sha 1a6ff60f) was five generic steps; pre-migration operations/processes/intake.md (673f546, 2026-08-06) distinguished framework feedback, insight, and task candidate with per-kind capture rules, dropped in the migration. Streams framework-usage and external-foundations had no intake process; task candidates had no intake path; no intake session type.

Decisions (maintainer): add a session type and update the processes; capture the originating observation as a record. Operator design choices, stated in notes: one intake.md with a kind/test/destination table for five kinds (framework feedback, insight, usage observation, external foundation, task candidate) rather than a page per kind; task candidates go to create_task backlog + label task-candidate; a separate session page that ends at capture; inputs arriving mid-session run intake inside the current session.

Changed: processes/intake.md rewritten (sha 2e5231ce); processes/sessions/intake.md new (final sha 2967b483, names type aps-intake); processes/README.md edited (sha e53ba440); session type aps-intake (id 884f4d3f, manual, processes/sessions/intake.md, resolves); streams framework-usage and external-foundations now intakeProcess processes/intake.md; record APS-R-33 captured (framework-feedback, P1, labels intake/process, ungroomed, disposition note points here). No framework/ change.

Incident: repeated S-44's. save_session_type `intake` moved Chaos House's global `intake` type (9a1f7a62, created 2026-08-15) into the APS project. Restored to chaos-house-development with processes/intake-session.md and a description rewritten from that page; APS type re-created as aps-intake. S-44's lesson (get_session_type before save_session_type) was available and not applied; now bitten twice — candidate for design-rules.md via retrospective.

Process deviation: pages applied session-bound on the maintainer's direct instruction before line-by-line text review; presented for correction afterwards (process: note recorded).

Expected effect by next retrospective on intake: records captured after 2026-08-21 carry a kind that grooming keeps unchanged in ≥ 4 of 5 cases; no capture outside a session; no further global-name collisions.

Verification: all written pages re-read; session types resolve without warnings; CH and APS type listings checked. P1 signal: unchanged — process change only, no loop run; next trigger is the first aps-intake session and the next grooming of APS-R-33. Backup: not inspected this session; S-44 reported export failing since 2026-08-17 (integrity-failure) — still a surfaced durability condition.

Handoffs: grooming of APS-R-33; optional dogfooding.md step 2 pointer to intake.md; design-rules candidate on global session-type names.
