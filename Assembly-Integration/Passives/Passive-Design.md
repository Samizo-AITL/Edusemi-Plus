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
3. [受動部品の配置と配線 / Placement & Routing](#-受動部品の配置と配線--placement--routing)  
4. [高周波設計の考慮点 / RF & High-Speed Considerations](#-高周波設計の考慮点--rf--high-speed-considerations)  
5. [熱設計と信頼性 / Thermal & Reliability](#-熱設計と信頼性--thermal--reliability)  
6. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  
8. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
受動部品（抵抗・コンデンサ・インダクタ）は PCB 設計の基本要素であり、**SI/PI/EMI/熱** の全てに影響します。  
*Passive components (R, C, L) are fundamental PCB elements impacting SI, PI, EMI, and thermal performance.*  

適切な部品選択・配置・配線により、システムの性能と信頼性を大きく左右します。  
*Proper selection, placement, and routing strongly determine system performance and reliability.*  

---

## 🎯 設計ゴール / Design Targets
- **最小パラジティクス**（寄生成分）の実現  
  *Minimize parasitics (ESL, ESR, stray capacitance)*  
- **低インダクタンスな電源デカップリング**  
  *Low-inductance decoupling of power delivery*  
- **高周波損失の低減**  
  *Reduce RF/high-speed losses*  
- **熱分散と信頼性向上**  
  *Enhance thermal dissipation and long-term reliability*  

---

## 🧩 受動部品の配置と配線 / Placement & Routing
- **抵抗 (R)**：クロックライン終端はソース/ロード近傍に配置。  
  *Place termination resistors near source/load.*  
- **コンデンサ (C)**：デカップリングは IC 電源ピン直近、広い GND 接続。  
  *Place decoupling capacitors close to IC power pins, with wide ground vias.*  
- **インダクタ (L)**：電源フィルタや EMI フィルタ用途で、ループ最小化。  
  *Use inductors in power/EMI filters with minimized current loops.*  

---

## 📡 高周波設計の考慮点 / RF & High-Speed Considerations
- **ESL低減**: 複数サイズの MLCC を並列配置。  
  *Reduce ESL by paralleling MLCCs of different sizes.*  
- **共振抑制**: デカップリングネットワークを広帯域化。  
  *Broaden bandwidth of decoupling networks to suppress resonance.*  
- **Q値調整**: RFフィルタでは部品 Q のバランス設計。  
  *Balance Q factor for RF filters.*  

---

## 🌡 熱設計と信頼性 / Thermal & Reliability
- 抵抗器：許容電力と基板放熱を考慮。  
  *Resistors: consider rated power and board heat dissipation.*  
- コンデンサ：DCバイアスによる容量低下に注意。  
  *Capacitors: watch out for capacitance drop under DC bias.*  
- インダクタ：コア損失と飽和電流を評価。  
  *Inductors: evaluate core loss and saturation current.*  

---

## 🎯 学習目標 / Learning Goals
- 受動部品配置と配線のベストプラクティスを理解する。  
  *Understand best practices for passive placement & routing.*  
- SI/PI/EMI 観点での部品選定と設計を習得する。  
  *Learn component selection and design for SI/PI/EMI.*  
- 高周波設計と熱信頼性を統合的に考慮できる。  
  *Integrate RF design and thermal reliability considerations.*  

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
