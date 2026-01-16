---
layout: default
title: Legacy Technology
---

# Legacy Technology

Legacy Technology is not a collection of obsolete processes.

This archive documents **canonical failure-and-recovery cases**
where physical mechanisms directly constrained
**yield, reliability, and business decisions**.

These cases are preserved not as nostalgia,
but as **reference structures** that still reappear
in modern semiconductor, system, and AI-integrated designs.

---

## 🔐 Note on Confidentiality

> **All materials in this archive are based on semiconductor technologies  
> developed more than 20 years ago (late 1990s–early 2000s).**
>
> This archive **does not contain** proprietary process recipes,  
> confidential design rules, equipment tuning parameters,  
> or operational know-how applicable to current semiconductor manufacturing.
>
> The purpose of this archive is to preserve  
> **structural patterns of failure, recovery, and decision-making**,  
> not implementation-level secrets.

---

## Introduction

This archive is introduced and positioned in detail here:

→ **[Introduction — Legacy Technology](./introduction.md)**

---

## Scope of This Archive

- **Semiconductor process integration** (1990s–2000s)
- **Memory technologies** (DRAM, VSRAM, eDRAM)
- **Failure physics** (leakage, disturb, retention)
- **Yield recovery** and decision-making under constraints

---

## How to Read

Each case is organized as a causal chain:

1. **Process / Structure**  
2. **Observed Failure Mode**  
3. **Physical Root Cause**  
4. **Test / Bin Manifestation**  
5. **Yield Recovery or Strategic Decision**

This order mirrors actual manufacturing problem-solving,
not post-hoc explanation.

---

## Case Index

### 📁 DRAM (0.25µm, 64M) — 3rd Generation
- **Case overview**  
  → [`dram_025um/`](./dram_025um/)
- **Process integration**  
  → [`dram_025um/process_flow.md`](./dram_025um/process_flow.md)
- **Wafer test & bin classification**  
  → [`dram_025um/wafer_test_bin.md`](./dram_025um/wafer_test_bin.md)
- **Failure physics (Pause / Disturb)**  
  → [`dram_025um/pause.md`](./dram_025um/pause.md)

---

### 📁 VSRAM (Pseudo-SRAM, 2001) — Mobile Memory
- **Case overview**  
  → [`vsram_2001/`](./vsram_2001/)
- **Architecture & concept**  
  → [`vsram_2001/vsram_architecture.md`](./vsram_2001/vsram_architecture.md)
- **Pause / Disturb under mobile usage**  
  → [`vsram_2001/pause_disturb_vsram.md`](./vsram_2001/pause_disturb_vsram.md)
- **Yield recovery & countermeasures**  
  → [`vsram_2001/yield_recovery.md`](./vsram_2001/yield_recovery.md)

---

## Positioning

Legacy Technology cases are archived here because they expose
**structural limits**, not because they are old.

Modern systems often fail for the **same reasons**:
only the scale, names, and integration context change.
