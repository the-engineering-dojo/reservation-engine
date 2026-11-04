# 🗺️ Reservation Engine — engineering roadmap

[← Project home](../README.md) · [🧪 Labs](../labs/README.md)

**Planning only.** Each stage is a learning milestone, not a release deadline. Move forward only when the team can explain and verify the previous stage.

| Phase | Focus | Proof of learning |
| --- | --- | --- |
| **0 · Understand** | Domain language, use cases, invariants, ADRs | Every participant can challenge the model |
| **1 · Local correctness** | Domain rules, single process, first tests | Reproducible lifecycle scenarios |
| **2 · Durable correctness** | PostgreSQL, transactions, constraints, optimistic/pessimistic alternatives | No conflicting committed reservations in integration tests |
| **3 · Evidence & tooling** | Docker Compose, deterministic tests, baseline load testing | Reproducible local environment and documented latency/error rate |
| **4 · Messaging & reliability** | Outbox/Inbox, RabbitMQ, retries, idempotency, fault injection | Recovery from commit/publish failure without lost effects |
| **5 · Distributed boundaries** | A notification worker/service; communication contracts | Documented failure behavior and independent lifecycle |
| **6 · Kubernetes** | kind, Services, Deployments, probes, config, replicas | Same correctness invariant with multiple API replicas |
| **7 · Operability** | OpenTelemetry, dashboards, SLO thinking, load/chaos experiments | Compare latency, error rate, and recovery with recorded evidence |
| **8 · Reflect** | Refactor, compare alternatives, write lessons learned | Peer-reviewed decisions and teach-back session |

### 🥋 Recommended first session

Do **Phase 0 only**: agree on what a “hold” is, write the five invariants, draw two alternative models, and choose the first failure to reproduce.

### ⛔ Not the goal

A 12-service demo, maximizing technology count, or deploying infrastructure before its learning problem is defined.

### 🔁 Repeatable format

**Question → Prediction → Experiment → Evidence → Review → Decision.** See [the challenge catalog](challenges.md) and [the handbook](https://github.com/the-engineering-dojo/engineering-handbook).