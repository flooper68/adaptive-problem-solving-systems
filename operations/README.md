# APSS framework operations

This directory is the capsule of the
[APSS Framework Operations System](SYSTEM.md). Its purpose is to improve the
normative [`framework/`](../framework/) so that other people can understand and
apply it effectively. The system uses [`examples/`](../examples/) as supporting
explanations and validation cases.

- `processes/` defines feedback and backlog intake and grooming, AI agent tasks,
  the complete framework loop, and release.
- `work/` holds the durable current plan, work log, and uncommitted backlog.
- `streams/` explains how raw stewardship evidence is retained, including
  direct framework-feedback reports.
- `validation/` separates artifact correctness from consumer outcome evidence.
- `knowledge/` contains reusable lessons compiled from operating the system.

The problem, vision, current goal, strategy, boundary, and authority belong to
this operations system, not to the repository as a whole. Its implementation
choices are not universal APSS requirements unless adopted by the normative
framework.
