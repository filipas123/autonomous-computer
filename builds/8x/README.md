# Personal AI Computer — 8× Configuration (On-Prem Business)

<div align="center"><a href="../../README.md">← All builds</a></div>

https://github.com/user-attachments/assets/3e410e5d-83f4-4aed-a8b4-2426781f3ebd



<div align="center">

<img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
<img src="https://img.shields.io/github/stars/autonomous-ai/autonomous-computer" alt="GitHub stars">
<img src="https://img.shields.io/badge/Status-In%20Development-blue" alt="Status">
<img src="https://img.shields.io/github/downloads/autonomous-ai/autonomous-computer/total" alt="Downloads">
<img src="https://img.shields.io/github/v/release/autonomous-ai/autonomous-computer" alt="Version">
<img src="https://img.shields.io/github/repo-size/autonomous-ai/autonomous-computer" alt="Repo Size">
<img src="https://img.shields.io/github/issues/autonomous-ai/autonomous-computer" alt="Open Issues">
<img src="https://img.shields.io/github/issues-pr/autonomous-ai/autonomous-computer" alt="Open Pull Requests">

</div>

---

<div align="center">
    <b><i>
        The largest build — 8× GPU (RTX 4090 or 5090) on a dual-EPYC (Genoa) platform. A team's AI on your own floor, where your IP and data never leave the building. From hardware selection to software setup, follow each step to a stable, high-performance platform.
    </i></b>
</div>

---

## Table of Contents
- [Introduction](#introduction)
- [Preparation](#preparation)
- [Assembly](#assembly)
- [Setup](#setup)
- [Testing](#testing)
- [Bill of Materials](#bill-of-materials)
- [Other Builds](#other-builds)
- [License](#license)

---

## Introduction

<table>
    <tr>
        <td align="center" width="55%">
            <b><i>
                This tutorial is for anyone aiming to build their own Personal AI Computer with 2x / 4x/ 8x GPUs. Whether you're a researcher, developer, or enthusiast, you'll learn everything from hardware selection and assembly to system configuration and initial testing. Finish with a robust platform ready for demanding AI workloads.
            </i></b>
        </td>
        <td align="center" width="45%">
            <img src="photos/8gpu/introduction/EdgeAI-8GPU-1.png" width="420" height="370" style="border-radius: 8px;">
        </td>
    </tr>
</table>

---

## Preparation

### 1. [Electronic & Electrical](docs/Prepare_EE.md)

### 2. [Mechanical & Housing](docs/Prepare_ME.md)

---

## Assembly

[See detailed steps](docs/Assembly.md)

---

## Setup

### BIOS Optimization for GPU Performance

> **Tip:** The default BIOS settings may not deliver optimal performance for multi-GPU workloads. Adjust these parameters for best results:

- **PCIe Settings** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Set all PCIe slots to the highest supported speed (Gen4/Gen5) and configure bifurcation for your GPUs.<br>
    ```
    Advanced -> Chipset Configuration -> PCIE link width -> set MCIO2/1, MCIO4/3, MCIO6/5, MCIO8/7, MCIO12/11, MCIO14/13, MCIO16/15, MCIO18/17 to x16
    ```

- **Above 4G Decoding** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Enable "Above 4G Decoding" to address large GPU memory.<br>
    ```
    May be enabled by default
    ```

- **Resizable BAR** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    Activate "Resizable BAR" for improved CPU-GPU data transfer.<br>
    ```
    Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
    ```

- **Power Management**<br>
    Disable unnecessary power-saving features (C-states, ASPM) that may throttle GPU performance.<br>
    `Optional`

- **Memory Configuration**<br>
    Set RAM to rated speed and enable XMP/DOCP profiles for max bandwidth.<br>
    `Optional`

- **Fan and Thermal Controls**<br>
    Adjust fan curves and thermal limits for optimal cooling.<br>
    `Optional`

After saving changes, reboot and monitor GPU performance and stability.

**References:**
- [Motherboard User Manual](docs/UM_motherboard.pdf)
- [BMC Documents](docs/UM_BMC.pdf)

<p align="center">
    <!-- Upload How-to-set-up-BIOS.mp4 to this repo and replace this line with the video tag -->
</p>

---

## Testing

Boot with WinPE from USB to verify hardware, or install Linux, NVIDIA drivers, and check with `nvtop`. Once confirmed, install your OS and start your AI work.

<table>
    <tr>
        <td align="center">
            <img src="photos/8gpu/testing/Nvtop.png" width="700"><br>
        </td>
        <td align="center">
            <img src="photos/8gpu/assembly/40.png" width="400"><br>
        </td>
    </tr>
</table>

<p align="center">
    <!-- Upload Booting.mp4 to this repo and replace this line with the video tag -->
</p>

---

## Bill of Materials

- [Bill of Materials](bom/BOM.md)

---

## Other Builds

<table>
    <tr>
        <td align="center" width="50%">
            <a href="../2x/README.md">
                <img src="../2x/photos/2gpu/introduction/introduction.png" width="420" style="border-radius: 8px;">
            </a>
            <br><b>2× — Home</b> · 2× RTX 5090<br>
            <a href="../2x/README.md">View Build Guide →</a>
        </td>
        <td align="center" width="50%">
            <a href="../4x/README.md">
                <img src="../4x/photos/4gpu/introduction/rack1.jpg" width="420" style="border-radius: 8px;">
            </a>
            <br><b>4× — Team</b> · 4× RTX PRO 6000 Blackwell<br>
            <a href="../4x/README.md">View Build Guide →</a>
        </td>
    </tr>
</table>

See all builds and the software guides on the [main page](../../README.md).

---

## License

This project is open source under the [MIT License](../../LICENSE).

---

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=1800&pause=1000&color=11F732&width=840&lines=If+this+helped%2C+toss+us+a+%E2%AD%90.+Got+questions%3F+Open+an+issue." alt="Typing SVG" /></a>
</p>
