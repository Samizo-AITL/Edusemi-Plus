---
title: "VSRAM (Pseudo-SRAM) 2001 — Mobile Memory Case"
layout: default
---

# VSRAM (Pseudo-SRAM) — 2001 Mobile Memory Case

This directory documents the **VSRAM (Pseudo-SRAM)** developed and mass-produced in **2001**
using a **0.25µm DRAM-derived process** for mobile applications.

This case represents a **transition point** where
standard DRAM technology was pushed beyond its original operating envelope
to meet **low-power, high-temperature (90 °C)** mobile requirements.

---

## Why This Case Matters

VSRAM exposed limits that were **not visible in standard DRAM**:

- Long refresh interval under mobile standby
- High-temperature (90 °C) operation
- Strong coupling between **Pause / Disturb** and **system usage**
- Yield recovery under **simultaneous production pressure**

This was not a clean-sheet design, but a **constraint-driven evolution**.

---

## Contents

- **Architecture & Concept**
  - [`vsram_architecture.md`](./vsram_architecture.md)  
    → Pseudo-SRAM concept and DRAM reuse strategy

- **Failure Modes**
  - [`pause_disturb_vsram.md`](./pause_disturb_vsram.md)  
    → Pause / Disturb failures under mobile conditions

- **Yield Recovery**
  - [`yield_recovery.md`](./yield_recovery.md)  
    → Process, bias, and CD countermeasures

---

## How to Read This Case

1. Understand **why DRAM was reused**
2. Examine **new failure modes introduced by usage**
3. Follow **yield recovery under time pressure**
4. Observe the **strategic endpoint** of DRAM-derived memory

---

## Positioning in Legacy Technology

VSRAM is a **boundary case**:

- Between DRAM and logic
- Between process reuse and redesign
- Between laboratory reliability and field reality

It directly informed later decisions
to **terminate DRAM-derived memory paths**
and redirect resources to mixed-signal and HV-CMOS products.
