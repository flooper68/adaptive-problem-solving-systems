---
entity:
  identity:
    type: key
    value: APS-58
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-17T09:39:40.748Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-58
  keyNumber: 58
  labels:
    - migration-follow-up
    - repository-backup
  originSchedule: null
  originSession: session:key:APS-S-34
  originTask: null
  parent: null
  priority: 3
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: backlog
  summary: null
  title: Promote the proven repository projection to main
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-17T09:39:40.748Z
---

## Intent

After the Chaos House repository projection has operated reliably long enough for the owner to trust it, make the synchronized projection the repository's `main` branch and update the APS repository-backup configuration to write to `main` instead of `chaos-house-backup`.

## Trigger

Do not act immediately. Revisit when observed backup operation and a recovery or restore check give the owner enough confidence that Chaos House can remain the canonical writer without losing or corrupting project state.

## Work

- Confirm the projected branch is current, the backup reports converged, and `main` has no independent changes that would be lost.
- Review the exact merge or fast-forward plan and preserve a recoverable pre-cutover reference.
- Merge the synchronized projection into `main`.
- Change the APS repository-backup setup so future projections target `main`.
- Verify a subsequent projection succeeds and that the repository remains a one-way backup rather than a second source of truth.

## Context

Chaos House became the canonical APS system of record during the 2026-08-17 migration. The temporary `chaos-house-backup` branch isolates the new projection while its reliability is being established.
