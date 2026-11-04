# 🟡 Lab 04 — Docker and reproducible environments

[← Labs](README.md) · [🐳 Cloud-native path](https://github.com/the-engineering-dojo/engineering-handbook/blob/main/learning-paths/04-cloud-native.md)

### 🎯 Question

Can every teammate reproduce the same service + database environment on their machine?

### 🧪 Plan (later)

1. Explain the dependency graph and each container's purpose.
2. Compare a multi-stage image build with a naive image.
3. Identify runtime configuration and secrets that must not be committed.
4. Explain container networking and persistent data volumes.
5. Design health/readiness checks and clean teardown.
6. Verify startup under different ordering and slow dependencies.

### ✅ Evidence

One documented startup flow, reproducible environment settings, an image-size comparison, and a clear story for persisting PostgreSQL data.

### 🪜 Stretch

Explain why “container started” does not mean “service ready.”

**Status: planning; no Dockerfile or Compose configuration is published yet.**