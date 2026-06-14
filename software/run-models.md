# Run Models Locally

> **🚧 In progress.** This is the half that turns a GPU box into *your* intelligence. Guides below are placeholders — we're writing them now. Want to help? See [CONTRIBUTING](../CONTRIBUTING.md).

The goal: serve open models on your own machine and point your tools and agents at `localhost` — no API key, no rate limit, no one who can cut you off.

## Planned contents

- **Serving engines**
  - [ ] **Ollama** — easiest start; pull and run a model in one command.
  - [ ] **vLLM** — high-throughput serving, OpenAI-compatible endpoint.
  - [ ] **llama.cpp** — maximum control, quantization, GGUF.
- **Which open models to run** *(by build / VRAM)*
  - [ ] DeepSeek (V3 / R1)
  - [ ] Qwen
  - [ ] Llama
  - [ ] Quantization and model-fit guidance per VRAM tier (64 GB / 384 GB / 256 GB)
- **Connect an agent**
  - [ ] Point an OpenAI-compatible client at your local endpoint.
  - [ ] Wire up an agent (e.g. OpenClaw / Claude Code-style harness) to your local model.
- **Benchmarks**
  - [ ] Tokens/sec per build and model, so you know what to expect before you buy.

Check back, or open a PR to fill a section.
