---
name: APS Framework Operations System

problem: APS cannot become reliably effective and usable if the framework evolves without disciplined operations that connect consumer experience, explicit decisions, validated changes, and learning.
verification: processes/verification.md
strategy: STRATEGY.md
process: processes/process.md

work_sessions:
  - id: brainstorming
    description: Discuss an APS idea, task, or research topic with the maintainer and iteratively compile reviewable changes into the framework or a concrete APS instantiation.
    process: processes/sessions/brainstorming.md
  - id: grooming
    description: Review captured inputs — feedback, insights, task candidates, problems, and verification evidence — with the maintainer and record one approved disposition per item, guided by the system strategy.
    process: processes/sessions/grooming.md
  - id: automated-brainstorming
    description: Run a brainstorming session autonomously on one maintainer-named task or topic, deciding and compiling as the maintainer would, have an independent reviewer agent examine the uncommitted result, and present the changes with the recorded decisions and review findings for maintainer approval before delivery. Experimental.
    process: processes/sessions/automated-brainstorming.md
  - id: automated-grooming
    description: Groom captured inputs autonomously into proposed dispositions, have an independent reviewer agent check the proposals, and present them for per-item maintainer approval before recording and delivery. Experimental.
    process: processes/sessions/automated-grooming.md

streams:
  - id: insights
    purpose: Preserve independently useful interpretations with their source evidence, reasoning, scope, uncertainty, and explicit epistemic disposition.
    source: Maintainer, contributor, validator, consumer, and agent interpretations derived from declared evidence streams.
    access: Capture insights under streams/insights/ with processes/intake.md and assess them with processes/sessions/grooming.md.
    consumed_by: processes/sessions/grooming.md
    grill: Follow processes/intake.md; ask one load-bearing question at a time about the source evidence, inference, scope, alternatives, and possible use.
  - id: framework-feedback
    purpose: Preserve direct consumer reports about understanding, applying, or adopting APS and explicitly disposition them.
    source: Framework users, maintainers, reviewers, and adopters reporting an experience.
    access: Capture reports under streams/framework-feedback/ with processes/intake.md and assess them with processes/sessions/grooming.md.
    consumed_by: processes/sessions/grooming.md
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
