# Build your own Personal AI Computer

The best models live in someone else's cloud, behind someone else's terms and someone else's government — a model you rent can be cut off overnight; a model in your own house can't. These are open-source guides to build that machine: every part, every bracket, every BIOS setting, every assembly photo. Pick the size that fits your budget and your work. **Build it once; own it for good.**

https://github.com/user-attachments/assets/3e410e5d-83f4-4aed-a8b4-2426781f3ebd

## Quick start

1. **Pick a build** below by budget and the models you want to run — [2×](2x/README.md) · [4×](4x/README.md) · [8×](8x/README.md).
2. **Source the parts** from that build's Bill of Materials — [2×](2x/bom/BoM.md) · [4×](4x/bom/bom.md) · [8×](8x/bom/BOM.md).
3. **Make the housing** — print the STL files or CNC the STEP files — [2×](2x/stl-models) · [8×](8x/stl-models).
4. **Assemble** — follow the photo-by-photo assembly guide — [2×](2x/docs/Assembly.md) · [4×](4x/docs/assembly.md) · [8×](8x/docs/Assembly.md).
5. **Software** — [BIOS setup](setup.md), [GPU testing](testing.md), and [Grid](https://github.com/autonomous-ai/autonomous-grid).

## Hardware: Pick your build

There's a build for every budget and use case. Each is a complete, self-contained guide: bill of materials, housing files, wiring, BIOS, and assembly photos.

<table>
<tr>
<td align="center" width="33%">
<a href="2x/README.md"><img src="2x/build-2x.jpg" alt="The 2× build" width="280"></a><br><br>
<a href="2x/README.md"><b>2× — Home</b></a>
</td>
<td align="center" width="33%">
<a href="4x/README.md"><img src="4x/build-4x.jpg" alt="The 4× build" width="280"></a><br><br>
<a href="4x/README.md"><b>4× — Team</b></a>
</td>
<td align="center" width="33%">
<a href="8x/README.md"><img src="8x/build-8x.jpg" alt="The 8× build" width="280"></a><br><br>
<a href="8x/README.md"><b>8× — On-prem business</b></a>
</td>
</tr>
</table>

## Software

1. **[Setup](setup.md)** — BIOS tuning for multi-GPU, NVIDIA drivers, and your OS.
2. **[Testing](testing.md)** — confirm every GPU is detected, linked at full PCIe width, and stable under load.
3. **[Run Grid](https://github.com/autonomous-ai/autonomous-grid)** — Grid is our open-source orchestration layer for local AI: it pools the computers you already own — this rig, your Mac, the workstation in the corner — behind **one OpenAI-compatible endpoint** and routes each request to whichever machine is running the right model, on your local network or remotely.

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
