---
layout: default
title: "PCB | Stack-up 層構成"
---

# 📐 PCB - Stack-up / 層構成  

---

## 📖 概要 / Overview
PCBの層構成は、信号品質・電源分配・熱設計に大きな影響を与えます。  
*Stack-up design strongly affects signal integrity, power distribution, and thermal design.*  

---

## 🔑 キートピック / Key Topics
- 層構成の基本 (Signal, Power, Ground)  
- 高速信号用の層分離  
- 電源/グラウンドプレーンの最適化  
- 熱拡散設計  

---

## 📊 図解 / Diagram
```mermaid
graph TD
  A[Top Layer] --> B[Ground Plane]
  B --> C[Signal Layer]
  C --> D[Power Plane]
  D --> E[Bottom Layer]
```

---

## ⬆️ Back to PCB
| Link | Badge |
|---|---|
| 🌐 Back to PCB Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-PCB-green?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 Back to PCB Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-PCB-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |
