---
layout: default
title: "1.3｜EUV導入の背景と7nm以降の製造技術変化 / Background of EUV Introduction and Manufacturing Changes Beyond 7nm"
---

---

# 🌌 1.3｜EUV導入の背景と7nm以降の製造技術変化  
**1.3｜Background of EUV Introduction and Manufacturing Changes Beyond 7nm**

---

## 📌 概要 / Overview

**JP:**  
EUV（Extreme Ultraviolet Lithography）は、波長13.5nmの光を用いる次世代リソグラフィ技術です。  
TSMCは7nm世代で部分的に導入し、5nm世代から本格運用を開始しました。これにより、マルチパターニング工程の削減、寸法精度の向上、製造コストの抑制が可能になりました。  

**EN:**  
EUV (Extreme Ultraviolet Lithography) is a next-generation lithography technology using 13.5nm wavelength light.  
TSMC introduced it partially at the 7nm node and began full-scale operation from 5nm. This reduced multi-patterning steps, improved dimensional accuracy, and helped control manufacturing costs.

---

## 🕰️ 導入の時系列 / Introduction Timeline

| 年 / Year | ノード / Node | EUV導入状況 / EUV Adoption Status |
|-----------|---------------|-----------------------------------|
| 2018 | N7 (DUVベース) | No EUV (SAQP等による多重パターニング) |
| 2019 | N7+ | 部分EUV導入（4層程度） / Partial EUV (~4 layers) |
| 2020 | N5 | 本格EUV（14〜15層） / Full EUV (14–15 layers) |
| 2022–23 | N3 | EUVレイヤー数拡大（>20層） / Expanded EUV (>20 layers) |
| 2025予定 | N2 | High-NA EUV検討中 / Considering High-NA EUV |

---

## 🔍 導入背景 / Background Factors

**JP:**
1. **マルチパターニングの限界**：SAQPやLELELEによる工程増加でコスト・歩留まりが悪化  
2. **寸法制御精度の必要性**：7nm以下でのパターンずれ許容度低下  
3. **競争優位性確保**：Samsungとの先端ノード競争に対応  

**EN:**
1. **Limits of multi-patterning**: Increased process steps from SAQP and LELELE led to higher costs and lower yield  
2. **Need for dimensional accuracy**: Tighter overlay tolerance below 7nm  
3. **Maintaining competitive edge**: Keep up with Samsung in leading-edge nodes

---

## 🛠️ 製造技術の変化 / Manufacturing Changes

| 項目 / Item | 7nm時代 / At 7nm | 5nm時代 / At 5nm | 3nm時代 / At 3nm |
|-------------|------------------|------------------|------------------|
| パターニング工程 / Patterning | 多重パタ（SAQP主体） / Multi-patterning (mainly SAQP) | EUV主体＋一部DUV / Mainly EUV + partial DUV | EUV拡大 / Expanded EUV |
| レイヤー数 / Layer Count | ~80層 | ~70層 | ~65層 |
| 歩留まり / Yield | 中 | 高 | 高だがコスト増 / High but costly |
| マスクコスト / Mask Cost | 高 | 減少（EUV効果） | 再上昇（マスク複雑化） |

---

## ⚖️ EUVの利点と課題 / Advantages & Challenges

**利点 / Advantages**
- 工程短縮によるコスト低減
- 寸法精度向上 → 高歩留まり
- 設計自由度向上（セルピッチ縮小）

**課題 / Challenges**
- 光源出力・マスク欠陥の管理
- レジスト感度・LWR（Line Width Roughness）
- High-NA EUV設備コスト（>3億ドル/台）

---

## 📎 関連リンク / Related Links

- [1.2｜FinFET技術の確立と5nm世代までの設計手法](1_2_finfet_to_5nm.md)
- [README (TSMC Insight)](../README.md)

---

## 🔙 戻る・進む / Navigation
- **前節 / Previous:** [1.2｜FinFET技術の確立と5nm世代までの設計手法](1_2_finfet_to_5nm.md)  
- **次節 / Next:** [1.4｜N2 / GAA構造（ナノシートFET）の登場と設計課題](1_4_gaa_intro.md)  
- **章トップ / Chapter Top:** [README](../README.md)
