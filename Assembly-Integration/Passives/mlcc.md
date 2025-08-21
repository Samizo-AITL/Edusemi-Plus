---
layout: default
title: "MLCC | 積層セラミックコンデンサ"
---

---

# 🔋 MLCC / 積層セラミックコンデンサ

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/mlcc/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/mlcc.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [特性と課題 / Characteristics & Issues](#-特性と課題--characteristics--issues)  
3. [デカップリング設計 / Decoupling Design](#-デカップリング設計--decoupling-design)  
4. [直流バイアス特性 / DC Bias Effects](#-直流バイアス特性--dc-bias-effects)  
5. [実装上の考慮事項 / Layout Considerations](#-実装上の考慮事項--layout-considerations)  
6. [信頼性と試験 / Reliability & Testing](#-信頼性と試験--reliability--testing)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  
8. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
MLCC（Multi-Layer Ceramic Capacitor, 積層セラミックコンデンサ）は、  
**電源デカップリング・ノイズ除去・タイミング調整** に最も広く用いられる受動部品です。  
*MLCCs are the most widely used passive components for decoupling, noise suppression, and timing adjustment.*  

---

## 📊 特性と課題 / Characteristics & Issues
- **容量値依存**: 温度係数 (X7R, X5R, C0G) により容量安定性が変動。  
- **直流バイアス**: DC印加で容量が低下（特に高誘電率系）。  
- **ESR/ESL**: 高周波特性は小型サイズの方が有利。  

*Capacitance stability depends on temperature coefficient (X7R, X5R, C0G).  
DC bias reduces capacitance (notably in high-k dielectrics).  
Smaller sizes yield better ESR/ESL performance.*  

---

## ⚡ デカップリング設計 / Decoupling Design
- 広帯域ノイズ抑制のため、容量値の異なるMLCCを並列配置。  
- 電源ピン直近に配置してESLを低減。  
- GNDプレーンとのリターンパスを最短化。  

*Use multiple MLCCs of different values for broadband suppression.  
Place close to IC pins to reduce ESL.  
Keep shortest return path to ground plane.*  

---

## 📉 直流バイアス特性 / DC Bias Effects
- 公称容量 10 µF → 実効容量 3–4 µF（Vdd印加時）に低下する場合あり。  
- 高電圧定格品やC0Gタイプで低減可能。  

*10 µF nominal may drop to 3–4 µF under bias.  
Use higher voltage rating or C0G for mitigation.*  

---

## 🛠 実装上の考慮事項 / Layout Considerations
- **BGA下配置**: 電源ピン直近に小型MLCC配置。  
- **並列配置**: 容量の異なるMLCCをサイズ混合して配置。  
- **インピーダンス整合**: 周波数帯ごとの最適化が必要。  

---

## 🧪 信頼性と試験 / Reliability & Testing
- 熱衝撃・曲げストレスでクラック発生 → **ソフト端子品**採用で改善。  
- 高湿・高温下での絶縁劣化試験（85°C/85%RH bias test）。  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📏 Resistors | 抵抗器の種類と特性<br>*Types and properties of resistors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/resistors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/resistors.md) |
| 🌀 Inductors | インダクタ設計と損失要因<br>*Inductor design and loss mechanisms* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/inductors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/inductors.md) |
| ⚡ Capacitors | アルミ/タンタル/フィルム<br>*Aluminum/Tantalum/Film capacitors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/capacitors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/capacitors.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
