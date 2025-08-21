---
layout: default
title: "Capacitors | コンデンサ"
---

---

# ⚡ Capacitors / コンデンサ

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Capacitors) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Capacitors.md) |

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
コンデンサは、**電荷の蓄積・放出、AC結合、フィルタリング、安定化** などに用いられる代表的な受動部品です。  
*Capacitors are passive components used for charge storage, AC coupling, filtering, and stabilization.*  

---

## 🔎 種類 / Types

### 🟤 セラミックコンデンサ / Ceramic Capacitors
- 誘電体にセラミックを使用。  
  *Dielectric made of ceramic material.*  
- 小型・低ESRで高周波特性に優れる。  
  *Compact, low ESR, excellent high-frequency performance.*  
- Class 1（NP0, C0G）: 高安定・低損失  
  *Class 1 (NP0, C0G): high stability, low loss*  
- Class 2（X7R, Y5V）: 大容量・温度依存性あり  
  *Class 2 (X7R, Y5V): larger capacitance, temperature-dependent*  

### 🔵 電解コンデンサ / Electrolytic Capacitors
- アルミ電解：大容量・低コスト、リプル吸収用。  
  *Aluminum electrolytic: large capacitance, low cost, ripple absorption.*  
- タンタル電解：安定した容量、低ESR、ただし高価。  
  *Tantalum electrolytic: stable, low ESR, but expensive.*  
- 極性あり、逆電圧に弱い。  
  *Polarized, sensitive to reverse voltage.*  

### 🟡 フィルムコンデンサ / Film Capacitors
- プラスチックフィルムを誘電体に使用。  
  *Plastic film as dielectric.*  
- 安定性・耐圧に優れ、オーディオ・電源用途に最適。  
  *Good stability and voltage handling; used in audio and power circuits.*  

### ⚪ スーパーキャパシタ / Supercapacitors
- 大容量（Fレベル）、電源バックアップ用途。  
  *Very large capacitance (farads), for backup power.*  
- 高ESRで高周波用途には不向き。  
  *High ESR, unsuitable for high-frequency use.*  

---

## 📏 主要パラメータ / Key Parameters

| パラメータ / Parameter | 意味 / Meaning |
|----------------|-------------------------------|
| 静電容量 (F) / Capacitance | 電荷を蓄積する能力 / *Charge storage capacity* |
| 定格電圧 (V) / Rated Voltage | 最大印加可能電圧 / *Maximum applied voltage* |
| ESR (Ω) / Equivalent Series Resistance | 内部抵抗、リプル特性に影響 / *Series resistance affecting ripple* |
| ESL (nH) / Equivalent Series Inductance | 高周波での特性劣化要因 / *Inductance affecting high-frequency performance* |
| 温度特性 / Temp. Coefficient | 容量変動率 / *Variation of capacitance with temperature* |
| リプル電流 / Ripple Current | 許容交流電流 / *Allowable AC current* |

---

## 🧮 電気特性と数式 / Electrical Characteristics & Formulas
- **容量と電荷 / Capacitance and Charge**  

$$
Q = C \cdot V
$$

- **エネルギー蓄積 / Stored Energy**  

$$
E = \tfrac{1}{2} C V^2
$$

- **インピーダンス特性 / Impedance**  

$$
Z = \frac{1}{j \omega C}
$$

---

## ⚙️ 代表用途 / Applications
- **デカップリング**：IC電源の安定化  
  *Decoupling for IC power stabilization*  
- **カップリング**：信号ラインの直流カット  
  *AC coupling between signal stages*  
- **フィルタリング**：ノイズ低減、電源リップル除去  
  *Noise suppression and power ripple filtering*  
- **タイミング回路**：RC時定数の形成  
  *Forming RC time constants in circuits*  
- **エネルギー保持**：スーパーキャパシタによるバックアップ電源  
  *Backup power using supercapacitors*  

---

## 🧵 設計上の考慮事項 / Design Considerations
- **定格電圧**：印加電圧の2倍程度のマージンを確保。  
  *Ensure ~2× margin of rated voltage over applied voltage.*  
- **ESR/ESL**：スイッチング電源やRF回路では低ESR/低ESL品を選択。  
  *Select low-ESR/low-ESL types for switching and RF circuits.*  
- **温度特性**：セラミックClass 2は容量変動が大きい。  
  *Ceramic Class 2 capacitors exhibit large capacitance variation with temperature.*  
- **寿命**：電解コンデンサは乾燥劣化に注意。  
  *Electrolytic capacitors degrade over time due to electrolyte drying.*  

---

## 🛡 信頼性と故障モード / Reliability & Failure Modes
- **短絡**：絶縁破壊によりショート。  
  *Short circuit due to dielectric breakdown.*  
- **容量抜け**：電解液乾燥や誘電体劣化による容量低下。  
  *Capacitance loss from electrolyte drying or dielectric degradation.*  
- **ESR上昇**：高温劣化で発熱しやすくなる。  
  *ESR increases with aging, leading to overheating.*  
- **リーク電流増加**：極性部品で逆電圧印加時に顕著。  
  *Leakage current increases, especially under reverse voltage.*  

---

## 🎯 学習目標 / Learning Goals
- 各種コンデンサの種類と特性を理解する。  
  *Understand capacitor types and their characteristics.*  
- ESR/ESLなど周波数依存特性を説明できる。  
  *Explain frequency-dependent characteristics such as ESR and ESL.*  
- フィルタ・デカップリング設計に応用できる。  
  *Apply capacitors in filtering and decoupling design.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🔩 Resistors | 電流制御・分圧用途<br>*For current limiting and voltage division* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/resistors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/resistors.md) |
| 🌀 Inductors | 磁束エネルギー蓄積・フィルタリング<br>*Magnetic flux storage and filtering* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/inductors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/inductors.md) |
| 🔧 Passive Design | 受動部品設計最適化<br>*Design optimization with passives* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/passive-design/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/passive-design.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
