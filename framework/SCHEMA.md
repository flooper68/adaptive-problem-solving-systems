# APSS system declaration schema

[`system.schema.json`](system.schema.json) is the normative machine-readable
contract for APSS `SYSTEM.md` frontmatter version `0.1`. The Markdown template
explains how to fill it; when they disagree, the JSON Schema controls structural
conformance and this framework definition controls APSS semantics.

The schema requires the fields needed to identify, operate, validate, learn
from, and adapt a system. This includes one `work_sessions` entry for
`brainstorming`, with only an `id`, `description`, and linked `process`. Other
adaptive-loop responsibilities remain implemented through their existing
declaration fields rather than being duplicated as work-session metadata.

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
- `processes/brainstorming.md` exists and implements the iterative user-review
  session described by its declaration.

YAML frontmatter can be validated by parsing it to a data object and applying
the JSON Schema with any standards-compliant validator. APSS does not mandate a
particular YAML parser or validator implementation. Generated maps should use
the same schema rather than inventing their own required-field list.

Files:

- [SYSTEM.template.md](SYSTEM.template.md) — authoring template.
- [system.schema.json](system.schema.json) — normative structural contract.
- [../examples/cnc-part-production/SYSTEM.md](../examples/cnc-part-production/SYSTEM.md)
  — complete proposed-system example.
