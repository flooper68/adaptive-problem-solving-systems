---
id: apss.deduplicate-readme-against-vocabulary
type: task
status: open
owner: APS framework maintainer
created: 2026-07-27
source: Maintainer feedback during the task-family review session
source_records:
  [operations/streams/working-sessions/2026-07-27-task-family-review.md]
---

# Make the framework definition reference the vocabulary instead of restating it

## Proposed action

Pass over `framework/README.md` section by section, and for each concept it
explains, replace restated definitions with a reference to the corresponding
`framework/VOCABULARY.md` entry, keeping only the explanation of how the
concept operates in the loop. Apply the division of labor now recorded in
`operations/processes/knowledge-compilation.md`: the vocabulary carries exact
meaning and boundary; the definition explains operation and references the
vocabulary.

## Intended result

Each concept's definition lives in exactly one place. A reader of the README
gets enough to understand the loop and a link for the exact boundary; a change
to a concept requires editing one file, not keeping two in sync.

## Motivation

Maintainer feedback on 2026-07-27: the compiled output "does not reference
vocabulary and repeats the definitions too much; the main readme should have
enough information, but reference the detailed definitions in vocabulary."

The evidence is concrete. The task-family review found `Selected task` stale
one day after a careful edit pass, because the same content lived in five
places and the pass missed one. The README's task section was 47 lines of
which roughly half restated the vocabulary; the Core definitions section
restates seven vocabulary entries as bullets. Duplicated definitions are where
the framework's inconsistencies have actually appeared.

## Evidence

- The task section rewrite in the
  [task-family review](../streams/working-sessions/2026-07-27-task-family-review.md)
  is the worked example: definition referenced, operational guidance kept.
- The `Core definitions` section (`Problem hierarchy and strategy` bullets) is
  the largest remaining duplication.
- Prior reviews repaired divergence between README and VOCABULARY wording for
  signal, outcome, open, and strategy — each a place the duplication had
  already drifted.

## Open questions

- Does the Core definitions section survive as a short orientation list with
  links, or fold into the sections that use each concept?
- Should `SCHEMA.md` and `VISUALIZATION.md` be checked for the same
  duplication in the same pass?
- How much definition may the README keep inline before a reader has to flip
  files too often? The maintainer's bar is "enough information" — that needs
  one worked section reviewed to calibrate.

## Grooming log

### 2026-07-27 — captured

Captured by the Claude Code operator from direct maintainer feedback during
the task-family review session. The task section of the README was rewritten
in that session as the first application; the rest of the file is this task.
The compilation principle itself is already recorded in
`knowledge-compilation.md`, so this task is the backfill, not the rule.
