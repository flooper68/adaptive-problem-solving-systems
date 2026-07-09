---
apss_version: "0.1"
id: apss.framework-operations
name: APSS Framework Operations System
status: proposed
parent: null

problem: APSS cannot become reliably effective and usable if the framework evolves without disciplined operations that connect consumer experience, explicit decisions, validated changes, and learning.
vision: People can readily understand and apply APSS to build adaptive problem-solving systems that improve their intended outcomes.
purpose: Improve the APSS framework so it is effective and usable by others.
goals:
  - Complete and validate the first evidence-driven framework improvement cycle, from an observed consumer need through an approved change and its outcome.
strategy: Treat the framework as the primary product, use examples and real applications as tests of its clarity and usefulness, preserve feedback and ideas before prioritizing them, select bounded improvements into a durable plan, validate artifact correctness separately from consumer outcomes, compile what is learned, and require human approval for normative adaptation and release.

constraints:
  - Keep the normative framework distinguishable from operations and non-normative examples.
  - Preserve evidence, decisions, and uncertainty instead of presenting assumptions as validated results.
  - Keep APSS domain-independent while allowing implementations to make domain-specific choices.

roles:
  owner: [APSS framework maintainer]
  operators: [APSS framework maintainer, authorized contributors and agents]
  consumers: [designers and operators of adaptive problem-solving systems]
  validators: [APSS framework maintainer, framework users applying APSS]
  adaptation_approvers: [APSS framework maintainer]

inputs:
  - Captured ideas, questions, issues, research, and decisions.
  - Feedback and observed results from applying the framework.
  - Validation failures and inconsistencies in framework artifacts or examples.
  - Relevant external research and established practice.

artifact:
  primary: ../framework/
  medium: informational
  supporting:
    - ../examples/
  consumers: [designers and operators of adaptive problem-solving systems]
  intended_outcome: Consumers can define, inspect, operate, validate, and improve complete adaptive problem-solving systems.

planning:
  process: processes/backlog-grooming.md
  plan: work/PLAN.md
  log: work/LOG.md

execution:
  process: processes/framework-loop.md
  invocation: On an approved work item, material new evidence, a validation failure, or a maintainer-requested review.

validation:
  artifact: Follow validation/artifact.md to check schema conformance, references, consistency, examples, and review approval.
  outcome: Follow validation/outcome.md to collect evidence that consumers can understand and successfully apply APSS.

streams:
  - id: operations-work
    purpose: Preserve ideas, decisions, execution history, and unresolved questions.
    source: work/
    access: Read backlog items, the current plan, and the append-only work log.
    consumed_by: processes/framework-loop.md
    grill: null
  - id: framework-feedback
    purpose: Preserve direct consumer reports about understanding, applying, or adopting APSS and explicitly disposition them.
    source: Framework users, maintainers, reviewers, and adopters reporting an experience.
    access: Capture reports under streams/framework-feedback/ and groom them with processes/framework-feedback-grooming.md.
    consumed_by: processes/framework-feedback-grooming.md
    grill: Ask what the reporter attempted, what happened, what they expected, what effect the gap had, and what evidence can be retained.
  - id: framework-usage
    purpose: Learn whether APSS is understandable and useful when applied.
    source: Implementation examples, consumer trials, reviews, and observed applications.
    access: Retain durable summaries or references as described in streams/README.md.
    consumed_by: processes/framework-loop.md
    grill: Ask what the user attempted, where interpretation was uncertain, what APSS exposed, and whether the resulting change helped.
  - id: external-foundations
    purpose: Compare APSS choices with established theory and practice.
    source: Authoritative research and domain references.
    access: Preserve citations and a synthesis in the relevant research work item or retained evidence.
    consumed_by: processes/framework-loop.md
    grill: null

uncertainty:
  discussion: Elicit the problem, intended outcome, constraints, trade-offs, and observed use from the proposer, maintainer, or framework user.
  research: Consult authoritative external sources when terminology, prior art, or empirical claims are load-bearing.
  experimentation: Apply proposed changes to examples, prototypes, or real systems before treating usefulness claims as established.

learning:
  compilation_process: processes/framework-loop.md
  compiled_knowledge: knowledge/README.md
  changelog: knowledge/CHANGELOG.md
  adaptation_process: processes/framework-loop.md

authority:
  execution: Authorized operators may capture and groom work, edit artifacts within an approved plan, and run non-destructive validation. AI agents follow processes/ai-agent-tasks.md and require maintainer approval before committing or pushing.
  adaptation: The APSS framework maintainer approves normative framework changes, release decisions, and changes to the operations system.

health: The operations system must keep the normative framework distinguishable from its own processes and from non-normative examples, retain durable work history, and avoid claiming effectiveness without consumer-outcome evidence.

relations:
  feeds: []
  verifies: []
  verified_by: []
  invokes: []
  depends_on: []
  scheduled_by: []
  governed_by: []
  improves: []
---

# APSS Framework Operations System

## Purpose and direction

This system exists to improve APSS so that other people can understand it,
apply it, and achieve useful outcomes. Its vision describes that durable future;
its current goal is the bounded first demonstration of the improvement loop.
After that result is validated, the maintainer replaces it with the next bounded
goal rather than treating routine operation as a goal.

## Boundary

The system's operational capsule is this `operations/` directory. It owns the
processes, work state, evidence handling, validation, knowledge, release history,
and authority used to improve APSS. Its primary produced artifact is the sibling
`framework/` directory. The sibling `examples/` directory contains supporting
applications used to explain and test the framework.

The repository is a container for the system and its outputs; it is not itself
declared as an adaptive system. APSS applications owned by other people or
organizations remain outside this system's authority, although their observed
results may enter as evidence.

## Complete loop

Direct feedback enters the framework-feedback stream and is groomed as evidence;
an actionable disposition may create a linked work candidate. Ideas enter the
durable backlog through the intake process. Backlog grooming clarifies
their problem, expected outcome, evidence, scope, uncertainty, and validation
approach, then assigns a recorded disposition. The maintainer selects ready
work into the durable plan. Operators execute the plan, validate artifact
correctness and consumer outcomes separately, record material decisions, and
compile reusable learning. Normative adaptations and releases require
maintainer approval.

## Artifact contract

The versioned package in `../framework/` is the primary, normative artifact.
Implementations in `../examples/` are supporting,
non-normative artifacts: they demonstrate possible applications and provide
validation evidence, but do not create requirements unless the framework
explicitly adopts them.

## Learning and adaptation

Raw evidence remains recoverable through work items, logs, feedback summaries,
research citations, validation results, and git history. Stable lessons are
compiled into `knowledge/README.md`. The maintainer approves changes
to the framework, this declaration, operating processes, or release state.

## Open design gaps

This system remains `proposed` until it completes and records a full cycle that
includes selecting work, changing an artifact, validating artifact and outcome,
compiling learning, and applying an approved adaptation to a subsequent run.
