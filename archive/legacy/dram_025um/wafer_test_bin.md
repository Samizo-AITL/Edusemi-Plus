---
title: "0.25µm DRAM Wafer Test & Bin Classification"
layout: default
---

# 🧾 0.25µm DRAM Wafer Test & Bin Classification

This document summarizes the **wafer test bin classification**
used for **0.25µm-generation DRAM**, based on a strict
**fail-stop test strategy**.

Rather than treating bins as simple pass/fail labels,
this classification system functioned as a
**projection layer**, mapping physical failure mechanisms
into **manufacturing and business decisions**.

---

## 🧠 Test Philosophy: Fail-Stop

Tests are executed sequentially in order of **severity and irreversibility**:

1. 💥 **Fatal DC defects**  
2. ⚙️ **Functional correctness**  
3. ⏱ **Retention-related behavior**  
4. 📉 **Voltage / timing margin checks**

### Why Fail-Stop?

- Early termination on fatal failures
- Fast yield visibility at wafer level
- Clear attribution of dominant failure modes

📌 This philosophy was essential for
**rapid yield learning** during ramp-up.

---

## 📊 Bin Classification Overview

| Bin | Category | Failure Meaning (Physical Perspective) |
|---:|---|---|
| 1 | Open / Short | Catastrophic wiring or bridging defects |
| 2 | Standby Idd | Excessive off-state leakage |
| 3 | Active Idd | Abnormal current during operation |
| 4 | Function | Read / write / decode failures |
| 5 | Pause Refresh | Intrinsic retention failure |
| 6 | Disturb Refresh | Access-induced retention loss |
| 7 | Margin | Voltage or timing margin insufficiency |

Each bin corresponds to a **distinct physical stress domain**.

---

## ⏸ Bin5 — Pause Refresh Fail

### 🎯 Purpose
Evaluate **intrinsic cell retention**
without refresh assistance.

### 🧪 Typical Test Method
1. Write a known data pattern  
2. Pause refresh for a defined interval  
3. Read out and count bit errors  

### 🔍 Observed Characteristics

| Aspect | Behavior |
|---|---|
| Temperature | Strongly HT-dependent |
| Dominant mechanism | **Junction leakage** |
| Process sensitivity | Plasma damage, surface condition |
| Spatial behavior | Often localized, tail-dominated |

📌 **Key insight:**  
Capacitance was sufficient —  
**leakage, not C, defined retention limits**.

---

## 🔁 Bin6 — Disturb Refresh Fail

### 🎯 Purpose
Detect **interference-induced retention loss**
caused by aggressive neighbor access.

### 🧪 Typical Test Method
1. Hold victim word line  
2. Repeatedly toggle adjacent rows  
3. Read victim row and evaluate errors  

### 🔍 Observed Characteristics

| Aspect | Behavior |
|---|---|
| Physical origin | WL coupling, short-channel effects |
| Temperature | Strong HT acceleration |
| Pattern dependence | High |
| Visibility | Often hidden at RT |

📌 **Key insight:**  
Disturb failures reveal **dynamic coupling effects**
not observable in static retention tests.

---

## 🌡 Temperature Strategy

| Temperature | Purpose |
|---|---|
| RT (~25 °C) | Initial functional screening |
| HT (80–90 °C) | **Primary retention & leakage discriminator** |
| LT (≈ −25 °C) | Timing and margin verification |

HT testing was the **decisive filter**
for Bin5 and Bin6 separation.

---

## 🧭 How to Interpret Bin Data

Wafer test bins should be read as:

> **Electrical symptoms of underlying physical damage**

not merely as quality labels.

| Layer | Role |
|---|---|
| Process | Introduces latent damage |
| Device physics | Amplifies damage under stress |
| Wafer test | Projects physics into bins |
| Business | Converts bins into yield decisions |

This projection structure is **technology-agnostic**
and reappears in advanced nodes under different names.

---

## 🧠 Legacy Insight

The Bin5 / Bin6 separation was one of the clearest examples where:

- Physics, not design intent, defined yield
- Test conditions *created visibility* of failure
- Small process shifts caused large business impact

📘 *Modern memories still follow the same structure —
only the vocabulary has changed.*

---

## 🔗 Related Documents

- [`process_flow.md`](./process_flow.md)
- [`pause.md`](./pause.md)

---

