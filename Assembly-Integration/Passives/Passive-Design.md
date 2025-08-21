---
layout: default
title: "Passive Design | 受動部品設計"
permalink: /Assembly-Integration/Passives/Passive-Design/
---

---

# ⚡ Passive Design / 受動部品設計

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Passive-Design/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Passive-Design.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [設計ゴール / Design Targets](#-設計ゴール--design-targets)  
3. [受動部品の寄生成分 / Parasitics](#-受動部品の寄生成分--parasitics)  
4. [配置と配線 / Placement & Routing](#-配置と配線--placement--routing)  
5. [高周波・高速設計 / RF & High-Speed Considerations](#-高周波高速設計--rf--high-speed-considerations)  
6. [熱設計と信頼性 / Thermal & Reliability](#-熱設計と信頼性--thermal--reliability)  
7. [モデル化とシミュレーション / Modeling & Simulation](#-モデル化とシミュレーション--modeling--simulation)  
8. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
9. [関連リンク / Related Links](#-関連リンク--related-links)  
10. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
受動部品（抵抗 R、コンデンサ C、インダクタ L）は PCB 設計における**最小構成要素**ですが、寄生成分や実装条件によって性能が大きく変化します。  
*Resistors, capacitors, and inductors are fundamental building blocks, but their real-world behavior strongly depends on parasitics and implementation.*  

適切な設計ができなければ、SI/PI/EMC の劣化や熱問題を引き起こし、システム信頼性に直結します。  

---

## 🎯 設計ゴール / Design Targets
- **SI/PIの安定化**: インピーダンス制御とデカップリング設計  
  *Stabilize SI/PI with impedance control and decoupling*  
- **寄生成分の抑制**: ESL, ESR, stray C の最小化  
  *Minimize parasitics such as ESL, ESR, stray capacitance*  
- **熱負荷耐性**: 定格電力・温度上昇を抑える配置  
  *Maintain rated power and minimize thermal rise*  
- **長期信頼性**: DC bias / aging / 環境条件を考慮  
  *Consider DC bias, aging, and environmental stresses*  

---

## 🧮 受動部品の寄生成分 / Parasitics
| 部品 / Component | 主な寄生要素 / Parasitics | 影響 / Impact |
|------------------|--------------------------|----------------|
| 抵抗 (R) | ESL, stray C | GHz帯でインピーダンス不安定 |
| コンデンサ (C) | ESR, ESL, DC bias効果 | デカップリング効果低下 |
| インダクタ (L) | 直流抵抗 DCR、コア損失、分布C | 飽和・高周波損失 |

- **直列モデル近似**:  
  コンデンサ実デバイスは  
  $$ Z(j\omega) \approx ESR + j\omega L_{ESL} + \frac{1}{j\omega C} $$  
  で表現され、周波数で最適動作点が変化します。  

---

## 🧩 配置と配線 / Placement & Routing
- 抵抗：終端抵抗はクロック/高速I/Oにてソース直近へ。  
  *Termination resistors placed near source for clocks/high-speed I/O.*  
- コンデンサ：IC電源ピン直近、**多Via接続**で低インダクタンス化。  
  *Place decoupling capacitors close to IC power pins with multiple vias.*  
- インダクタ：フィルタ回路は電源ラインに直列配置、ループ面積を最小化。  
  *Inductors in filters placed in series with minimized loop area.*  

---

## 📡 高周波・高速設計 / RF & High-Speed Considerations
- **デカップリングネットワーク**: 0.1 µF + 1 µF + 10 µF の並列で広帯域化。  
  *Use multiple capacitors in parallel for broadband decoupling.*  
- **配線長**: 1/20 λ 以上で寄生インダクタンス無視不可。  
  *Above 1/20 λ, trace inductance significantly affects behavior.*  
- **フィルタ設計**: LC共振周波数 $f = \frac{1}{2\pi\sqrt{LC}}$ を明示的に管理。  
  *Filter cutoff defined by LC resonance frequency.*  

---

## 🌡 熱設計と信頼性 / Thermal & Reliability
- **抵抗器**: 定格電力の 50–70% 以下で設計。  
  *Design resistors below 50–70% of rated power.*  
- **コンデンサ**: セラミック MLCC は DC バイアスで容量が 20–60% 減少。  
  *MLCC capacitance drops 20–60% under DC bias.*  
- **インダクタ**: 飽和電流 ($I_{sat}$) と温度上昇 ($ΔT$) を同時考慮。  
  *Evaluate inductors for both saturation current and thermal rise.*  

---

## 🔍 モデル化とシミュレーション / Modeling & Simulation
- **等価回路モデル (RLC)** を用いた SPICE シミュレーション。  
- **Sパラメータ**（メーカー提供 Touchstoneファイル）を活用。  
- **3D EM シミュレーション**で高周波寄生を評価。  

*Use RLC equivalent circuits, S-parameters, and EM solvers for accuracy.*  

---

## 🎯 学習目標 / Learning Goals
- 部品寄生を考慮した正確な設計ができる。  
  *Design with awareness of parasitics.*  
- 配置・配線と高周波挙動の関係を理解できる。  
  *Understand placement/routing vs RF behavior.*  
- 熱・信頼性を含めた統合設計が可能になる。  
  *Perform integrated design including thermal & reliability aspects.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📘 Resistor | 抵抗器の種類と特性<br>*Types and characteristics of resistors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Resistor/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Resistor.md) |
| 📗 Capacitor | コンデンサの種類と特性<br>*Types and characteristics of capacitors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Capacitor/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Capacitor.md) |
| 📙 Inductor | インダクタの種類と特性<br>*Types and characteristics of inductors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Inductor/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Inductor.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives 全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
