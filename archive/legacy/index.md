---
layout: default
title: Legacy Technology
---

# 🧭 Legacy Technology

**Legacy Technology** is not a collection of obsolete processes.

This archive documents **canonical failure-and-recovery cases**
in which **physical mechanisms directly constrained**
yield, reliability, and ultimately **business decisions**.

These cases are preserved not as nostalgia,
but as **reference structures**—patterns of causality
that continue to reappear in modern semiconductor systems,
SoCs, and AI-integrated architectures.

---

## 🔗 Links

| Language | GitHub Pages 🌐 | GitHub 💻 |
|----------|----------------|-----------|
| 🇺🇸 English | [![GitHub Pages EN](https://img.shields.io/badge/GitHub%20Pages-English-brightgreen?logo=github)](https://samizo-aitl.github.io/Edusemi-Plus/archive/legacy) | [![GitHub Repo EN](https://img.shields.io/badge/GitHub-English-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/archive/legacy) |

---

## 🔐 Note on Confidentiality

> **All materials in this archive are based on semiconductor technologies  
> developed more than 20 years ago (late 1990s–early 2000s).**
>
> This archive **does not contain**:
> - Proprietary process recipes  
> - Confidential design rules  
> - Equipment tuning parameters  
> - Operational know-how applicable to current manufacturing
>
> The purpose is to preserve  
> **structural patterns of failure, recovery, and decision-making**,  
> not implementation-level secrets.

This archive is intended for **education, analysis, and architectural reference**.

---

## 📘 Introduction

The philosophy and positioning of *Legacy Technology*
are explained in detail here:

→ **[Introduction — Legacy Technology](./introduction.md)**

---

## 🎯 Scope of This Archive

This archive focuses on the intersection of
**process physics, manufacturability, and strategic decision-making**.

- 🏗 **Semiconductor process integration** (1990s–2000s)
- 💾 **Memory technologies** (DRAM, PSRAM, eDRAM)
- ⚛️ **Failure physics** (leakage, disturb, retention)
- 📈 **Yield recovery under constraints**
- 🧠 **Engineering decisions under business pressure**

The emphasis is on **causal structure**, not historical completeness.

---

## 🧭 How to Read This Archive

Each case is organized as a **causal chain**:

1. **Process / Structure**  
2. **Observed Failure Mode**  
3. **Physical Root Cause**  
4. **Test / Bin Manifestation**  
5. **Yield Recovery or Strategic Decision**

This order mirrors **actual manufacturing problem-solving**,
not post-hoc academic explanation.

📌 Readers are encouraged to follow the chain,
not jump directly to conclusions.

---

## 📂 Case Index

### 💾 DRAM (0.25µm, 64M) — 3rd Generation

A canonical baseline case exposing
retention, leakage, and test–yield coupling
before deep-submicron scaling.

- **Case overview**  
  → [`dram_025um/`](./dram_025um/)
- **Process integration**  
  → [`dram_025um/process_flow.md`](./dram_025um/process_flow.md)
- **Wafer test & bin classification**  
  → [`dram_025um/wafer_test_bin.md`](./dram_025um/wafer_test_bin.md)
- **Failure physics (Pause / Disturb)**  
  → [`dram_025um/pause.md`](./dram_025um/pause.md)

---

### 📱 PSRAM (Pseudo-SRAM, 2001) — Mobile Memory

A boundary case where DRAM technology
was pushed beyond its original operating envelope
to meet mobile requirements.

- **Case overview**  
  → [`psram_2001/`](./psram_2001/)
- **Architecture & concept**  
  → [`psram_2001/psram_architecture.md`](./psram_2001/psram_architecture.md)
- **Pause / Disturb under mobile usage**  
  → [`psram_2001/pause_disturb_psram.md`](./psram_2001/pause_disturb_psram.md)
- **Yield recovery & countermeasures**  
  → [`psram_2001/yield_recovery.md`](./psram_2001/yield_recovery.md)

---

## 🧱 Positioning

Legacy Technology cases are archived here
**because they expose structural limits**—not because they are old.

Modern systems often fail for the **same reasons**:
only the scale, terminology, and integration context change.

📌 Understanding these patterns
is essential for designing **robust modern systems**.

---

## Author

| 📌 Item | Details |
|--------|---------|
| **Name** | Shinichi Samizo |
| **Expertise** | Semiconductor devices (logic, memory, high-voltage mixed-signal)<br>Thin-film piezo actuators for inkjet systems<br>PrecisionCore printhead productization, BOM management, ISO training |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |

---

## License

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](https://samizo-aitl.github.io/Edusemi-Plus/archive/legacy/#---license)

| 📌 Item | License | Description |
|--------|---------|-------------|
| **Source Code** | [**MIT License**](https://opensource.org/licenses/MIT) | Free to use, modify, and redistribute |
| **Text Materials** | [**CC BY 4.0**](https://creativecommons.org/licenses/by/4.0/) or [**CC BY-SA 4.0**](https://creativecommons.org/licenses/by-sa/4.0/) | Attribution required; share-alike applies for BY-SA |
| **Figures & Diagrams** | [**CC BY-NC 4.0**](https://creativecommons.org/licenses/by-nc/4.0/) | Non-commercial use only |
| **External References** | Follow the original license | Cite the original source properly |
