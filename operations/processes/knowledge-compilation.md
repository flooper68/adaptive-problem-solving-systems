# Knowledge compilation

## Purpose

Turn retained evidence into a coherent candidate for the APSS framework, which
is this system's primary compiled-knowledge artifact. Preserve provenance and
uncertainty, and keep the candidate separate from the published framework until
adaptation is approved.

## Inputs

For the question or completed work being compiled, read:

- the current problem, goal, strategy, plan, and published framework knowledge;
- relevant records from every declared stream, including working sessions,
  insight claims and dispositions, groomed feedback, usage evidence, work
  history and its framework baseline, and external foundations;
- artifact- and outcome-validation results; and
- the raw source or durable reference behind every material claim.

Missing context is an uncertainty to record or resolve through discussion,
research, or experimentation. It is not evidence for a convenient conclusion.

## Compilation procedure

1. State the compilation question and its evidence boundary: what period, work,
   outcome, or decision is being synthesized.
2. Gather the relevant evidence and retain a source link, stable ID, Git object,
   or other recoverable provenance for each material observation.
3. Separate direct observations, external source claims, operator inference,
   and unresolved uncertainty.
4. Assess whether a lesson is reusable beyond one event. Record the context in
   which it applies and its validation state. Do not present an unvalidated
   usefulness claim as established knowledge.
5. Classify each reusable conclusion by target:
   - domain-independent APSS knowledge belongs in a candidate framework;
   - lessons about running the framework-producing system propose changes to
     its `SYSTEM.md`, processes, validation, plan, or stream handling; and
   - context-specific demonstrations or observations remain in examples or
     their source evidence unless the framework adopts a general lesson.
6. Create `../work/compilations/<date>-<slug>/` containing:
   - a candidate `framework/` document or coherent package;
   - a report stating the evidence boundary, provenance, inference,
     uncertainty, validation state, and material differences from the currently
     published framework; and
   - a proposed framework changelog entry when publication would change APSS.
7. Keep operations-specific conclusions in the compilation report and name the
   authoritative operational document they would change. Detailed provenance
   stays in streams, work records, and Git history.
8. Pass the sealed candidate, report, and any proposed operational adaptations to
   [`framework-adaptation.md`](framework-adaptation.md). Compilation alone does
   not authorize publication.

## Output contract

The published compiled-knowledge artifact is `../../framework/`, which is also
this system's primary normative output. A compilation run first writes a
candidate under `../work/compilations/`; after validation and maintainer
approval, adaptation publishes that candidate into `../../framework/` and
updates `../../framework/CHANGELOG.md`.

There is no secondary operations knowledge artifact. Current operational
knowledge lives in `../SYSTEM.md` and `../processes/`; observations and
provenance remain in `../work/` and declared streams. This keeps the published
framework as the single compiled-knowledge destination.

## Validation

Validate compilation by applying the process to retained evidence and checking
whether an independently produced candidate preserves the source's material
decisions, provenance, scope, and uncertainty. When a historical compiled
output is available, keep it hidden from the compiler until the candidate is
sealed; otherwise the exercise tests copying rather than compilation.

For a historical comparison, use a fresh compiler context containing only the
declared input evidence, this process, and the compilation instruction. Hide
the current framework, later operations documents, Git history, acceptance
criteria, and expected output until the candidate is sealed. A separate
evaluator then compares source, candidate, and expected output for semantic
coverage, contradictions, unsupported additions, and material omissions. Exact
prose is not required. Retain the candidate and evaluation report under
`../work/compilations/<date>-<slug>/`.
