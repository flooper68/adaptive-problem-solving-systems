# Knowledge compilation

## Purpose

Turn retained evidence into coherent updates to the APS framework, which is
this system's primary compiled-knowledge artifact. Preserve material scope and
uncertainty in the resulting knowledge, and keep the edits uncommitted until
adaptation is approved.

## Inputs

For the question or completed work being compiled, read:

- the current system problem and strategy, open-problem hierarchy, task files,
  and published framework knowledge;
- relevant records from every declared stream, including insight claims and
  dispositions, groomed feedback, usage evidence, work history and its
  framework baseline, and external foundations;
- verification results; and
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
   - domain-independent APS knowledge belongs in the framework;
   - lessons about running the framework-producing system propose changes to
     its `SYSTEM.md`, processes, validation, task handling, or streams; and
   - context-specific demonstrations or observations remain in their source
     evidence unless the framework adopts a general lesson.
6. Edit the authoritative target directly as an uncommitted change. Keep
   operations-specific conclusions in the authoritative operational document
   they change rather than creating a second knowledge artifact.
7. Append a concise entry to the target knowledge artifact's changelog when the
   compilation materially changes it. Raw evidence and detailed provenance stay
   in their source streams, work records, and Git history.
8. Pass the uncommitted changes to [`framework-adaptation.md`](framework-adaptation.md).
   Compilation alone does not authorize commit, publication, or later use.

## Output contract

The compiled-knowledge artifact is `../../framework/`, which is also this
system's primary normative output. Compilation edits it directly and updates
`../../framework/CHANGELOG.md`; the uncommitted Git diff is the reviewable
proposal. Maintainer-approved adaptation authorizes the change to be committed
and used by later work.

There is no secondary operations knowledge artifact. Current operational
knowledge lives in `../SYSTEM.md` and `../processes/`; observations and
provenance remain in `../work/` and declared streams. This keeps the published
framework as the single compiled-knowledge destination.

## Validation

Validate compilation by applying the process to retained evidence and checking
whether the resulting knowledge preserves the source's material decisions,
scope, and uncertainty. When a historical compiled output is available, keep it
hidden from the compiler until the proposed output is complete; otherwise the
exercise tests copying rather than compilation.

For a historical comparison, use a fresh compiler context containing only the
declared input evidence, this process, and the compilation instruction. Hide
the current framework, later operations documents, Git history, acceptance
criteria, and expected output until the proposed output is complete. A separate
evaluator then compares source, output, and expected output for semantic
coverage, contradictions, unsupported additions, and material omissions. Exact
prose is not required. Use temporary isolation for the exercise. Retain only
the evidence needed by the system's working-session or validation stream.
