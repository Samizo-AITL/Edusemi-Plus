---
layout: default
title: "USB-TypeC | USB-Cコネクタ"
---

---

# 🔌 USB-TypeC / USB-C コネクタ
*USB-TypeC Connectors for Power Delivery and High-Speed I/O*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/USB-TypeC/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/USB-TypeC.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [機能と特徴 / Features](#-機能と特徴--features)  
3. [主要用途 / Applications](#-主要用途--applications)  
4. [設計パラメータ / Design Parameters](#-設計パラメータ--design-parameters)  
5. [信頼性・環境要因 / Reliability & Environmental Factors](#-信頼性環境要因--reliability--environmental-factors)  
6. [設計指針 / Design Guidelines](#-設計指針--design-guidelines)  
7. [関連リンク / Related Links](#-関連リンク--related-links)  
8. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
USB-TypeCは、**リバーシブル構造・高速データ伝送・電力供給（PD）** を同時に実現する最新規格のコネクタです。  
*USB Type-C provides reversible design, high-speed data transfer, and power delivery (PD) in a single connector.*  

USB 3.2/4、DisplayPort Alt Mode、Thunderbolt 互換性を持ち、ノートPC・スマートフォンから産業機器まで幅広く採用されています。  

---

## ⚡ 機能と特徴 / Features
- **リバーシブル設計**: 上下どちらの向きでも接続可能  
  *Reversible connector orientation*  
- **USB Power Delivery (PD)**: 最大 20V/5A (100W) まで給電対応  
  *Supports up to 20V/5A (100W) via PD*  
- **高速通信**: USB4/Thunderbolt 4 で最大 40 Gbps  
  *High-speed up to 40 Gbps (USB4/Thunderbolt 4)*  
- **Alt Mode対応**: DisplayPort/HDMI/PCIe over USB-C  
  *Supports DisplayPort, HDMI, PCIe via Alt Mode*  
- **小型・高密度**: 24ピン構造で電源・信号を集約  
  *Compact 24-pin connector integrating power and signals*  

---

## ⚙️ 主要用途 / Applications
- **ノートPC/スマートフォン充電**  
  *Charging for laptops and smartphones*  
- **外部ディスプレイ接続 (DisplayPort Alt Mode)**  
  *External display connectivity (DP Alt Mode)*  
- **高速データ通信 (USB4/Thunderbolt 4)**  
  *High-speed data transfer (USB4/Thunderbolt 4)*  
- **産業機器・医療機器の電源供給**  
  *Power delivery in industrial/medical devices*  
- **ドッキングステーション/ハブ**  
  *Docking stations and hubs*  

---

## 📏 設計パラメータ / Design Parameters
- **定格電流**: 3A 標準, 5A (E-markerケーブル必要)  
  *3A standard, 5A with E-marker cable*  
- **定格電圧**: 最大 20V  
  *Up to 20V*  
- **挿抜耐久性**: 10,000 回以上  
  *10,000+ mating cycles*  
- **高速信号特性**: 差動インピーダンス 90 Ω ±10%  
  *Differential impedance 90 Ω ±10%*  
- **EMC対策**: シールド付きレセプタクル必須  
  *Receptacles with shielding required for EMC*  

---

## 🛡 信頼性・環境要因 / Reliability & Environmental Factors
- **接触信頼性**: 金メッキ端子による低接触抵抗  
  *Gold-plated contacts for low contact resistance*  
- **熱管理**: 高電流供給時の発熱対策必須  
  *Thermal design critical under high current PD*  
- **耐環境性**: 防水USB-C (IP67) も存在  
  *Waterproof USB-C (IP67) available*  
- **ケーブル品質依存**: 長尺・低品質ケーブルはSI劣化要因  
  *Signal integrity sensitive to cable length/quality*  

---

## 📝 設計指針 / Design Guidelines
- **E-markerケーブル検出**により PD電力を制御  
  *Use E-marker cable detection to control PD power levels*  
- **高速信号ライン**は差動配線、90Ω整合を確保  
  *Maintain 90Ω differential impedance for high-speed lines*  
- **放熱設計**: 5A供給時は端子/基板の温度上昇を抑制  
  *Thermal management required at 5A supply*  
- **Alt Mode切替**は CCライン制御で実現  
  *Alt Mode switching controlled via CC lines*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| ⚡ High-Speed | 高速差動伝送コネクタ<br>*High-speed differential connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/High-Speed/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/High-Speed.md) |
| 🔋 Power | 電源コネクタ<br>*Power connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |
| 🧿 Circular | 丸形コネクタ<br>*Circular connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Circular/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Circular.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors 全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to Connectors repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
