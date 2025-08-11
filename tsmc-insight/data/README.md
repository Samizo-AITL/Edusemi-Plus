---
layout: default
title: データディレクトリ – `tsmc-insight/data/`
---

---

# 📊 データディレクトリ – `tsmc-insight/data/`

このディレクトリには、**TSMC Insightの各章で使用される統計データ・時系列情報・補助ファイル（CSV, JSON など）**を保存します。  
図表や分析資料の元データ、教育用データセット、シミュレーション用構造などに活用されます。

---

## 📁 初期構成例（収録予定ファイル）

| ファイル名 | 内容 | 対応章 |
|------------|------|--------|
| `capex_tsmc_2020_2025.csv` | TSMCの設備投資額（年度別・用途別） | 第5章 |
| `node_density_map.csv` | プロセスノード別のロジック密度・性能指標 | 第1章 |
| `global_fab_locations.json` | 拠点名・緯度経度・国・特徴（JASM, Arizona等） | 第4章・5章 |
| `supplychain_dependencies.csv` | 各工程における主要国・企業依存 | 第4章 |
| `university_collab_list.csv` | TSMCと提携する大学・機関情報 | 第6章 |

---

## 🔗 使用例（Markdown + Python教材での利用）

```python
import pandas as pd
df = pd.read_csv('../data/capex_tsmc_2020_2025.csv')
df.plot(kind='bar', x='Year', y='CapEx_BillionUSD')
```
または：
```
[年度別設備投資データはこちら](../data/capex_tsmc_2020_2025.csv)
```

---

## 📝 注意事項

- データ出典は各ファイル冒頭のコメントまたは [`../refs/tsmc_references.md`](../refs/tsmc_references.md) に明記してください。
- 公開可能な範囲で収集・簡易加工したデータのみを格納してください。
- ファイル形式は `.csv`, `.tsv`, `.json`, `.yaml` などの構造化形式を推奨します。
- 列名は英語・スネークケースで統一し、意味の明確な命名を心がけてください。
- Python教材・可視化ツール等との連携を前提に、読みやすく整形されたデータ構造を推奨します。

---

## 📅 更新履歴

| 日付 | 内容 |
|------|------|
| 2025-07-13 | 初版作成（教育データ構成・使用例を含む設計指針策定） |

