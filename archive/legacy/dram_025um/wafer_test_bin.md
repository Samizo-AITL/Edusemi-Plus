---
title: "0.25µm DRAM Wafer Test & Bin Classification"
layout: default
---

# 0.25µm DRAM Wafer Test & Bin Classification

This document summarizes the **wafer test bin classification**
used for **0.25µm-generation DRAM**, based on a **fail-stop test strategy**.

---

## Test Philosophy: Fail-Stop

Tests are executed in order of **severity**:

1. Fatal DC defects first  
2. Functional correctness  
3. Retention-related behavior  
4. Margin checks  

This ensures rapid yield visibility and efficient screening.

---

## Bin Classification Overview

| Bin | Category | Description |
|----:|----------|-------------|
| 1 | Open / Short | Catastrophic wiring or bridging defects |
| 2 | Standby Idd | Excessive leakage in standby |
| 3 | Active Idd | Abnormal current during operation |
| 4 | Function | Read/write or decode failures |
| 5 | Pause Refresh | Retention failure without refresh |
| 6 | Disturb Refresh | Retention loss due to neighbor access |
| 7 | Margin | Voltage / timing margin insufficiency |

---

## Bin5: Pause Refresh Fail

**Purpose:**  
Evaluate intrinsic cell retention.

**Typical method:**
1. Write known pattern
2. Pause refresh for defined time
3. Read and count bit errors

**Characteristics:**
- Strong temperature dependence
- Dominated by **junction leakage**
- Highly sensitive to plasma damage history

---

## Bin6: Disturb Refresh Fail

**Purpose:**  
Detect interference from aggressive neighbor access.

**Typical method:**
1. Hold victim row
2. Repeatedly toggle adjacent rows
3. Read victim row

**Characteristics:**
- Short-channel effects
- Word-line coupling
- Exacerbated at high temperature

---

## Temperature Strategy

- RT (~25 °C): initial screening
- HT (80–90 °C): **most critical for retention**
- LT (≈ −25 °C): timing margin verification

---

## Interpretation

Wafer test bins are not merely pass/fail labels.
They act as a **projection of physical failure mechanisms**
into a manufacturable decision space.

---

## Related Documents

- [`process_flow.md`](./process_flow.md)
- [`pause_disturb.md`](./pause_disturb.md)
