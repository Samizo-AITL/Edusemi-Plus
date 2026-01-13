---
title: "0.25µm 64M DRAM Process Flow (Reconstructed)"
layout: default
---

# 0.25µm 64M DRAM Process Flow (Reconstructed)

This document provides a **reconstructed, end-to-end process flow**
for a **0.25µm-generation 64M DRAM**, covering both **cell** and **peripheral** regions.

> ⚠️ Note  
> This flow is reconstructed from manufacturing experience and period knowledge.
> It is intended for **educational and archival reference**, not as a foundry recipe.

---

## Scope

- Technology node: **0.25µm (KrF generation)**
- Device type: **64M DRAM**
- Coverage:
  - Cell array
  - Peripheral CMOS
  - Integration points critical to retention and disturb behavior

---

## High-Level Flow Overview

1. Isolation & well formation  
2. Gate stack and word-line formation  
3. LDD / spacer / deep S/D formation  
4. Bit-line formation  
5. Capacitor formation (stacked, ONO dielectric)  
6. Interlayer dielectric & contacts  
7. Metal interconnects and passivation  

Each block below highlights **why it mattered**, not just *what was done*.

---

## 1. Isolation & Well Formation

- LOCOS-based isolation with pre-oxide and sacrificial oxidation
- Triple-well structure adopted in cell region
- Purpose:
  - Suppress substrate noise
  - Improve soft-error and retention margin

**Key sensitivity:**  
Early surface condition strongly affected later **junction leakage**.

---

## 2. Gate Stack & Word Line (WSA)

- Thin gate oxide (~80 Å class)
- Poly-Si + WSi word-line stack
- KrF lithography at critical CD

**Key sensitivity:**  
Plasma exposure during gate etch directly influenced
**junction damage and retention failures** observed later.

---

## 3. Source / Drain Formation

- Separate optimization for:
  - Cell NMOS
  - Peripheral NMOS / PMOS
- LDD + spacer + deep S/D sequence

**Key sensitivity:**  
Excessive plasma or HF cleaning amplified **junction leakage**.

---

## 4. Bit Line Formation (WSB)

- Simultaneous bit-line and contact formation
- WSi-based low-resistance interconnect

**Key sensitivity:**  
Overlay and contact integrity affected early functional yield.

---

## 5. Capacitor Formation

- Stacked capacitor structure
- Surface roughening for capacitance boost (≈1.5–1.8×)
- ONO dielectric

**Key sensitivity:**  
Capacitance itself was sufficient;
**retention failures were leakage-dominated**, not C-limited.

---

## 6. Interlayer Dielectric & Contacts

- BPSG deposition and reflow
- Tungsten plug without CMP (etch-back approach)

**Key sensitivity:**  
Contact leakage and interface damage directly mapped to
Pause Refresh failures at high temperature.

---

## 7. Metal & Passivation

- Dual-layer Al-based interconnect
- Final hydrogen sinter for leakage suppression

---

## Summary

This process flow shows how **seemingly local process choices**
(plasma steps, cleaning strategy, junction handling)
propagated upward into:

- Wafer test binning
- Retention / disturb behavior
- Yield and product decisions

---

## Related Documents

- [`wafer_test_bin.md`](./wafer_test_bin.md)
- [`pause_disturb.md`](./pause_disturb.md)
