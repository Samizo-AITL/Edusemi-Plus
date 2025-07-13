# 📈 第1章：TSMCの技術ロードマップ

本章では、**TSMC（台湾積体電路製造）** における技術ロードマップの変遷を時系列で分析し、  
先端ノードにおける進化（7nm → 5nm → 3nm → 2nm → A16）と、それを支える**EUV・GAA・製造プロセス革新**の要点を解説します。

---

## 🧭 本章の目的

- TSMCにおけるプロセスノードの進化と世代ごとの特徴整理
- FinFETからGAAFET（N2以降）への移行と設計影響の理解
- EUVリソグラフィの導入時期と適用層数の増加動向
- ロジック密度、性能、消費電力のトレードオフ分析
- Aシリーズ（A14, A16等）命名規則と実体の技術的含意

---

## 🗂 内容構成

| セクション | 内容 |
|------------|------|
| 1.1 | ノード年表とマーケティング命名の差異（例：5nmとN5） |
| 1.2 | FinFET技術の確立と5nm世代までの設計手法 |
| 1.3 | EUV導入の背景と7nm以降の製造技術変化 |
| 1.4 | N2 / GAA構造（ナノシートFET）の登場と設計課題 |
| 1.5 | A16ノード：A14との違い、性能密度、チップレットとの関係 |
| 1.6 | 今後の予測（A10以降、ナノワイヤ化、CMOS Beyond） |

---

## 🧮 代表的ノード比較（例）

| ノード | 発表年 | 構造 | リソグラフィ | ロジック密度 | 特記事項 |
|--------|--------|--------|----------------|----------------|------------|
| 7nm (N7) | 2018 | FinFET | DUV（一部EUV） | 1.0x | 初期EUV導入準備期 |
| 5nm (N5) | 2020 | FinFET | EUV本格導入 | 1.8x | Apple A14搭載 |
| 3nm (N3) | 2022–23 | FinFET改良 | EUV拡張 | 1.7–1.9x | 高コスト、歩留まり課題 |
| 2nm (N2) | 2025予定 | GAA（ナノシート） | High-NA EUV？ | 2.6x〜 | 全面構造転換 |
| A16 | 2025〜 | 拡張GAA | 未公表（命名戦略） | N/A | Aシリーズ再編との関連 |

---

## 🧠 補足キーワード

- EUV（極端紫外線リソグラフィ）／High-NA EUV
- GAA（Gate All Around）／ナノシート構造
- ロジック密度（MTr/mm²）／PPA（Performance, Power, Area）
- チップレット対応性／パッケージ前提設計（CoWoS / InFO）

---

## 📎 関連章

- [第2章：ファウンドリと地政学](../chapter2_geopolitics/README.md)
- [Edusemi 特別編：FinFET / GAA](https://github.com/Samizo-AITL/Edusemi-v4x/blob/main/f_chapter1_finfet_gaa/README.md)
- [Edusemi 応用編：PDKとEDA環境](https://github.com/Samizo-AITL/Edusemi-v4x/blob/main/d_chapter6_pdk_and_eda_environment/README.md)
- 

---

## 📅 更新履歴

| 日付 | 内容 |
|------|------|
| 2025-07-13 | 初版作成（章構成・比較表・教材リンク修正） |
