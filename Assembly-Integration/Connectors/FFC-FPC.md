---
layout: default
title: "FFC-FPC | フレキシブルコネクタ"
---

---

# 📜 FFC-FPC / フレキシブルフラットケーブル・フレキ基板コネクタ
*Flexible Flat Cable & Flexible Printed Circuit Connectors*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/FFC-FPC/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/FFC-FPC.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [種類 / Types](#-種類--types)  
3. [主要用途 / Applications](#-主要用途--applications)  
4. [設計パラメータ / Design Parameters](#-設計パラメータ--design-parameters)  
5. [実装と信頼性 / Mounting & Reliability](#-実装と信頼性--mounting--reliability)  
6. [設計指針 / Design Guidelines](#-設計指針--design-guidelines)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  
8. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
FFC（Flexible Flat Cable）、FPC（Flexible Printed Circuit）コネクタは、**低背・狭ピッチ・柔軟性**を特徴とし、モバイル機器や薄型電子機器に広く使用されます。  
*FFC/FPC connectors are low-profile, fine-pitch connectors designed for compact, flexible interconnections in mobile and slim electronic devices.*  

---

## 🧩 種類 / Types

| 種類 / Type | 特徴 / Characteristics |
|-------------|-------------------------|
| **ZIF (Zero Insertion Force)** | フラップでケーブルを固定、嵌合作業性が高い |
| **Non-ZIF** | ケーブルを押し込む方式、低コスト |
| **上下両接続タイプ / Dual Contact** | ケーブルの接触面上下両方に対応 |
| **バックフリップ / Back Flip** | フラップが基板後方に倒れる構造 |
| **狭ピッチタイプ** | 0.2–0.5 mm ピッチで高密度実装 |
| **補強付きコネクタ** | EMIシールドやメカ強度を強化 |

---

## ⚡ 主要用途 / Applications
- **モバイル機器**：LCDパネル、カメラモジュール  
  *Mobile devices: LCD panels, camera modules*  
- **PC/タブレット**：キーボード、タッチパネル  
  *Laptops/tablets: keyboards, touch panels*  
- **車載機器**：クラスタディスプレイ、センターインフォメーション  
  *Automotive: cluster displays, infotainment systems*  
- **医療機器**：小型センサ、表示モジュール  
  *Medical devices: compact sensors and display modules*  

---

## 📏 設計パラメータ / Design Parameters
- **ピッチ**：0.2, 0.3, 0.5 mm が主流  
  *Pitch mainly 0.2, 0.3, 0.5 mm*  
- **高さ**：0.6–2.0 mm の低背型  
  *Connector height between 0.6–2.0 mm*  
- **嵌合回数**：20–50 回が一般、耐久タイプで 100 回以上  
  *Mating cycles typically 20–50, up to 100+ for durable versions*  
- **電流容量**：0.2–0.5 A/Pin 程度  
  *Current rating around 0.2–0.5 A per pin*  

---

## 🛡 実装と信頼性 / Mounting & Reliability
- **ZIF構造**でケーブル摩耗を防止。  
  *ZIF design prevents cable wear during insertion.*  
- **補強テープ**付きFPCで機械的強度を確保。  
  *Reinforcement tape on FPC improves mechanical strength.*  
- **狭ピッチ実装**ははんだブリッジリスクが高く、リフロー条件管理が必須。  
  *Fine-pitch soldering prone to bridging, requires strict reflow control.*  
- **振動対策**：ロック機構や補強板の採用。  
  *Locking mechanisms and stiffeners for vibration resistance.*  

---

## 📝 設計指針 / Design Guidelines
- **嵌合方向**（上挿し/下挿し）を機構設計と整合させる。  
  *Align insertion direction (top/bottom entry) with mechanical design.*  
- **EMIシールド付きFFC**を高速信号ラインに採用。  
  *Use shielded FFCs for high-speed signals.*  
- **折り曲げR**を大きくし、FPCの断線を防止。  
  *Maintain large bend radius to avoid FPC cracking.*  
- **自動実装対応品**を選定し、リフロー条件を事前確認。  
  *Select reflow-compatible connectors for automated assembly.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🧵 Wire-to-Board | ワイヤ対基板コネクタ<br>*Wire-to-Board connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Wire-to-Board/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Wire-to-Board.md) |
| 🧲 RF-Coax | 高周波同軸コネクタ<br>*RF coaxial connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF-Coax/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF-Coax.md) |
| ⚡ High-Speed | 高速信号用コネクタ<br>*High-speed connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/High-Speed/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/High-Speed.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors 全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
