# Framework adaptation

## Purpose

Review a sealed compilation candidate, decide how its learning changes future
operation, and publish approved normative knowledge to the correct target. This
process is separate from compilation so producing a candidate cannot silently
replace the published APSS framework.

## Inputs and authority

An adaptation starts from linked evidence, a sealed compilation candidate and
report or an explicit reason no candidate was needed, and a selected work item
with acceptance and validation conditions. The APSS framework maintainer is the
adaptation approver. Operators may prepare a proposal and uncommitted edits only
within their granted scope.

## Procedure

1. Review the candidate's lesson, provenance, inference, uncertainty,
   validation state, and proposed future behavior.
2. Select the smallest correct target:
   - `operations/` for how the framework-producing system works;
   - `examples/` for a non-normative demonstration or test; or
   - `framework/` only for a domain-independent normative APSS change.
3. Record alternatives, uncertainty, compatibility effects, and why the target
   follows from the evidence. If the evidence is insufficient, request the
   needed discussion, research, experiment, or outcome observation instead of
   adapting.
4. Obtain maintainer approval for the target and any normative framework
   publication. A sealed candidate never substitutes for approval.
5. Make the smallest coherent change. For an approved normative candidate,
   publish it into `framework/`, append `framework/CHANGELOG.md`, and keep the
   definition, schema, template, and visualization guidance consistent as
   applicable.
6. Run artifact validation and arrange outcome validation. Record delayed
   outcome evidence honestly rather than claiming effectiveness at merge time.
7. Record the decision, evidence links, changed target, validation results, and
   next trigger in the work log and plan. If the adaptation or its later outcome
   changes the underlying lesson, initiate another evidence-bounded compilation
   rather than silently amending the published framework.

## Completion condition

Adaptation is complete only when an authorized change affects a subsequent run
through the plan, strategy, process, stream, validation, knowledge, system
structure, example, or normative framework. A proposed or compiled lesson that
has not changed future behavior remains unapplied learning.
