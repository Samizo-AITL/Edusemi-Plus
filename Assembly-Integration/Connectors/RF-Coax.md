---
layout: default
title: "RF-Coax | 高周波同軸コネクタ"
---

---

# 🧲 RF-Coax / 高周波同軸コネクタ
*RF Coaxial Connectors (SMA, SMB, MMCX, U.FL, etc.)*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF-Coax/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF-Coax.md) |

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
RF同軸コネクタは、**GHz帯の信号伝送**に対応する低損失・低反射設計のコネクタです。  
*RF coaxial connectors are designed for GHz-range transmission, offering low loss and low reflection.*  

インピーダンス（通常 50 Ω）が厳格に規定され、**VSWR（Voltage Standing Wave Ratio）** を抑制することが重要です。  

---

## 🧩 種類 / Types

| 規格 / Standard | 特徴 / Characteristics | 主な用途 / Applications |
|-----------------|------------------------|--------------------------|
| **SMA** | 18 GHz対応、スクリューロック | 通信機器、計測機器 |
| **SMB** | 小型、スナップ結合 | 車載、産業機器 |
| **MCX/MMCX** | 超小型、プッシュ結合 | IoT機器、GPSモジュール |
| **U.FL / I-PEX MHF** | 基板直付け、狭小スペース向け | モバイル端末、Wi-Fi/Bluetooth |
| **N型** | 高出力対応、防水 | 屋外基地局、アンテナ |

---

## ⚡ 主要用途 / Applications
- **無線通信機器**：Wi-Fi, LTE, 5G  
  *Wireless communication: Wi-Fi, LTE, 5G*  
- **GPS/測位**：アンテナモジュール接続  
  *GPS modules and antennas*  
- **計測器**：VNA, スペアナ, オシロスコープ入力  
  *VNAs, spectrum analyzers, oscilloscopes*  
- **RFモジュール**：Bluetooth, ZigBee, LoRaWAN  
  *Short-range RF modules (Bluetooth, ZigBee, LoRaWAN)*  

---

## 📏 設計パラメータ / Design Parameters
- **特性インピーダンス**: 50 Ω が標準  
  *Characteristic impedance typically 50 Ω*  
- **周波数帯域**: 1–18 GHz（規格に依存）  
  *Frequency range 1–18 GHz depending on type*  
- **VSWR**: 1.1–1.3 以下が理想  
  *Target VSWR < 1.3*  
- **挿入損失**: 0.1–0.3 dB 程度  
  *Insertion loss around 0.1–0.3 dB*  
- **嵌合作業性**: ネジ式（堅牢） vs プッシュ式（容易）  
  *Threaded (robust) vs push-fit (easy handling)*  

---

## 🛡 実装と信頼性 / Mounting & Reliability
- **基板設計**: コネクタ直下の GND via 配置で反射低減。  
  *Place ground vias near connector pads to suppress reflections.*  
- **嵌合耐久性**: U.FL 約 30 回、SMA 数千回。  
  *U.FL ~30 cycles, SMA several thousand cycles.*  
- **防水性**: N型・TNCは屋外用に適す。  
  *N-type and TNC suitable for outdoor use.*  
- **メカ強度**: 小型タイプは引張応力に弱い → ケーブル固定が必須。  
  *Small connectors are fragile; secure cables mechanically.*  

---

## 📝 設計指針 / Design Guidelines
- **50 Ωライン**に正確にマッチングさせる。  
  *Maintain precise 50 Ω matching in PCB layout.*  
- **ストリップライン/マイクロストリップ**の遷移設計を最適化。  
  *Optimize transition from microstrip/stripline to connector pad.*  
- **Sパラメータ**を用いたSI/PI/EMC検証が必須。  
  *Validate with S-parameter simulations.*  
- **高周波テスト**は VNA で実施。  
  *Perform RF validation using VNAs.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📜 FFC-FPC | フレキシブルコネクタ<br>*FFC/FPC connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/FFC-FPC/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/FFC-FPC.md) |
| ⚡ High-Speed | 高速データコネクタ<br>*High-speed connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/High-Speed/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/High-Speed.md) |
| 🔋 Power | 電源用コネクタ<br>*Power connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors 全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
