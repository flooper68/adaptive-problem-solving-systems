---
name: APS Framework Operations System

problem: APS cannot become reliably effective and usable if the framework evolves without disciplined operations that connect consumer experience, explicit decisions, validated changes, and learning.
verification: processes/verification.md
strategy: STRATEGY.md
process: processes/process.md

work_sessions:
  - id: brainstorming
    description: Discuss an APS idea, task, or research topic with the maintainer and iteratively compile reviewable changes into the framework or a concrete APS instantiation.
    process: processes/brainstorming.md
  - id: problem-grooming
    description: Use the system strategy to revisit current open problems with the maintainer, update their evidence and strategy, and record an authorized retain, revise, address, or close decision.
    process: processes/problem-grooming.md

streams:
  - id: working-sessions
    purpose: Preserve material brainstorming and problem-grooming invocations with their decisions, affected files, and stopping points.
    source: Maintainer-agent discussions and other declared work-session invocations.
    access: Retain one file per material session under streams/working-sessions/ and link the affected problem and task files.
    consumed_by: processes/process.md
    grill: null
  - id: insights
    purpose: Preserve independently useful interpretations with their source evidence, reasoning, scope, uncertainty, and explicit epistemic disposition.
    source: Maintainer, contributor, validator, consumer, and agent interpretations derived from declared evidence streams.
    access: Capture insights under streams/insights/ with processes/insight-intake.md and assess them with processes/insight-grooming.md.
    consumed_by: processes/insight-grooming.md
    grill: Follow processes/insight-intake.md; ask one load-bearing question at a time about the source evidence, inference, scope, alternatives, and possible use.
  - id: framework-feedback
    purpose: Preserve direct consumer reports about understanding, applying, or adopting APS and explicitly disposition them.
    source: Framework users, maintainers, reviewers, and adopters reporting an experience.
    access: Capture reports under streams/framework-feedback/ and groom them with processes/framework-feedback-grooming.md.
    consumed_by: processes/framework-feedback-grooming.md
    grill: Ask what the reporter attempted, what happened, what they expected, what effect the gap had, and what evidence can be retained.
  - id: framework-usage
    purpose: Learn whether APS is understandable and useful when applied.
    source: Framework Operations, consumer trials, reviews, and other observed applications.
    access: Retain durable summaries or references as described in streams/README.md.
    consumed_by: processes/process.md
    grill: Ask what the user attempted, where interpretation was uncertain, what APS exposed, and whether the resulting change helped.
  - id: external-foundations
    purpose: Compare APS choices with established theory and practice.
    source: Authoritative research and domain references.
    access: Preserve citations and a synthesis in the relevant research work item or retained evidence.
    consumed_by: processes/process.md
    grill: null

---
