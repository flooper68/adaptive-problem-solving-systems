---
entity:
  identity:
    type: slug
    value: key-aps-s-44-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-21T08:45:32.501Z
  outcome: completed
  session: session:key:APS-S-44
---

Brainstorming APS-S-44 — replace the automated session types with a dogfooding-style type. Problem P1.

Participants: maintainer, Claude Code agent.

Decisions (maintainer): retire automated-brainstorming and automated-grooming (never used, 0 sessions, no schedules) and delete their pages; add a session type modelled on Chaos House dogfooding: record one observation, work out what it means, decide, and apply a small clear change to the affected page in the same sitting. Different session types may have different flows, so no change to intake.md (R-29) or grooming.md step 8. Prefer small clear processes over one big one — a separate type, not a grooming fast path. The session may change any page the input points at, framework/ included, following knowledge-compilation.md + framework-adaptation.md as brainstorming does; a process-page change states its expected effect for the retrospective. Whoever starts the session judges whether the item is small enough. Fix is applied in the session (knowledge project, no development stage); a task only on handoff.

Changed: processes/sessions/dogfooding.md (new, SHA per wiki); session type aps-dogfooding (manual); automated-brainstorming and automated-grooming retired 08:40Z; processes/sessions/automated-brainstorming.md and automated-grooming.md deleted; processes/README.md edited (final SHA 8e4e2630). No framework/ change.

Incident: session-type names are global. The first save_session_type under the name dogfooding moved Chaos House's own type into the APS project. Restored it (project chaos-house-development, processes/dogfooding.md, rewritten description) and created ours as aps-dogfooding. Lesson: check get_session_type before save_session_type.

Verification: pages re-read, type resolves without warnings, CH and APS type listings checked. P1 signal unchanged — process change only; next trigger is the first real aps-dogfooding run. Backup export failing (integrity-failure) since 2026-08-17; surfaced, not acted on. APS-S-43 left open (other conversation).
