---
entity:
  identity:
    type: slug
    value: key-aps-s-31-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-07-12T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-31
---

# Review the system strategy concept

## Frame

Give system strategy the smallest clear definition, boundary, relationships,
ownership, representation, and lifecycle needed by the complete APS loop. The
responsible user and decision authority is the APS framework maintainer. This
review addresses P1's concept-simplification strategy after the system,
boundary, and system-problem dependencies were reviewed.

A useful stopping point is one reviewed disposition propagated through the
normative framework and Framework Operations, with downstream questions
captured without deciding problem-strategy or other lower-level concepts beyond
what consistency requires.

## Current evidence

- The normative [definition](../../../framework/VOCABULARY.md#system-strategy)
  makes system strategy the current theory, interpretation, and approach for
  solving the stable root system problem.
- The [framework explanation](../../../framework/README.md#problem-hierarchy-and-strategy)
  assigns it system-wide evidence interpretation, problem decomposition and
  comparison, guidance of problem strategies, execution, verification,
  learning, and adaptation.
- The declaration [contract](../../../framework/SCHEMA.md) represents it as a
  sibling `STRATEGY.md` linked from `SYSTEM.md`.
- The Framework Operations [strategy](../../STRATEGY.md) currently contains an
  approach, problem-grooming guidance, and adaptation authority.
- The [problem-grooming process](../../processes/problem-grooming.md) limits
  system-strategy changes to changes in the overall approach and keeps
  problem-specific methods in each problem strategy.

## Confirmed strengths

Applying the concept review test surfaced no defects in the concept's
structure:

- Its authoritative state has one location, the sibling `STRATEGY.md` linked
  from `SYSTEM.md`. Nothing competes with it as a source of truth.
- It owns no durable identity or state beyond a document that changes with
  evidence, so it correctly has no lifecycle machinery.
- Its change authority is explicit: the maintainer approves changes to the
  Framework Operations strategy, and the current strategy stays authoritative
  until an approved change replaces it.
- Its working line against problem strategy already exists in the
  problem-grooming process: system strategy owns the overall approach, and
  problem-specific methods stay in each problem's strategy.

## Load-bearing question raised

The review asked whether system strategy is one concept or two conflated ones.

The general strategy definition already covers "the current evidence-informed
theory and approach for changing one problem" and states that the system
strategy is the one belonging to the root system problem. Under that definition
alone, system strategy needs no separate entry.

The vocabulary and framework definitions then assign it a second and different
job: how the system interprets evidence, decomposes and compares problems,
guides lower strategies, executes, verifies, learns, adapts, and coordinates
subsystems. That is an operating model rather than an approach to one problem.
The Framework Operations strategy shows the same split in practice: its
*Approach* section is a theory of the root problem, while *Guidance for problem
grooming* and *Adaptation* describe how the loop runs.

The operator's recommendation was to demote the concept, keeping one general
strategy definition and moving the operating-model responsibilities to the
process surfaces that perform them.

## Maintainer decision

The maintainer decided to **retain** system strategy as-is and tighten wording
only. System strategy legitimately carries the system-wide operating
responsibilities alongside the root-problem approach; they are one concept in
use, and separating them would add a concept rather than remove one. The
standalone definition, the system-wide scope, and the existing representation
are kept.

The accepted tightening does not change scope:

- The vocabulary and framework definitions previously named different
  responsibilities in different order. They now name the same responsibilities
  in the same order.
- The vocabulary definition said "validates" for the loop stage. APS reserves
  validation for artifact and outcome validation and uses verification for
  evaluating attempts against a problem signal, so the definition now says
  "verifies results."
- "Theory, interpretation, and approach" dropped its redundant middle term,
  since evidence interpretation is already named in the responsibility list.
- The scope distinction from problem strategy is now stated in the definition
  rather than left to the problem-grooming process.
- Strategy change is now linked to adaptation, which already governs
  authority-bearing changes to strategy.

## Deferred

The conflation question is recorded rather than closed. If the teach-back or
adversarial passes in P1's validation strategy show that readers cannot tell
system strategy from problem strategy, or cannot locate the operating-model
responsibilities, this concept is a candidate for reopening. No downstream
concept was decided by this review.

## Validation

Immediate validation passes: the vocabulary and framework definitions now name
the same responsibilities; the declaration contract, the `strategy` link from
`SYSTEM.md`, and the Framework Operations strategy required no change under a
retain disposition; all declared strategy, loop, verification, work-session,
and stream process paths resolve; the task references P1; and
`git diff --check` passes.

## Acceptance and delivery

The maintainer accepted the retain disposition and the wording alignment on
2026-07-26. Commit `e5a7b7d` contains the accepted framework change; the task is
closed and archived.

---

Legacy participants: APS framework maintainer, Codex operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-07-12-system-strategy-review.md","legacyId":"apss.session.system-strategy-review"}

---

[repository-import:session:apss.session.system-strategy-review@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-07-12-system-strategy-review.md]
