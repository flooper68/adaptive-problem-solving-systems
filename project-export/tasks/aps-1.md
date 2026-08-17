---
entity:
  identity:
    type: key
    value: APS-1
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:30.288Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-17T09:59:27.320Z
  key: APS-1
  keyNumber: 1
  labels:
    - repository-import
    - aps-legacy
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 3
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: done
  summary: |
    Published and verified the representation-neutral APS system declaration contract. Repository capsules and Chaos House structured projects are now explicit profiles of one responsibility-level contract; live filename-bound strategy definitions were removed, P1 evidence/current state were refreshed, and the repository backup converged successfully.
  title: Make the system declaration contract representation-neutral
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-17T09:59:27.323Z
---

# Make the system declaration contract representation-neutral

## Intended result

Revise the normative declaration contract so it requires the system name,
stable root problem, strategy, verification, complete-loop process, work
sessions, and streams to be recoverable and connected without requiring one
`SYSTEM.md` file, YAML, colocation, or separation.

Keep the repository capsule as one valid representation profile and document
the migrated Chaos House project as another. Propagate the decision through
the framework definition, vocabulary, schema, and changelog.

## Evidence

- `APS-R-7`: direct maintainer feedback that the repository's separate
  strategy and verification files were confusing and asymmetric with problem
  files.
- `APS-S-34`: the migration showed that Framework Operations can preserve the
  same responsibilities through four connected declarations and native
  work-session and stream entities without a `SYSTEM.md`.
- `APS-S-35`: the migrated APS operation and evidence paths were reconciled
  without changing the system problem, strategy, or framework meaning.
- P1's strategy: prefer the smallest model the maintainer can understand and
  add structure only from observed need.

## Acceptance

- The framework states declaration responsibilities independently of storage.
- Colocation and separation are both valid when navigation is clear.
- The repository and structured-project shapes are examples, not universal
  rules.
- Every live normative reference that defines system strategy through
  `SYSTEM.md` or `STRATEGY.md` is corrected; historical changelog entries stay
  unchanged as history.
- Framework Operations remains semantically conformant in Chaos House with no
  duplicate canonical declaration.

## Legacy provenance

Imported from `apss.colocate-system-declaration` at source commit
`43b9f6918677ef654578c2276e1c8e4d615fcbf7`. The migration supplied new
evidence that revised the proposed response from mandatory colocation to a
representation-neutral contract.
