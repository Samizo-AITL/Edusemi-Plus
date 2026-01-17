---
title: "PSRAM Architecture and Concept"
layout: default
---

# PSRAM Architecture and Concept

PSRAM (Pseudo-SRAM) is a **DRAM-based memory**
that emulates SRAM behavior by integrating
**internal refresh control logic**.

---

## Motivation

- SRAM: fast but large cell area and high cost
- DRAM: dense but requires external refresh

PSRAM aimed to:
- Retain DRAM density
- Hide refresh from the system
- Reduce mobile standby power

---

## Core Concept

- Standard DRAM cell array
- On-chip refresh controller
- Extended refresh interval
- SRAM-like interface to the system

---

## Architectural Consequence

This approach introduced **new stress conditions**:

- Cells remained unrefreshed for longer periods
- Disturb accumulated during active access
- High-temperature operation amplified leakage

These conditions directly surfaced **Pause / Disturb failures**.

---

## Architectural Trade-off

| Aspect | Benefit | Cost |
|------|--------|------|
| DRAM reuse | Fast development | Inherited leakage |
| Internal refresh | System simplicity | Long pause stress |
| Mobile focus | Low power | 90 °C reliability |

---

## Key Insight

PSRAM demonstrated that:
> **Architecture can amplify latent physical weaknesses**  
> even when the base process is unchanged.

This insight later generalized to SoC and AI accelerators.
