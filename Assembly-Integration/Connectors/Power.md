---
layout: default
title: "Power | 電源コネクタ"
---

---

# 🔋 Power / 電源コネクタ
*Power Connectors (High Current, Low Impedance, Thermal Reliability)*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |

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
電源コネクタは、**高電流・低インピーダンス・長期信頼性**を満たすよう設計されたインタフェースです。  
*Power connectors are designed to support high current, low impedance, and long-term reliability.*  

大電流用途では**接触抵抗の低減・発熱管理・嵌合耐久性**が重要になります。  

---

## 🧩 種類 / Types

| 種類 / Type | 特徴 / Characteristics | 用途 / Applications |
|-------------|-----------------------|----------------------|
| **Board-to-Board Power** | 高電流対応スタッキング端子 | サーバ、電源分配基板 |
| **Wire-to-Board Power** | 圧着端子、大電流配線向け | 車載、産業機器 |
| **Busbar Connectors** | 100A 超の大電流分配 | データセンター、UPS |
| **Blade / Tab Terminals** | 汎用・簡易着脱 | 家電、低電圧機器 |
| **Hybrid Power-Signal** | 電源＋信号混在設計 | サーババックプレーン |

---

## ⚡ 主要用途 / Applications
- **サーバ/データセンター**: 電源バックプレーン、バスバー  
  *Server/datacenter: power backplanes, busbars*  
- **車載機器**: 12V/48V 系電源配線  
  *Automotive: 12V/48V power systems*  
- **産業機器**: 高出力モータ駆動  
  *Industrial: high-power motor drives*  
- **家電**: AC/DC入力コネクタ  
  *Consumer electronics: AC/DC input connectors*  

---

## 📏 設計パラメータ / Design Parameters
- **定格電流 (A)**: 設計電流の 1.25〜1.5 倍を確保  
  *Rated current with 25–50% safety margin*  
- **接触抵抗 (mΩ)**: 低抵抗化し、$I^2R$ 発熱を抑制  
  *Low contact resistance to reduce $I^2R$ heating*  
- **インピーダンス (mΩ)**: PDN特性に直結  
  *Affects power delivery network impedance*  
- **温度上昇 (ΔT)**: 30°C 以下を目標  
  *Limit connector temperature rise to <30°C*  
- **嵌合サイクル**: 数百〜数千回の耐久性  
  *Mating cycles in hundreds to thousands*  

---

## 🛡 実装と信頼性 / Mounting & Reliability
- **熱管理**: 電流密度が高いと局所発熱 → ヒートシンク/銅箔強化  
  *Thermal design with heatsinks or reinforced copper planes*  
- **表面処理**: 金メッキは低抵抗だが高コスト、錫めっきは酸化に注意  
  *Gold plating: low resistance, costly; tin plating: oxidation risk*  
- **振動/衝撃**: 車載・産業機器ではロック機構必須  
  *Locking mechanisms required for automotive/industrial use*  
- **腐食耐性**: 湿度・塩害環境に対応する防護設計  
  *Protection against humidity and salt spray environments*  

---

## 📝 設計指針 / Design Guidelines
- 定格電流の**1.25〜1.5倍マージン**を確保  
- **電源と信号を分離**してノイズ干渉を回避  
- **大電流経路には多ピン並列接続**を検討  
- **FEM/熱解析**で温度上昇を事前検証  

*Ensure current margin, isolate power and signals, use multi-pin paths, and validate with FEM/thermal simulations.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🧩 Board-to-Board | 基板間コネクタ<br>*Board-to-board connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |
| 🧲 RF-Coax | 高周波同軸コネクタ<br>*RF coaxial connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF-Coax/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF-Coax.md) |
| 🔌 USB-TypeC | 電源＋高速I/Oコネクタ<br>*USB Type-C connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/USB-TypeC/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/USB-TypeC.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors 全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
