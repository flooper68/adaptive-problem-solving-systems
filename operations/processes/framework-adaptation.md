# Framework adaptation

## Purpose

Review uncommitted compiled-knowledge changes, decide how their learning changes
future operation, and authorize approved normative knowledge in the correct
target. Compilation and adaptation are distinct responsibilities even when a
system combines them in one operational process.

## Inputs and authority

An adaptation starts from linked evidence, uncommitted changes or an explicit
reason none are needed, and selected work with acceptance and validation
conditions. The APSS framework maintainer is the adaptation approver. Operators
may prepare proposals only within their granted scope.

## Procedure

1. Review the proposed change, relevant source evidence, uncertainty,
   validation state, and intended future behavior.
2. Select the smallest correct target:
   - `operations/` for how the framework-producing system works;
   - `examples/` for a non-normative demonstration or test; or
   - `framework/` only for a domain-independent normative APSS change.
3. Record alternatives, uncertainty, compatibility effects, and why the target
   follows from the evidence. If the evidence is insufficient, request the
   needed discussion, research, experiment, or outcome observation instead of
   adapting.
4. Obtain maintainer approval for the target and any normative framework
   publication. An uncommitted diff never substitutes for approval.
5. Make the smallest coherent change. For approved normative knowledge, keep
   `framework/`, its simple changelog, and related guidance consistent as
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
