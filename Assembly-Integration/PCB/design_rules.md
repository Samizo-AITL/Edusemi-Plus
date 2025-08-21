---
layout: default
title: "PCB Design Rules | 設計ルール"
---

---

# 📏 PCB Design Rules / 設計ルール

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/design-rules) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/design-rules.md) |

---

## 📑 目次 / Table of Contents
1. [🏗 概要 / Overview](#-概要--overview)  
2. [🔑 主要ルール / Key Rules](#-主要ルール--key-rules)  
   - [トレース幅と間隔 / Trace Width & Spacing](#-トレース幅と間隔--trace-width--spacing)  
   - [ビア設計 / Via Design](#-ビア設計--via-design)  
   - [クリアランス / Clearance](#-クリアランス--clearance)  
   - [アスペクト比 / Aspect Ratio](#-アスペクト比--aspect-ratio)  
   - [ランドサイズ / Pad Size](#-ランドサイズ--pad-size)  
3. [📏 国際規格と基準 / Standards & Guidelines](#-国際規格と基準--standards--guidelines)  
4. [🛠 設計支援ツール / Design Aids](#-設計支援ツール--design-aids)  
5. [🎯 学習目標 / Learning Goals](#-学習目標--learning-goals)  
6. [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
7. [⬆️ Back to PCB](#️-back-to-pcb)  

---

## 🏗 概要 / Overview
PCB設計における設計ルールは、**製造可能性・信頼性・性能** を保証するための基準です。  
*Design rules in PCB layout ensure manufacturability, reliability, and performance.*  

これにはトレース幅・間隔、ビア径、クリアランス、アスペクト比、最小ランドサイズなどが含まれます。  
*Includes trace width/spacing, via diameter, clearance, aspect ratio, and minimum pad size.*  

---

## 🔑 主要ルール / Key Rules

### 🛤 トレース幅と間隔 / Trace Width & Spacing
- 電流容量とジュール発熱に基づき設計。  
  *Designed based on current capacity and Joule heating.*  
- インピーダンス制御が必要な場合は伝送線路モデルで算出。  
  *For controlled impedance, calculated using transmission line models.*  
- IPC-2221 に基づく最小値を基準にする。  
  *Minimum values follow IPC-2221 guidelines.*  

---

### 🕳 ビア設計 / Via Design
- スルーホール、ブラインド、ベリード、マイクロビアの選択。  
  *Through, blind, buried, and microvia options.*  
- アスペクト比（穴径と基板厚の比）による製造制約。  
  *Aspect ratio constraints from hole diameter vs board thickness.*  
- SI/PI を考慮したスタブ長抑制が重要。  
  *Stub length minimization is critical for SI/PI.*  

---

### ⚡ クリアランス / Clearance
- 高電圧設計では沿面距離・空間距離を規格に従い確保。  
  *For high voltage, maintain creepage and clearance per standards.*  
- 高周波設計ではクロストーク・不要結合を低減するために配慮。  
  *For high frequency, minimize crosstalk and unintended coupling.*  

---

### 📐 アスペクト比 / Aspect Ratio
- 推奨値：≦10:1（例：基板厚 1.6mm / 穴径 0.15mm → 限界近い）。  
  *Recommended ≤10:1 (e.g., 1.6mm board thickness / 0.15mm hole diameter is near limit).*  
- 高密度基板ではレーザービアや埋めビアを検討。  
  *For high-density boards, consider laser or buried vias.*  

---

### 🎯 ランドサイズ / Pad Size
- 実装信頼性に直結するため、ランド径ははんだ接合強度に合わせる。  
  *Pad diameter directly impacts solder joint reliability.*  
- BGA・CSP ではメーカー推奨ランドパターンを遵守。  
  *For BGA/CSP, follow manufacturer-recommended patterns.*  

---

## 📏 国際規格と基準 / Standards & Guidelines
- **IPC-2221**: 汎用設計ルール  
  *Generic Standard on Printed Board Design*  
- **IPC-7351**: ランドパターン設計ガイド  
  *Land Pattern Standard*  
- **IEC 60664**: 絶縁クリアランス・沿面距離規格  
  *Insulation clearance & creepage distance standard*  
- **UL 796**: プリント配線板の安全規格  
  *Safety standard for printed wiring boards*  

---

## 🛠 設計支援ツール / Design Aids
- **DRC (Design Rule Check)**: CADツールでの自動チェック。  
  *Automatic verification of rules in PCB CAD tools.*  
- **シグナルインテグリティシミュレーション**: HyperLynx, ADS, SIwave 等。  
  *Signal integrity simulations using HyperLynx, ADS, SIwave, etc.*  
- **製造側DFMルール**: PCBメーカーが提示するルールセット。  
  *DFM rules provided by PCB fabricators.*  

---

## 🎯 学習目標 / Learning Goals
- 製造と信頼性を両立するための設計ルールを理解する。  
  *Understand design rules for manufacturability and reliability.*  
- IPC/IEC 規格に基づいたクリアランス・ランド設計を習得する。  
  *Learn clearance and pad design based on IPC/IEC standards.*  
- DRCとシミュレーションを活用した設計フローを構築できる。  
  *Establish design flow using DRC and simulations.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📑 Stack-up | 層構成と設計ルールの関係<br>*Layer stack-up vs design rules* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./stackup.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](../PCB/stackup) |
| 🕳 Via Design | ビア設計ルール<br>*Rules for via design* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./via-design.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](../PCB/via-design) |
| 📏 Impedance Control | トレース幅・間隔とインピーダンス<br>*Trace geometry & impedance* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./impedance-control.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](../PCB/impedance-control) |
| 🛠 Assembly | 実装に直結する設計ルール<br>*Design rules affecting assembly* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./assembly.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](../PCB/assembly) |

---

## ⬆️ Back to PCB

| Link | Badge |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |
