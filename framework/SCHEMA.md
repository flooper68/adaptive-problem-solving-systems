# APSS system declaration schema

[`system.schema.json`](system.schema.json) is the normative machine-readable
contract for APSS `SYSTEM.md` frontmatter version `0.1`. The Markdown template
explains how to fill it; when they disagree, the JSON Schema controls structural
conformance and this framework definition controls APSS semantics.

The schema requires the fields needed to identify, operate, validate, learn
from, and adapt a system. This includes `work_sessions` entries for
`brainstorming` and `problem-grooming`, each with only an `id`, `description`,
and linked `process`. Other adaptive-loop responsibilities remain implemented
through their existing declaration fields rather than being duplicated as
work-session metadata.
Current open problems and executable responses are maintained as one file per
item in the locations named by `planning.problems` and `planning.tasks`.
Selected and active tasks live at the task root, candidates under `backlog/`,
and inactive tasks under `archive/`. Their status and relationships remain in
those files; APSS requires neither a separate plan nor a generic work log.

The required `strategy` string references the system's independent
`STRATEGY.md` document beside `SYSTEM.md`, which states the current goal. Schema
validation can verify that the value is a non-empty string; semantic validation
must resolve the local path and confirm that problem grooming uses it to guide
problem selection and strategy.

The schema deliberately permits additional properties at every level so a
system can express domain-specific constraints without waiting for a framework
revision. Extension authors should use clear names and avoid redefining core
fields; an `x_` prefix is recommended when collision risk is meaningful.

JSON Schema validation covers local structure and types. A system registry or
map generator must additionally check semantic relationships that one file
cannot prove:

- system IDs are globally unique;
- the primary-parent graph is complete and acyclic;
- relation targets resolve to declared systems;
- referenced local files exist;
- exactly one root exists within a mapped hierarchy;
- an `active` system has executed its complete loop rather than only declaring
  it;
- declared authority and validations are actually followed;
- the `strategy` path resolves to an independent system-strategy document with
  a current goal;
- the problem and task directories resolve; each active problem contains its
  goal, evidence, desired change, strategy, and signal; and each selected task
  identifies which problem strategy it implements or tests; and
- work-session IDs are unique; `processes/brainstorming.md` implements iterative
  user review and `processes/problem-grooming.md` implements evidence-aware
  problem disposition and retention as described by their declarations.

YAML frontmatter can be validated by parsing it to a data object and applying
the JSON Schema with any standards-compliant validator. APSS does not mandate a
particular YAML parser or validator implementation. Generated maps should use
the same schema rather than inventing their own required-field list.

Files:

- [SYSTEM.template.md](SYSTEM.template.md) — authoring template.
- [system.schema.json](system.schema.json) — normative structural contract.
- [../examples/cnc-part-production/SYSTEM.md](../examples/cnc-part-production/SYSTEM.md)
  — complete proposed-system example.
