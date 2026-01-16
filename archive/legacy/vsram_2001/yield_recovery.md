---
title: "Yield Recovery and Countermeasures in VSRAM"
layout: default
---

# Yield Recovery and Countermeasures in VSRAM

## Background

VSRAM was developed in 2001 by reusing a 0.25 µm DRAM process
to address the emerging mobile phone market, which demanded
**low power consumption, long refresh intervals, and guaranteed
high-temperature operation up to 90 °C**.

To secure early market entry—most notably for the world's first
camera-equipped mobile phones—mass production was initiated
despite an **extremely low initial yield of approximately 30%**.
Yield recovery therefore had to be executed **in parallel with
volume production**, under severe schedule and business pressure
:contentReference[oaicite:1]{index=1}.

---

## Constraints

- No major process redesign allowed (DRAM base process fixed)
- Extremely short recovery timeline
- Mobile market timing prioritized over yield maturity
- 90 °C operation requirement (beyond standard DRAM spec)

---

## Dominant Failure Modes

Two DRAM-derived failure modes became critical under mobile
conditions:

### Pause Refresh Fail
- Retention failure during long refresh pauses
- Strong temperature dependence
- Root cause: **junction leakage increase (Ijunc)**

### Disturb Refresh Fail
- Bit flipping induced by adjacent word-line activity
- Strong correlation with **short-channel effects (SCE)** and Ioff
- Aggravated at high temperature and long refresh cycles

Both failure modes, previously marginal in standard DRAM,
were amplified by **high-temperature mobile operation**
:contentReference[oaicite:2]{index=2}.

---

## Physical Root Causes

### Pause Failure Mechanism

Cell retention time follows:

$$
\tau = \frac{C_{cell} V_{cell}}{I_{leak}}
$$

- Ccell and Vcell met design targets
- Storage capacitor integrity confirmed
- Dominant degradation factor: **junction leakage (Ileak)**

Leakage increased exponentially with temperature, pointing to
**plasma-induced junction damage** accumulated during DRAM
processing steps.

---

### Disturb Failure Mechanism

- Failures aligned along specific word-line directions
- Shorter channel devices showed higher Ioff
- High-temperature operation worsened SCE behavior

This identified **critical transistor CD control** as essential
for disturb suppression.

---

## Yield Recovery Countermeasures

### Process-Side Measures

- **Elimination of plasma exposure**
  - Replaced repeated O₂ plasma ashing with sulfuric wet stripping
- **HF clean count minimization**
  - Preserved gate oxide remnants after gate etch
  - Suppressed junction leakage paths at SN contacts

---

### Device-Side Measures

- **Back-bias strengthening**
  - Vbs increased from −1 V to −3 V
  - Reduced junction leakage and raised effective Vth
- **Critical CD tightening**
  - Enforced channel length margins
  - Suppressed short-channel induced disturb behavior

---

### Operation-Side Measures

- Refresh condition redefinition aligned with actual leakage behavior
- Stress conditions recalibrated for mobile temperature profiles

All measures were implemented through **cross-functional
coordination between process, device, and manufacturing teams**,
while production continued uninterrupted :contentReference[oaicite:3]{index=3}.

---

## Result

- Yield improved from **~30% to stable 80% class**
- Pause and Disturb failures were largely suppressed
- Enabled stable supply for early mobile camera phones
- Marked the culmination of DRAM-derived memory development
at Sakata Fab

---

## Strategic Outcome

Despite the technical recovery:

- Temperature margin beyond 90 °C could not be guaranteed
- Junction leakage scaled unfavorably with further node shrink
- DRAM-derived architectures showed **limited scalability**

Evaluation of a 0.18 µm trench-based DRAM process confirmed
that high-temperature leakage fundamentally constrained
future mobile deployment.

As a result, **DRAM-derived mobile memory development was
strategically terminated**, and resources were redirected toward
high-voltage mixed CMOS and logic-oriented products
:contentReference[oaicite:4]{index=4}.

---

## Legacy Insight

VSRAM represents a rare but critical lesson:

> **Yield can be recovered, reliability can be met,
> yet architectural scalability may still fail.**

It stands as a textbook case demonstrating that
**engineering success does not necessarily ensure
long-term strategic success**.
