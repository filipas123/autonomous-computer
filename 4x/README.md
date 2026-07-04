<div align="center">

# Personal AI Computer — 4× Configuration (Team)

<a href="../../README.md">← All builds</a>

<img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
<img src="https://img.shields.io/github/stars/autonomous-ai/autonomous-computer" alt="GitHub stars">
<img src="https://img.shields.io/badge/Status-Completed-brightgreen" alt="Status">
<img src="https://img.shields.io/github/repo-size/autonomous-ai/autonomous-computer" alt="Repo Size">
<img src="https://img.shields.io/github/issues/autonomous-ai/autonomous-computer" alt="Open Issues">
<img src="https://img.shields.io/github/issues-pr/autonomous-ai/autonomous-computer" alt="Open Pull Requests">

</div>

---

<div align="left">
    <b><i>
        <br>This guide shows you how to build a 5U workstation-class build with 4× NVIDIA RTX PRO 6000 Blackwell GPUs on an AMD EPYC SP5 platform.</br>
        <br>From hardware selection to assembly and BIOS tuning, follow each step to create a high-performance platform for deep learning, fine-tuning, and GPU-intensive workloads.</br>
    </i></b>
</div>

<img width="1637" height="646" alt="image" src="https://github.com/user-attachments/assets/472e8c4e-d263-4722-87ee-be61cf65fffb" />

---

## 📚 Table of Contents
- [Introduction](#-introduction)
- [Preparation](#-preparation)
- [Assembly](#-assembly)
- [Setup](#-setup)
- [Testing](#-testing)
- [BOM](#-bill-of-materials-bom)
- [Discussion](#-discussion)
- [License](#-license)

---

## 🏁 Introduction

This tutorial targets researchers, developers, and enthusiasts building the 4× configuration based on the ASRock Rack **TURIN2D24G-2L+** motherboard, **AMD EPYC 9124** CPU, **384 GB** DDR5 ECC RDIMM (8× 48 GB), and **4× Leadtek RTX PRO 6000 Blackwell Workstation** GPUs in a 5U chassis. You'll go from boxed parts to a stable platform ready for demanding AI workloads.

---

## 🛠️ Preparation

### 1. [Electronic & Electrical](docs/prepare-ee.md)

### 2. [Mechanical & Housing](docs/prepare-me.md)

---

## 🤖 Assembly

[See detailed steps](docs/assembly.md)

---

## ⚙️ Setup

### BIOS Optimization for GPU Performance

> **Tip:** The default BIOS settings may not deliver optimal performance for multi-GPU workloads. Adjust these parameters for best results:

- **PCIe Settings**

  ⚠️    Set all PCIe slots feeding the GPUs to Gen5 x16 and configure MCIO bifurcation accordingly.
    ```
    Advanced -> Chipset Configuration -> PCIE link width -> set MCIO pairs feeding the 4 GPUs to x16
    ```

- **Above 4G Decoding**

  ⚠️    Enable "Above 4G Decoding" so the platform can map the GPUs' large BARs.
    ```
    May be enabled by default
    ```

- **Resizable BAR**

  ⚠️    Activate "Resizable BAR" for improved CPU-GPU data transfer.
    ```
    Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
    ```

- **Power Management** — Disable unnecessary power-saving features (C-states, ASPM) that may throttle GPU performance. `Optional`

- **Memory Configuration** — Run all 8 DDR5 ECC RDIMM modules at the rated 1DPC speed for max bandwidth on EPYC SP5. `Optional`

- **Fan and Thermal Controls** — Adjust fan curves and thermal limits for optimal cooling under sustained GPU load. `Optional`

After saving changes, reboot and monitor GPU performance and stability.

**References:**
- ASRock Rack **TURIN2D24G-2L+** — see the vendor's motherboard and BMC manuals for exact menu locations.

---

## 🧪 Testing

Boot with WinPE from USB to verify hardware, or install Linux + NVIDIA drivers and check with `nvtop` / `nvidia-smi`. Once confirmed, install your OS and start your AI work.

---

## 📦 Bill of Materials (BOM)

- [Bill of Materials](bom/bom.md)

---

## 💬 Discussion

Alternative build options brainstormed before settling on this baseline — Turin upgrade path, single-socket variants, and a 3× H100 PCIe alternative — with verification notes.

- [Brainstorm & Discussion](docs/discussion.md)

---

## 📝 License

This project is open source under the [MIT License](LICENSE).
