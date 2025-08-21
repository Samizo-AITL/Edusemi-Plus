---
layout: default
title: "PCB Routing | 配線"
---

---

# 🛤 PCB Routing / 配線

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|---------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/routing/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/routing.md) |

---

## 📑 目次 / Table of Contents
1. [🏗 概要 / Overview](#-概要--overview)  
2. [🔑 主要ルール / Key Routing Practices](#-主要ルール--key-routing-practices)  
   - [📏 インピーダンス制御 / Impedance Control](#-インピーダンス制御--impedance-control)  
   - [🔀 差動配線 / Differential Pair Routing](#-差動配線--differential-pair-routing)  
   - [⚡ クロストーク抑制 / Crosstalk Mitigation](#-クロストーク抑制--crosstalk-mitigation)  
   - [🏗 層間配線 / Multi-Layer Routing](#-層間配線--multi-layer-routing)  
   - [🔋 電源/グラウンド設計 / Power & Ground Design](#-電源グラウンド設計--power--ground-design)  
3. [🛠 実務上の考慮事項 / Practical Considerations](#-実務上の考慮事項--practical-considerations)  
4. [📏 国際規格 / Standards](#-国際規格--standards)  
5. [🎯 学習目標 / Learning Goals](#-学習目標--learning-goals)  
6. [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
7. [⬆️ Back to PCB](#️-back-to-pcb)  

---

## 🏗 概要 / Overview
PCB配線 (Routing) は、デバイス間の信号・電源を基板上で最適に結線する工程です。  
*PCB routing is the process of optimally connecting signals and power between devices on the board.*  

インピーダンス制御、差動配線、クロストーク対策、層間配線、電源/グラウンドプレーン設計を含みます。  
*Includes impedance control, differential routing, crosstalk mitigation, inter-layer routing, and power/ground plane design.*  

---

## 🔑 主要ルール / Key Routing Practices

### 📏 インピーダンス制御 / Impedance Control
- トレース幅・間隔・層構成を基に特性インピーダンスを制御。  
- 高速バス (PCIe, DDR, USB3.x) は 50Ω / 100Ω 差動を標準化。  
- スタブを避け、反射を低減する設計が必須。  

*Controlled by trace width, spacing, and stackup.  
High-speed buses (PCIe, DDR, USB3.x) typically require 50Ω single-ended / 100Ω differential.  
Avoid stubs and reflections to maintain signal quality.*  

---

### 🔀 差動配線 / Differential Pair Routing
- ペア長を揃える「スキュー制御」が必須。  
- 配線はできるだけ近接させ、外乱に対する共通モード抑制を狙う。  
- ビアの使用は最小化し、左右対称に配置。  

*Requires length matching (skew control).  
Keep pairs close for common-mode noise rejection.  
Minimize vias and use symmetry when unavoidable.*  

---

### ⚡ クロストーク抑制 / Crosstalk Mitigation
- 配線間距離をトレース幅の **3倍以上** 確保。  
- 高速ラインはシールドグラウンド隣接が望ましい。  
- 並走配線を避け、層を跨いで直交配置。  

*Maintain at least 3× trace-width spacing.  
Route near ground shields for critical high-speed lines.  
Avoid parallel runs; use orthogonal layer routing.*  

---

### 🏗 層間配線 / Multi-Layer Routing
- 信号層と GND 層を交互に積層してリターンパスを安定化。  
- 内層配線でノイズを低減し、外層は主に低速信号・部品接続に使用。  
- クロストークと EMI 対策として電源/GND プレーンを挟む構成が効果的。  

*Alternate signal and ground layers for stable return paths.  
Use inner layers for high-speed routing; outer layers for slower signals/components.  
Power-ground planes between signal layers reduce EMI and crosstalk.*  

---

### 🔋 電源/グラウンド設計 / Power & Ground Design
- グラウンドは連続面で確保し、スリットや分割を避ける。  
- 電源プレーンはデカップリングコンデンサ配置とセットで設計。  
- 電源/GND 間のインピーダンスを最小化し、PI を安定化。  

*Ground planes should be continuous without splits.  
Power planes require decoupling capacitors for stability.  
Minimize power/ground impedance to maintain PI.*  

---

## 🛠 実務上の考慮事項 / Practical Considerations
- **BGA配線**: ファンアウトパターンとビア方式（スルーホール vs マイクロビア）。  
- **クロック配線**: 最短・対称・周辺ノイズ源から隔離。  
- **高速バス**: バス間 skew、シミュレーションによるタイミング検証。  
- **EMI/EMC**: リターンパス制御・フェラビーズ活用・シールド強化。  

---

## 📏 国際規格 / Standards
- **IPC-2221**: 汎用PCB設計規格 / *Generic PCB design standard*  
- **IPC-2141**: 伝送線路設計ガイドライン / *Design guide for high-speed transmission lines*  
- **JEDEC JESD-8**: 高速I/O規格に基づく配線設計 / *Wiring design per JEDEC high-speed I/O standards*  
- **IEC 61000**: EMC 適合性基準 / *EMC compliance standards*  

---

## 🎯 学習目標 / Learning Goals
- 高速信号と電源配線の最適化ルールを理解する。  
  *Understand optimization rules for high-speed signal and power routing.*  
- 差動配線・インピーダンス制御の実装を習得する。  
  *Learn implementation of differential pairs and impedance control.*  
- EMI/EMC 対策を踏まえた多層配線設計を実践できる。  
  *Apply multi-layer routing with EMI/EMC considerations.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📐 Stack-up | 層構成の設計指針<br>*PCB layer stack-up guidelines* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/stackup/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/stackup.md) |
| 📏 Design Rules | 設計ルール<br>*PCB design rules* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/design_rules/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/design_rules.md) |
| 🕳 Via Design | ビアの種類と設計指針<br>*Types of vias and design guidelines* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/via-design/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/via-design.md) |
| ✅ Validation | 解析・検証プロセス<br>*Validation and verification processes* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/validation/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/validation.md) |

---

## ⬆️ Back to PCB

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | PCB全体ページへ戻る<br>*Back to PCB site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |
