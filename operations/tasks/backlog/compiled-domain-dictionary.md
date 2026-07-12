---
id: apss.compiled-domain-dictionary
type: task
status: captured
owner: APS framework maintainer
created: 2026-07-10
source: APS framework maintainer idea intake
---

# Compile and maintain a domain dictionary

## Idea

Make a domain dictionary a first-class compiled-knowledge output, deriving
terms, meanings, aliases, relationships, context, and provenance from retained
domain knowledge instead of relying only on a manually maintained glossary.

## Motivation

Consistent terminology helps people and agents interpret system declarations,
evidence, plans, and knowledge in the same way. Compilation could also expose
ambiguous, conflicting, context-dependent, or deprecated terms that need
resolution rather than silently choosing one meaning.

## Evidence

- APS requires each system to compile reusable knowledge with provenance and
  uncertainty preserved.
- The proposed `framework/VOCABULARY.md` now gives APS itself one concise,
  authoritative terminology surface, but it does not define a generated or
  domain-specific dictionary output or compilation rules.
- No evidence yet establishes which dictionary fields or representations are
  useful across domains.

## Open questions

- Is a dictionary universally required, recommended when terminology becomes
  material, or specific to selected systems?
- What should remain in the normative APS vocabulary, and what belongs in a
  system-specific compiled domain dictionary?
- Should it be part of the primary compiled-knowledge artifact, a generated
  projection, or a supporting artifact?
- Which fields are needed for definitions, aliases, deprecated language,
  examples, counterexamples, concept relations, ownership, confidence,
  provenance, and revision history?
- How should conflicting or context-specific meanings be represented without
  flattening legitimate differences?
- Which sources qualify terms for inclusion, and which approval rules govern
  normative definitions?
- What human-readable and machine-consumable formats should share the same
  source of truth?
- Should this be shaped together with the knowledge-compilation refinement
  item or remain independently deliverable?

## Grooming log

### 2026-07-10 — captured

Captured from the APS framework maintainer's proposal that a domain dictionary
be compiled. No artifact contract or universal framework requirement has been
approved.

### 2026-07-10 — narrowed by initial APS vocabulary

The open-problem framework compilation starts a manually maintained normative
APS vocabulary with exact framework meanings. This is a smaller and distinct
result from the candidate's broader generated domain-dictionary concept. The
candidate remains captured for later grooming rather than treating the initial
vocabulary as evidence that every system needs such a dictionary.
