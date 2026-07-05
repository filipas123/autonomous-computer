https://github.com/user-attachments/assets/36f7aa02-42ac-4b35-b757-a5dd3b43ef1a

## The future of AI is local

The models got good. The GPUs got affordable. The only question left is where the intelligence lives — in someone else's cloud, or under your own roof. In 2026, homes and businesses are reaching the same answer: on-prem. Three reasons:

1. **No one can switch you off.** In June 2026 the US government took Fable 5 offline for most of a month and gated GPT-5.6 behind an approved-partner list. Weights on your own disk can't be revoked.
2. **Your business is their training data.** Every prompt you send OpenAI or Anthropic carries your product, your process, your edge. They will turn your secret sauce into their product.
3. **Inference becomes free.** Open weights on a cloud API already cut the bill 20–30×. On your own machine there is no bill at all. No API, no meter.

## The end-to-end open-source local AI stack

Open software on closed hardware is half an answer — you still can't see, fix, or rebuild the box it runs on, so you're still renting, one layer down. Local AI is only truly yours when the whole stack is open, metal included. So we open-sourced both halves:

- **Hardware — this repo.** Your Personal AI Computer in four sizes, below: every part, every bracket, every BIOS setting, every assembly photo.
- **Software — your choice.** Run any local AI framework — vLLM, Ollama, llama.cpp — or [Grid](https://github.com/autonomous-ai/autonomous-grid), our local AI orchestrator.

## 2× 5090 — Home

2× RTX 5090. Enough for Llama, Qwen, and DeepSeek with quantization. Run OpenClaw, Hermes Agent, or your own LangChain stack locally.

**64 GB VRAM · 192 GB RAM · 1600 W · print or CNC the housing yourself**

<a href="2x-5090/README.md"><img src="2x-5090/photos/gallery/hero.webp" alt="The 2× 5090 build — two RTX 5090s on the open frame"></a>

<table>
<tr>
<td width="50%"><img src="2x-5090/photos/gallery/riser-detail.webp" alt="Seating the PCIe riser"></td>
<td width="50%"><img src="2x-5090/photos/gallery/riser-frame.webp" alt="Mounting the PCIe 5.0 risers"></td>
</tr>
<tr>
<td width="50%"><img src="2x-5090/photos/gallery/fan-tray.webp" alt="The fan tray"></td>
<td width="50%"><img src="2x-5090/photos/gallery/side-panel.webp" alt="Closing the side panel"></td>
</tr>
</table>

<img src="2x-5090/photos/gallery/finished.webp" alt="The finished 2× 5090">

**[Build the 2× 5090 →](2x-5090/README.md)**

## 4× 5090 — Team

4× RTX 5090. Built for larger open models like Kimi, MiniMax, and GLM. No API bills. Low latency. Private data.

**128 GB VRAM · 256 GB RAM · dual-chamber airflow: intake below, GPUs above**

<a href="4x-5090/README.md"><img src="4x-5090/photos/gallery/hero.webp" alt="The 4× 5090 build — airflow through the dual-chamber housing"></a>

<table>
<tr>
<td width="50%"><img src="4x-5090/photos/gallery/fan-chassis.webp" alt="Motherboard on the fan chassis"></td>
<td width="50%"><img src="4x-5090/photos/gallery/psu-cabling.webp" alt="Cabling the power supplies"></td>
</tr>
<tr>
<td width="50%"><img src="4x-5090/photos/gallery/cooler-mount.webp" alt="Mounting a GPU to the frame"></td>
<td width="50%"><img src="4x-5090/photos/gallery/gpu-stack.webp" alt="All four RTX 5090s on the frame"></td>
</tr>
</table>

<img src="4x-5090/photos/gallery/finished.webp" alt="The finished 4× 5090">

**[See the 4× 5090 →](4x-5090/README.md)**

## 4× 6000 — Workstation

4× RTX PRO 6000 Blackwell in a 5U chassis. The full-precision machine: fine-tune and serve the biggest open models without quantizing.

**384 GB VRAM · 384 GB RAM · 3× 2000 W · off-the-shelf 5U chassis, no CNC work**

<a href="4x-6000/README.md"><img src="4x-6000/build-4x.jpg" alt="The 4× 6000 build — four RTX PRO 6000 Blackwell in the 5U chassis"></a>

**[Build the 4× 6000 →](4x-6000/README.md)**

## 8× 5090 — On-prem business

8× RTX 5090 on dual EPYC. A local inference box for teams shipping with open models. Develop, serve, fine-tune — the work that should never leave your floor.

**256 GB VRAM · 8000 W · CNC-milled, anodized aluminum housing**

<a href="8x-5090/README.md"><img src="8x-5090/photos/gallery/hero.webp" alt="The 8× 5090 build — eight GPUs in the anodized aluminum housing"></a>

<table>
<tr>
<td width="50%"><img src="8x-5090/photos/gallery/parts-layout.webp" alt="Every part laid out before assembly"></td>
<td width="50%"><img src="8x-5090/photos/gallery/mcio-adapter.webp" alt="Placing an MCIO adapter"></td>
</tr>
<tr>
<td width="50%"><img src="8x-5090/photos/gallery/pcie-adapters.webp" alt="Cabling the PCIe adapters"></td>
<td width="50%"><img src="8x-5090/photos/gallery/gpu-install.webp" alt="Installing the GPUs"></td>
</tr>
</table>

<img src="8x-5090/photos/gallery/finished.webp" alt="The finished 8× 5090">

**[Build the 8× 5090 →](8x-5090/README.md)**

## Software

1. **[BIOS tuning and GPU testing](setup.md)** — multi-GPU BIOS settings, NVIDIA drivers, and confirming every GPU is detected, linked at full PCIe width, and stable under load.
2. **[Run Grid](https://github.com/autonomous-ai/autonomous-grid)** — Grid is our open-source orchestration layer for local AI: it pools the computers you already own — this rig, your Mac, the workstation in the corner — behind **one OpenAI-compatible endpoint** and routes each request to whichever machine is running the right model, on your local network or remotely.

   ```bash
   curl -fsSL https://grid.autonomous.ai/install.sh | bash
   ```

## Contributing

Built one? Improved a part? Found a better component? See [**CONTRIBUTING.md**](CONTRIBUTING.md) — and [share your build](https://github.com/autonomous-ai/autonomous-computer/issues/new?template=share-your-build.md). The best community builds get featured.

## License

Open source under the [MIT License](LICENSE). Fork it, change it, build your own and sell it — we just want it built.

---

<div align="center">
<b>Autonomous</b> — the AI hardware company.<br>
Questions? <a href="https://github.com/autonomous-ai/autonomous-computer/issues">Open an issue.</a>
</div>
