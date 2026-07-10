---
id: apss.relax-system-declaration-schema
type: task
status: captured
owner: APSS framework maintainer
created: 2026-07-10
source: APSS framework maintainer request
source_records: []
---

# Remove the system declaration schema while the framework evolves

## Proposed action

Temporarily remove the current machine-readable system declaration schema and
all schema enforcement while the framework's concepts and structure are still
changing. Do not replace it with a minimal core schema during this phase. Keep
the declarative `SYSTEM.md` structure and describe it through the human-readable
template and framework guidance.

## Intended result

Framework and example declarations retain a consistent, understandable
declarative structure but can evolve without schema migrations or
schema-validation work whenever that structure changes.

## Motivation

The strict schema adds coordination and maintenance work while the framework is
being simplified and its declaration shape remains unsettled. Relaxing it for
now may make iteration faster and reduce premature commitment to structure.

## Evidence

- The APSS framework maintainer requested full removal of the schema for now,
  rather than retaining a minimal core.
- The maintainer clarified that the declarative structure remains wanted; the
  formal schema definition is the over-engineered part.
- The current repository treats `framework/system.schema.json` as the normative
  machine-readable contract and validates system declarations against it.

## Open questions

- Which documentation, examples, validation steps, and tooling would need to
  change together so the schema's removal is represented consistently?
- No trigger for reconsidering a formal schema is known yet; grooming should
  determine whether an explicit trigger is useful.

## Grooming log

### 2026-07-10 — captured

Captured from the APSS framework maintainer's request to ditch the strict
schema for now in order to simplify the framework. The exact replacement level
and the conditions for restoring stricter validation remain to be clarified.

### 2026-07-10 — full removal clarified

The maintainer clarified that the schema should be removed fully for now, with
no minimal core schema retained. Guidance and the trigger for reconsidering a
schema remain open.

### 2026-07-10 — declarative structure retained

The maintainer clarified that the declarative structure is still wanted and
should remain documented. Only the separate formal schema definition and its
enforcement are considered unnecessary at this stage.

### 2026-07-10 — reconsideration trigger left open

The maintainer was unsure what future condition should trigger reconsidering a
formal schema. No trigger was inferred; the question remains for grooming if it
becomes relevant.
