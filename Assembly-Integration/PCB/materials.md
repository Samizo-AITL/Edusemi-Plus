---
layout: default
title: "PCB Materials | 材料"
---

---

# 🧪 PCB Materials / 材料

---

## 📑 目次 / Table of Contents
- [🏗 概要 / Overview](#-概要--overview)  
- [🎯 設計ゴール / Design Targets](#-設計ゴール--design-targets)  
- [🔑 キートピック / Key Topics](#-キートピック--key-topics)  
- [📊 代表的材料 / Typical Materials](#-代表的材料--typical-materials)  
- [🧮 電気特性と数式 / Electrical Properties & Formulas](#-電気特性と数式--electrical-properties--formulas)  
- [🔥 熱特性 / Thermal Properties](#-熱特性--thermal-properties)  
- [🌱 環境規格 / Environmental Standards](#-環境規格--environmental-standards)  
- [🧩 DFM/信頼性考慮 / DFM & Reliability](#-dfm信頼性考慮--dfm--reliability)  
- [✅ チェックリスト / Checklist](#-チェックリスト--checklist)  
- [🧭 ドキュメント雛形 / Handoff Template](#-ドキュメント雛形--handoff-template)  
- [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
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
  *FR-4 limited at >10 Gbps due to insertion loss*  
- Dk・Dfの管理がインピーダンス制御・SIに直結  
  *Dk/Df strongly impact impedance & SI*  
- 樹脂系材料 vs セラミック系材料の違い  
  *Resin vs ceramic-based laminates*  
- 熱膨張係数（CTE）がBGA実装信頼性に影響  
  *CTE mismatch impacts BGA solder reliability*  

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
- **伝搬速度 / Propagation velocity**
  
$$
v = \frac{c}{\sqrt{\varepsilon_{eff}}}
$$

  $c$: 光速, $\varepsilon_{eff}$: 有効比誘電率  

- **挿入損失の近似**

$$
\alpha \approx \frac{\pi f}{c} \sqrt{\mu_r \varepsilon_r} \cdot Df
$$

  $f$: 周波数, $Df$: 損失正接  

---

## 🔥 熱特性 / Thermal Properties
- 熱伝導率 (Thermal Conductivity):  
  FR-4 ~0.3 W/m·K, セラミック基板 (AlN, Al₂O₃) 100–200 W/m·K  
- 熱膨張係数 (CTE):  
  樹脂基板は ~70 ppm/°C、銅 ~17 ppm/°C → BGA接合部に応力発生  
- Tg（ガラス転移温度）:  
  FR-4: 130–170°C、Polyimide: 250°C以上  

---

## 🌱 環境規格 / Environmental Standards
- **RoHS**：鉛・水銀・Cd など有害物質制限  
- **Halogen-free**：燃焼時有毒ガス低減  
- **UL94V-0**：難燃規格  

---

## 🧩 DFM/信頼性考慮 / DFM & Reliability
- 材料は**ファブ標準在庫**から選定 → コスト削減。  
- 高速設計では**周波数依存Dk/Df特性**を確認。  
- 高Tg材はリフロー耐性向上、クラック防止に有効。  
- 熱サイクル信頼性試験（-40〜125°C）を考慮。  

---

## ✅ チェックリスト / Checklist
- [ ] ターゲット周波数でのDk/Dfは適正か？  
- [ ] 熱伝導率・Tgは設計要求を満たすか？  
- [ ] CTEはBGA実装信頼性に許容範囲か？  
- [ ] RoHS/UL94V-0に準拠しているか？  
- [ ] 材料がファブの標準供給範囲か？  

---

## 🧭 ドキュメント雛形 / Handoff Template
| 項目 / Item | 指定 / Spec |
|---|---|
| 材料 / Material | FR-4 Tg170 |
| 誘電率 / Dk | 4.1 (at 1 GHz) |
| 損失正接 / Df | 0.018 |
| Tg / Glass Transition | 170 °C |
| 熱伝導率 / Thermal k | 0.3 W/m·K |
| 環境対応 / Compliance | RoHS, Halogen-free, UL94V-0 |
| 用途 / Application | 10 Gbps未満汎用 |

---

## 🔗 関連リンク / Related Links
- [📖 Stack-up](./stackup.md)  
- [📖 Impedance Control](./impedance-control.md)  
- [📖 Reliability](./reliability.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
