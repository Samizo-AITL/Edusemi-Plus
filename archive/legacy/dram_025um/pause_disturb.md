---
title: "Pause / Disturb Refresh Failure Physics"
layout: default
---

# Pause / Disturb Refresh Failure Physics

This document explains the **physical mechanisms**
behind **Pause Refresh** and **Disturb Refresh** failures
observed in **0.25µm-generation DRAM**.

---

## Pause Refresh Failure

### Definition
Loss of stored charge when refresh is suspended.

### Dominant Mechanism
- **Junction leakage current**
- Thermally activated
- Exponentially increases with temperature

### Key Contributors
- Plasma-induced junction damage
- Excessive interface states
- Aggressive cleaning / ashing steps

> Capacitor capacitance was generally sufficient;  
> **leakage, not Ccell, dominated retention loss.**

---

## Device Structure Reference

<p align="center">
  <img
    src="https://samizo-aitl.github.io/Edusemi-Plus/archive/legacy/figs/pause_lakage.png"
    width="80%">
</p>

<p align="center">
  <em>
    Fig. Physical origin of Pause refresh failures
    in 0.25µm-generation DRAM
  </em>
</p>

---

## Disturb Refresh Failure

### Definition
Retention loss caused by repeated activation of neighboring rows.

### Dominant Mechanism
- Short-channel effects
- Subthreshold leakage (Ioff)
- Word-line coupling

### Key Contributors
- CD shrink variability
- Back-bias sensitivity
- Elevated temperature operation

---

## Structural Comparison

| Aspect | Pause | Disturb |
|------|-------|---------|
| Trigger | Time | Neighbor access |
| Root cause | Junction leakage | Short-channel / coupling |
| Temp sensitivity | Very high | High |
| Process sensitivity | Plasma / interface | CD / doping |

---

## Why These Failures Matter

Pause and Disturb failures revealed that:

- Reliability was **process-history dependent**
- Test strategy had to reflect physical reality
- Yield improvement required **damage avoidance**, not tuning alone

These insights directly influenced later decisions,
including **VSRAM evolution** and eventual **technology pivot**.

---

## Related Documents

- [`process_flow.md`](./process_flow.md)
- [`wafer_test_bin.md`](./wafer_test_bin.md)
