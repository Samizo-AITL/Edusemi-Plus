# 📘 64M DRAM 第3世代（0.25μm）立ち上げ記録 （1998）

📘 **64M DRAM 3rd Gen (0.25μm) Startup Record (1998)**  

---

⚠️ 本記録は、1998年当時における**技術移管・立ち上げ業務の実体験**に基づく教育資料です。  
エプソン社におけるDRAMは**汎用技術の一部であり主力製品ではありません**。  
本記録には**現在の事業機密や設計情報は一切含まれていません**。  
すべて三溝真一個人の記憶に基づき、**教育・技術アーカイブ目的で再構成**したものです。  

⚠️ This document is based on the author's actual experience during a technology transfer and ramp-up in 1998.  
At Epson, DRAM was not a core product but a transitional legacy technology.  
This archive contains no proprietary or confidential design data. It is reconstructed from memory for educational and archival purposes.

---

## 🧭 プロジェクト概要 | Project Overview

| 項目 / Item             | 内容 / Details                                                |
|------------------------|---------------------------------------------------------------|
| 製品名 / Product       | 64M DRAM（第3世代 / 0.25μm）                                  |
| 年度 / Year            | 1998年                                                       |
| 担当者 / Lead Engineer | 三溝真一（Shinichi Samizo, at age 26）                            |
| 移管元 / Transfer Fab   | 三菱電機 熊本工場 KD棟（MotherFab）                          |
|                        | Mitsubishi Electric Kumamoto Fab (KD Building)               |
| 立ち上げ先 / Ramp-up Site | セイコーエプソン 酒田工場 T棟                                |
|                        | Seiko Epson Sakata Fab (T Building)                          |

---

## 🏗️ プロセス立ち上げ戦略 | Ramp-up Strategy

- KD棟の処理条件（**フロッピー2枚分**）を、T棟の各要素工程に展開  
  → *Deploy process specs (2 floppy disks) from KD Fab to each module at T Fab*

- 形状確認用ロット5本を各モジュール工程に分配し、**最適プロセス条件を検討**  
  → *Allocate 5 pilot lots to each module process to evaluate and adjust key process parameters*

- **露光量・フォーカス・成膜条件など、各プロセスの条件出しを実施**  
  → *Performed process condition tuning for parameters such as exposure dose, focus, and film deposition*

- **電子流動票（Caps-T）**により工程条件を標準化  
  → *Standardize via Caps-T digital flow control*

- 条件確立後、**信頼性評価用の本番ロット**を投入  
  → *Launch production lots for reliability testing after stabilization*

---

## 🔗 プロセスフロー詳細 | Full Process Flow

📂 プロセスフローは以下にて別途整理：  
📂 The full process flow is provided in the following separate documents:

**📝 教材目的の再構成であり、技術的完全性は保証されません。**  
**📝 This flow is reconstructed for educational purposes and does not guarantee complete technical accuracy.**

- 📄 [`DRAM_Process_Flow_Full.md`](DRAM_Process_Flow_Full.md)（日本語 / Japanese）  
- 📄 [`DRAM_Process_Flow_Full_en.md`](DRAM_Process_Flow_Full_en.md)（英語 / English）

---

## 📊 本番ロット投入後の展開 | Post-Production Lot Developments

### ① 🔍 フェーズ別の解析と改善 | Phase-by-Phase Analysis & Fix

| 🧭 フェーズ / Phase         | 📄 日本語 / Description (JP)                                         | 🌐 英語 / Description (EN) |
|----------------------------|---------------------------------------------------------------------|-----------------------------|
| 🚀 本番ロット投入           | 信頼性評価用に**3ロット投入（Burn-in付き）**                       | 3 lots submitted for **burn-in and reliability testing** |
| 📉 初回歩留まり             | 歩留まり約**65%**、主不良は **ポーズリフレッシュ不良**             | Initial yield was **~65%**, main failure: **pause refresh** |
| 🔍 不良解析                 | **ポーズリフレッシュ条件でのビットエラー発生原因**を調査            | Investigated root cause of **bit errors under pause refresh conditions** |
| ⚡ セル容量確認             | **セル容量は正常** → **SNコンタクト〜N+/P-Well間リーク**を疑う      | Cap OK → Suspected **junction leakage between storage node contact and N+/P-Well** |
| 🧐 SEM観察                 | **SNコンタクト構造に大きな欠陥なし**（THB領域含む）                 | No major defect in **storage node contact** structure (including THB region) |
| 📌 原因特定                 | **Gate-OX後のアッシングによるプラズマダメージ**                     | **Plasma damage** during **resist ashing after gate oxidation** |
| 🛠️ 改善処置                 | レジスト剥離を**アッシング → ウエット処理**に変更しダメージを抑制    | Changed **resist removal** from **ashing to wet process** to reduce plasma damage |
| 🟢 歩留まり改善             | 歩留まりが**約80%に向上**、信頼性試験もクリアし**量産へ移行**       | Improved to **~80% yield**, passed reliability → entered **mass production phase** |

---

### ② 🧪 ポーズリフレッシュ不良とは | What is Pause Refresh Failure?

