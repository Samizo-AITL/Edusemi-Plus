---
layout: default
title: "Power Connectors | 電源用コネクタ"
---

---

# 🔋 Power Connectors / 電源用コネクタ
*Power delivery connectors for boards and systems*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [用途 / Applications](#-用途--applications)  
3. [種類 / Types](#-種類--types)  
4. [主要パラメータ / Key Parameters](#-主要パラメータ--key-parameters)  
5. [設計上の考慮事項 / Design Considerations](#-設計上の考慮事項--design-considerations)  
6. [信頼性と試験 / Reliability & Testing](#-信頼性と試験--reliability--testing)  
7. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
8. [関連リンク / Related Links](#-関連リンク--related-links)  
9. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
Power Connectors は、**基板間・基板外への電力供給**を行うためのコネクタ群です。  
*Power connectors are used for delivering electrical power between boards or to external systems.*  

大電流対応、低接触抵抗、耐熱性が重要です。  
*Key requirements are high current capability, low contact resistance, and thermal endurance.*  

---

## 🎯 用途 / Applications
- **電源モジュール接続**: DC/DC コンバータ、電源ボード  
  *Connecting power modules such as DC/DC converters*  
- **高電流ライン**: サーバ・ストレージ・車載 ECU  
  *High-current lines in servers, storage, and automotive ECUs*  
- **バッテリ接続**: モバイル機器・UPS・EV  
  *Battery interfaces for mobile devices, UPS, and EVs*  
- **産業機器**: 高電圧・大電流制御系  
  *Industrial systems with high-voltage or high-current requirements*  

---

## 🧩 種類 / Types
| 種類 / Type | 構造・用途 / Structure & Use | 特徴 / Characteristics |
|-------------|-------------------------------|-------------------------|
| **バレルジャック / Barrel Jack** | 外部ACアダプタ入力 / *External AC adapter input* | 安価・汎用、電流容量小 / *Low-cost, limited current* |
| **Molex/Mini-Fit** | 基板電源用 / *Board-level power connectors* | 数A〜数十A対応 / *Supports several to tens of amps* |
| **板バスバー / Busbar** | 大電流直結 / *Direct busbar connection* | 数百A級対応、低抵抗 / *Supports hundreds of amps, ultra-low resistance* |
| **スクリュー端子 / Terminal Block** | フィールド配線 / *Field wiring* | 産業用途、着脱容易 / *Industrial use, easy wiring* |
| **バッテリコネクタ / Battery Connectors** | バッテリ着脱 / *Battery plug/unplug* | 高接触信頼性、耐衝撃性 / *Reliable contacts, shock resistant* |

---

## 📊 主要パラメータ / Key Parameters
- **定格電流 / Current Rating**  
  *Maximum continuous current capacity*  
- **接触抵抗 / Contact Resistance**  
  *Resistance at contact points affecting heat generation*  
- **定格電圧 / Voltage Rating**  
  *Maximum operating voltage*  
- **耐熱性 / Temperature Endurance**  
  *Connector performance under high temperatures*  
- **寿命 (挿抜回数) / Mating Cycles**  
  *Durability over repeated insertions/removals*  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **電流容量**：I²R 損失を最小化。  
  *Design to minimize I²R power loss.*  
- **熱設計**：高電流では接触部の発熱対策が必須。  
  *Manage thermal rise in contacts under high current.*  
- **メカ強度**：産業用途では振動・衝撃対策が必要。  
  *Mechanical strength needed for vibration/shock environments.*  
- **冗長化**：重要系では複数ピン並列で信頼性向上。  
  *Use redundant/pin-parallel designs for reliability.*  

---

## 🛡 信頼性と試験 / Reliability & Testing
- **温度サイクル試験**：接触抵抗と発熱変動評価。  
  *Test contact resistance and heat under thermal cycling.*  
- **振動/衝撃試験**：車載・産業機器用途で必須。  
  *Required for automotive and industrial connectors.*  
- **耐湿試験**：腐食による接触劣化を評価。  
  *Evaluate corrosion effects under humidity.*  
- **挿抜耐久試験**：繰返し使用時の性能維持。  
  *Check performance under repeated mating cycles.*  

---

## 🎯 学習目標 / Learning Goals
- 電源コネクタの種類と特徴を理解する。  
  *Understand the types and characteristics of power connectors.*  
- 電流容量・接触抵抗・発熱設計の重要性を説明できる。  
  *Explain current capacity, contact resistance, and thermal design.*  
- 高信頼用途への設計・評価方法を習得する。  
  *Learn design and validation methods for high-reliability applications.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🧩 Board-to-Board | 基板間接続コネクタ<br>*Board-to-board connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |
| 🛰 RF Connectors | 高周波コネクタ<br>*RF connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF.md) |
| 🔌 Connectors | コネクタ全体カテゴリ<br>*Overview of connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to Connectors repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
