# APSS stewardship operations

This directory implements the operating side of the root
[APSS Framework Stewardship System](../SYSTEM.md). Its contents produce, check,
and improve the consumer-facing material under [`artifacts/`](../artifacts/).

- `processes/` defines intake, grooming, AI agent tasks, the complete framework
  loop, and release.
- `work/` holds the durable current plan, work log, and uncommitted backlog.
- `streams/` explains how raw stewardship evidence is retained.
- `validation/` separates artifact correctness from consumer outcome evidence.
- `knowledge/` contains reusable lessons compiled from operating the system.

These are implementation choices of this system. They are not universal APSS
requirements unless adopted by the normative framework.
