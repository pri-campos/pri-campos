# Observability Patterns

This directory defines observability patterns used to detect deviations in transaction behavior and identify violations of system invariants in production environments.

Observability is not limited to logs, metrics, or traces. It is a risk-oriented capability focused on identifying signals that indicate inconsistency, failure propagation, or unexpected system behavior.

## Purpose

The purpose of these patterns is to enable early detection of risk materialization by monitoring aggregated behavior across transaction flows.

They help answer:

- What signals indicate that an invariant was violated?
- How can deviations be detected before causing impact?
- Which patterns reveal systemic issues rather than isolated failures?

## Structure

Each observability pattern includes:

- **ID**: unique identifier
- **Objective**: what deviation it aims to detect
- **What to observe**: signals or metrics to monitor
- **What it reveals**: type of failure or inconsistency exposed
- **Expected invariants**: properties that should hold
- **Failure signals**: observable evidence of violation
- **Related risks**: associated domains or risk entries

## Index

- [OBS-001 — Dangling Transactions Detection](./OBS-001.md)
- [OBS-002 — Semantic Divergence Detection](./OBS-002.md)
- [OBS-003 — Latency Outlier Detection](./OBS-003.md)
- [OBS-004 — Rollback Rate Monitoring](./OBS-004.md)
- [OBS-005 — Event Sequencing Anomalies](./OBS-005.md)
- [OBS-006 — Retry Efficiency Monitoring](./OBS-006.md)

## Notes

Observability patterns are cross-domain capabilities. They should be designed to detect system-level behavior, not just component-level failures.

They are especially relevant in distributed payment systems, where inconsistencies often emerge from interactions between components rather than isolated faults.
