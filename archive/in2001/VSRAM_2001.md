---
layout: default
title: モバイル用疑似SRAM（VSRAM）技術アーカイブ（2001年）
---

---

# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ（2001年）  
*Edusemi-Plus/archive/in2001/VSRAM_2001.md*  
**最終更新: 2025-07-28**

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../README.md#著者・ライセンス--author--license)

---

## 🧭 概要 / **Overview**

本ドキュメントは、2001年に量産された **モバイル用疑似SRAM（VSRAM）** の技術アーカイブである。  
**0.25μm世代の64M DRAM（第3世代）プロセス**をそのまま流用し、内部リフレッシュ制御によってSRAM的に動作。  
世界初の **カメラ付き携帯電話（SHARP製）** に搭載された。

This document archives the technology of a **pseudo-SRAM (VSRAM)** product mass-produced in 2001.  
It was based on a **0.25μm 64M DRAM 3rd-generation process**, reusing it as-is with internal refresh logic to behave like SRAM.  
The product was adopted in the **world’s first camera-equipped mobile phone** (by SHARP).

> ⚠️ 本記録に関する注意 / Disclaimer  
>
> 本VSRAM技術は2001年に量産されたものですが、**2000年代前半にはすでに生産終了**しており、  
> また社内においても**後続技術としての展開は行われませんでした**。  
> よって、本記録には**現行の事業機密や設計情報は含まれておらず**、  
> 教育目的および技術アーカイブ目的での**公開に問題はない**と判断しています。  
>
> The VSRAM technology documented here was mass-produced in 2001,  
> but production ended in the **early 2000s**, and **no further internal development was pursued**.  
> Therefore, this archive contains **no proprietary or confidential information**,  
> and it is released solely for **educational and historical purposes**.

---

## 1️⃣ 基本構成と特徴 / **Architecture and Features**

| 要素 | 内容 / Description |
|------|-------------------|
| プロセス流用 | **0.25μm世代の64M DRAMセル構造をそのまま使用**<br>*Direct reuse of 0.25μm 64M DRAM Gen3 process* |
| 疑似SRAM動作 | **0.25μmプロセス上で、内部リフレッシュ制御によりSRAM的に機能**<br>*SRAM-like operation via internal refresh logic on 0.25μm process* |
| モバイル仕様 | モバイル機器向けに以下を実現：<br>・低消費電力設計<br>・**標準80℃のDRAM保証を90℃へ拡張**<br>*Mobile features: low-power design, extended temperature range (from DRAM’s standard 80°C to 90°C)* |
| 採用実績 | 世界初カメラ付き携帯電話（SHARP）<br>*Adopted in SHARP’s first camera phone* |

---

## 2️⃣ 初期量産の課題と対策 / **Startup Challenges and Solutions**

### 🔸 概要 / Summary

| 項目 | 内容 / Description |
|------|-------------------|
| 初期歩留まり | 約30%、技術導入直後の課題<br>*Initial yield ~30%* |
| 改善主導者 | 筆者（当時29歳）が担当<br>*Led by author at age 29* |

---

### 2.1 ポーズリフレッシュ不良と対策（高温・長時間リフレッシュ間隔）  
**Pause Refresh Failure and Countermeasures (High Temp, Extended Refresh Interval)**

| 要素 | 内容 / Description |
|------|-------------------|
| 問題 | **標準DRAM保証温度（80℃）を超える90℃環境**での動作を求めた結果、<br>ポーズリフレッシュ時に**保持時間不足**が発生。<br>主因は**ジャンクションリークの増加**。<br>*Pause refresh failure occurred under 90°C operation (beyond standard 80°C DRAM spec), mainly due to increased junction leakage.* |

#### 🔧 対策分類と実施内容 / Classification of Countermeasures

| 区分 | 対策内容 | 説明 / Description |
|------|-----------|------------------|
| **① プロセス・物理的対策**<br>*Process/Physical* | **HF洗浄回数の最小化**<br>（WSA後の酸化膜保持）<br>*Minimized HF cleaning to preserve gate oxide post-WSA* | ストレージノードコンタクト接続部などにおいてゲート酸化膜の厚みが不足すると、リークが増大し保持不良に直結。<br>**WSA後のウェット洗浄工程を最小化**することで酸化膜を保護。<br>*Gate oxide thinning at Storage Node Contacts causes leakage; minimized wet etch post-WSA to preserve oxide integrity.* |
| **② 電気的設定対策**<br>*Electrical Parameter* | **バックバイアス強化：Vbs = −1V → −3V**<br>*Stronger back-biasing to suppress leakage* | セルのボディバイアスを負方向に強化することで、ジャンクションリークを低減し、保持特性を改善。<br>*Applied −3V back-bias to reduce leakage current under high-temp standby.* |

> 🔗 **この不良モードは、ウエハテストにおける [Bin5：Pause Refresh Fail](../in1998/dram_wafer_test_binclass_0.25um.md) に対応しています。**  
> This failure mode corresponds to [**Bin5: Pause Refresh Fail**](../in1998/dram_wafer_test_binclass_0.25um.md) in the wafer test bin classification for 0.25 µm DRAM.

---

### 2.2 ディスターブリフレッシュ対策  
**Disturb Refresh Failure Control**

| 要素 | 内容 / Description |
|------|-------------------|
| 問題 | 0.25μm特有のShort Channel Effect（SCE）により、セル反転（disturb）現象が発生。<br>**特に、標準保証温度の80℃では顕在化しなかったが、90℃保証を求めた際にリークが急増し、SCEが問題化した。**<br>*Disturb failures due to short-channel effects at 0.25μm node, which became prominent under elevated 90°C condition, though not critical at 80°C.* |
| 対策 | ゲートCD（寸法）の中心値管理を徹底し、セル間ばらつきによるリークを抑制。<br>*Tightened gate length (CD) centering to suppress variation-induced leakage.* |

> 🔗 **この不良モードは、ウエハテストにおける [Bin6：Disturb Refresh Fail](../in1998/dram_wafer_test_binclass_0.25um.md) に対応しています。**  
> This failure mode corresponds to [**Bin6: Disturb Refresh Fail**](../in1998/dram_wafer_test_binclass_0.25um.md) in the wafer test bin classification for 0.25 µm DRAM.

---

## 3️⃣ 次世代VSRAMの検討と不採用判断 / **Evaluation and Rejection of Next-Gen VSRAM (0.18μm)**

### 3.1 NANYA / 東芝プロセス 0.18μm VSRAM

| 要素 | 内容 / Description |
|------|-------------------|
| 評価対象 | NANYA製 0.18μm DRAM（東芝プロセス）<br>*NANYA/Toshiba 0.18μm DRAM process* |
| 検討内容 | 次世代VSRAM候補として検討<br>*Evaluated as next-gen VSRAM* |
| 問題点1 | トレンチキャパシタ構造により、ジャンクション面積が増大<br>*Trench capacitor increased junction area* |
| 問題点2 | 高温時の保持力が不足（90℃要件未達）<br>*Insufficient retention at 90°C* |
| 結果 | 実装不可と判断（保持力不足）<br>*Rejected due to failure to meet mobile retention specs* |

---

### 3.2 Mosys社 1T-SRAMの評価（参考）

| 要素 | 内容 / Description |
|------|-------------------|
| 評価対象 | Mosys社製 1T-SRAMマクロ<br>*MoSys 1T-SRAM macro* |
| プロセス | 0.18μm ロジックプロセス<br>*0.18μm logic process* |
| 特徴 | リフレッシュ不要・DRAMセル不要な高柔軟性構造<br>*No refresh and no DRAM cell; flexible structure* |
| 評価状況 | 筆者が当時高耐圧インテグレーション業務に従事しており、工数不足により未完了<br>*Evaluation not completed due to resource constraints* |
| 補足資料 | 📄 [`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md)<br>→ Mosys社の1T‑SRAM技術に関する概要・外部資料リンク集<br>*Supplementary reference for MoSys 1T‑SRAM technology*

---

## 4️⃣ 関連リンク / **Related Link**

📂 **64M DRAM 立ち上げ技術アーカイブ（1998年）**  
📄 [`DRAM_Startup_64M_1998.md`](../in1998/DRAM_Startup_64M_1998.md)

- **日本語**：64M DRAM（第3世代 / 0.25μm）の量産立ち上げ記録。プロセス条件展開、不良解析（Pause Refresh）、ゲート酸化膜ダメージ対策などを収録  
- **English**：Technical archive of 64M DRAM (3rd Gen / 0.25μm) startup, including process tuning, pause refresh failures, and gate oxide damage mitigation

---
