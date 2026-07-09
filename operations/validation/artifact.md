# Framework artifact validation

Artifact validation asks whether the repository produced a coherent APSS
framework package and accurate supporting examples.

For every material change:

1. Validate `SYSTEM.md` and example declarations against
   `artifacts/framework/system.schema.json`.
2. Confirm every declared local process, plan, log, validation, and knowledge
   path exists relative to its system boundary.
3. Check Markdown links and local file references after moves or renames.
4. Check consistency among the framework definition, normative schema,
   template, schema explanation, visualization contract, and changelog.
5. Check that implementation examples conform to the framework version they
   claim and do not present example-specific choices as universal rules.
6. Confirm `artifacts/framework/` is clearly normative and
   `artifacts/examples/` clearly supporting and non-normative.
7. Review terminology, required fields, acceptance conditions, and declared
   authority for ambiguity or contradiction.
8. Record commands, review findings, failures, and unresolved exceptions in the
   relevant work item or `operations/work/LOG.md`.

A change passes artifact validation when required automated checks pass, manual
consistency review finds no known blocking contradiction, examples remain
honest, and the maintainer accepts any explicitly recorded limitations.
