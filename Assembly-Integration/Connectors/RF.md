---
layout: default
title: "RF Connectors | 高周波コネクタ"
---

---

# 🛰 RF Connectors / 高周波コネクタ
*Connectors for RF and high-frequency applications*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/RF/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/RF.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [用途 / Applications](#-用途--applications)  
3. [種類 / Types](#-種類--types)  
4. [主要パラメータ / Key Parameters](#-主要パラメータ--key-parameters)  
5. [設計考慮事項 / Design Considerations](#-設計考慮事項--design-considerations)  
6. [材料とメッキ / Materials & Plating](#-材料とメッキ--materials--plating)  
7. [信頼性と試験 / Reliability & Testing](#-信頼性と試験--reliability--testing)  
8. [国際規格 / Standards](#-国際規格--standards)  
9. [学習目標 / Learning Goals](#-学習目標--learning-goals)  
10. [関連リンク / Related Links](#-関連リンク--related-links)  
11. [⬆️ Back to Connectors](#️-back-to-connectors)  

---

## 🏗 概要 / Overview
RFコネクタは、**高周波信号の伝送**に特化し、**50Ω/75Ω のインピーダンス整合**、**低反射 (VSWR)**、**低損失 (Insertion Loss)** を実現するように設計されています。  
*RF connectors are designed for high-frequency transmission, ensuring impedance matching, low reflection, and low insertion loss.*  

主な用途は、**通信（5G/6G, Wi-Fi, 衛星通信）**、**車載レーダ**、**測定機器**、**航空宇宙** です。  

---

## 🎯 用途 / Applications
- **無線通信機器**：基地局、アンテナ接続、RFモジュール  
  *Base stations, antenna connections, RF modules*  
- **計測器**：VNA（ベクトルネットワークアナライザ）、スペアナ  
  *VNAs, spectrum analyzers*  
- **車載**：24GHz / 77GHz レーダ、V2X 通信  
  *Automotive radar and V2X communication*  
- **航空宇宙/衛星**：耐環境・高信頼性コネクタ  
  *Aerospace and satellite high-reliability connectors*  

---

## 🧩 種類 / Types
| 種類 / Type | 構造・特徴 / Structure & Characteristics | 周波数範囲 / Frequency Range |
|-------------|-------------------------------------------|-----------------------------|
| **SMA** | 最も普及。18GHz対応、精密タイプは26.5GHz | *DC–18/26.5 GHz* |
| **SMB / SMC** | 小型、着脱容易。SMCはねじ固定 | *SMB: DC–4 GHz / SMC: DC–10 GHz* |
| **BNC** | ベイオネットロック。計測用途中心 | *DC–4 GHz* |
| **N型** | 大電力対応、低損失。11GHzまで | *DC–11 GHz* |
| **MCX / MMCX** | 超小型、携帯端末向け | *DC–6 GHz* |
| **QMA** | スナップオン式、組立効率大 | *DC–6 GHz* |
| **2.92 mm (K)** | 精密測定、40GHz対応 | *DC–40 GHz* |
| **2.4 mm / 1.85 mm (V)** | ミリ波帯用、50GHz/65GHz | *DC–50–65 GHz* |
| **1.0 mm / 0.8 mm** | 110GHz超対応、研究用途 | *DC–110 GHz* |

---

## 📊 主要パラメータ / Key Parameters
- **特性インピーダンス (Characteristic Impedance)**  
  50Ωが標準（通信・RF）、75Ωは放送/映像向け  
  *50Ω for RF/comm, 75Ω for broadcast/video*  

- **VSWR (Voltage Standing Wave Ratio)**  
  理想は 1.0、実際は <1.2 (SMA)、<1.05 (高精度品)  
  *Ideally 1.0, typically <1.2 (SMA), <1.05 (precision connectors)*  

- **挿入損失 (Insertion Loss)**  
  $$ IL(dB) = -20 \log \frac{V_{out}}{V_{in}} $$  
  *Defines signal attenuation through the connector*  

- **自己共振点 (SRF)**  
  GHz帯でのインダクタンスと容量の共振周波数  
  *Self-resonant frequency of connector parasitics*  

- **耐久性 (Mating Cycles)**  
  通常 500回〜2000回、試験用精密コネクタは100回程度  
  *500–2000 cycles, precision connectors ~100 cycles*  

---

## 🛠 設計考慮事項 / Design Considerations
- **PCBフットプリント**：パッド形状・GND via配置でインピーダンス連続性を確保  
  *Ensure impedance continuity with optimized footprint and GND vias*  
- **リターンパス設計**：複数のグラウンドvia配置で電流ループ最小化  
  *Use multiple ground vias for minimized return path*  
- **接触抵抗**：表面酸化・汚染による劣化を考慮  
  *Consider degradation from oxidation/contamination*  
- **周波数依存性**：40GHz以上では機械寸法誤差もSパラ特性に影響  
  *At >40GHz, even small machining tolerances affect S-parameters*  

---

## ⚙️ 材料とメッキ / Materials & Plating
- **中心導体**：金メッキ銅合金  
  *Gold-plated copper alloy for conductivity and durability*  
- **外部シェル**：真鍮 (Brass)、ステンレス鋼  
  *Brass or stainless steel for strength and shielding*  
- **絶縁体**：PTFE（低誘電率、低損失）、PEEK（高耐熱）  
  *PTFE (low-loss), PEEK (high-heat applications)*  
- **表面処理**：金メッキ (耐腐食・低接触抵抗)、銀 (低損失)  
  *Gold plating (corrosion resistance), Silver (low loss)*  

---

## 🛡 信頼性と試験 / Reliability & Testing
- **熱衝撃試験**：-40〜+125℃ サイクルで性能確認  
  *Thermal cycling test from -40°C to +125°C*  
- **機械耐久**：挿抜繰返し後のVSWR変動評価  
  *Check VSWR after repeated mating cycles*  
- **振動・衝撃試験**：車載/航空宇宙用で必須  
  *Required for automotive and aerospace applications*  
- **湿度試験 (85/85)**：高温高湿で絶縁抵抗劣化を確認  
  *85°C/85%RH test for insulation reliability*  

---

## 📏 国際規格 / Standards
- **IEC 61169**: RFコネクタの規格全般  
  *IEC standard for RF coaxial connectors*  
- **MIL-STD-348**: コネクタ寸法・インタフェース規格  
  *Military standard for RF connector interfaces*  
- **ISO 19642**: 車載用途コネクタ規格  
  *Automotive RF connector standards*  
- **IEEE 287**: 精密高周波コネクタ規格 (mm-wave)  
  *IEEE standard for precision coaxial connectors*  

---

## 🎯 学習目標 / Learning Goals
- 各種RFコネクタの **周波数対応と用途** を理解する。  
  *Understand frequency range and applications of RF connectors.*  
- **VSWR / Insertion Loss / Impedance** の関係を説明できる。  
  *Explain relationships among VSWR, insertion loss, and impedance.*  
- 材料・メッキ・構造が **高周波特性と信頼性** に与える影響を把握する。  
  *Grasp how materials, plating, and structure affect RF performance.*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🧩 Board-to-Board | 基板間コネクタ<br>*Board-to-board connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Board-to-Board/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Board-to-Board.md) |
| 🔋 Power Connectors | 電源コネクタ<br>*Power connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/Power/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Connectors/Power.md) |
| 🔌 Connectors | コネクタ全体カテゴリ<br>*Overview of connectors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) <br> [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |

---

## ⬆️ Back to Connectors

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Connectors全体ページへ戻る<br>*Back to Connectors site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Connectors/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to Connectors repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Connectors) |
