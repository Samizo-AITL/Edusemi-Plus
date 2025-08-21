---
layout: default
title: "PCB Reliability | 信頼性"
---

---

# 🛡 PCB Reliability / 信頼性

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [主な要素 / Key Aspects](#-主な要素--key-aspects)  
3. [代表的な故障モード / Typical Failure Modes](#-代表的な故障モード--typical-failure-modes)  
4. [信頼性試験と規格 / Reliability Tests & Standards](#-信頼性試験と規格--reliability-tests--standards)  
5. [解析技術 / Analysis Techniques](#-解析技術--analysis-techniques)  
6. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  

---

## 📖 概要 / Overview
信頼性設計は、プリント基板の長期使用に耐える性能を保証するために不可欠です。  
*Reliability design is essential to ensure that printed circuit boards can withstand long-term use.*  

熱サイクル、機械的応力、湿度、環境要因が寿命や不具合に直結します。  
*Thermal cycling, mechanical stress, humidity, and environmental factors directly affect lifetime and failures.*  

---

## 🔑 主な要素 / Key Aspects
- **熱信頼性**  
  リフローはんだ付け後の熱サイクルによるはんだ接合やビアの劣化。  
  *Degradation of solder joints and vias under thermal cycling after reflow soldering.*  

- **機械的信頼性**  
  曲げや振動によるランド、配線、ビアの破壊。  
  *Fracture of pads, traces, and vias under bending or vibration.*  

- **湿度・環境耐性**  
  CAF（Conductive Anodic Filament）、電解腐食、イオンマイグレーション。  
  *CAF, electrolytic corrosion, and ionic migration under humid environments.*  

- **経年劣化試験**  
  HAST（高温高湿試験）、THB（温湿度バイアス試験）、温度サイクル試験。  
  *HAST, THB, and temperature cycling as accelerated lifetime tests.*  

---

## 💥 代表的な故障モード / Typical Failure Modes
- **はんだ接合部クラック**  
  繰返し熱サイクルや衝撃で発生。  
  *Cracks in solder joints due to repeated thermal cycling or shock.*  

- **ビア断線**  
  熱膨張差による銅めっき疲労。  
  *Via barrel fracture from copper plating fatigue under CTE mismatch.*  

- **CAF（導電性陽極フィラメント）**  
  ガラス繊維に沿ったイオン伝導路の形成。  
  *Formation of conductive path along glass fibers.*  

- **レジスト剥離・腐食**  
  湿気や化学反応による表面保護膜の劣化。  
  *Degradation of solder mask or corrosion from moisture/chemicals.*  

---

## 🧪 信頼性試験と規格 / Reliability Tests & Standards
- **IPC-9701**: はんだ接合部の信頼性試験  
  *Solder joint reliability testing*  

- **JESD22**: JEDEC加速試験規格（温度サイクル、HASTなど）  
  *JEDEC reliability standards for thermal cycling, HAST, etc.*  

- **IPC-TM-650**: CAF試験やイオンマイグレーション評価  
  *Test methods for CAF and ionic migration*  

- **UL 746E**: 樹脂材料の長期耐久性評価  
  *Evaluation of long-term endurance of polymeric materials*  

---

## 🔍 解析技術 / Analysis Techniques
- **断面解析 (Cross-section analysis)**  
  ビアや接合部の劣化確認。  
  *Inspection of vias and joints degradation.*  

- **X線検査 / X-ray inspection**  
  BGAや内部欠陥の非破壊観察。  
  *Non-destructive observation of BGAs and internal voids.*  

- **SEM/EDX解析**  
  クラック進展や元素分析による腐食メカニズム特定。  
  *Crack propagation and corrosion analysis by SEM/EDX.*  

- **寿命予測モデリング**  
  Coffin-Manson式やArrhenius式による加速寿命評価。  
  *Lifetime modeling using Coffin-Manson and Arrhenius equations.*  

---

## 📚 学習目標 / Learning Goals
- PCB信頼性の評価手法を理解する。  
  *Understand PCB reliability evaluation methods.*  

- 熱・機械・湿度要因が信頼性に与える影響を把握する。  
  *Grasp the impact of thermal, mechanical, and humidity factors on reliability.*  

- 加速試験と解析技術を設計フィードバックに活用できる。  
  *Apply accelerated testing and analysis techniques for design feedback.*  

---

## 🔗 関連リンク / Related Links
- [📖 Materials](./materials.md)  
- [📖 Fabrication](./fabrication.md)  
- [📖 Simulation](./simulation.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
