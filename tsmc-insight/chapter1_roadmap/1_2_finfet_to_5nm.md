---
layout: default
title: "1.2｜FinFET技術の確立と5nm世代までの設計手法 / Establishment of FinFET Technology and Design Methods up to 5nm"
---

---

# 🏗️ 1.2｜FinFET技術の確立と5nm世代までの設計手法  
**1.2｜Establishment of FinFET Technology and Design Methods up to 5nm**

---

## 📌 概要 / Overview

**JP:**  
FinFET（Fin Field-Effect Transistor）は、従来のプレーナ型MOSFETの短チャネル効果を抑制するために開発された3次元構造トランジスタです。2010年代以降、TSMCは16nm世代からFinFETを導入し、7nm・5nmまで性能向上と消費電力低減を両立しました。  

**EN:**  
FinFET (Fin Field-Effect Transistor) is a 3D transistor architecture developed to suppress short-channel effects in traditional planar MOSFETs. Since the 16nm generation, TSMC has adopted FinFET, achieving both performance improvements and power reduction through 7nm and 5nm nodes.

---

## 🧬 FinFET構造の特徴 / Characteristics of FinFET Structure

| 特徴 / Feature (JP) | Feature (EN) | 説明 / Description |
|---------------------|--------------|--------------------|
| 3D構造 / 3D Structure | 3D fin-shaped channel | チャネルが立体化され、ゲートが3面を包み込むことで制御性向上 / Channel is raised, with gate wrapping around three sides for better control |
| 短チャネル効果抑制 | Suppression of short-channel effects | DIBL・リーク電流の低減 / Reduced DIBL and leakage current |
| 高ドライブ電流 | High drive current | Fin数を増やすことで駆動能力を調整可能 / Drive strength can be tuned by increasing number of fins |
| 高密度集積 | High density integration | スケーリングとともに配線層・セルライブラリ設計が進化 / Scaling accompanied by improved interconnect and cell library design |

---

## 🛠️ 設計手法の進化 / Evolution of Design Methods

**16nm世代（初期FinFET） / 16nm Generation (Early FinFET):**
- DRCルールが複雑化（Fin間隔、ゲート長の量子化）
- PDKのFin単位でのトランジスタ選択
- 電力と速度のバランスを取るためのセルライブラリ拡充

**7nm世代 / 7nm Generation:**
- 部分的EUV導入による配線精度向上
- RC遅延対策として低k材料と配線層構造最適化
- マルチパターニング（SAQP等）の設計影響

**5nm世代 / 5nm Generation:**
- EUV本格導入によりレイヤー数削減
- セル高さ・配線ピッチ縮小（~48nm M0 pitch）
- 高密度標準セルライブラリ（HD/HP variants）

---

## ⚖️ PPAトレードオフの変化 / PPA Trade-off Changes

| ノード / Node | 性能向上 / Perf. Gain | 消費電力低減 / Power Reduction | ロジック密度 / Logic Density |
|---------------|-----------------------|--------------------------------|------------------------------|
| 16nm → 7nm    | ~35%                  | ~55%                           | ~3.3x                        |
| 7nm → 5nm     | ~15–20%               | ~30%                           | ~1.8x                        |

---

## 🔍 設計上の課題 / Design Challenges

- **配線抵抗・容量増加**による遅延悪化 → BEOL改善が必須  
- **リーク電流の制御**：スケーリングによるVth調整難度増加  
- **EDAツール対応**：EUV・マルチパターニングに伴う新規DRC/DFMルール

---

## 📎 関連リンク / Related Links

- [1.1｜ノード年表とマーケティング命名の差異](1_1_node_timeline.md)
- [README (TSMC Insight)](../README.md)

---

## 🔙 戻る・進む / Navigation
- **前節 / Previous:** [1.1｜ノード年表とマーケティング命名の差異](1_1_node_timeline.md)  
- **次節 / Next:** [1.3｜EUV導入の背景と7nm以降の製造技術変化](1_3_euv_intro.md)  
- **章トップ / Chapter Top:** [README](../README.md)
