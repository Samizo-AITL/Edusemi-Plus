---
layout: default
title: 📊 データディレクトリ – `tsmc-insight/data/` / Data Directory
---

---

# 📊 データディレクトリ – `tsmc-insight/data/`  
**Data Directory – `tsmc-insight/data/`**

このディレクトリには、**TSMC Insight の各章で使用される統計データ・時系列情報・補助ファイル（CSV, JSON など）**を保存します。  
図表や分析資料の元データ、教育用データセット、シミュレーション用構造などに活用されます。

This directory stores **statistical data, time-series information, and supplementary files (CSV, JSON, etc.)** used in each chapter of TSMC Insight.  
It serves as the source for charts, analysis, educational datasets, and simulation structures.

---

## 📁 初期構成例（収録予定ファイル） / Initial Structure (Planned Files)

| ファイル名 / Filename | 内容 / Description | 対応章 / Related Chapter |
|-----------------------|--------------------|--------------------------|
| `capex_tsmc_2020_2025.csv` | TSMCの設備投資額（年度別・用途別）<br>TSMC capital expenditures by year & category | 第5章 / Ch.5 |
| `node_density_map.csv` | プロセスノード別のロジック密度・性能指標<br>Logic density & performance metrics by process node | 第1章 / Ch.1 |
| `global_fab_locations.json` | 拠点名・緯度経度・国・特徴（JASM, Arizona等）<br>Fab names, coordinates, country, characteristics | 第4章・5章 / Ch.4 & Ch.5 |
| `supplychain_dependencies.csv` | 各工程における主要国・企業依存<br>Key country & corporate dependencies in each process stage | 第4章 / Ch.4 |
| `university_collab_list.csv` | TSMCと提携する大学・機関情報<br>Universities & institutions collaborating with TSMC | 第6章 / Ch.6 |

---

## 🔗 使用例（Markdown + Python教材での利用）  
**Usage Examples (Markdown + Python)**

```python
import pandas as pd
df = pd.read_csv('../data/capex_tsmc_2020_2025.csv')
df.plot(kind='bar', x='Year', y='CapEx_BillionUSD')
```

または / Or:

```markdown
[年度別設備投資データはこちら / Annual CapEx Data Here](../data/capex_tsmc_2020_2025.csv)
```

---

## 📝 注意事項 / Notes

- **データ出典は各ファイル冒頭のコメントまたは [`../refs/tsmc_references.md`](../refs/tsmc_references.md) に明記**してください。  
  Clearly specify the **data source** at the beginning of each file or in [`../refs/tsmc_references.md`](../refs/tsmc_references.md).
- **公開可能な範囲**で収集・簡易加工したデータのみを格納してください。  
  Only include data that is permissible for public use.
- 推奨形式：`.csv`, `.tsv`, `.json`, `.yaml` などの構造化形式。  
  Preferred formats: `.csv`, `.tsv`, `.json`, `.yaml`.
- 列名は **英語・スネークケース** で統一し、意味を明確にする。  
  Use **English snake_case** for column names with clear meaning.
- Python教材・可視化ツールとの連携を考慮し、**整形済みのデータ構造**を推奨。  
  Ensure the data structure is well-formatted for Python scripts & visualization tools.

---

## 📅 更新履歴 / Update History

| 日付 / Date | 内容 / Details |
|-------------|----------------|
| 2025-07-13 | 初版作成（教育データ構成・使用例を含む設計指針策定）<br>First draft: Guidelines with dataset structure & usage examples |

---

## 🔙 戻る / Back
- **JP:** [TSMC Insight トップへ戻る](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)  
- **EN:** [Return to TSMC Insight Top](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)
