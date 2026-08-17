---
entity:
  identity:
    type: slug
    value: key-aps-s-36-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-17T09:59:41.795Z
  outcome: completed
  session: session:key:APS-S-36
---

# Working-session record — APS-S-36

## Outcome

Completed APS-1 by making the APS system declaration contract
representation-neutral.

## Scope and decision

The session reviewed the pre-migration colocation proposal against the observed
Chaos House migration. The maintainer approved revising the response: APS now
requires a connected orientation to the system name, stable root problem,
strategy, verification, complete-loop process, work sessions, and streams, but
does not require one `SYSTEM.md`, YAML, colocation, or separation.

The repository capsule and Chaos House structured project are documented as
valid representation profiles rather than competing sources of truth or
universal formats. The strongest alternative — retain mandatory `SYSTEM.md`
and synthesize it from Chaos House — was rejected because it preserved a
storage mandate contradicted by observed use.

## Changed canonical state

- Reframed and linked task APS-1 to P1.
- Replaced `framework/SCHEMA.md` with the responsibility-level contract and
  two representation profiles.
- Updated `framework/README.md` and `framework/VOCABULARY.md` to remove live
  filename-bound definitions.
- Added the 2026-08-17 decision to `framework/CHANGELOG.md` and updated its
  audit-trail description for the Chaos House source of truth.
- Appended the APS-S-36 reading to `records/problem-state-log.md` and refreshed
  `problems/p1/current-state.html`.

## Verification

- Exact canonical SCHEMA content read back successfully.
- Remaining `SYSTEM.md` and `STRATEGY.md` mentions are limited to the explicit
  repository profile or historical changelog context.
- APS Framework Operations reports no declaration warnings.
- P1 improved in understandability: the maintainer understood and approved the
  responsibility-versus-representation distinction. The concept inventory
  remains 12 reviewed and 18 remaining; teach-back and adversarial verification
  remain never run; a full unaided explain-and-run check remains untested.
- Repository backup converged with `pending: false` at projection commit
  `7459e04d2b5e1d940df5fed4eeb6982d2480b3c9`.

## Lessons and friction

Observed migration exposed a normative storage assumption that repository-only
review had not. One responsibility-level conformance checklist preserves
portability without requiring every implementation to mimic the first one's
files. The interactive process required a separate exact-draft approval and a
separate close decision; no other material friction occurred.

## Stopping point

APS-1 and APS-S-36 are ready for the maintainer's explicit completion and
close decision. P1 remains open. After closure, task grooming should select the
next P1 concept review from current evidence.
