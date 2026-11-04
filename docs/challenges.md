# 🧪 Challenge catalog

[← Project](../README.md) · [📚 Handbook](https://github.com/the-engineering-dojo/engineering-handbook)

Every challenge should end with a **short debrief and evidence**, not a screenshot of “it works”.

| ID | Difficulty | Question | Lab |
| --- | --- | --- | --- |
| RES-01 | 🟢 Explore | How can two clients both believe a seat is available? | [Double booking](../labs/01-double-booking.md) |
| RES-02 | 🟡 Practice | Which transaction/constraint prevents conflicting commits? | [Transactions](../labs/02-transactions.md) |
| RES-03 | 🟠 Deep dive | How do we recover an event after publish fails? | [Messaging + outbox](../labs/03-messaging-outbox.md) |
| RES-04 | 🟡 Practice | What makes a reproducible multi-container development setup? | [Docker](../labs/04-docker.md) |
| RES-05 | 🟠 Deep dive | Why do two pods expose assumptions about state? | [Kubernetes](../labs/05-kubernetes.md) |
| RES-06 | 🟡 Practice | How do we distinguish throughput from correctness? | [Load testing](../labs/06-load-testing.md) |

## ✅ The review checklist

- [ ] The question and hypotheses are written before experimenting.
- [ ] Failure and success conditions are explicitly defined.
- [ ] Inputs, environment, and assumptions are reproducible.
- [ ] Tests/observations provide meaningful evidence.
- [ ] Trade-offs and alternative approaches are discussed.
- [ ] Team members can explain the result independently.

**Current status:** all challenge implementations are **proposed**, not complete. Browse the [repository issues](https://github.com/the-engineering-dojo/reservation-engine/issues) for discussion and ownership.