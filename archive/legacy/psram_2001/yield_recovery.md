---
title: "Yield Recovery and Countermeasures in PSRAM"
layout: default
---

# Yield Recovery and Countermeasures in PSRAM

## Background

PSRAM was developed in 2001 by reusing a 0.25 µm DRAM process
to address the emerging mobile phone market, which demanded
**low power consumption, long refresh intervals, and guaranteed
high-temperature operation up to 90 °C**.

To secure early market entry—most notably for the world’s first
camera-equipped mobile phones—mass production was initiated
despite an **extremely low initial yield of approximately 30%**.
Yield recovery therefore had to be executed **in parallel with
volume production**, under severe schedule and business pressure.

This development took place in a context where the company’s
strategic focus was already shifting toward **LCD driver ICs
and high-voltage mixed CMOS**, placing strict limits on the level
of investment and manpower that could be allocated to
continued mobile memory development.

---

## Constraints

- No major process redesign allowed (DRAM base process fixed)
- Extremely short recovery timeline
- Market entry prioritized over yield maturity
- Guaranteed 90 °C operation required for mobile use
- Limited long-term investment capacity for memory-specific process evolution

---

## Dominant Failure Modes

Two DRAM-derived failure modes became critical under mobile
operating conditions:

### Pause Refresh Fail

- Retention failure during long refresh pauses
- Strong temperature dependence
- Root cause: **junction leakage increase (Ijunc)**

### Disturb Refresh Fail

- Bit flipping induced by adjacent word-line activity
- Strong correlation with **short-channel effects (SCE)** and transistor Ioff
- Significantly aggravated at high temperature and long refresh cycles

Both failure modes, previously marginal in conventional DRAM
applications, were amplified by **high-temperature mobile operation**.

---

## Physical Root Causes

### Pause Failure Mechanism

Cell retention time is governed by:

$$
\tau = \frac{C_{cell} V_{cell}}{I_{leak}}
$$

- Cell capacitance (Ccell) and operating voltage (Vcell) met design targets
- Storage capacitor integrity was confirmed
- Dominant degradation factor was **junction leakage current (Ileak)**

Experimental evaluation showed that leakage increased
exponentially with temperature, indicating **process-induced
junction damage**, strongly linked to accumulated plasma exposure
in the DRAM process flow.

---

### Disturb Failure Mechanism

- Failures appeared systematically along specific word-line directions
- Devices with shorter effective channel length exhibited higher Ioff
- Elevated temperature further worsened short-channel behavior

This identified **critical transistor CD control** as a necessary
condition for suppressing disturb-related failures.

---

## Yield Recovery Countermeasures

### Process-Side Measures

- **Elimination of plasma exposure**
  - Replaced repeated O₂ plasma ashing with sulfuric wet stripping
- **HF clean count minimization**
  - Preserved residual gate oxide after gate etch
  - Suppressed leakage paths at storage-node contacts

These measures directly targeted the physical origin of
junction leakage rather than masking its symptoms.

---

### Device-Side Measures

- **Back-bias strengthening**
  - Substrate bias increased from −1 V to −3 V
  - Junction leakage reduced and effective threshold voltage raised
- **Critical CD tightening**
  - Channel length margins enforced at the process level
  - Short-channel-induced disturb behavior suppressed

---

### Operation-Side Measures

- Refresh parameters redefined based on actual leakage behavior
- Stress conditions recalibrated to reflect mobile temperature profiles

All countermeasures were implemented through **cross-functional
coordination between process, device, and manufacturing teams**,
while mass production continued without interruption.

---

## Result

- Yield improved from **~30% to stable 80% class**
- Pause and Disturb failures were largely suppressed
- Enabled stable supply for early mobile camera phones
- Represented the technical culmination of DRAM-derived memory
  development at the Sakata Fab

From a purely technical standpoint, the yield recovery effort
was successful and met immediate market requirements.

---

## Strategic Outcome

Despite technical recovery:

- Temperature margin beyond 90 °C could not be guaranteed
- Junction leakage scaled unfavorably with further node shrink
- DRAM-derived architectures showed **inherent scalability limits**
  under mobile thermal conditions

Subsequent evaluation of a 0.18 µm trench-based DRAM process
confirmed that high-temperature leakage was **structural rather
than incidental**, eliminating a viable long-term path for
mobile memory scaling.

At the same time, corporate strategy had clearly converged on
**LCD driver ICs and high-voltage mixed CMOS** as the company’s
core semiconductor business. Sustaining mobile memory would
have required continuous, large-scale investment in
memory-specific process development and dedicated manpower—
a commitment incompatible with this strategic direction.

As a result, **DRAM-derived mobile memory development was
strategically terminated**, and resources were redirected toward
logic-oriented and mixed-signal products where existing process
assets could be leveraged more effectively.

---

## Legacy Insight

PSRAM represents a rare but instructive case in semiconductor
development:

> **Yield can be recovered, and reliability targets can be met,
> yet architectural scalability and business sustainability
> may still fail.**

It stands as a textbook example demonstrating that
**engineering success does not necessarily ensure
long-term strategic success**, and that timely, rational
reallocation of resources can itself be a form of success.
