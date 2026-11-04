# 🟠 Lab 05 — Kubernetes, replicas and state

[← Labs](README.md) · [☸️ Cloud-native path](https://github.com/the-engineering-dojo/engineering-handbook/blob/main/learning-paths/04-cloud-native.md)

### 🎯 Question

Does adding two API replicas change correctness or only capacity?

### 🎬 Scenario

Run the same reservation API behind a Kubernetes Service. Compare process-local holds with a database-enforced invariant.

### 🧪 Proposed sequence

1. Explain Service vs Deployment vs Pod.
2. Draw requests routed to pod A and pod B.
3. Predict the bug if each pod stores authoritative seat state locally.
4. Plan readiness, liveness, resource requests, and rollout behavior.
5. Discuss what happens when a pod dies after a commit but before reply.
6. Compare traces from different replicas.

### ✅ Evidence

A request timeline across replicas, successful protection of the seat invariant, and a deployment/rollback explanation.

### ⚠️ Caution

Kubernetes schedules work; it does **not** replace database consistency or durable storage.

**Status: planning; no Kubernetes manifests or cluster resources yet.**