# 🧾 wafer_basics.md  
## シリコンウエハ基板の基礎と実務知識  
## Fundamentals and Practical Aspects of Silicon Wafers

---

## 📘 概要｜Overview

シリコンウエハは半導体製造の出発点であり、その**結晶性・濃度・表面特性**がデバイス性能や歩留まりに大きく影響します。本資料では、ウエハ基板の基礎仕様と実務で重要となる**酸素濃度・COP・アライメント構造・歪み問題**などについて解説します。

---

## 🧱 基板の基本仕様｜Basic Substrate Specifications

| 項目 / Parameter | 内容 / Description |
|------------------|---------------------|
| 結晶方位 | Si(100), Si(111) など（主に100） |
| 導電型 | P-type / N-type |
| 抵抗率 | 1–20 Ω·cm（ロジック用途）<br>>1kΩ·cm（ハイウエハ：HV用途） |
| 成長法 | CZ（チョクラルスキー法） / FZ（浮遊帯法） / Epi（エピタキシャル層） |
| サイズ | 6 inch, 8 inch（0.35μm〜0.18μm）<br>12 inch（90nm以降） |
| エッジ形状 | オリフラ / ノッチ |

---

## 🌬️ 酸素濃度と酸素析出｜Oxygen Content and Precipitation

- CZ法ウエハは酸素を多く含み（10¹⁸ atoms/cm³以上）、酸化/アニールにより析出しやすい。
- 酸素析出は**微小空孔形成**や**歪み変形**を引き起こし、**合わせ検査不良**の原因にも。
- 特に酸化工程後に生じる応力によって、**ウエハが湾曲・反り返る**ことがある。

✅ **実務対策例：**
- Epiウエハの採用（表面を新生結晶化）
- 低酸素CZの採用（O≦5×10¹⁷ atoms/cm³）
- 熱処理レシピの見直し（酸素析出抑制）

---

## 🧨 COP（Crystal-Originated Particle）リスク

- 特にCZウエハにおいて**表面下に微細空洞（COP）**が形成されることがある。
- **CMP後でも除去しきれない場合があり、HV素子・絶縁膜破壊の起点に。**
- FZでは酸素濃度が極端に低いため、COPは**ほぼゼロ**。

✅ **設計・工程対策：**
- HVデバイスにはFZまたはEpiベース推奨
- CMP条件の見直し（研磨量の確保）
- Active領域配置の工夫（COP領域回避）

---

## 🧭 ウエハアライメント構造｜Wafer Alignment Structures

| 項目 | 内容 |
|------|------|
| オリフラ | Flat面で方位判定（6, 8 inchの主流） |
| ノッチ | 円周切り欠きで方位判定（12 inch以降で主流） |
| チップ設計への影響 | 方位固定によるレイアウト最適化、エッジ近傍設計の制約 |

---

## 📏 ウエハ歪みと検査不良｜Wafer Warpage and Overlay Failure

- 高温工程後、酸素析出や膜応力によりウエハに**渦巻きベクトル状の歪み**が発生。
- **アライメントマークと実パターンがずれ**、**合わせ検査でNG**となる事例もある。
- 特に8 inch以下のウエハで、**中心-端部間の膜応力差が顕著**。

---

## ✅ まとめ｜Summary

- CZウエハは標準的だが、酸素濃度管理・COP対策が必須
- FZやEpiはコストが高いが、高信頼設計に適している
- 歪み・合わせ不良の要因は材料起因も含まれるため、**前工程のウエハ品質も設計・工程最適化の一部**

---

## 🔗 関連リンク｜Related Resources

- [`0.18um_Logic_ProcessFlow.md`](../docs/0.18um_Logic_ProcessFlow.md)
- [`5a.1 ポリ抵抗とばらつき`](../d_chapter5_analog_mixed_signal/5a1_poly_resistor.md)
- [`ams_node_selection.md`](../d_chapter5_analog_mixed_signal/ams_node_selection.md)
