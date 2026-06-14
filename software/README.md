# Software — Bringing the Box to Life

Hardware is half of a Personal AI Computer. This is the other half: getting the OS, drivers, and BIOS right, verifying the GPUs, and then **serving open models locally** so your intelligence runs on your machine and answers to no one.

> **Status:** Setup and testing are documented below. The local model-serving guides (Ollama / vLLM / llama.cpp, picking open models, connecting an agent) are **in progress** — see [`run-models.md`](run-models.md).

## Steps

1. **[Setup](setup.md)** — BIOS tuning for multi-GPU, NVIDIA drivers, and OS install.
2. **[Testing](testing.md)** — verify every GPU is seen and stable before you rely on it.
3. **[Run models](run-models.md)** — serve open models locally and point an agent at them. *(In progress.)*

## Per-build specifics

The steps here are common to all three builds. Exact BIOS menu paths and board manuals differ per motherboard — see each build's own `docs/` for board-specific detail:

- [2× RTX 5090 — docs](../builds/2x/docs/)
- [4× RTX PRO 6000 — docs](../builds/4x/docs/)
- [8× GPU — docs](../builds/8x/docs/)
