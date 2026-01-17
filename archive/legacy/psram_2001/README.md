# 📱 PSRAM (Pseudo-SRAM) — 2001 Mobile Memory Case

This directory documents the **PSRAM (Pseudo-SRAM)** technology
developed and mass-produced in **2001**, using a
**0.25µm DRAM-derived process** for mobile applications.

This case represents a **critical transition point** where
standard DRAM technology was deliberately pushed
**beyond its original operating envelope** to satisfy:

- 🔋 Low-power standby requirements  
- 🌡 Sustained **high-temperature operation (≈90 °C)**  
- 📲 Mobile-specific usage patterns  

PSRAM was not a clean-sheet innovation, but a
**constraint-driven adaptation** of an existing DRAM platform.

---

## 🔐 Note on Confidentiality

> **All materials in this case are based on semiconductor technologies  
> developed more than 20 years ago.**
>
> This documentation intentionally excludes:
>
> - Proprietary process recipes  
> - Confidential design rules  
> - Equipment tuning parameters  
> - Operational know-how applicable to modern semiconductor manufacturing
>
> 🎯 The objective is to preserve  
> **structural patterns of failure, recovery, and engineering decision-making**,  
> not implementation-level secrets.

This makes the case suitable for **education, architectural analysis,
and legacy technology study**.

---

## ⭐ Why This Case Matters

PSRAM exposed **limitations that were invisible in standard DRAM operation**.

| Constraint | Why It Mattered |
|---|---|
| Long refresh interval | Mobile standby amplified retention weakness |
| High temperature (90 °C) | Leakage-driven failures became dominant |
| Pause / Disturb coupling | Usage pattern directly triggered physics |
| Production pressure | Yield recovery had to occur *in parallel* with shipping |

📌 **Key distinction:**  
Failures were no longer revealed only by wafer test,
but by **real system usage conditions**.

---

## 📂 Contents Overview

### 🧠 Architecture & Concept
- [`psram_architecture.md`](./psram_architecture.md)  
  → Pseudo-SRAM concept, DRAM reuse strategy,
  and architectural compromises.

---

### ⚛️ Failure Modes
- [`pause_disturb_psram.md`](./pause_disturb_psram.md)  
  → Pause / Disturb behavior under
  **mobile temperature and access conditions**.

---

### 📈 Yield Recovery
- [`yield_recovery.md`](./yield_recovery.md)  
  → Process, bias, and CD countermeasures
  executed under **simultaneous production pressure**.

---

## 🧭 How to Read This Case

Recommended reading flow:

1. 🧠 **Why DRAM was reused**  
   — business and schedule constraints  
2. ⚠️ **New failure modes introduced by usage**  
   — not by process scaling  
3. 🛠 **Yield recovery under time pressure**  
   — mitigation without redesign  
4. 🎯 **Strategic endpoint**  
   — what conclusions were ultimately drawn

This mirrors how decisions were actually made,
not how they might appear in hindsight.

---

## 🧱 Positioning in Legacy Technology

PSRAM stands as a **boundary case** in semiconductor history:

- Between **memory and logic**
- Between **process reuse and redesign**
- Between **laboratory reliability** and **field reality**

It directly informed later strategic decisions to:

- ❌ Terminate DRAM-derived memory paths  
- 🔀 Redirect engineering resources toward  
  **mixed-signal** and **HV-CMOS–based products**

📘 **Legacy insight:**  
PSRAM did not fail because the engineers were wrong —  
it failed because **the operating context changed faster than physics allowed**.

---


