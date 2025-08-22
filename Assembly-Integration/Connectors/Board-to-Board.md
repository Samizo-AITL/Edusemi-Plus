---
layout: default
title: "Board-to-Board | 基板対基板コネクタ"
---

---

# 🔗 Board-to-Board Connectors / 基板対基板コネクタ

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [種類 / Types](#-種類--types)  
3. [特性パラメータ / Key Parameters](#-特性パラメータ--key-parameters)  
4. [設計上の考慮事項 / Design Considerations](#-設計上の考慮事項--design-considerations)  
5. [信頼性と実装 / Reliability & Mounting](#-信頼性と実装--reliability--mounting)  
6. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  
8. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
基板対基板コネクタは、**複数のプリント基板を電気的・機械的に接続**するために用いられます。  
*Board-to-board connectors are used to provide both electrical and mechanical connection between multiple PCBs.*  

用途はスマートフォン、産業機器、サーバー、車載機器など広範囲にわたります。  

---

## 🧩 種類 / Types
| 種類 / Type | 特徴 / Characteristics |
|-------------|-------------------------|
| **スタッキング型 / Stacking** | 垂直方向に基板を積層接続。高密度化に適す。<br>*Vertical stacking of boards for high-density integration.* |
| **メザニン型 / Mezzanine** | 平行に基板を接続。高速信号伝送向き。<br>*Parallel board connection, suited for high-speed signals.* |
| **直角型 / Right-Angle** | 水平方向に基板を接続。L字構造で筐体設計に柔軟。<br>*Right-angle connection for compact system design.* |
| **フローティング型 / Floating** | ±0.5 mm 程度の位置ずれ吸収。車載や産業用に多用。<br>*Absorbs misalignment (±0.5 mm), widely used in automotive/industrial.* |

---

## 📊 特性パラメータ / Key Parameters
- **ピッチ / Pitch**: 0.3 mm〜1.0 mm が主流  
  *Pitch ranges from 0.3 mm to 1.0 mm.*  
- **定格電流 / Current Rating**: 0.3〜2 A 程度  
  *Typical current rating 0.3–2 A.*  
- **信号速度 / Signal Speed**: 最大 28 Gbps 対応品も存在  
  *Some support up to 28 Gbps transmission.*  
- **耐久性 / Durability**: 30〜100 回程度の嵌合サイクル  
  *Mating cycles typically 30–100 times.*  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **SI/PI**: インピーダンス整合を考慮し、GNDピンを挟んで配置。  
  *Consider impedance matching, interleave GND pins.*  
- **フットプリント**: はんだクラック防止のためランド強度を確保。  
  *Ensure pad strength to prevent solder cracks.*  
- **メカ設計**: 基板ズレ・筐体変形を吸収するフローティング型を検討。  
  *Floating connectors help absorb misalignment and chassis stress.*  
- **熱設計**: 高電流モデルでは発熱に注意。  
  *Monitor heating in high-current applications.*  

---

## 🛡 信頼性と実装 / Reliability & Mounting
- **車載用途**: AEC-Q100/Q200 に準拠する部品を推奨。  
- **はんだ実装**: BGA/SMT タイプはリフロー条件を厳守。  
- **振動試験**: IEC 60512 に基づく振動耐性確認が必要。  
- **接触抵抗**: 長期使用による上昇をモニタリング。  

---

## 🎯 学習目標 / Learning Goals
- 基板対基板コネクタの種類と特徴を理解する。  
  *Understand the types and characteristics of board-to-board connectors.*  
- SI/PI を考慮した設計上の注意点を説明できる。  
  *Explain design considerations with SI/PI in mind.*  
- 車載・高速用途での信頼性設計を適用できる。  
  *Apply reliability design practices for automotive and high-speed use cases.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🔌 Wire-to-Board | ケーブル・ハーネス接続<br>*Cable & harness connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Wire-to-Board/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Wire-to-Board.md) |
| ⚡ High-Speed | 高速信号対応コネクタ<br>*Connectors for high-speed signals* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/High-Speed/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/High-Speed.md) |
| 🔋 Power | 電源用大電流コネクタ<br>*High-current power connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
