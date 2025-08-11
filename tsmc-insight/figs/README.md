---
layout: default
title: 🖼️ 図表ディレクトリ – `tsmc-insight/figs/` / Figures Directory
---

---

# 🖼️ 図表ディレクトリ – `tsmc-insight/figs/`  
**Figures Directory – `tsmc-insight/figs/`**

このディレクトリには、**TSMC Insight 各章に関連する図表・年表・地図・グラフ**を収録します。  
教材の可視化・比較・分析を支援するための補助資料として活用されます。

This directory stores **figures, timelines, maps, and graphs** related to each chapter of TSMC Insight.  
These resources support visualization, comparison, and analysis in educational content.

---

## 📚 図表一覧（初期構成） / Figures List (Initial Structure)

| ファイル名 / Filename | 内容 / Description | 関連章 / Related Chapter |
|-----------------------|--------------------|--------------------------|
| `node_timeline.svg` | TSMCのプロセスノード進化年表（7nm→2nm→A16）<br>TSMC Process Node Evolution Timeline (7nm→2nm→A16) | 第1章 / Ch.1 |
| `tsmc_vs_samsung_table.png` | TSMCとサムスンのGAA/EUV比較表（図形式）<br>Comparison Table of TSMC vs Samsung (GAA/EUV) | 第3章 / Ch.3 |
| `supply_chain_map.svg` | 半導体素材・装置・設計依存の国別マップ<br>Country-based Map of Semiconductor Material, Equipment & Design Dependencies | 第4章 / Ch.4 |
| `fab_locations_world.svg` | 世界におけるTSMC主要拠点（熊本・アリゾナ・ドイツ）<br>Global TSMC Locations (Kumamoto, Arizona, Germany) | 第5章 / Ch.5 |
| `capex_chart_tsmc.png` | TSMCの設備投資額推移（2020〜2025）<br>TSMC Capital Expenditure Trends (2020–2025) | 第5章 / Ch.5 |

---

## 🔗 図表の使用方法（Markdown内埋め込み）  
**How to Use Figures in Markdown**

```markdown
![TSMCノード年表 / TSMC Node Timeline](../figs/node_timeline.svg)

もしくはリンク形式で引用 / Or link directly:
[ノード進化図を表示 / View Node Evolution Figure](../figs/node_timeline.svg)
```

---

## 📝 注意事項 / Notes

- 図表の再利用・編集には **MITライセンス** が適用されます。  
  Figures are subject to the **MIT License** for reuse and modification.
- 出典元がある場合は、**ファイル内または本文中** に明記してください。  
  If a source exists, indicate it **inside the file or in the text**.
- 作図元データ（`.drawio`, `.pptx`, `.xlsx` など）は必要に応じて `/figs_src/` 等に格納可能です。  
  Original drawing data may be stored in `/figs_src/` if needed.
- ファイル命名は、**対応章番号またはテーマ名を含める**ことを推奨します。  
  Recommended to include **chapter number or theme name** in the filename.  
  例 / Example: `fig_ch3_samsung_compare.png`

---

## 📅 更新履歴 / Update History

| 日付 / Date | 内容 / Details |
|-------------|----------------|
| 2025-07-13 | 初版作成（図表分類・使用ガイド整備）<br>First draft: Figure classification & usage guide |

---

## 🔙 戻る / Back
- **JP:** [TSMC Insight トップへ戻る](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)  
- **EN:** [Return to TSMC Insight Top](https://samizo-aitl.github.io/Edusemi-Plus/tsmc-insight/index.html)
