# 🎨 Conceptual interface sketches

[← Project](../README.md) · [🎬 Brief](product-brief.md)

These are **discussion mockups**, not frontend implementations. We want the smallest interface that makes correctness problems visible.

## Screen A — Event seats

| Seat | Availability | Action |
| --- | --- | --- |
| A-01 | 🟢 Available | Request hold |
| A-02 | 🟠 Held (expires soon) | Unavailable |
| A-03 | 🔒 Confirmed | Unavailable |

**Design question:** can the UI display a stale seat state? Yes. How should the server respond to a rejected hold?

## Screen B — Race lab dashboard

| Signal | Example display |
| --- | --- |
| 👥 Concurrent attempts | 100 |
| ✅ Accepted holds | 0–1 expected |
| ❌ Conflict responses | Remaining valid conflicts |
| ⏱️ Latency distribution | p50 / p95 / p99 |
| 🔁 Retries | Count and resulting effects |
| 🧩 Invariant violation | Must stay at 0 |

These numbers are **illustrative expectations**, not benchmark results.

## Screen C — Failure timeline

Show a single operation across:
- Client: request / timeout / retry
- API: validation / transaction / response
- Database: read / write / commit
- Broker and worker (later): publish / acknowledge / consume

### ✅ UI principle

Show **why a result happened**, not just green/red success icons. Use accessible labels and enough contrast so color is never the sole signal.