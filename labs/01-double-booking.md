# 🟢 Lab 01 — The double-booking race

[← Labs](README.md) · [🔐 Concurrency note](https://github.com/the-engineering-dojo/engineering-handbook/blob/main/notes/concurrency-transactions.md)

### 🎯 Question

What happens when many clients concurrently request the same seat?

### 🎬 Scenario

One event, one seat, 100 independent clients. Each client submits one hold request at nearly the same time. The initial design is intentionally simple so the race can be understood.

### 🧠 Predict first

- How might two requests read “available” before either commits?
- Can a process-local lock help when there is more than one API process?
- Does “all tests passed” mean the invariant is guaranteed?

### 🧪 Proposed experiment

1. Draw the interleaving of two competing requests.
2. Identify a naive read-then-write implementation's failure window.
3. Design a repeatable test plan with synchronized starts.
4. State a safety property: **at most one conflicting active reservation**.
5. Discuss liveness separately: what should happen if all clients fail or time out?

### ✅ Evidence to collect later

An event timeline, reproduction steps, number of accepted conflicting claims, and explanation of the enforcement mechanism.

### 🪜 Stretch

What changes if the clients all retry due to a lost response?

**Status: planning. No implementation yet.**