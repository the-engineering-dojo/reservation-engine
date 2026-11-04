# 🟡 Lab 02 — Transactions and isolation

[← Labs](README.md) · [🔒 Correctness path](https://github.com/the-engineering-dojo/engineering-handbook/blob/main/learning-paths/02-reliable-data.md)

### 🎯 Question

Which database mechanisms can enforce seat exclusivity under concurrency?

### 🧩 Compare

| Approach | What to investigate |
| --- | --- |
| Unique/partial unique constraint | Can conflicting active claims ever commit simultaneously? |
| Optimistic version check | Which writes must fail and retry? |
| Explicit row locking | When is the lock acquired and released? |
| Serializable transaction | Which anomalies are prevented and when must we retry? |

### 🧪 Plan

Choose two competing client timelines. Document the expected reads, writes, and commits for each option. Describe deadlock/serialization-failure handling and how errors map to an API response.

### ✅ Acceptance evidence

- A documented invariant enforced at the persistence boundary.
- Repeatable integration-test design for competing requests.
- Reasoning about throughput vs contention.
- An explanation of how expiration and confirmation interact with the constraint.

### 🪜 Stretch

Discuss a multi-seat hold requiring all-or-nothing success.

**Status: planning. No database implementation yet.**