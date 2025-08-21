---
layout: default
title: "MLCC | 積層セラミックコンデンサ"
---

---

# 🔋 MLCC / 積層セラミックコンデンサ

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/mlcc/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/mlcc.md) |

---

## 📑 目次 / Table of Contents
1. [🏗 概要 / Overview](#-概要--overview)  
2. [📊 特性と課題 / Characteristics & Issues](#-特性と課題--characteristics--issues)  
3. [⚡ デカップリング設計 / Decoupling Design](#-デカップリング設計--decoupling-design)  
4. [📉 直流バイアス特性 / DC Bias Effects](#-直流バイアス特性--dc-bias-effects)  
5. [🛠 実装・レイアウト考慮 / Layout Considerations](#-実装レイアウト考慮--layout-considerations)  
6. [🧪 信頼性と試験 / Reliability & Testing](#-信頼性と試験--reliability--testing)  
7. [📏 国際規格 / Standards](#-国際規格--standards)  
8. [✅ チェックリスト / Checklist](#-チェックリスト--checklist)  
9. [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
10. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
MLCC（Multi-Layer Ceramic Capacitor, 積層セラミックコンデンサ）は、**電源デカップリング・フィルタ・高周波回路**で最も多用される受動部品です。  
*MLCCs are the most widely used passive components for decoupling, filtering, and RF circuits.*  

- サイズは 0201 (0.6×0.3 mm) 〜 1210 (3.2×2.5 mm) が主流。  
- 高誘電率系（X5R, X7R）は容量密度に優れるが直流バイアスで容量低下。  
- C0G/NPO 系は容量安定性に優れるが容量値が小さい。  

---

## 📊 特性と課題 / Characteristics & Issues

| 分類 | 温度係数 / Temp Coefficient | 特徴 / Characteristics | 課題 / Issues |
|------|-----------------------------|-------------------------|----------------|
| C0G / NP0 | ±30 ppm/°C | 高安定・低損失・RF用途 | 容量小（pF〜nF） |
| X7R | ±15% (-55〜125°C) | 広く使用、容量密度大 | DCバイアスで容量劣化 |
| X5R | ±15% (-55〜85°C) | 小型化に適す | 温度範囲狭い |
| Y5V | -82〜+22% | 超大容量MLCC | 温度/電圧安定性悪い |

*Capacitance stability and loss strongly depend on dielectric class.*  

---

## ⚡ デカップリング設計 / Decoupling Design
MLCCは **複数容量の並列配置** により、広帯域の電源ノイズ除去を行います。  

- **低周波域** → 大容量（10–100 µF）  
- **中周波域** → 中容量（1–4.7 µF）  
- **高周波域** → 小容量（0.01–0.1 µF, C0G系推奨）  

### 📐 インピーダンス近似式
$$
Z_c = \frac{1}{2 \pi f C}
$$

- f: 周波数 [Hz]  
- C: 静電容量 [F]  

> 周波数が高くなると ESL が支配的 → 実効インピーダンスは「V字カーブ」を描く。  

---

## 📉 直流バイアス特性 / DC Bias Effects
- 公称 10 µF (X5R, 6.3 V) → Vdd=3.3 V で実効 3–4 µF に低下。  
- 高電圧定格品（16 V, 25 V）を選ぶと容量劣化を緩和可能。  
- 直流バイアス低下率はメーカーの「Capacitance vs. DC Bias」曲線で確認必須。  

---

## 🛠 実装・レイアウト考慮 / Layout Considerations
- **IC電源ピン直近**に配置（寄生インダクタ最小化）。  
- **複数のGND viaで接続** → 低ESL化。  
- **BGA下配置**は有効だがリワーク性低下。  
- **サイズ混在**: 0402と0201を並列で用いるとESL分布が広がり、高周波特性が改善。  

---

## 🧪 信頼性と試験 / Reliability & Testing
- **熱衝撃試験**: リフロー後の急冷でクラック発生。  
- **曲げ試験**: 基板応力によるMLCC割れ → ソフト端子MLCCで改善。  
- **高湿バイアス試験 (85°C/85%RH)**: 絶縁抵抗劣化の有無を確認。  
- **寿命推定**: Arrhenius式により温度加速モデル化。  

---

## 📏 国際規格 / Standards
- **IEC 60384-1**: 固定コンデンサ一般規格  
- **EIA-198**: MLCCサイズコード（0201, 0402, 0603...）  
- **JEITA RC-5325**: セラミックコンデンサ特性分類  
- **AEC-Q200**: 自動車用途信頼性規格  

---

## ✅ チェックリスト / Checklist
- [ ] 容量値はDCバイアスを加味して選定したか？  
- [ ] 高周波特性に応じて容量のサイズ混在を検討したか？  
- [ ] 熱衝撃・曲げストレス対策を実装設計に盛り込んだか？  
- [ ] 車載/高信頼用途では AEC-Q200 品を採用したか？  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📏 Resistors | 抵抗器の種類と特性<br>*Types and properties of resistors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/resistors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/resistors.md) |
| 🌀 Inductors | インダクタ設計と損失要因<br>*Inductor design and loss mechanisms* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/inductors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/inductors.md) |
| ⚡ Capacitors | アルミ/タンタル/フィルム<br>*Aluminum/Tantalum/Film capacitors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/capacitors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/capacitors.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
