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
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Resistors) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Resistors.md) |

---

## 📑 目次 / Table of Contents
1. [🏗 概要 / Overview](#-概要--overview)  
2. [🔎 種類 / Types](#-種類--types)  
3. [📏 主要パラメータ / Key Parameters](#-主要パラメータ--key-parameters)  
4. [🧮 電気特性と数式 / Electrical Characteristics & Formulas](#-電気特性と数式--electrical-characteristics--formulas)  
5. [⚙️ 代表用途 / Applications](#-代表用途--applications)  
6. [🧵 設計上の考慮事項 / Design Considerations](#-設計上の考慮事項--design-considerations)  
7. [🛡 信頼性と故障モード / Reliability & Failure Modes](#-信頼性と故障モード--reliability--failure-modes)  
8. [🎯 学習目標 / Learning Goals](#-学習目標--learning-goals)  
9. [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
10. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
抵抗器は最も基本的な受動部品であり、**電流制御、電圧分圧、終端、バイアス設定**などに不可欠です。  
*Resistors are the most fundamental passive components, essential for current limiting, voltage division, termination, and biasing.*  

---

## 🔎 種類 / Types

### 🟤 カーボン抵抗 / Carbon Composition
- 炭素粉末と樹脂を混合した抵抗体。  
  *Resistive element made of carbon powder and resin mixture.*  
- 安価だが温度係数とノイズが大きく、精度が低い（±5〜10%）。  
  *Low-cost, but high noise and poor accuracy (±5–10%).*  
- 過去の一般用途に広く使われたが、現在は限定用途。  
  *Once widely used, now limited to niche applications.*  

### 🔵 金属皮膜抵抗 / Metal Film
- 金属膜をガラス基板に形成。  
  *Metal film deposited on glass substrate.*  
- 高精度 (±0.1〜1%)、低ノイズ、温度係数が小さい。  
  *High accuracy (±0.1–1%), low noise, small temp. coefficient.*  
- 信号処理回路や計測器に最適。  
  *Used in signal processing and instrumentation.*  

### 🌀 巻線抵抗 / Wirewound
- 金属線を絶縁体に巻いた構造。  
  *Constructed by winding metal wire on insulator.*  
- 高精度・高電力（数W〜数百W）対応。  
  *Supports high accuracy and high power (several W–hundreds W).*  
- インダクタンスを持つため高周波用途には不適。  
  *Inductive nature unsuitable for high-frequency circuits.*  

### ⚪ チップ抵抗 / Chip (SMD)
- 小型化に優れ、表面実装用。  
  *Compact, suitable for surface mounting.*  
- 高周波特性良好で量産に最適。  
  *Good high-frequency characteristics, ideal for mass production.*  
- サイズ：0201〜2512、定格電力はサイズ依存。  
  *Sizes from 0201 to 2512; power rating depends on size.*  

### 🟡 特殊抵抗 / Special Types
- **シャント抵抗 (Shunt)**：電流検出用、低抵抗（mΩ領域）。  
  *Shunt resistors for current sensing, very low resistance (mΩ).*  
- **サーミスタ (Thermistor)**：温度依存型（NTC/PTC）。  
  *Thermistors with temperature-dependent resistance (NTC/PTC).*  
- **可変抵抗 (Potentiometer, VR)**：調整用。  
  *Variable resistors for tuning circuits.*  
- **フォトレジスタ (CdS, LDR)**：光依存型。  
  *Light-dependent resistors for optical sensing.*  

---

## 📏 主要パラメータ / Key Parameters

| パラメータ / Parameter | 意味 / Meaning |
|----------------|-------------------------------|
| 抵抗値 (Ω) / Resistance | 電流制御値 / *Resistance value controlling current* |
| 許容差 (%) / Tolerance | 公称値に対する誤差範囲 / *Deviation from nominal value* |
| 定格電力 (W) / Power Rating | 発熱許容能力 / *Power handling capability* |
| 温度係数 (ppm/°C) / Temp. Coefficient | 抵抗値の温度依存性 / *Temperature dependence of resistance* |
| ノイズ特性 / Noise | 材料起因の雑音 / *Noise due to material* |
| 最大動作電圧 / Max Operating Voltage | 安全動作範囲 / *Safe operating voltage* |

---

## 🧮 電気特性と数式 / Electrical Characteristics & Formulas
- **オームの法則 / Ohm’s Law**  
  *Defines relationship between voltage, current, resistance.*  

$$
V = IR
$$

- **ジュール熱 / Joule Heating**  
  *Heat dissipation in resistor.*  

$$
P = I^2 R = \frac{V^2}{R}
$$

- **分圧回路 / Voltage Divider**  
  *Voltage division between two resistors.*  

$$
V_{out} = V_{in} \cdot \frac{R_2}{R_1 + R_2}
$$

---

## ⚙️ 代表用途 / Applications
- **電流制御**：LED点灯制御、回路保護  
  *Current limiting for LEDs, circuit protection*  
- **分圧回路**：ADC基準電圧生成  
  *Voltage division for ADC references*  
- **終端抵抗**：高速信号のインピーダンス整合  
  *Line termination for impedance matching in high-speed signals*  
- **センシング**：シャント抵抗による電流検出  
  *Current sensing with shunt resistors*  
- **温度補償**：サーミスタによる温度制御  
  *Temperature compensation using thermistors*  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **発熱**：$P = I^2R$ により発熱するため定格電力に注意。  
  *Watch resistor heating due to $P = I^2R$, select suitable rating.*  
- **公差**：精密回路では ±1% 以下を選択。  
  *Choose ≤ ±1% tolerance for precision circuits.*  
- **寄生要素**：高周波では配線インダクタンス・寄生容量を考慮。  
  *Consider parasitic inductance and capacitance at high frequency.*  
- **フットプリント**：実装密度と放熱設計を両立。  
  *Balance footprint density and thermal dissipation in PCB layout.*  

---

## 🛡 信頼性と故障モード / Reliability & Failure Modes
- **開回路**：長期ストレスで抵抗体が断線。  
  *Open circuit from long-term stress.*  
- **抵抗値変動**：高温・湿度で抵抗値が変動。  
  *Resistance drift under high temp/humidity.*  
- **過熱劣化**：電力過大印加による焼損。  
  *Burnout due to excessive power dissipation.*  
- **はんだクラック**：熱サイクルや振動で発生。  
  *Solder joint cracks from thermal cycling or vibration.*  

---

## 🎯 学習目標 / Learning Goals
- 抵抗器の種類と特徴を理解する。  
  *Understand resistor types and characteristics.*  
- 主要パラメータと設計上の注意点を説明できる。  
  *Explain key parameters and design considerations.*  
- 実際の応用（終端、分圧、電流検出）に適用できる。  
  *Apply resistors in real applications (termination, division, sensing).*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| ⚡ Capacitors | 電荷蓄積とフィルタリング<br>*Charge storage and filtering* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Capacitors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Capacitors.md) |
| 🌀 Inductors | 磁束蓄積とフィルタリング<br>*Magnetic flux storage and filtering* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/inductors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/inductors.md) |
| 🔧 Passive Design | 受動部品の組合せ・最適化<br>*Design optimization using passives* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/passive-design/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/passive-design.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
