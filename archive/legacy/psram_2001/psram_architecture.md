---
title: "PSRAM Architecture and Concept"
layout: default
---

# 📱 PSRAM Architecture and Concept  
*(Mobile-Oriented DRAM Reuse, circa 2001)*

PSRAM (Pseudo-SRAM) is a **DRAM-based memory architecture**
designed to **emulate SRAM behavior** by integrating
**internal refresh control logic** on-chip.

Unlike conventional DRAM, PSRAM intentionally hides refresh operations
from the system, presenting a **simple, SRAM-like interface**
to mobile processors.

---

## 🎯 Motivation: Why PSRAM Existed

Around 2000–2001, mobile systems faced conflicting requirements:

| Memory Type | Strength | Limitation |
|---|---|---|
| SRAM | Fast, simple interface | Large cell area, high cost |
| DRAM | High density, low cost | External refresh, high standby overhead |

### PSRAM aimed to bridge this gap by targeting:

- 📉 **Lower standby current than DRAM**
- 📦 **Higher density than SRAM**
- 🔌 **No external refresh burden on the system**
- 🌡 **Guaranteed operation at up to 90 °C (mobile spec)**

---

## 🧠 Core Architectural Concept

PSRAM retained the **standard DRAM cell array**, but added:

- On-chip refresh controller
- Autonomous refresh scheduling
- SRAM-like asynchronous interface
- Internally managed timing margins

### High-level structure

- DRAM cell array (unchanged)
- Internal refresh FSM
- Refresh suppression during active access
- Refresh stretching during standby

📌 From the system’s viewpoint, PSRAM behaved like **slow SRAM**.  
📌 From the silicon’s viewpoint, it was **DRAM under new stress conditions**.

---

## 📊 Target Operating Numbers (Typical, circa 2001)

> ⚠️ The following values are **design targets / typical guarantees**,  
> not proprietary specifications.

### 🌡 Temperature

- Guaranteed operation: **−25 °C to +90 °C**
- Retention-critical regime: **≥ 80 °C**

---

### 🔋 Standby Current (Mobile Focus)

| Mode | Typical Target |
|---|---|
| Deep standby | **≤ 10–30 µA** |
| Light standby | **≤ 50–100 µA** |
| Active access | Comparable to DRAM burst |

📌 For comparison:  
Standard DRAM standby at HT often exceeded **100–200 µA**.

---

### ⏱ Refresh Behavior

| Parameter | Typical Value |
|---|---|
| Nominal DRAM refresh | ~64 ms |
| PSRAM effective pause | **100–300 ms** |
| Worst-case standby pause | **> 500 ms (system-dependent)** |

📌 These extended pause intervals were **architectural**,  
not process-driven.

---

## ⚠️ Architectural Consequences

The PSRAM architecture introduced **qualitatively new stress modes**:

### 1️⃣ Extended Retention Stress
- Cells remained unrefreshed far longer than DRAM assumptions
- Marginal cells crossed retention limits at HT

### 2️⃣ Accumulated Disturb
- Repeated access to active rows
- Neighbor rows left idle for extended periods
- Disturb effects integrated over time

### 3️⃣ Temperature-Leakage Amplification
- Junction leakage increased exponentially near 90 °C
- Pause + HT formed the **worst possible corner**

📌 These conditions directly surfaced  
**Pause Refresh** and **Disturb Refresh** failures.

---

## ⚖️ Architectural Trade-offs

| Aspect | Benefit | Cost |
|---|---|---|
| DRAM reuse | Fast development, low NRE | Inherited leakage physics |
| Internal refresh | Simple system design | Long pause stress |
| Extended standby | Low average power | HT retention exposure |
| Mobile focus | Market differentiation | Narrow reliability margin |

This was not a design mistake —  
it was a **deliberate trade-off under market pressure**.

---

## 🧠 Key Insight (Legacy Lesson)

> **Architecture can amplify latent physical weaknesses**  
> even when the base process and cell design remain unchanged.

PSRAM demonstrated that:

- Reliability limits can shift **without scaling**
- Usage patterns can dominate physics
- System-level goals can invalidate wafer-level assumptions

📘 This insight later generalized to:
- SoC power gating
- Always-on domains
- AI accelerators with extreme duty cycling

---

## 🔗 Related Documents

- [`pause_disturb_psram.md`](./pause_disturb_psram.md)
- [`yield_recovery.md`](./yield_recovery.md)

---

