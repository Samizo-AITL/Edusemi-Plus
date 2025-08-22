---
layout: default
title: "Board-to-Board | 基板間コネクタ"
---

---

# 🧩 Board-to-Board / 基板間コネクタ
*High-speed interconnects for dense PCB assemblies*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |

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
Board-to-Board コネクタは、**複数基板を物理的かつ電気的に接続**するためのコネクタです。  
*Board-to-board connectors provide both physical and electrical interconnects between multiple PCBs.*  

高速信号伝送、電源ライン供給、実装密度向上のために広く用いられます。  
*They are widely used for high-speed signal transmission, power delivery, and compact system integration.*  

---

## 🎯 用途 / Applications
- **モジュール間インターフェース**：CPU基板と拡張ボード  
  *Inter-module interface such as CPU boards and daughter cards*  
- **高速バス伝送**：PCIe, USB4, MIPI, DDR インターフェース  
  *High-speed bus connections such as PCIe, USB4, MIPI, DDR*  
- **省スペース実装**：スマートフォン、IoT機器  
  *Space-saving assemblies for smartphones and IoT devices*  
- **産業機器・車載**：耐振動・耐環境構造  
  *Industrial and automotive applications requiring vibration resistance*
- **LVDSインターフェース**：LCDパネルやカメラモジュール接続  
  *LVDS interface for LCD panels and camera modules*

---

## 🧩 種類 / Types
| 種類 / Type | 構造・用途 / Structure & Use | 特徴 / Characteristics |
|-------------|-------------------------------|-------------------------|
| **スタッキング型 / Stacking** | 基板を垂直方向に積層 / *Vertical stacking of PCBs* | 電源・信号接続両用 / *For both power and signals* |
| **メザニン型 / Mezzanine** | 平行基板接続 / *Parallel board connection* | 高速信号対応、シールド可能 / *Supports high-speed signals with shielding* |
| **カードエッジ型 / Card Edge** | 基板エッジ接点 / *Edge contacts on PCB* | 高電流・拡張カード向け / *Suitable for high-current and expansion cards* |
| **フローティング型 / Floating** | コネクタ位置ずれ吸収 / *Absorbs misalignment* | 耐振動・組立誤差吸収 / *Vibration resistance and assembly tolerance* |

---

## 📊 主要パラメータ / Key Parameters
- **定格電流 / Current Rating**  
  *Maximum current capacity per pin*  
- **特性インピーダンス / Characteristic Impedance**  
  *Impedance control for high-speed signals*  
- **挿抜寿命 / Mating Cycles**  
  *Durability defined by number of mating operations*  
- **接触抵抗 / Contact Resistance**  
  *Resistance at connector contact points*  
- **耐電圧 / Voltage Rating**  
  *Maximum voltage withstand capability*  
- **動作温度範囲 / Operating Temperature Range**  
  *Temperature limits for reliable operation*  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **高速信号**：差動ペアのインピーダンス整合必須。  
  *Differential pair impedance matching is mandatory for high-speed signals.*  
- **電源供給**：複数ピン並列化で低インピーダンス化。  
  *Use parallel power pins to reduce impedance.*  
- **組立誤差吸収**：フローティング構造により実装ずれを吸収。  
  *Floating structures improve tolerance to assembly errors.*  
- **EMI対策**：シールド付きタイプを利用。  
  *Use shielded mezzanine connectors for EMI reduction.*
- **LVDS差動信号**：100 Ω差動インピーダンス維持とスキュー管理が必須。  
  *Maintain 100 Ω differential impedance and control skew for LVDS signals.*

---

## 🛡 信頼性と試験 / Reliability & Testing
- **温度サイクル試験**：接触抵抗の変動確認。  
  *Evaluate contact resistance under thermal cycling.*  
- **振動試験**：フローティング構造の有効性確認。  
  *Verify floating connectors under vibration tests.*  
- **湿度試験**：腐食や劣化を評価。  
  *Assess corrosion and degradation under humidity.*  
- **挿抜耐久試験**：規定サイクル後の性能維持を確認。  
  *Confirm performance after specified mating cycles.*  

---

## 🎯 学習目標 / Learning Goals
- 各種 Board-to-Board コネクタの特徴を理解する。  
  *Understand the characteristics of various board-to-board connectors.*  
- 高速信号・電源供給における設計考慮点を説明できる。  
  *Explain design considerations for high-speed and power delivery.*  
- 信頼性試験を設計に反映できる。  
  *Apply reliability testing results to design decisions.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🔌 Connectors | コネクタカテゴリ全体<br>*Overview of connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
| 🔋 Power Connectors | 電源用コネクタ<br>*Power connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |
| 🛰 RF Connectors | 高周波用コネクタ<br>*RF connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF.md) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to Connectors repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
