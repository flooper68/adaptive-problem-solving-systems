---
id: apss.modular-system-concerns
type: task
status: closed
owner: APS framework maintainer
created: 2026-07-10
source: APS framework maintainer idea intake
---

# Modularize growing concerns from `SYSTEM.md`

## Idea

Allow substantial and growing concerns such as strategy to move from the main
`SYSTEM.md` into clearly visible dedicated folders, beginning with
`strategy/`, while retaining a concise declaration and navigable source of
truth.

## Motivation

A single declaration can become difficult to inspect as strategy and other
concerns accumulate. Dedicated modules could make the framework setup and its
major concerns visible from the directory structure, give each concern room to
evolve, and keep `SYSTEM.md` focused on system identity and integration.

## Evidence

- The current schema requires `strategy` as a string in `SYSTEM.md`.
- The standard capsule permits required concepts to share files when clearer
  and says empty ceremonial directories add no value.
- The framework already permits produced artifacts outside the capsule when
  their paths and ownership remain explicit, but it does not define extraction
  rules for declaration concerns such as strategy.
- Framework Operations links to a separate strategy file, but no additional
  application validates whether the modular layout generalizes.

## Open questions

- Which concerns may be extracted, and what growth or complexity threshold
  justifies a dedicated module?
- Must `SYSTEM.md` retain a concise strategy summary and link, or may the
  required field become a path or structured reference?
- Should a module use `strategy/README.md`, `strategy/index.md`, or another
  predictable entry contract?
- How will declaration review, visualization generation, compilation, and tools
  resolve modular content?
- How should authority, provenance, and duplication be handled between the
  declaration and detailed modules?
- Is `strategy/` a framework convention, an optional example pattern, or a
  system-specific layout choice?
- Which other concerns are credible candidates, and how can modularity avoid
  fragmentation or empty ceremony?

## Grooming log

### 2026-07-10 — captured

Captured from the APS framework maintainer's proposal to move growing content
such as strategy from `SYSTEM.md` into a dedicated folder so the setup is more
visible and extensible. Strategy is the first example, not an approved schema
change or a decision to create other folders.

### 2026-08-07 — closed: contradicted by current maintainer direction

Groomed in the
[first cadenced grooming invocation](../../streams/working-sessions/2026-08-06-first-cadenced-grooming.md);
approved by the maintainer, sequenced after approval of the colocation
feedback. The maintainer's groomed
[colocation feedback](../../streams/framework-feedback/archived/2026-08-06-system-declaration-colocation.md)
pulls the opposite direction — fold strategy and verification into
`SYSTEM.md` rather than extracting concerns into dedicated folders — and the
strategy prefers the smaller reversible change. **Closed as contradicted**;
its executable successor is
[`apss.colocate-system-declaration`](../colocate-system-declaration.md).
Reconsideration trigger: declarations growing past comfortable single-file
reading after colocation.
