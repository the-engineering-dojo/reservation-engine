# 🎬 Product brief — the reservation playground

[← Project home](../README.md) · [🧩 Domain model](domain-model.md)

## 🧑‍💻 Why this case study?

The point is **not** to launch a ticketing startup. Reserving limited resources naturally creates real software engineering questions.

### 🎟️ Happy path (future)

1. A person browses an event and its seats.
2. They request a temporary hold for a seat.
3. The system accepts or rejects the request without violating availability.
4. The hold is confirmed or expires.
5. A notification may be sent asynchronously.

### ⚠️ Failure scenarios worth studying

| Scenario | Engineering question |
| --- | --- |
| A hundred simultaneous requests | Can more than one hold win for the same seat? |
| Retry after a lost response | Can the same customer accidentally reserve twice? |
| Server restarts mid-operation | Was the transaction committed? |
| Hold expires during confirmation | Who wins, expiration or confirmation? |
| Notification is published twice | How do consumers avoid repeated effects? |
| Two API replicas handle traffic | Do database guarantees hold across processes? |
| Broker is temporarily unavailable | Can events be recovered after the database commit? |

### 📌 Non-goals (for now)

Real payment processing, personal customer information, commercial availability, advanced authentication flows, polished frontend, and production deployment.

### 👥 Who this is for

Backend engineers who want to practice modeling, reasoning, testing, distributed systems, DevOps, and communication together.

**Success means:** learning outcomes explained with diagrams, tests, and measurements—not the number of implemented services.