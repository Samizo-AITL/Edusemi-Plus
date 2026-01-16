---
title: Introduction
---

# Introduction

Legacy Technology is not an archive of obsolete techniques.

It is a collection of **canonical failure-and-recovery cases** from an era
when semiconductor devices were still directly constrained by
**physical limits**, not abstracted away by software or system-level mitigation.

These cases document moments where
process integration, cell structure, and device physics
**directly dictated yield, reliability, and business decisions**.

They are preserved here not as nostalgia,
but as **structural references** that continue to reappear
in modern semiconductor, system, and AI-integrated designs.

---

## Historical Context

Until the mid-1990s, Japan was the global leader in DRAM technology.

Multiple Japanese manufacturers simultaneously operated
world-class DRAM development and mass production,
with competition centered on **cell stability, retention, and reliability**,
not only on density or cost.

During this period, DRAM cell design was treated as
an inherently **analog, physical problem**:

- Cell capacitance was secured by structure, not assumptions
- Time-dependent failures were considered unacceptable anomalies
- Market behavior was assumed to stress devices in unforeseen ways

This design culture produced highly robust memories,
but it was built on the premise that
**physical margins must not be violated**.

---

## The Turning Point (Late 1990s – Early 2000s)

As scaling progressed into the 0.25µm generation and beyond,
this assumption began to fail.

- Cell capacitance margins collapsed
- Leakage, disturb, and retention failures became structural
- Market pressure prioritized speed and cost over physical certainty

At the same time, DRAM pricing entered a prolonged collapse,
forcing manufacturers into aggressive ramp decisions
before failure mechanisms were fully understood.

Failures such as **Pause, Disturb, and Retention loss**
were no longer hypothetical —
they emerged in real products, real systems, and real user behavior.

---

## Why These Cases Matter Now

The technologies documented here are more than 20 years old.
However, the **failure structures are not**.

Modern systems repeat the same pattern:

- Device-level limits are masked by system-level compensation
- Reliability problems are deferred to firmware or software
- Physical uncertainty is absorbed into business decisions

Only the scale and terminology have changed.

---

## Scope of This Archive

This archive focuses on:

- Semiconductor process integration (1990s–early 2000s)
- DRAM and pseudo-SRAM memory technologies
- Physical failure mechanisms (leakage, disturb, retention)
- Yield recovery and decision-making under constraint

It deliberately avoids proprietary recipes, parameters,
or operational know-how applicable to current manufacturing.

---

## How to Read This Archive

Each case is structured as a causal chain:

1. **Process / Structure**
2. **Observed Failure Mode**
3. **Physical Root Cause**
4. **Test / Bin Manifestation**
5. **Yield Recovery or Strategic Decision**

This order reflects how problems were actually encountered and addressed
in manufacturing — not how they are explained afterward.

---

## Positioning

Legacy Technology exists because
**physical reality does not disappear when technology advances**.

It only becomes easier to ignore.

This archive preserves the moments
when ignoring physics was no longer possible.
