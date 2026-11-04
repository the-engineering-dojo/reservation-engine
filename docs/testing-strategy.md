# 🔬 Testing strategy (proposal)

[← Project](../README.md) · [📈 Load-testing lab](../labs/06-load-testing.md)

**Status: planned**, not executed.

| Layer | Purpose | Example claim |
| --- | --- | --- |
| Domain unit | Pure rules and valid transitions | Expired holds cannot confirm |
| Integration (database) | Actual transactional behavior | Conflicting active holds cannot both commit |
| API behavior | Error semantics and idempotency | Same request key returns consistent effect |
| Contract | Event and API compatibility | Consumers tolerate compatible field changes |
| Concurrency | Realistic interleavings | At most one active claim per seat |
| Load | Capacity and latency under named workloads | Error rates and tail latency stay within defined thresholds |
| Failure injection | Recovery from restarts/network faults | Outbox events are eventually recovered |

### ✅ Principles

- Assert **invariants**, not just status codes.
- Prefer integration tests for database concurrency assumptions.
- Re-run races; one green stress test isn't a proof.
- Measure baseline before optimizing.
- Document test setup and environmental limitations.
- Separate business rejections (seat unavailable) from internal failures.

### 🧩 First test review

Before coding, agree on a minimum acceptance test that catches double-booking and describe what DB mechanism makes violations impossible to commit.