# ADR-0001: Begin with a modular monolith

**Status:** Proposed  
**Scope:** Reservation Engine learning architecture  
**Date:** 2026-11-04

## 🎯 Context

We want to learn DDD, concurrency, transactional consistency, and distributed systems. Starting with several independently deployed services would introduce network, deployment, and operational concerns before we understand the seat-reservation invariant.

## 🧭 Options

| Option | Pros | Cons |
| --- | --- | --- |
| Modular monolith | Single-transaction reasoning, simpler debugging, faster iteration | Requires intentional module boundaries |
| Multiple microservices immediately | More network and deployment scenarios early | Premature complexity; business boundaries and consistency harder to reason about |

## ✅ Proposed decision

Start with an application structured by **domain capabilities** and explicit interfaces. Use a durable transactional database when the correctness lab begins. Split an asynchronous, low-consistency-sensitivity capability (e.g. notifications) as a later learning exercise.

## ⚖️ Consequences

We can explore distributed failures **incrementally**, measure the added complexity, and change our minds based on evidence. This is a **proposal to discuss**, not a decision imposed on contributors.

## 🔄 Revisit when

A documented lab demonstrates a compelling reason for independent deployment, scaling, ownership, or failure isolation.