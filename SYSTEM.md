---
apss_version: "0.1"
id: apss.framework-stewardship
name: APSS Framework Stewardship System
status: proposed
parent: null

problem: Problem-solving systems are often defined without a complete, inspectable feedback loop, while framework changes can become disconnected from evidence about their usefulness.
vision: APSS remains a coherent, practical, evidence-informed framework that can itself demonstrate the adaptive behavior it specifies.
goals:
  - Operate the repository as a self-describing APSS instance.
  - Turn captured ideas into explicit dispositions through repeatable grooming.
  - Produce and validate coherent framework releases and implementation examples.
strategy: Separate consumer-facing artifacts from stewardship operations; use durable intake, grooming, planning, validation, learning, and human-approved adaptation to evolve the artifacts.

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
  primary: artifacts/framework/
  medium: informational
  supporting:
    - artifacts/examples/
  consumers: [designers and operators of adaptive problem-solving systems]
  intended_outcome: Consumers can define, inspect, operate, validate, and improve complete adaptive problem-solving systems.

planning:
  process: operations/processes/backlog-grooming.md
  plan: operations/work/PLAN.md
  log: operations/work/LOG.md

execution:
  process: operations/processes/framework-loop.md
  invocation: On an approved work item, material new evidence, a validation failure, or a maintainer-requested review.

validation:
  artifact: Follow operations/validation/artifact.md to check schema conformance, references, consistency, examples, and review approval.
  outcome: Follow operations/validation/outcome.md to collect evidence that consumers can understand and successfully apply APSS.

streams:
  - id: stewardship-work
    purpose: Preserve ideas, decisions, execution history, and unresolved questions.
    source: operations/work/
    access: Read backlog items, the current plan, and the append-only work log.
    consumed_by: operations/processes/framework-loop.md
    grill: null
  - id: framework-usage
    purpose: Learn whether APSS is understandable and useful when applied.
    source: Implementation examples, user feedback, reviews, and observed applications.
    access: Retain durable summaries or references as described in operations/streams/README.md.
    consumed_by: operations/processes/framework-loop.md
    grill: Ask what the user attempted, where interpretation was uncertain, what APSS exposed, and whether the resulting change helped.
  - id: external-foundations
    purpose: Compare APSS choices with established theory and practice.
    source: Authoritative research and domain references.
    access: Preserve citations and a synthesis in the relevant research work item or retained evidence.
    consumed_by: operations/processes/framework-loop.md
    grill: null

uncertainty:
  discussion: Elicit the problem, intended outcome, constraints, trade-offs, and observed use from the proposer, maintainer, or framework user.
  research: Consult authoritative external sources when terminology, prior art, or empirical claims are load-bearing.
  experimentation: Apply proposed changes to examples, prototypes, or real systems before treating usefulness claims as established.

learning:
  compilation_process: operations/processes/framework-loop.md
  compiled_knowledge: operations/knowledge/README.md
  changelog: operations/knowledge/CHANGELOG.md
  adaptation_process: operations/processes/framework-loop.md

authority:
  execution: Authorized operators may capture and groom work, edit artifacts within an approved plan, and run non-destructive validation. AI agents follow operations/processes/ai-agent-tasks.md and require maintainer approval before committing or pushing.
  adaptation: The APSS framework maintainer approves normative framework changes, release decisions, and changes to the stewardship system.

health: The repository must keep the normative artifact distinguishable from operations, retain durable work history, and avoid presenting unvalidated examples or proposals as normative requirements.

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

# APSS Framework Stewardship System

## Boundary

This system owns the definition, examples, release history, and stewardship of
APSS. It begins with ideas or evidence about the framework and ends with
validated artifacts plus learning for later iterations. Applications of APSS
owned by other people or organizations are outside its authority; their
observed results may enter as evidence.

The repository root is the system boundary. `artifacts/` contains what the
system produces for consumers. `operations/` contains how it produces, checks,
and improves those artifacts.

## Complete loop

Ideas enter the durable backlog through the intake process. Grooming clarifies
their problem, expected outcome, evidence, scope, uncertainty, and validation
approach, then assigns a recorded disposition. The maintainer selects ready
work into the durable plan. Operators execute the plan, validate artifact
correctness and consumer outcomes separately, record material decisions, and
compile reusable learning. Normative adaptations and releases require
maintainer approval.

## Artifact contract

The versioned framework package in `artifacts/framework/` is the primary,
normative artifact. Implementations in `artifacts/examples/` are supporting,
non-normative artifacts: they demonstrate possible applications and provide
validation evidence, but do not create requirements unless the framework
explicitly adopts them.

## Learning and adaptation

Raw evidence remains recoverable through work items, logs, feedback summaries,
research citations, validation results, and git history. Stable lessons are
compiled into `operations/knowledge/README.md`. The maintainer approves changes
to the framework, this declaration, operating processes, or release state.

## Open design gaps

This system remains `proposed` until it completes and records a full cycle that
includes selecting work, changing an artifact, validating artifact and outcome,
compiling learning, and applying an approved adaptation to a subsequent run.
