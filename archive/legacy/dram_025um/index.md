---
title: "VSRAM (Pseudo-SRAM) 2001 — Mobile Memory Case"
layout: default
---

# 0.25µm 64M DRAM (3rd Generation)

This directory documents a **0.25µm-generation 64M DRAM**
brought up and mass-produced in the late 1990s.

This case is preserved as a **canonical example** where
process integration, device physics, wafer test strategy,
and yield recovery were tightly coupled.

It represents one of the final DRAM generations
before deep-submicron scaling fundamentally changed
failure mechanisms and business structures.

---

## Why This Case Matters

This generation exposed several structural constraints:

- Leakage-dominated retention behavior
- Plasma-induced junction damage
- Pause / Disturb refresh failures at high temperature
- Tight coupling between process margin and test binning

Many modern technologies reproduce the **same causal structure**
under different names and scales.

---

## Contents

- **Process Integration**
  - [`process_flow.md`](./process_flow.md)  
    → Full reconstructed 0.25µm DRAM process flow

- **Wafer Test & Bin Classification**
  - [`wafer_test_bin.md`](./wafer_test_bin.md)  
    → Fail-stop binning, Pause / Disturb definition

- **Failure Physics**
  - [`pause_disturb.md`](./pause_disturb.md)  
    → Retention, leakage, and disturb mechanisms

---

## How to Read This Case

Recommended order:

1. Process flow (what was built)
2. Wafer test bins (how failures appeared)
3. Failure physics (why it failed)
4. Yield recovery or strategic decision

This mirrors the **actual problem-solving flow**
in a manufacturing environment.
