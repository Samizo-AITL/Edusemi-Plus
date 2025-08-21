---
layout: default
title: "Resistors | 抵抗器"
---

---

# 🔩 Resistors / 抵抗器

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/resistors) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/resistors.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [種類 / Types](#-種類--types)  
   - [カーボン抵抗 / Carbon Composition](#-カーボン抵抗--carbon-composition)  
   - [金属皮膜抵抗 / Metal Film](#-金属皮膜抵抗--metal-film)  
   - [巻線抵抗 / Wirewound](#-巻線抵抗--wirewound)  
   - [チップ抵抗 / Chip (SMD)](#-チップ抵抗--chip-smd)  
   - [特殊抵抗 / Special Types](#-特殊抵抗--special-types)  
3. [主要パラメータ / Key Parameters](#-主要パラメータ--key-parameters)  
4. [電気特性と数式 / Electrical Characteristics & Formulas](#-電気特性と数式--electrical-characteristics--formulas)  
5. [代表用途 / Applications](#-代表用途--applications)  
6. [設計上の考慮事項 / Design Considerations](#-設計上の考慮事項--design-considerations)  
7. [信頼性と故障モード / Reliability & Failure Modes](#-信頼性と故障モード--reliability--failure-modes)  
8. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
9. [関連リンク / Related Links](#-関連リンク--related-links)  
10. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
抵抗器は最も基本的な受動部品であり、**電流制御、電圧分圧、終端、バイアス設定**などに不可欠です。  
*Resistors are the most fundamental passive components, essential for current limiting, voltage division, termination, and biasing.*  

---

## 🔎 種類 / Types

### 🟤 カーボン抵抗 / Carbon Composition
- 炭素粉末と樹脂を混合した抵抗体。  
- 安価だが温度係数とノイズが大きく、精度が低い（±5〜10%）。  
- 過去の一般用途に広く使われたが、現在は限定用途。  

### 🔵 金属皮膜抵抗 / Metal Film
- 金属膜をガラス基板に形成。  
- 高精度 (±0.1〜1%)、低ノイズ、温度係数が小さい。  
- 信号処理回路や計測器に最適。  

### 🌀 巻線抵抗 / Wirewound
- 金属線を絶縁体に巻いた構造。  
- 高精度・高電力（数W〜数百W）対応。  
- インダクタンスを持つため高周波用途には不適。  

### ⚪ チップ抵抗 / Chip (SMD)
- 小型化に優れ、表面実装用。  
- 高周波特性良好で量産に最適。  
- サイズ：0201〜2512、定格電力はサイズ依存。  

### 🟡 特殊抵抗 / Special Types
- **シャント抵抗 (Shunt)**：電流検出用、低抵抗（mΩ領域）。  
- **サーミスタ (Thermistor)**：温度依存型（NTC/PTC）。  
- **可変抵抗 (Potentiometer, VR)**：調整用。  
- **フォトレジスタ (CdS, LDR)**：光依存型。  

---

## 📏 主要パラメータ / Key Parameters

| パラメータ / Parameter | 意味 / Meaning |
|----------------|-------------------------------|
| 抵抗値 (Ω) / Resistance | 電流制御値 |
| 許容差 (%) / Tolerance | 公称値に対する誤差範囲 |
| 定格電力 (W) / Power Rating | 発熱許容能力 |
| 温度係数 (ppm/°C) / Temp. Coefficient | 抵抗値の温度依存性 |
| ノイズ特性 / Noise | 材料起因の雑音 |
| 最大動作電圧 / Max Operating Voltage | 安全動作範囲 |

---

## 🧮 電気特性と数式 / Electrical Characteristics & Formulas

- **オームの法則 / Ohm’s Law**  

$$
V = IR
$$

- **ジュール熱 / Joule Heating**  

$$
P = I^2 R = \frac{V^2}{R}
$$

- **分圧回路 / Voltage Divider**  

$$
V_{out} = V_{in} \cdot \frac{R_2}{R_1 + R_2}
$$

---

## ⚙️ 代表用途 / Applications
- **電流制御**：LED点灯制御、回路保護  
- **分圧回路**：ADC基準電圧生成  
- **終端抵抗**：高速信号のインピーダンス整合  
- **センシング**：シャント抵抗による電流検出  
- **温度補償**：サーミスタによる温度制御  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **発熱**：$P = I^2R$ により発熱するため定格電力に注意。  
- **公差**：精密回路では ±1% 以下を選択。  
- **寄生要素**：高周波では配線インダクタンス・寄生容量を考慮。  
- **フットプリント**：実装密度と放熱設計を両立。  

---

## 🛡 信頼性と故障モード / Reliability & Failure Modes
- **開回路**：長期ストレスで抵抗体が断線。  
- **抵抗値変動**：高温・湿度で抵抗値が変動。  
- **過熱劣化**：電力過大印加による焼損。  
- **はんだクラック**：熱サイクルや振動で発生。  

---

## 🎯 学習目標 / Learning Goals
- 抵抗器の種類と特徴を理解する。  
- 主要パラメータと設計上の注意点を説明できる。  
- 実際の応用（終端、分圧、電流検出）に適用できる。  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| ⚡ Capacitors | 電荷蓄積とフィルタリング<br>*Charge storage and filtering* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/capacitors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/capacitors.md) |
| 🌀 Inductors | 磁束蓄積とフィルタリング<br>*Magnetic flux storage and filtering* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/inductors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/inductors.md) |
| 🔧 Passive Design | 受動部品の組合せ・最適化<br>*Design optimization using passives* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/passive-design/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/passive-design.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
