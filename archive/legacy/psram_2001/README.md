# PSRAM (Pseudo-SRAM) — 2001 Mobile Memory Case

This directory documents the **PSRAM (Pseudo-SRAM)** developed and mass-produced in **2001**
using a **0.25µm DRAM-derived process** for mobile applications.

This case represents a **transition point** where
standard DRAM technology was pushed beyond its original operating envelope
to meet **low-power, high-temperature (90 °C)** mobile requirements.

---

## 🔐 Note on Confidentiality

> **All materials in this case are based on semiconductor technologies  
> developed more than 20 years ago.**
>
> This documentation does **not** include proprietary process recipes,
> confidential design rules, equipment tuning parameters,
> or operational know-how applicable to modern semiconductor manufacturing.
>
> The purpose of this case study is to preserve  
> **structural patterns of failure, recovery, and engineering decision-making**,  
> not implementation-level secrets.

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
  - [`psram_architecture.md`](./psram_architecture.md)  
    → Pseudo-SRAM concept and DRAM reuse strategy

- **Failure Modes**
  - [`pause_disturb_psram.md`](./pause_disturb_psram.md)  
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

PSRAM is a **boundary case**:

- Between DRAM and logic
- Between process reuse and redesign
- Between laboratory reliability and field reality

It directly informed later decisions
to **terminate DRAM-derived memory paths**
and redirect resources to mixed-signal and HV-CMOS products.

