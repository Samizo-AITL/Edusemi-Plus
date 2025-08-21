---
layout: default
title: "PCB Validation | 検証"
---

---

# ✅ PCB Validation / 検証

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [検証カテゴリ / Validation Categories](#-検証カテゴリ--validation-categories)  
   - [SI (Signal Integrity)](#-si-signal-integrity)  
   - [PI (Power Integrity)](#-pi-power-integrity)  
   - [熱解析 / Thermal Analysis](#-熱解析--thermal-analysis)  
   - [EMC/EMI 評価](#-emcemi-評価)  
   - [DFM (Design for Manufacturability)](#-dfm-design-for-manufacturability)  
3. [解析手法 / Validation Methods](#-解析手法--validation-methods)  
4. [国際規格 / Standards](#-国際規格--standards)  
5. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
6. [関連リンク / Related Links](#-関連リンク--related-links)  

---

## 🏗 概要 / Overview
PCB検証 (Validation) は、設計された基板が **性能・信頼性・製造性** の全ての要求を満たすことを確認する工程です。  
*PCB validation ensures that the designed board meets requirements for performance, reliability, and manufacturability.*  

対象は **信号品質 (SI)、電源安定性 (PI)、熱特性、EMC適合性、製造性 (DFM)** に及びます。  

---

## 🔑 検証カテゴリ / Validation Categories

### 📡 SI (Signal Integrity)
- 反射・スキュー・ジッタ解析  
- スタブやビアによる反射影響の評価  
- Eye diagram / TDR シミュレーション  

*Reflection, skew, jitter analysis.  
Evaluation of via stubs.  
Eye diagram and TDR simulations.*  

---

### 🔋 PI (Power Integrity)
- IR Drop、グラウンドバウンス解析  
- デカップリング配置最適化  
- PDN (Power Delivery Network) のインピーダンス確認  

*IR drop and ground bounce analysis.  
Optimization of decoupling capacitor placement.  
PDN impedance verification.*  

---

### 🌡 熱解析 / Thermal Analysis
- 熱分布とホットスポットの特定  
- 冷却設計（ヒートシンク・サーマルビア・ファン）評価  
- パッケージと基板間の熱抵抗 (θJB, θJC) 検証  

*Heat distribution and hotspot detection.  
Cooling efficiency validation (heatsink, thermal vias, airflow).  
Thermal resistance verification between package and board.*  

---

### 📶 EMC/EMI 評価
- 放射ノイズ、伝導ノイズ解析  
- フィルタ、シールド、リターンパス設計の有効性  
- 規格（FCC, CISPR, VCCI）への適合性確認  

*Radiated and conducted emissions analysis.  
Effectiveness of filters, shielding, and return path design.  
Compliance with FCC, CISPR, VCCI standards.*  

---

### 🏭 DFM (Design for Manufacturability)
- 最小クリアランス・ドリルサイズのチェック  
- アスペクト比・レジスト厚みの検証  
- アセンブリ工程での実装可能性確認  

*Check of clearance, drill size, aspect ratio.  
Verification of solder mask, land size, and assembly feasibility.*  

---

## 🛠 解析手法 / Validation Methods
- **シミュレーション**: SPICE, SI/PIツール (HyperLynx, Sigrity, ADS など)  
- **実測検証**: オシロスコープ, VNA, TDR, EMI チャンバー  
- **加速試験**: 熱サイクル、HAST、振動試験での設計妥当性確認  
- **設計レビュー**: クロスチェック、DRC/DFM 自動検証  

*Simulation with SI/PI tools.  
Measurements with oscilloscope, VNA, TDR, EMI chamber.  
Accelerated reliability tests.  
Design reviews with DRC/DFM automation.*  

---

## 📏 国際規格 / Standards
- **IPC-6012**: リジッド基板の性能仕様  
- **IPC-2221/2222**: PCB一般設計規格  
- **IEC 61000シリーズ**: EMC適合性基準  
- **JEDEC JESD**: 半導体パッケージ/システムレベル試験規格  

---

## 🎯 学習目標 / Learning Goals
- SI/PI/熱/EMC の各観点で検証フローを理解する。  
  *Understand validation flow for SI, PI, thermal, and EMC.*  
- シミュレーションと実測を組み合わせた設計検証を実践できる。  
  *Combine simulation and measurement for validation.*  
- 国際規格への適合性を考慮した設計フローを構築する。  
  *Build design flow considering compliance with international standards.*  

---

## 🔗 関連リンク / Related Links
- [📑 Stackup](./stackup.md)  
- [📏 Design Rules](./design_rules.md)  
- [🛤 Routing](./routing.md)  
- [🛡 Reliability](./reliability.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
