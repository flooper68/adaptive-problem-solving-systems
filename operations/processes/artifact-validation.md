# Framework artifact validation

Artifact validation asks whether the repository produced a coherent APSS
framework package and accurate supporting examples.

For every material change:

1. Validate `operations/SYSTEM.md` and example declarations against
   `framework/system.schema.json`.
2. Confirm every declared local process, problem directory, task directory,
   validation, and knowledge path exists relative to its system boundary.
3. Confirm the declared system-strategy path resolves and problem grooming uses
   it to guide selection and problem strategies.
4. Confirm active problem files contain their goal, evidence, desired change,
   strategy, signal, and grooming history, and selected tasks reference
   existing problem IDs.
5. Check Markdown links and local file references after moves or renames.
6. Check consistency among the framework definition, normative schema,
   template, schema explanation, visualization contract, and changelog.
7. Check that implementation examples conform to the framework version they
   claim and do not present example-specific choices as universal rules.
8. Confirm `framework/` is clearly normative, `examples/` is clearly supporting
   and non-normative, and `operations/` is clearly the system producing them.
9. Review terminology, required fields, acceptance conditions, and declared
   authority for ambiguity or contradiction.
10. When the knowledge-compilation process changes, confirm historical
   comparisons keep input evidence and expected output separate and do not
   expose the answer to the compiler.
11. Record commands, review findings, failures, and unresolved exceptions in the
   relevant task or working-session record.

A change passes artifact validation when required automated checks pass, manual
consistency review finds no known blocking contradiction, examples remain
honest, and the maintainer accepts any explicitly recorded limitations.
