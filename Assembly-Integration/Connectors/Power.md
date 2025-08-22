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
5. [電流容量と熱設計 / Current Capacity & Thermal Design](#-電流容量と熱設計--current-capacity--thermal-design)  
6. [接触メカニズムと材料 / Contact Mechanism & Materials](#-接触メカニズムと材料--contact-mechanism--materials)  
7. [信頼性と試験 / Reliability & Testing](#-信頼性と試験--reliability--testing)  
8. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
9. [関連リンク / Related Links](#-関連リンク--related-links)  
10. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
Power Connectors は、**基板内・基板間・外部機器への電力供給**を担う重要インターフェースです。  
*Power connectors are critical interfaces for delivering electrical power within a board, between boards, and to external systems.*  

電源ラインは信号ラインよりも高電流・低抵抗を要求され、  
**接触抵抗・熱設計・メカニカル強度**がシステム信頼性に直結します。  

---

## 🎯 用途 / Applications
- **マザーボード – 電源ボード間**  
  *Motherboard to power module interconnects*  
- **サーバ・ストレージ**の大電流給電  
  *High-current supply for servers and storage systems*  
- **車載 ECU / EV** の電源バス接続  
  *Automotive ECU and EV power bus connections*  
- **産業制御機器** の高電圧ライン  
  *Industrial controllers with high-voltage lines*  
- **バッテリインターフェース**（モバイル・UPS・ロボティクス）  
  *Battery interface for mobile, UPS, and robotics*  

---

## 🧩 種類 / Types
| 種類 / Type | 構造・用途 / Structure & Use | 特徴 / Characteristics |
|-------------|-------------------------------|-------------------------|
| **バレルジャック / Barrel Jack** | DCアダプタ入力 / *External AC/DC adapter* | 安価・小電流 / *Low-cost, limited current* |
| **Molex / Mini-Fit Jr.** | 基板電源用 / *Board-level power* | 数A〜数十A対応、PC PSU標準 / *Supports several–tens of amps, PC PSU standard* |
| **High-Power Board-to-Board** | 高電流対応BTB / *High-current BTB connectors* | サーバ・GPUボードなど大電力供給 / *Server, GPU board power delivery* |
| **Busbar / Edge Connector** | 大電流直結 / *Direct busbar/edge interface* | 数百A級、大型装置向け / *Hundreds of amps, industrial/EV use* |
| **Terminal Block** | ネジ固定 / *Screw-type terminal* | 産業・制御用、着脱容易 / *Industrial use, easy field wiring* |
| **Battery Connector** | バッテリ接続 / *Battery plug/unplug* | 高接触信頼性、振動耐性 / *High reliability, vibration resistance* |

---

## 📊 主要パラメータ / Key Parameters
- **定格電流 (Current Rating, A)**  
  *Continuous allowable current per contact*  
- **接触抵抗 (Contact Resistance, mΩ)**  
  *Determines I²R loss and heat rise*  
- **定格電圧 (Voltage Rating, V)**  
  *Maximum safe operating voltage*  
- **挿抜耐久性 (Mating Cycles)**  
  *Durability under repeated mating/unmating*  
- **耐熱性 (Temperature Endurance, °C)**  
  *Max operating temperature including Joule heating*  

---

## 🔥 電流容量と熱設計 / Current Capacity & Thermal Design
- 電流容量は **断面積・接触面積・材料抵抗率**に依存。  
  *Current rating depends on conductor cross-section, contact area, and material resistivity.*  
- 接触抵抗上昇 → $P = I^2R$ に比例した発熱。  
- コネクタ温度上昇は UL / IEC 規格で **ΔT ≦ 30°C** を許容値とする場合が多い。  
- 大電流用途では **複数ピン並列** や **銅バスバー併用** が必須。  

---

## ⚙️ 接触メカニズムと材料 / Contact Mechanism & Materials
- **スプリング接触 / Spring Contacts**  
  高接触圧を確保、微小酸化膜を破壊して導通確保。  
  *Spring pressure breaks oxide films for stable conduction.*  
- **表面処理 / Plating**  
  - 錫 (Sn): 安価、酸化しやすい  
    *Tin: low cost, prone to oxidation*  
  - 金 (Au): 高信頼・低接触抵抗  
    *Gold: reliable, low resistance*  
  - 銀 (Ag): 高導電率、硫化に注意  
    *Silver: high conductivity, prone to sulfide film*  
- **材料選定**: 銅合金・リン青銅などが主流。  
  *Copper alloys and phosphor bronze widely used.*  

---

## 🛡 信頼性と試験 / Reliability & Testing
- **温度サイクル試験**: ΔR, ΔT の変化確認  
  *Check contact resistance and thermal rise under cycling*  
- **振動・衝撃試験**: 車載・航空宇宙必須  
  *Required for automotive and aerospace*  
- **耐湿試験**: 高湿環境での腐食進行評価  
  *Corrosion progression under humidity*  
- **挿抜耐久試験**: 摩耗・表面劣化を評価  
  *Wear-out and surface degradation from repeated mating*  

---

## 🎯 学習目標 / Learning Goals
- 電源コネクタの種類・用途を理解する。  
  *Understand types and applications of power connectors.*  
- 電流容量・接触抵抗・発熱の関係を説明できる。  
  *Explain relationship of current, resistance, and heat rise.*  
- 材料・表面処理と信頼性評価手法を習得する。  
  *Learn material/plating choices and reliability testing.*  

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
