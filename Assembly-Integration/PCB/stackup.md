---
layout: default
title: "PCB Stack-up | プリント基板の層構成"
---

---

# 📐 PCB Stack-up / プリント基板の層構成

---

## 🏗 概要 / Overview

プリント基板の層構成（スタックアップ）は、信号品質・電源安定性・製造コストに直結する重要要素です。  
*PCB stack-up is a critical factor that directly impacts signal integrity, power stability, and manufacturing cost.*

適切な層構成により、インピーダンス制御・クロストーク低減・熱拡散を実現できます。  
*A well-designed stack-up enables impedance control, crosstalk reduction, and thermal dissipation.*

---

## 🔑 キートピック / Key Topics

- 信号層・電源層・グラウンド層の配置バランス  
  *Balancing placement of signal, power, and ground layers*  
- 4層・6層・8層基板における代表的なスタックアップ例  
  *Typical stack-up examples for 4-layer, 6-layer, and 8-layer boards*  
- 高速伝送向けの差動ペア層設計  
  *Differential pair layer design for high-speed transmission*  
- 製造性とコストの最適化  
  *Optimization for manufacturability and cost*  

---

## 📊 スタックアップ例 / Example Stack-ups

| 層数 / Layer Count | 構成例 / Example Configuration |
|--------------------|--------------------------------|
| **4層基板 / 4-Layer PCB** | Signal – GND – Power – Signal |
| **6層基板 / 6-Layer PCB** | Signal – GND – Signal – Signal – Power – Signal |
| **8層基板 / 8-Layer PCB** | Signal – GND – Signal – Power – Power – Signal – GND – Signal |

---

## ✅ 学習目標 / Learning Goals

- PCBスタックアップの基本設計指針を理解する。  
  *Understand the fundamental design guidelines of PCB stack-up.*  
- インピーダンス制御やSI設計に直結する層構成を把握する。  
  *Learn how stack-up affects impedance control and signal integrity.*  
- 製造性とコストを考慮した層設計を行えるようになる。  
  *Gain ability to design layer structures considering manufacturability and cost.*  

---

## 🔗 関連リンク / Related Links

- [📖 Impedance Control](./impedance-control.md)  
- [📖 Via Design](./via-design.md)  
- [📖 Materials](./materials.md)

---

## ⬆️ Back to PCB

[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
