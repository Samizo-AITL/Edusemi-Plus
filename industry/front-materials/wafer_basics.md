# 🧱 ウエハ基板の基礎 / Basics of Silicon Wafers

本ドキュメントでは、半導体製造におけるシリコンウエハ（Silicon Wafer）の基礎的な性質、分類、注意点、および代表的なメーカーシェアについてまとめます。

---

## 🧾 1. ウエハの基本仕様 / Basic Wafer Specifications

| 項目 / Item       | 内容 / Description                              |
|------------------|------------------------------------------------|
| 材料 / Material   | 単結晶シリコン（Single-Crystalline Silicon）    |
| 方位 / Orientation | ⟨100⟩面が主流（⟨111⟩はパワー系やMEMS向け）      |
| 導電型 / Type     | P型（Boron）またはN型（Phosphorus, Arsenic）     |
| 抵抗率 / Resistivity | 1–20 Ω·cm（用途により異なる）                   |
| サイズ / Size     | 6インチ（150mm）、8インチ（200mm）、12インチ（300mm）|
| 厚さ / Thickness  | 725μm（200mm）〜775μm（300mm）など              |
| エッジ形状 / Edge | オリフラット（OF）またはノッチ（Notch）         |

---

## 🌫️ 2. 酸素濃度とCOPリスク / Oxygen Concentration and COPs

| 要素 | 説明 |
|------|------|
| 酸素濃度 | CZ法では酸素が結晶中に溶け込みやすい（Epiで除去可能） |
| COP（Crystal Originated Particles） | 酸素析出に起因する微小欠陥。HVデバイスやEpi面で問題に |
| 影響例 | STI歪み、合わせ検査での不合格、リーク電流のばらつき等 |

**補足**：FZ法では酸素濃度が極めて低く、COPリスクはほぼゼロ。

---

## 💥 3. ウエハの歪みと検査影響 / Warpage and Alignment Failures

高温酸化やアニール後の酸素析出、膜応力によってウエハが歪むと、以下の問題が発生します：

- アライメントマークが検出不能（合わせ検査NG）
- ライン幅やCDが位置依存でばらつく
- 特に周辺部に渦巻き状の歪みベクトルが発生しやすい

**対策**：
- CMP条件見直し（研磨量確保）
- アクティブダミーパターン配置で応力緩和

---

## 📍 4. エッジ形状と識別方式 / Edge Shape and Orientation Flats

| 世代 / Generation | サイズ / Size | 形状 / Shape | 備考 / Note |
|------------------|----------------|---------------|--------------|
| 古いプロセス      | 6インチ以下     | オリフラット（OF） | ⟨110⟩方向などに切欠きあり |
| 8インチ（0.35μm世代） | 200mm         | ノッチ（Notch）     | 中央の微小切欠きで自動整合 |
| 12インチ以降      | 300mm以上       | ノッチ（標準）       | 自動処理対応が前提 |

---

## 🏭 5. 世界のウエハメーカー / Global Wafer Manufacturers（2024年時点）

| メーカー名 / Manufacturer | 拠点 / Region | 主な特徴 / Key Features | シェア（概算） / Share (%) |
|---------------------------|---------------|---------------------------|-----------------------------|
| **信越化学（Shin-Etsu）** | 日本 / Japan | 最大手、全ノード対応、高品質 | 約 30% |
| **SUMCO**                 | 日本 / Japan | 300mmに強み、安定供給力     | 約 25% |
| **GlobalWafers（環球晶圓）** | 台湾 / Taiwan | ファウンドリとの強固な関係    | 約 18% |
| **Siltronic**             | ドイツ / Germany | FZ対応、SiCやGaN基板にも展開 | 約 10% |
| **SK Siltron**            | 韓国 / Korea | サムスン系向け供給強い       | 約 7% |
| **その他 / Others**       | —             | 小規模・ローカル向け供給等     | 約 10% |

> 出典：SEMI, 各社決算資料, 業界調査（2025年）

---

## 📚 関連資料 / Related Docs

- [`0.18um_Logic_ProcessFlow.md`](./0.18um_Logic_ProcessFlow.md)：0.18μm CMOSプロセスフロー
- [`process_node_comparison.md`](./process_node_comparison.md)：プロセスノード比較（180nm〜90nm）
- [`fem_constraints.md`](./fem_constraints.md)：SystemDKにおけるFEM物理制約

---

## 📝 備考 / Notes

- 本資料は教育・設計支援の目的で公開されています。
- 各数値・仕様は実務経験・公開資料をもとに記載されており、実際のラインとは異なる可能性があります。
