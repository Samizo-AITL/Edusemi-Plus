---
layout: default
title: 📈 第1章　TSMCの技術ロードマップ / Chapter 1 TSMC Technology Roadmap
---

---

# 📈 第1章：TSMCの技術ロードマップ  
**Chapter 1: TSMC Technology Roadmap**

本章では、**TSMC（台湾積体電路製造 / Taiwan Semiconductor Manufacturing Company）** における  
技術ロードマップの変遷を時系列で分析し、先端ノードにおける進化  
（7nm → 5nm → 3nm → 2nm → A16）と、それを支える **EUV・GAA・製造プロセス革新** の要点を解説します。

---

## 🧭 本章の目的 / Objectives

- **TSMCにおけるプロセスノードの進化**と世代ごとの特徴整理  
  Understanding the evolution of TSMC process nodes and generational characteristics
- **FinFETからGAAFET（N2以降）への移行**と設計影響  
  Transition from FinFET to GAAFET (N2 onwards) and design implications
- **EUVリソグラフィの導入時期**と適用層数の増加動向  
  Introduction timeline of EUV lithography and increase in EUV layer usage
- **ロジック密度・性能・消費電力のトレードオフ分析**  
  Trade-off analysis of logic density, performance, and power
- **Aシリーズ（A14, A16等）命名規則と実体の技術的含意**  
  Naming conventions of A-series nodes and technical implications

---

## 🗂 内容構成 / Contents

| セクション / Section | 内容 / Description |
|----------------------|--------------------|
| 1.1 | ノード年表とマーケティング命名の差異（例：5nmとN5）<br>Differences between marketing names and node labels |
| 1.2 | FinFET技術の確立と5nm世代までの設計手法<br>FinFET establishment and design methods up to 5nm |
| 1.3 | EUV導入の背景と7nm以降の製造技術変化<br>Background of EUV introduction and manufacturing changes beyond 7nm |
| 1.4 | N2 / GAA構造（ナノシートFET）の登場と設計課題<br>Introduction of N2/GAA nanosheet FET and design challenges |
| 1.5 | A16ノード：A14との違い、性能密度、チップレットとの関係<br>A16 node: Differences from A14, density, and chiplet relevance |
| 1.6 | 今後の予測（A10以降、ナノワイヤ化、CMOS Beyond）<br>Future outlook (post-A10, nanowire, CMOS beyond) |

---

## 🧮 代表的ノード比較（例） / Representative Node Comparison

| ノード / Node | 発表年 / Launch Year | 構造 / Structure | リソグラフィ / Lithography | ロジック密度 / Logic Density | 特記事項 / Notes |
|---------------|----------------------|------------------|----------------------------|------------------------------|------------------|
| 7nm (N7) | 2018 | FinFET | DUV（一部EUV） / DUV (partial EUV) | 1.0x | 初期EUV導入準備期 / Early EUV preparation |
| 5nm (N5) | 2020 | FinFET | EUV本格導入 / Full EUV adoption | 1.8x | Apple A14搭載 / Used in Apple A14 |
| 3nm (N3) | 2022–23 | FinFET改良 / Enhanced FinFET | EUV拡張 / Expanded EUV | 1.7–1.9x | 高コスト・歩留まり課題 / High cost & yield issues |
| 2nm (N2) | 2025予定 / Planned 2025 | GAA（ナノシート） / GAA (Nanosheet) | High-NA EUV？ | 2.6x〜 | 全面構造転換 / Full structural shift |
| A16 | 2025〜 | 拡張GAA / Enhanced GAA | 未公表 / TBA | N/A | Aシリーズ再編との関連 / Linked to A-series restructuring |

---

## 🧠 補足キーワード / Key Terms

- **EUV**（極端紫外線リソグラフィ / Extreme Ultraviolet Lithography）／High-NA EUV
- **GAA**（Gate All Around）／ナノシート構造 / Nanosheet structure
- **ロジック密度 / Logic Density**（MTr/mm²）／**PPA**（Performance, Power, Area）
- **チップレット対応性 / Chiplet Compatibility**／**パッケージ前提設計 / Package-Aware Design**（CoWoS / InFO）

---

## 📎 関連章 / Related Chapters

| 章 / Chapter | リンク / Link |
|--------------|--------------|
| 第2章：ファウンドリと地政学 | [README](../chapter2_geopolitics/README.md) |
| Edusemi 特別編：FinFET / GAA | [GitHubページ](https://github.com/Samizo-AITL/Edusemi-v4x/blob/main/f_chapter1_finfet_gaa/README.md) |
| Edusemi 応用編：PDKとEDA環境 | [GitHubページ](https://github.com/Samizo-AITL/Edusemi-v4x/blob/main/d_chapter6_pdk_and_eda_environment/README.md) |

---

## 📅 更新履歴 / Update History

| 日付 / Date | 内容 / Details |
|-------------|---------------|
| 2025-07-13 | 初版作成（章構成・比較表・教材リンク修正） / First draft with structure, comparison table, and links |

---

## 🔙 戻る / Back
- **JP:** [TSMC Insight トップへ戻る](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)  
- **EN:** [Return to TSMC Insight Top](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)
