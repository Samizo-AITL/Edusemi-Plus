---
title: "Yield Recovery and Countermeasures in PSRAM"
layout: default
---

# 📈 Yield Recovery and Countermeasures in PSRAM

---

## 🧠 Background

PSRAM was developed in **2001** by reusing a **0.25 µm DRAM base process**
to address the emerging **mobile phone market**, which demanded:

- 🔋 **Low standby power**
- ⏱ **Long effective refresh intervals**
- 🌡 **Guaranteed high-temperature operation up to 90 °C**

To secure early market entry—most notably for the **world’s first
camera-equipped mobile phones**—mass production was launched
despite an **extremely low initial yield of ~30%**.

Yield recovery therefore had to be executed **in parallel with
volume production**, under intense **schedule and business pressure**.

At the same time, the company’s long-term strategy was already
shifting toward **LCD driver ICs** and **high-voltage mixed CMOS**,
placing strict limits on:

- Available investment
- Dedicated manpower
- Long-term memory-specific process evolution

---

## 🚧 Constraints

| Category | Constraint |
|---|---|
| Process | No major redesign allowed (DRAM base fixed) |
| Schedule | Extremely short recovery timeline |
| Business | Market entry prioritized over yield maturity |
| Reliability | **90 °C guaranteed operation required** |
| Strategy | Limited long-term commitment to memory |

These constraints defined the **solution space** for yield recovery.

---

## ⚠️ Dominant Failure Modes

Two DRAM-derived failure modes became critical under
**mobile operating conditions**.

### ⏸ Pause Refresh Fail

- Retention failure during long refresh pauses
- Strong temperature dependence
- Root cause: **junction leakage increase (I<sub>junc</sub>)**

---

### 🔁 Disturb Refresh Fail

- Bit flipping induced by adjacent word-line activity
- Strong correlation with **short-channel effects (SCE)** and transistor I<sub>off</sub>
- Strongly aggravated at high temperature and extended refresh intervals

📌 Both modes were **minor or latent** in conventional DRAM,
but were **amplified by mobile usage and temperature requirements**.

---

## ⚛️ Physical Root Causes

### ⏸ Pause Failure Mechanism

Cell retention time is governed by:

$$
\tau = \frac{C_{cell} \cdot V_{cell}}{I_{leak}}
$$

| Parameter | Status |
|---|---|
| C<sub>cell</sub> | Met design target |
| V<sub>cell</sub> | Met operating spec |
| Capacitor integrity | Confirmed |
| Dominant limiter | **Junction leakage (I<sub>leak</sub>)** |

Leakage current increased **exponentially with temperature**,
indicating **process-induced junction damage**.

Root cause analysis linked this behavior to
**accumulated plasma exposure** in the DRAM process flow.

---

### 🔁 Disturb Failure Mechanism

Observed characteristics:

- Failures aligned along specific word-line directions
- Devices with shorter effective channel length showed higher I<sub>off</sub>
- Elevated temperature further worsened short-channel behavior

📌 This identified **critical CD control of cell transistors**
as essential for suppressing disturb failures.

---

## 🛠 Yield Recovery Countermeasures

Yield recovery required **multi-layer optimization**
without stopping mass production.

---

### ⚙️ Process-Side Measures

| Measure | Intent |
|---|---|
| Plasma exposure elimination | Reduce junction defect density |
| O₂ plasma → wet stripping | Suppress plasma-induced damage |
| HF clean count minimization | Preserve gate oxide integrity |
| Contact damage suppression | Reduce leakage paths |

🎯 Focus: **remove physical damage**, not mask symptoms.

---

### 🧱 Device-Side Measures

| Measure | Effect |
|---|---|
| Back-bias (−1 V → −3 V) | Reduced junction leakage, higher effective V<sub>th</sub> |
| Critical CD tightening | Suppressed SCE-induced disturb |
| Channel length margin enforcement | Stabilized I<sub>off</sub> |

---

### 🔄 Operation-Side Measures

- Refresh parameters redefined based on **measured leakage behavior**
- Stress and screening conditions recalibrated
  to reflect **actual mobile temperature profiles**

📌 All measures were executed through **cross-functional coordination**
between process, device, and manufacturing teams.

---

## ✅ Result

| Metric | Outcome |
|---|---|
| Initial yield | ~30% |
| Recovered yield | **Stable 80% class** |
| Reliability | Pause / Disturb largely suppressed |
| Production | Continuous, no line stop |
| Market impact | Enabled early mobile camera phones |

From a **purely technical standpoint**, the yield recovery
was successful and met immediate market needs.

---

## 🧭 Strategic Outcome

Despite technical recovery:

- Reliable operation beyond **90 °C** could not be guaranteed
- Junction leakage scaled unfavorably with further node shrink
- DRAM-derived memory showed **structural thermal limits**

Evaluation of a **0.18 µm trench DRAM** confirmed that
high-temperature leakage was **structural**, not incidental.

At the same time, corporate strategy had converged on:

- 📺 **LCD driver ICs**
- ⚡ **High-voltage mixed CMOS**

Sustaining mobile memory would have required:

- Continuous, large-scale memory-specific investment
- Dedicated long-term manpower

— commitments incompatible with this strategic direction.

As a result, **DRAM-derived mobile memory development was
strategically terminated**, and resources were reallocated to
logic-oriented and mixed-signal products where existing
process assets could be leveraged more effectively.

---

## 🧠 Legacy Insight

PSRAM represents a rare but instructive case:

> **Yield can be recovered, and reliability targets can be met,  
> yet architectural scalability and business sustainability  
> may still fail.**

This case demonstrates that:

- Engineering success ≠ long-term success
- Recognizing structural limits is a form of expertise
- **Timely withdrawal can itself be a successful decision**

📘 *PSRAM stands as a textbook example of  
technology pushed to its rational boundary.*