📌 **ポーズリフレッシュ不良（Pause Refresh Failure）**とは、DRAMセルの**電荷保持能力（リテンション）**を評価するため、  
リフレッシュ動作を一時停止し、**一定時間経過後にセル内容を読み出してビット誤りを検出する**試験で発生する不良です。  
This failure mode occurs during **retention testing** by pausing refresh operations and reading cell contents after a delay to detect bit errors.

> 🔗 **この不良モードはウエハテストBin分類において [Bin5：Pause Refresh Fail](./dram_wafer_test_binclass_0.25um.md) に対応しています。**  
> This failure corresponds to [**Bin5: Pause Refresh Fail**](./dram_wafer_test_binclass_0.25um.md) in the DRAM wafer test bin classification.

---

#### 🔍 不良の概要 | Failure Characteristics

- 通常のリフレッシュ周期では問題なし  
  No issue under normal auto-refresh intervals

- **Pause Refresh条件下**でビットエラーが発生  
  Bit errors observed under **pause refresh condition**

- エラービットの解析より、**ストレージノードコンタクトからのリークの疑い**が示唆された  
  Analysis suggested **possible leakage from the storage node contact**

---

#### 💡 推定原因 | Suspected Root Cause

- **Gate-OX後のアッシング処理によるプラズマストレス**  

 → Plasma stress from resist ashing after gate oxidation

- **SNコンタクトとN+/P-Well間の微小リークパス形成**  
  → Formation of minor leakage path between storage node contact and N+/P-Well

- **セルキャパシタ自体に異常はなし**  
  → Capacitor itself was confirmed to be intact

---

#### ✅ 対策と効果 | Countermeasure & Effect

- Gate-OX後のレジスト剥離工程を**アッシング → ウエット処理**に変更  
  → Changed resist removal from **ashing to wet strip** to reduce plasma damage

- **Pause Refresh不良は再現せず、安定性確認済み**  
  → Pause refresh failures were no longer observed after the fix

- 歩留まりは**65% → 80%に改善し、量産移行**  
  → Yield improved from **~65% to ~80%**, enabling transition to mass production

---

## 📎 補足技術資料 | Supplementary Technical References

以下の資料は、本記録の理解を深めるための**補足教材**です。DRAMセル構造、メーカーごとの特徴、世代別進化などを整理しています。  
The following documents serve as supplementary materials to enhance understanding of this record. They include comparisons of DRAM cell structures, vendors, and generational evolution.

- 📄 [`DRAM_Maker_Comparison_1998.md`](DRAM_Maker_Comparison_1998.md)  
　→ **1998年当時の主要DRAMメーカー比較 / Comparison of Major DRAM Makers in 1998**  
　→ セル構造・製造拠点・技術的強みに基づく一覧資料 / Tabulated vendor traits by structure, fab, and strengths  

- 📄 [`DRAM_Cell_Structure_Comparison.md`](DRAM_Cell_Structure_Comparison.md)  
　→ **トレンチセル vs スタックセルの構造比較 / Structural Comparison: Trench vs Stacked Cells**  
　→ 製造難易度、微細化適性、リテンションなどの観点での整理 / Compared on scalability, process, and retention  

- 📄 [`DRAM_Cell_Technology_Chronology.md`](DRAM_Cell_Technology_Chronology.md)  
　→ **1M〜256Mまでのセル技術年表 / Cell Technology Chronology: From 1M to 256M**  
　→ 世代別の構造変遷と技術転換点を年表形式で整理 / Timelined transition from planar to stacked with key inflection points

- 📄 [`dram_wafer_test_binclass_0.25um.md`](dram_wafer_test_binclass_0.25um.md)  
　→ **0.25μm DRAM ウエハテストのBin分類表（日本語・英語併記） / 0.25µm DRAM Wafer Test Bin Classification (Bilingual)**  
　→ フェイルストップ方式に基づくBin分類と不良モード整理、教育用途向けドキュメント / Fail-stop-based bin classification and failure mode summary for educational use

---

## 🔗 関連リンク / **Related Link**

### 📂 **注目技術アーカイブ / Featured Archive：VSRAM（2001年）**

📄 **[`VSRAM_2001.md`](../in2001/VSRAM_2001.md)**  
> 🚀 **モバイル用疑似SRAMとしてDRAMプロセスを転用！**  
> 世界初の **カメラ付き携帯電話（SHARP製）** に搭載された革新メモリ

- **日本語**：64M DRAM（第3世代）のプロセスをそのまま流用し、内部リフレッシュによる擬似SRAMとして動作。  
　ポーズリフレッシュ不良やディスターブ不良に対し、**HF洗浄工程の最適化**、**バックバイアス制御**、**ゲートCD管理**などを駆使して量産対応。

- **English**：A pseudo-SRAM leveraging the 3rd-gen 64M DRAM process with built-in refresh logic.  
　Adopted in the world’s first **camera-equipped mobile phone by SHARP**.  
　Key engineering responses included **reduced HF clean steps**, **back-bias tuning**, and **tight gate CD control** to address pause-refresh and disturb failures.

---

> 📘 教材・アーカイブ目的で再構成された資料です。内容は歴史的再現であり、現行技術や設計とは異なります。  
> 📘 These materials are reconstructed for archival and educational purposes, and do not represent current DRAM design or technology.

---
