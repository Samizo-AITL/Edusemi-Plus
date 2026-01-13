---
title: "Pause / Disturb Failures in VSRAM"
layout: default
---

# Pause / Disturb Failures in VSRAM

This document describes how **Pause** and **Disturb** failures
manifested differently in **VSRAM** compared to standard DRAM.

---

## Pause Failure in VSRAM

### Difference from DRAM

- Much longer effective pause time
- System-level standby directly mapped to cell stress

### Root Cause

- Junction leakage (temperature-accelerated)
- Inherited plasma damage from DRAM process
- Insufficient recovery margin under mobile usage

---

## Disturb Failure in VSRAM

### Difference from DRAM

- Repeated access patterns from application behavior
- Disturb accumulated during normal operation

### Root Cause

- Short-channel effects
- Word-line coupling
- Elevated Ioff at 90 °C

---

## Combined Stress Effect

Pause and Disturb were no longer independent:

- Long pause weakened cells
- Disturb accelerated failure during wake-up

This coupling was **system-visible**, not just test-visible.

---

## Key Insight

VSRAM showed that:
> **Usage model is part of the failure mechanism.**

This realization marked a shift from
process-centric to **system-aware reliability thinking**.
