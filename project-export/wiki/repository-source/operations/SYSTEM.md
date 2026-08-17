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
    description: Independently useful interpretations with their source evidence, reasoning, scope, and uncertainty, captured under streams/insights/ with processes/intake.md.
    process: processes/sessions/grooming.md
  - id: framework-feedback
    description: Direct consumer reports about understanding, applying, or adopting APS, captured under streams/framework-feedback/ with processes/intake.md.
    process: processes/sessions/grooming.md
  - id: framework-usage
    description: Observed applications, trials, and reviews showing whether APS is understandable and useful, retained as durable summaries or references per streams/README.md.
    process: processes/process.md
  - id: external-foundations
    description: Authoritative research and domain references compared with APS choices, retained as citations and syntheses in the relevant work item or evidence.
    process: processes/process.md

---
