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
strategy: Treat the framework as the primary product, use examples and real applications as tests of its clarity and usefulness, preserve feedback, working-session evidence, and explicit insights before choosing responses, select bounded executable improvements into a durable plan, validate artifact correctness separately from consumer outcomes, compile what is learned, and require human approval for normative adaptation and release.

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
  - Working-session evidence, insights, unresolved questions, and authorized decisions.
  - Bounded candidate tasks, research inquiries, experiments, reviews, and remediations.
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
  artifact: Follow processes/artifact-validation.md to check schema conformance, references, consistency, examples, and review approval.
  outcome: Follow processes/outcome-validation.md to collect evidence that consumers can understand and successfully apply APSS.

streams:
  - id: operations-work
    purpose: Preserve candidate actions, planning decisions, execution history, and unresolved execution gaps.
    source: work/
    access: Read backlog items, the current plan, and the append-only work log.
    consumed_by: processes/framework-loop.md
    grill: null
  - id: working-sessions
    purpose: Preserve collaborative exploration and its observations, insights, questions, decisions, and candidate actions without treating them as work commitments.
    source: Maintainer, contributor, and agent working sessions.
    access: Retain one topic-focused summary or recoverable source reference per session under streams/working-sessions/ using processes/working-session.md.
    consumed_by: processes/framework-loop.md
    grill: Follow processes/working-session.md; when eliciting judgment, ask one load-bearing question at a time and preserve the source's distinctions.
  - id: insights
    purpose: Preserve independently useful interpretations with their source evidence, reasoning, scope, uncertainty, and explicit epistemic disposition.
    source: Maintainer, contributor, validator, consumer, and agent interpretations derived from declared evidence streams.
    access: Capture insights under streams/insights/ with processes/insight-intake.md and assess them with processes/insight-grooming.md.
    consumed_by: processes/insight-grooming.md
    grill: Follow processes/insight-intake.md; ask one load-bearing question at a time about the source evidence, inference, scope, alternatives, and possible use.
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
  discussion: Follow processes/working-session.md to elicit the problem, intended outcome, constraints, trade-offs, and observed use from the proposer, maintainer, or framework user and retain the result in the working-sessions stream.
  research: Consult authoritative external sources when terminology, prior art, or empirical claims are load-bearing.
  experimentation: Apply proposed changes to examples, prototypes, or real systems before treating usefulness claims as established.

learning:
  compilation_process: processes/knowledge-compilation.md
  compiled_knowledge: ../framework/
  changelog: ../framework/CHANGELOG.md
  candidate_location: work/compilations/
  adaptation_process: processes/framework-adaptation.md

authority:
  execution: Authorized operators may retain working sessions, capture and groom insights and candidate work, edit artifacts within an approved plan, and run non-destructive validation. Only declared authorities may approve insight dispositions, decisions, or work selection. AI agents follow processes/ai-agent-tasks.md and require maintainer approval before committing or pushing.
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
an actionable disposition may create a linked work candidate. Working sessions
retain collaborative exploration and distinguish observations, insights,
questions, decisions, and possible responses. Independently useful insights
enter their own stream for faithful intake and evidence-aware grooming. Only
executable responses enter the durable backlog through intake. Backlog grooming
clarifies their source, expected outcome, evidence, scope, uncertainty, and
validation approach, then assigns a recorded disposition. The maintainer
selects ready work into the durable plan. Operators execute the plan, validate
artifact correctness and consumer outcomes separately, record material
decisions, and compile reusable learning. Normative adaptations and releases
require maintainer approval.

## Artifact contract

The versioned package in `../framework/` is the primary, normative artifact.
Implementations in `../examples/` are supporting,
non-normative artifacts: they demonstrate possible applications and provide
validation evidence, but do not create requirements unless the framework
explicitly adopts them.

## Learning and adaptation

Raw evidence remains recoverable through working-session records, work items,
logs, feedback summaries, research citations, validation results, baseline
records, and git history. Explicit interpretations and their assessment remain
recoverable through the insight stream. The
[knowledge-compilation process](processes/knowledge-compilation.md) synthesizes
these streams into a candidate framework knowledge artifact. The published
compiled result is the primary artifact in `../framework/`; compilation stores
its candidate under `work/compilations/` and does not overwrite the published
framework. The separate
[adaptation process](processes/framework-adaptation.md) requires the maintainer
to approve publication of the candidate. Operations-specific learning changes
this declaration, its processes, or validation through the same explicit
adaptation path; it is not kept in a competing compiled-knowledge artifact.

## Open design gaps

This system remains `proposed` until it completes and records a full cycle that
includes selecting work, changing an artifact, validating artifact and outcome,
compiling learning, and applying an approved adaptation to a subsequent run.
