---
layout: default
title: "PCB Materials | 材料"
---

---

# 🧪 PCB Materials / 材料

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/materials) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/materials.md) |

---

## 📑 目次 / Table of Contents
- [🏗 概要 / Overview](#-概要--overview)  
- [🎯 設計ゴール / Design-Targets](#-設計ゴール--design-targets)  
- [🔑 キートピック / Key-Topics](#-キートピック--key-topics)  
- [📊 代表的材料 / Typical-Materials](#-代表的材料--typical-materials)  
- [🧮 電気特性と数式 / Electrical-Properties--Formulas](#-電気特性と数式--electrical-properties--formulas)  
- [🔥 熱特性 / Thermal-Properties](#-熱特性--thermal-properties)  
- [🌱 環境規格 / Environmental-Standards](#-環境規格--environmental-standards)  
- [🧩 DFM/信頼性考慮 / DFM--Reliability](#-dfm信頼性考慮--dfm--reliability)  
- [✅ チェックリスト / Checklist](#-チェックリスト--checklist)  
- [🧭 ドキュメント雛形 / Handoff-Template](#-ドキュメント雛形--handoff-template)  
- [🔗 関連リンク / Related-Links](#-関連リンク--related-links)  
- [⬆️ Back to PCB](#️-back-to-pcb)  

---

## 🏗 概要 / Overview
PCB材料は**信号品質・電力安定性・熱設計・機械強度・信頼性**を同時に規定します。  
*PCB materials determine signal quality, power stability, thermal design, mechanical strength, and reliability.*

- **FR-4**：最も普及、低コスト、だが高速 (>5 Gbps) では損失増。  
- **低損失材**（Rogers, Megtron, Nelco）：10–100 Gbps級の高速伝送、RF、5G基地局などで必須。  
- **ポリイミド**：高耐熱用途（航空宇宙、軍事）。  

---

## 🎯 設計ゴール / Design Targets
- ターゲット信号速度に応じた **Dk（比誘電率）とDf（損失正接）** を選択する。  
  *Select Dk/Df based on signal speed.*  
- 熱負荷・放熱経路を考慮し、**熱伝導率の高い材**を選定。  
  *Choose materials with adequate thermal conductivity.*  
- 環境規格（RoHS, halogen-free, UL94V-0）準拠を確保。  
  *Ensure compliance with RoHS, halogen-free, UL94V-0.*  

---

## 🔑 キートピック / Key Topics
- FR-4の限界：10 Gbps以上で挿入損失増大  
- Dk・Dfの管理がインピーダンス制御・SIに直結  
- 樹脂系 vs セラミック系の特性比較  
- 熱膨張係数（CTE）がBGA実装信頼性に影響  

---

## 📊 代表的材料 / Typical Materials
| 材料 / Material | Dk (10GHz) | Df (10GHz) | 熱伝導率 W/m·K | 用途 / Applications |
|-----------------|-----------|------------|----------------|----------------------|
| **FR-4 (Standard)** | 4.2 | 0.020 | 0.3 | 汎用多層基板 |
| **FR-4 (High-Tg)** | 4.1 | 0.018 | 0.3 | 高信頼性用途 |
| **Rogers 4350B** | 3.48 | 0.0037 | 0.62 | RF/マイクロ波回路 |
| **Rogers 3003** | 3.0 | 0.0013 | 0.5 | 低損失ミリ波/5G |
| **Megtron 6** | 3.4 | 0.0020 | 0.5 | 10–56 Gbps高速通信 |
| **Nelco SI** | 3.2–3.4 | 0.002–0.004 | 0.4 | ネットワーク機器 |
| **Polyimide** | 3.5 | 0.004 | 0.2 | 高耐熱・航空宇宙 |
| **AlN基板** | ~8.9 | ~0.0005 | 150–200 | 高放熱・高周波パワー素子 |

---

## 🧮 電気特性と数式 / Electrical Properties & Formulas
- **伝搬速度**

$$
v = \frac{c}{\sqrt{\varepsilon_{eff}}}
$$

- **挿入損失**

$$
\alpha \approx \frac{\pi f}{c} \sqrt{\mu_r \varepsilon_r} \cdot Df
$$

---

## 🔥 熱特性 / Thermal Properties
- FR-4: k ≈ 0.3 W/m·K, CTE ≈ 70 ppm/°C  
- 高熱伝導材 (AlN): k ≈ 150–200 W/m·K  
- Tg: FR-4 = 130–170 °C, Polyimide = 250 °C+  

---

## 🌱 環境規格 / Environmental Standards
- **RoHS**：有害物質制限  
- **Halogen-free**：燃焼時有毒ガス低減  
- **UL94V-0**：難燃性  

---

## 🧩 DFM & Reliability
- ファブ標準材を優先選定 → コスト削減  
- 高速設計では周波数依存Dk/Df確認必須  
- 高Tg材でリフロー耐性・クラック防止  
- 熱サイクル信頼性試験を考慮  

---

## ✅ チェックリスト / Checklist
- [ ] Dk/Dfはターゲット周波数に合致？  
- [ ] 熱伝導率とTgは要求に適合？  
- [ ] CTEはBGA信頼性に問題ない？  
- [ ] RoHS/UL94V-0に準拠？  
- [ ] ファブ標準材か？  

---

## 🧭 ドキュメント雛形 / Handoff Template
| 項目 / Item | 指定 / Spec |
|---|---|
| 材料 / Material | FR-4 Tg170 |
| 誘電率 / Dk | 4.1 (at 1 GHz) |
| 損失正接 / Df | 0.018 |
| Tg | 170 °C |
| 熱伝導率 | 0.3 W/m·K |
| 環境対応 | RoHS, Halogen-free, UL94V-0 |
| 用途 | <10 Gbps General |

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📖 Stack-up | 層構成とインピーダンス管理<br>*Layer stack-up and impedance management* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./stackup.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/stackup) |
| 📖 Impedance Control | インピーダンス設計と制御<br>*Impedance design & control* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./impedance-control.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/impedance-control) |
| 📖 Reliability | 材料信頼性・環境試験<br>*Material reliability & environmental tests* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./reliability.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/reliability) |
| 📖 Appendix: Fiber Issues | ガラスファイバー由来の構想不具合<br>*Fiber-induced structural issues (CAF, via offset)* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./Appendix-Fiber-Issues.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/Appendix-Fiber-Issues.md) |

---

## ⬆️ Back to PCB

| Link | Badge |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |
