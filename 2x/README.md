<p align="center">
    <a href="https://git.io/typing-svg">
        <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=32&duration=1800&pause=600&color=11F732&background=000000&width=1000&height=110&lines=Welcome+-+where+2%C3%975090s+become+your+new+roommate." alt="Typing SVG" />
    </a>
</p>

<p align="center">
    <img src="photos/2gpu/introduction/introduction.png" width="700" style="border-radius: 12px; box-shadow: 0 4px 16px #11F73255;">
</p>

<div align="center"><a href="../../README.md">← All builds</a></div>

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
        This guide shows you how to build a Personal AI Computer with 2× RTX 5090 — the Home configuration, the one you can start tonight. From hardware selection to software setup, follow each step to a high-performance platform for running open models locally.
    </i></b>
</div>

---

## 📚 Table of Contents
- 🏁 Introduction 
- 🛠️ Preparation 
- 🤖 Assembly 
- ⚙️ Setup
- 🧪 Testing 
- 📦 BOM
- 📝 License

---

# 🏁 Introduction &ensp; [🔝](#-table-of-contents)

<table>
    <tr>
        <td align="center" width="55%">
            <b><i>
                This tutorial guides you through building a high-performance Personal AI Computer with two GPUs. Whether you're a researcher, developer, or enthusiast, you'll learn everything from selecting and assembling the right hardware to configuring your system and performing initial tests. By the end, you'll have a powerful platform ready for demanding AI workloads.
            </i></b>
        </td>
        <td align="center" width="45%">
            <img src="photos/2gpu/introduction/introduction.png" width="350"  style="border-radius: 8px;">
        </td>
    </tr>
</table>

---

# 🛠️ Preparation &ensp; [🔝](#-table-of-contents)

### 1. [**Electronic & Electrical**](docs/Prepare_EE.md)

### 2. [**Mechanical & Housing**](step_models/)

---

# 🤖 Assembly &ensp; [🔝](#-table-of-contents)
[See detailed steps](docs/Assembly.md)

---

# ⚙️ Setup &ensp; [🔝](#-table-of-contents)
### BIOS Optimization for GPU Performance

> **Tip:** The default BIOS settings may not deliver optimal performance for multi-GPU workloads. Adjust these parameters for best results:


- **Above 4G Decoding** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    🚨📢🔔⚠️
    Enable "Above 4G Decoding" to address large GPU memory.<br>
    ```
    Advanced -> PCI Subsystems Settings -> Enable Above 4G Decoding
    ```

- **Resizable BAR** ![Static Badge](https://img.shields.io/badge/Important-8A2BE2)<br>
    🚨📢🔔⚠️
    Activate "Resizable BAR" for improved CPU-GPU data transfer.<br>
    ```
    Advanced -> PCI Subsystems Settings -> Enable Re-size BAR support
    ```

- **Power Management**  
    Disable unnecessary power-saving features (C-states, ASPM) that may throttle GPU performance.<br>
    `Optional`

- **Memory Configuration**  
    Set RAM to rated speed and enable XMP/DOCP profiles for max bandwidth.<br>
    `Optional`

- **Fan and Thermal Controls**  
    Adjust fan curves and thermal limits for optimal cooling.<br>
    `Optional`

After saving changes, reboot and monitor GPU performance and stability.

**References:**  
- [Motherboard User Manual 💻🖱️](docs/UM_Motherboard.pdf)  
- [BMC Documents 🤖](docs/UM_BIOS.pdf)

<p align="center">
    <video src=""></video>
</p>

---

# 🧪 Testing &ensp; [🔝](#-table-of-contents)

Boot with WinPE from USB to verify hardware, or install Linux, NVIDIA drivers, and check with `nvidia-smi or nvtop`. Once confirmed, install your OS and start your AI work.

<table>
        <td align="center">
            <img src="photos/2gpu/testing/nvidia-smi.png" width="700"><br>
        </td>
</table>

<p align="center">
    <video src=""></video>
</p>

---

# 📦 Bill of Materials (BOM) &ensp; [🔝](#-table-of-contents)

- [𝄜 Bill of Materials](bom/BoM.md)

---

# 📝 License &ensp; [🔝](#-table-of-contents)

This project is open source under the [MIT License](LICENSE).

---

<p align="center">
  <a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&duration=1800&pause=1000&color=11F732&width=840&lines=If+this+helped%2C+toss+us+a+%E2%AD%90.+Got+questions%3F+Open+an+issue." alt="Typing SVG" /></a>
</p>
