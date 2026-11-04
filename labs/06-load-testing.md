# 🟡 Lab 06 — Load testing without misleading numbers

[← Labs](README.md) · [🧪 Quality path](https://github.com/the-engineering-dojo/engineering-handbook/blob/main/learning-paths/05-testing-observability.md)

### 🎯 Question

How does our correctness and latency change as load increases?

### 🧪 Two distinct workloads

| Workload | Why it matters |
| --- | --- |
| **Hot seat:** many clients want one seat | Tests contention, conflicts, idempotency, and invariant enforcement |
| **Broad inventory:** many clients want different seats | Tests capacity, database/query bottlenecks, and scalable throughput |

Do **not** compare their RPS values as if they test the same thing.

### 📊 Collect

- Hardware/runtime, dataset size, image/DB versions, warmup, test duration.
- Arrival rate or virtual users, request mix, retries, and network assumptions.
- Success/error counts; duplicate/conflicting active reservations.
- p50/p95/p99 response latency, throughput, and server/resource metrics.
- A baseline and any test-run limitations.

### ✅ Evidence

A short reproducible report that separates **correctness** from **performance** and states whether the system saturated or the test generator did.

### 🪜 Stretch

Introduce a controlled DB slowdown or broker failure, then compare recovery and user-visible errors.

**Status: planning; no synthetic benchmark results are claimed.**