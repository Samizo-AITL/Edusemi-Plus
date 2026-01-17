---
title: "Pause / Disturb Failures in PSRAM"
layout: default
---

# ⏸🔁 Pause / Disturb Failures in PSRAM

This document describes how **Pause** and **Disturb** failures
manifested in **PSRAM**, and why **Disturb-related degradation**
became a dominant reliability concern under extended operating conditions.

---

## 🧠 Background: PSRAM Operating Characteristics

Compared to conventional DRAM, PSRAM exhibited:

- Internally managed refresh with **limited charge recovery margin**
- Long effective pause time during system standby
- High-frequency access patterns during active operation

As a result, **cell stress accumulated under real usage conditions**,
not only during explicit wafer-level test modes.

---

## ⏸ Pause Stress in PSRAM

### Characteristics

- Long standby periods mapped directly to intrinsic retention stress
- Junction leakage accelerated at elevated temperature
- Residual plasma damage inherited from DRAM-era process flow

Pause stress weakened marginal cells,
but **pause alone could not fully explain field failures**.

---

## 🔁 Disturb Stress as a Dominant Failure Accelerator

### Usage-Driven Disturb

In PSRAM, disturb stress accumulated during **normal operation**:

- Repeated word-line activation driven by application behavior
- No explicit disturb test required
- Failures emerged **after resume from standby**

📌 Disturb was no longer a *test condition*  
→ it became a **usage condition**.

---

## ⚛️ Device-Level Origin of Disturb Degradation

<p align="center">
  <img
    src="https://samizo-aitl.github.io/Edusemi-Plus/archive/legacy/figs/disturb.png"
    width="50%">
</p>

<p align="center">
  <em>
    Fig. Device-level leakage paths and disturb mechanisms
    observed in PSRAM cell structures
  </em>
</p>

Disturb stress caused:

- Increased **cell transistor subthreshold leakage**
- Enhanced **n⁺ / p⁻ junction leakage**
- Leakage across **isolation regions**
- Progressive charge loss from storage nodes

These effects were minor in standard DRAM operation,
but became critical under PSRAM usage.

---

## 🌡 Temperature Expansion Impact

PSRAM required an expanded operating guarantee:

- Conventional DRAM limit: **80 °C**
- PSRAM requirement: **90 °C**

At elevated temperature:

- Junction leakage increased exponentially
- Transistor Ioff rose sharply
- Isolation leakage between adjacent cells increased
- Disturb-induced charge loss became observable

📌 **Internal refresh alone was insufficient**
to compensate for combined pause + disturb stress.

---

## 📈 Temperature vs Fail Bit Count (Conceptual)

The following ASCII plot illustrates the **typical trend**
observed in PSRAM under Pause / Disturb stress.

> ⚠️ Values are **representative order-of-magnitude examples**,  
> intended to show *trend*, not exact measurement.

```

Fail Bit Count (conceptual)

25℃   | 0
50℃   | 0
80℃*  | 0        ← Mass-production guaranteed limit
85℃   | *****    ← Disturb-assisted failures appear
90℃   | ************************************

```

### Interpretation

| Temperature | Behavior |
|---|---|
| ≤ 60 °C | Fail bits mostly suppressed |
| ~70 °C | Marginal cells begin to appear |
| ~80 °C | Rapid population growth |
| 85–90 °C | Disturb-assisted failures dominate |

📌 **Key point:**  
Fail population growth was **continuous**, not step-like —  
a signature of **leakage- and disturb-driven degradation**.

---

## 🔗 Combined Effect: Pause × Disturb Coupling

Pause and disturb interacted **multiplicatively**:

- Pause stress weakened cells via leakage
- Subsequent disturb accesses accelerated charge loss
- Failures became **system-visible**, not just test-visible

This explains **intermittent errors after wake-up**
from standby in mobile usage.

---

## 🛠 Countermeasures Implemented

Effective mitigation required **process + design co-optimization**.

### Plasma Damage Reduction
- Plasma condition softening
- Ashing damage suppression
- Junction defect density reduction

### Bias Engineering
- Back-bias adjustment: **−1 V → −3 V**
- Improved suppression of subthreshold leakage

### Device & Layout Optimization
- Memory cell transistor **Vth increase**
- Gate length **center-value management**
- CD shrink variability reduction
- Enhanced isolation robustness

These measures reduced both
pause-induced leakage and disturb sensitivity.

---

## 🧠 Key Insight (Legacy)

> **Disturb failures are not test artifacts —  
> they are consequences of real usage and operating conditions.**

PSRAM forced a shift from:
- Process-only reliability thinking  
to:
- **System-aware, usage-driven reliability design**

This lesson directly influenced later
always-on domains and low-power SoC architectures.

---

