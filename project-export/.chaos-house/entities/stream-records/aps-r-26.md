---
entity:
  identity:
    type: key
    value: APS-R-26
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-17T16:50:10.314Z
  dispositionNote: "Act — routed to chaos-house-development, approved by the maintainer (APS-S-38). Remediation belongs to that project; captured there as CH-R-105 in its issues stream (task creation is not available cross-project from this session, so the record enters CHD's own grooming). Content: stale aps-vocabulary.md (05ef870 vs 43b9f69), refresh script and AGENTS.md pointing at a nonexistent checkout path, and the likely repointing of the refresh source to the canonical wiki framework/VOCABULARY.md."
  groomed: true
  key: APS-R-26
  keyNumber: 26
  labels:
    - migration-follow-up
  originSession: session:key:APS-S-34
  originTask: null
  problem: null
  stream: stream:slug:framework-feedback
  updatedAt: 2026-08-17T16:56:23.500Z
---

Cross-project staleness observed during the 2026-08-17 migration audit (APS-S-34): chaos-house-development/reference/aps-vocabulary.md is generated from APS commit 05ef870 while the migrated project is at 43b9f69. The refresh script's default source path points at the nonexistent ~/dev/adaptive-problem-solving-systems (actual checkout: ~/dev_personal/adaptive-problem-solving-systems), and AGENTS.md carries the same stale path. Additionally, now that the canonical vocabulary lives in this project's wiki at framework/VOCABULARY.md, the refresh source itself may need repointing from the Git checkout to the wiki projection. Remediation belongs to the chaos-house-development project; this record exists so the gap is dispositioned rather than lost.
