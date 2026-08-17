# Adaptive Problem Solving (APS)

This repository develops Adaptive Problem Solving, a general method for systems
that iteratively solve a defined problem, evaluate progress, learn from
evidence, and adapt later attempts.

Its purpose is to make APS understandable, usable across different domains, and
improvable through evidence from applying the method itself.

## Repository structure

- [`framework/`](framework/README.md) contains the normative APS definition,
  vocabulary, declaration contract, and supporting guidance.
- [`operations/`](operations/SYSTEM.md) contains the first APS application: the
  system that maintains and
  improves the framework, including its strategy, processes, evidence, problems,
  and current work.

The repository is a container for these parts, not itself an APS system.
Operational choices become APS requirements only when the normative framework
adopts them. Additional applications and examples can be added after the
framework is sufficiently stable for them to provide useful validation.
