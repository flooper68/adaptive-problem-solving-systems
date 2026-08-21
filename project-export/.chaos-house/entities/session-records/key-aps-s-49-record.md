---
entity:
  identity:
    type: slug
    value: key-aps-s-49-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-21T09:37:48.733Z
  outcome: completed
  session: session:key:APS-S-49
---

Topic: is a quick-groom session type missing? Trigger: maintainer wanted APS-62 moved backlog→todo without a root grooming. Orientation: process.md, processes/README.md, grooming.md, APS-62. Finding: grooming already declares an item scope but applied all nine steps to it verbatim; process.md step 3 (select one bounded task) is separate from step 2 (groom). Alternatives weighed: (1) treat backlog→todo as process.md step 3 inside the working session; (2) new triage/quick-groom type; (3) make item scope cheaper. Decision: (3), no new type. Changed path: processes/sessions/grooming.md (sha e6fc2724…), paragraph "Item scope is the quick groom" added under Invocation and scope. Expected effect and reopen trigger recorded in the session note. Validation: edit applied with no warnings; page re-read not needed (SHA-guarded). Handoff: APS-62 itself was not moved in this session — do it as an item-scope grooming or by starting its brainstorming session. Lesson: scope names in a process need matching step relief or they stay ceremonial.
