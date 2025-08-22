---
layout: default
title: "Wire-to-Board | ワイヤ対基板コネクタ"
---

---

# 🧵 Wire-to-Board / ワイヤ対基板コネクタ
*Wire-to-Board Connectors*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Wire-to-Board/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Wire-to-Board.md) |

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
ワイヤ対基板コネクタ（Wire-to-Board）は、ハーネス線をプリント基板に接続するためのコネクタです。  
*Wire-to-board connectors are used to connect harness wires to printed circuit boards.*  

- 電源供給、信号配線、フィールド配線に幅広く利用される。  
- ロック機構や防水構造を持つ製品もあり、自動車・産業用途で必須。  

---

## 🧩 種類 / Types

| 種類 / Type | 特徴 / Characteristics |
|-------------|-------------------------|
| **ピンヘッダ＋ハウジング / Pin Header + Housing** | 最も一般的、2.54 mm ピッチ標準 |
| **ロック付きハウジング / Locking Housing** | 嵌合保持力を強化、車載で多用 |
| **防水コネクタ / Waterproof** | ゴムパッキン内蔵、IP67〜IP69K 対応 |
| **圧着端子 / Crimp Terminals** | 安定接触、ハーネス作業に必須 |
| **IDC（Insulation Displacement）** | ケーブルの被覆を剥がさず接続 |
| **高電流対応 / High-Current** | 大電流ライン（10A〜数十A）に使用 |

---

## ⚡ 主要用途 / Applications
- **電源供給**：DCジャック、バッテリ配線  
  *Power supply connectors for DC input, batteries*  
- **信号配線**：センサ・I/O モジュールとの接続  
  *Signal connection with sensors and I/O modules*  
- **産業機器**：PLC・モータ制御基板への配線  
  *Industrial PLCs, motor driver wiring*  
- **自動車**：ECUや車載センサ接続、防水仕様必須  
  *Automotive ECUs and sensor harnesses, waterproof required*  

---

## 📏 設計パラメータ / Design Parameters
- **ピッチ**：0.5 mm〜5.08 mm  
  *Pitch from 0.5 mm to 5.08 mm*  
- **定格電流**：0.5 A〜数十 A（サイズ依存）  
  *Rated current from 0.5 A up to tens of amperes*  
- **接触抵抗**：数 mΩ 以下が望ましい  
  *Contact resistance ideally in milliohm range*  
- **耐電圧**：数百 V クラスまで対応品あり  
  *Withstand voltage up to several hundred volts*  
- **嵌合回数**：50〜500 回が標準、産業用は 1000 回以上も存在  
  *Mating cycles typically 50–500, up to 1000+ for industrial grade*  

---

## 🛡 実装と信頼性 / Mounting & Reliability
- **はんだ実装 vs 圧着実装**：大量生産では SMT/THT、フィールドでは圧着配線。  
  *SMT/THT for mass production, crimping for field wiring.*  
- **ロック機構**：嵌合外れ防止。振動・衝撃環境で必須。  
  *Locking features prevent unmating under vibration/shock.*  
- **防水構造**：IP67〜IP69K で屋外・車載用途をカバー。  
  *Waterproof types rated IP67–IP69K for automotive and outdoor use.*  
- **劣化要因**：酸化・フレッティング摩耗 → 表面金メッキやスズ合金で対策。  
  *Oxidation and fretting mitigated by gold or tin plating.*  

---

## 📝 設計指針 / Design Guidelines
- 電源ラインは**高電流対応端子**を選定し、接触抵抗・温度上昇を検証。  
- 高振動環境では**ロック付き・二重嵌合構造**を採用。  
- フィールド交換性を考慮し、**圧着ハウジングの標準化**が望ましい。  
- 防水用途は **Oリング＋背面シール構造**を確認。  

*Select high-current terminals for power lines.  
Adopt locking/dual mating for vibration resistance.  
Standardize crimp housings for field replacement.  
Verify O-ring and rear sealing for waterproofing.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🧩 Board-to-Board | 基板間コネクタ<br>*Board-to-Board connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |
| 📜 FFC-FPC | フレキ用コネクタ<br>*FFC/FPC connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/FFC-FPC/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/FFC-FPC.md) |
| 🧲 RF-Coax | 高周波同軸コネクタ<br>*RF coaxial connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF-Coax/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF-Coax.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors 全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
