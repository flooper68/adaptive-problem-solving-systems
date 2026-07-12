---
id: apss.visual-html-generator
type: task
status: captured
owner: APS framework maintainer
created: 2026-07-09
source: apss.feedback.visualization-tooling
---

# Generate visual HTML from APS system declarations

## Idea

Provide a repository-supported script that reads one or more APS `SYSTEM.md`
declarations, validates their structure and relationships, and generates a
polished visual HTML representation without making the output a second source
of truth.

## Motivation

APS already defines standard hierarchy, artifact-flow, and learning views plus
a generation contract, but consumers currently have to create those views
manually. Executable tooling would make systems easier to inspect and
communicate while reducing drift from declarations.

## Evidence

- Feedback report
  [`apss.feedback.visualization-tooling`](../../streams/framework-feedback/2026-07-09-visualization-tooling.md).
- [`framework/VISUALIZATION.md`](../../../framework/VISUALIZATION.md)
  says to generate projections from `SYSTEM.md` where practical and specifies
  derivable views and structural diagnostics.
- The repository currently contains no visualization generator.

## Open questions

- Should the first version accept one declaration, recursively discover a
  directory tree, or support both?
- Which runtime and dependency strategy makes the tool easiest to run and
  maintain?
- Which views and interactions are required for a useful first version?
- Should the HTML be self-contained, and must it work fully offline?
- How should validation errors and unresolved external relation targets appear?
- What accessibility, responsive-layout, export, and theming requirements are
  necessary?
- Should this be a supporting artifact in the framework package or stewardship
  tooling that can later be promoted?

## Grooming log

### 2026-07-09 — captured from groomed feedback

Created as the proposed response to an actionable framework-feedback report.
The consumer need and existing generation contract are established; scope,
technical approach, acceptance conditions, and validation participants remain
for task grooming.
