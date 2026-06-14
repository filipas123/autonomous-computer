# Testing

Verify the hardware before you rely on it. Confirm every GPU is detected, linked at full PCIe width, and stable under load.

## Quick verification

- **Fast hardware check:** boot **WinPE from USB** to confirm all cards enumerate, or
- **Linux check:** install Linux + NVIDIA drivers, then:
  ```bash
  nvidia-smi      # every GPU listed, correct VRAM, expected power/temp
  nvtop           # live per-GPU utilization and memory
  ```

Confirm:
- [ ] All GPUs appear in `nvidia-smi` (count matches your build: 2 / 4 / 8).
- [ ] Each card reports its full VRAM.
- [ ] PCIe link width/speed is what you set in BIOS (no cards dropped to x1/x4).
- [ ] Temperatures and power draw are sane at idle and under load.

Once confirmed, install your working OS and start running models — see [run-models.md](run-models.md).

## Reference

Per-build testing screenshots live in each build's `photos/.../testing/`.
