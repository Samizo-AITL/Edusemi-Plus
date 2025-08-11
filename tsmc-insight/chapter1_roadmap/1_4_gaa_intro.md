---
layout: default
title: "1.4｜N2 / GAA構造（ナノシートFET）の登場と設計課題 / Introduction of N2/GAA Nanosheet FET and Design Challenges"
---

---

# 🏗️ 1.4｜N2 / GAA構造（ナノシートFET）の登場と設計課題  
**1.4｜Introduction of N2/GAA Nanosheet FET and Design Challenges**

---

## 📌 概要 / Overview

**JP:**  
TSMCは2025年量産予定のN2ノードから、FinFETに代わる**GAA（Gate-All-Around）ナノシートFET**構造を採用します。  
これにより、短チャネル効果の抑制、ドライブ電流向上、配線密度最適化が可能となりますが、設計・製造両面で新たな課題も発生します。  

**EN:**  
From its N2 node planned for 2025, TSMC will adopt the **Gate-All-Around (GAA) nanosheet FET** structure, replacing FinFET.  
This enables suppression of short-channel effects, increased drive current, and optimized routing density, but introduces new challenges in both design and manufacturing.

---

## 🆚 FinFETとの比較 / Comparison with FinFET

| 項目 / Item | FinFET | GAA Nanosheet FET |
|-------------|--------|-------------------|
| ゲート形状 / Gate Geometry | 3面ゲート（Finの両側＋上面） / 3-sided gate | 全面ゲート（上下左右全て） / Fully wrapped gate |
| 電気特性 / Electrical Performance | 短チャネル制御が限界に近づく / Approaching short-channel limit | 短チャネル制御が改善 / Improved short-channel control |
| ドライブ電流 / Drive Current | Fin高さ依存 / Dependent on fin height | ナノシート幅・積層数で調整可能 / Tunable by sheet width & stacking |
| 設計自由度 / Design Flexibility | Finピッチ制約あり / Limited by fin pitch | シート幅で性能バランス調整 / Performance tuned by sheet width |
| 製造難易度 / Manufacturing Complexity | 高 / High | さらに高（選択エピ成長・埋め込み酸化） / Even higher (selective epi, buried oxide) |

---

## 🔍 技術的特徴 / Technical Features

- **ナノシート幅調整（Wn）**：性能とリークのバランスを最適化  
- **スタック数（Ns）可変**：電流量を設計段階で選択可能  
- **チャネル材料多様化**：Si, SiGe, III-V混成の検討  
- **配線層との統合最適化**：BEOL（Back-End-of-Line）密度制限との整合性が重要

---

## ⚠️ 設計課題 / Design Challenges

**JP:**
1. **PDK刷新**：GAA固有のレイアウトルール（ナノシート幅・スタック高さ制約）  
2. **寄生容量の増加**：全面ゲート化によるCgd・Cgsの増大  
3. **熱管理**：チャネル周囲の熱拡散経路が限定  
4. **ライブラリ再設計**：FinFET用セルの流用不可

**EN:**
1. **PDK renewal**: New layout rules unique to GAA (sheet width & stack height limits)  
2. **Increased parasitic capacitance**: Fully wrapped gate increases Cgd/Cgs  
3. **Thermal management**: Limited heat dissipation paths around channel  
4. **Library redesign**: FinFET cell reuse not feasible

---

## 🛠️ 製造課題 / Manufacturing Challenges

- **選択エピ成長（Selective Epitaxy）**精度確保  
- **ナノシートエッチング**による寸法ばらつき抑制  
- **ゲート酸化膜形成**の均一性  
- **多層積層**時のアライメント精度

---

## 📊 N2世代の予想PPA改善 / Expected PPA Improvement for N2

| 指標 / Metric | 改善率 / Improvement Rate | 備考 / Notes |
|---------------|--------------------------|--------------|
| 性能 / Performance | +10〜15% | 同一消費電力条件 |
| 消費電力 / Power | -25〜30% | 同一性能条件 |
| ロジック密度 / Logic Density | +1.1〜1.2x | N3比 |

---

## 📎 関連リンク / Related Links

- [1.3｜EUV導入の背景と7nm以降の製造技術変化](1_3_euv_intro.md)  
- [README (TSMC Insight)](../README.md)

---

## 🔙 戻る・進む / Navigation
- **前節 / Previous:** [1.3｜EUV導入の背景と7nm以降の製造技術変化](1_3_euv_intro.md)  
- **次節 / Next:** [1.5｜A16ノード：A14との違い、性能密度、チップレットとの関係](1_5_a16_node.md)  
- **章トップ / Chapter Top:** [README](../README.md)
