# Simulation Patterns

This directory defines simulation patterns used to intentionally induce risk conditions in a controlled environment.

Simulation is not a fixed strategy or an exhaustive set of practices. It is a heuristic quality dimension used to expose behaviors that may violate system invariants under concurrency, partial failures, retries, latency, and integration disruptions.

Each simulation pattern should help answer the following questions:

- What condition is being induced?
- Which invariant is expected to hold?
- Which failure signals would indicate that the invariant was violated?
- Which risk domains are most related to this pattern?

## Purpose

The purpose of these patterns is to support quality planning oriented by risk, invariants, and failure signals.

They are designed to be reusable across different payment risk domains, while still allowing contextual application depending on:

- system maturity
- transaction criticality
- operational capacity
- time and resource constraints

## Structure

Each simulation pattern should include:

- **ID**: unique identifier for the simulation pattern
- **Objective**: what the simulation is intended to expose
- **How to simulate**: how the condition can be induced
- **What it stresses**: which parts of the system are being stressed
- **Expected invariants**: properties that must still hold
- **Failure signals**: observable signs of invariant violation
- **Related risks**: risk domains or risk entries that are most associated with the pattern

## Index

- [SIM-001 — Critical Concurrency Induction](./SIM-001.md)
- [SIM-002 — Event Race Condition Simulation](./SIM-002.md)
- [SIM-003 — Idempotency with Payload Drift](./SIM-003.md)
- [SIM-004 — Partial Failure (Saga Interruption)](./SIM-004.md)
- [SIM-005 — Dependency Latency Injection](./SIM-005.md)
- [SIM-006 — Retry Reprocessing Across Steps](./SIM-006.md)
- [SIM-007 — Asynchronous Contract Break](./SIM-007.md)

## Notes

Simulation patterns are cross-domain capabilities. They should not be treated as domain-exclusive practices.

The same simulation pattern may apply to multiple domains, such as architectural boundaries, integration, operational resilience, and data consistency, depending on the nature of the risk being analyzed.
