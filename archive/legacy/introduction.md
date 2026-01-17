---
layout: default
title: Introduction
---

# 🧭 Introduction

**Legacy Technology** is not an archive of obsolete techniques.

It is a collection of **canonical failure-and-recovery cases**
from an era when semiconductor devices were still
**directly constrained by physical limits** —
before those limits were routinely abstracted away
by software, firmware, or system-level mitigation.

These cases document moments when
process integration, cell structure, and device physics
**directly dictated yield, reliability, and business decisions**.

They are preserved here not as nostalgia,
but as **structural references** —
patterns of causality that continue to reappear
in modern semiconductor systems, SoCs,
and AI-integrated architectures.

---

## 🕰 Historical Context

Until the mid-1990s, Japan was the global leader in DRAM technology.

Multiple Japanese manufacturers simultaneously operated
world-class DRAM **development and mass production**,
with competition centered on:

- Cell stability
- Retention margin
- Long-term reliability

—not only on density or cost.

During this period, DRAM cell design was treated as
an inherently **analog, physical problem**.

### Design assumptions of the era

- Cell capacitance was secured by **structure**, not by statistical assumption
- Time-dependent failures were considered **unacceptable anomalies**
- Market behavior was assumed to stress devices
  in **unpredictable and adversarial ways**

This design culture produced exceptionally robust memories,
but it rested on a strict premise:

> **Physical margins must not be violated.**

---

## ⚠️ The Turning Point  
*(Late 1990s – Early 2000s)*

As scaling progressed into the **0.25 µm generation and beyond**,
this premise began to collapse.

### What changed

| Aspect | Reality |
|---|---|
| Cell capacitance | Margins collapsed structurally |
| Leakage & disturb | Became unavoidable, not incidental |
| Retention | Shifted from anomaly to dominant limiter |
| Market pressure | Speed and cost outweighed physical certainty |

At the same time, DRAM pricing entered a prolonged collapse,
forcing manufacturers into **aggressive ramp decisions**
before failure mechanisms were fully understood.

Failures such as **Pause**, **Disturb**, and **Retention loss**
were no longer hypothetical.

They emerged in **real products**,  
in **real systems**,  
under **real user behavior**.

---

## 🔍 Why These Cases Matter Now

The technologies documented here are more than **20 years old**.

The **failure structures are not**.

Modern systems increasingly repeat the same pattern:

- Device-level limits are masked by system-level compensation
- Reliability risks are deferred to firmware or software
- Physical uncertainty is absorbed into business decisions

Only the **scale, vocabulary, and abstraction layer** have changed.

📌 The underlying causality remains the same.

---

## 🎯 Scope of This Archive

This archive focuses on the intersection of
**physics, manufacturability, and decision-making**.

- 🏗 Semiconductor process integration (1990s–early 2000s)
- 💾 DRAM and pseudo-SRAM memory technologies
- ⚛️ Physical failure mechanisms  
  (leakage, disturb, retention)
- 📈 Yield recovery under severe constraints
- 🧠 Engineering decisions made under business pressure

It deliberately avoids:

- Proprietary process recipes
- Confidential design rules
- Operational know-how applicable to modern fabs

---

## 🧭 How to Read This Archive

Each case is structured as a **causal chain**:

1. **Process / Structure**  
2. **Observed Failure Mode**  
3. **Physical Root Cause**  
4. **Test / Bin Manifestation**  
5. **Yield Recovery or Strategic Decision**

This order reflects how problems were
**actually encountered and solved in manufacturing** —
not how they are explained after the fact.

---

## 🧱 Positioning

Legacy Technology exists because

> **Physical reality does not disappear when technology advances.**

It only becomes easier to ignore.

This archive preserves the moments
when ignoring physics was no longer possible.
