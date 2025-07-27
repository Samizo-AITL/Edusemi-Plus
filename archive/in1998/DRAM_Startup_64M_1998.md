## 📘 64M DRAM 第3世代（0.25μm）立ち上げ記録 – 三溝真一（1998）  
📘 64M DRAM 3rd Gen (0.25μm) Startup Record – Shinichi Samizo (1998)

> 📝 本文書は現在 **記録中** の技術資料です。内容は中途段階であり、今後追記・整理・補完予定です。  
> 📝 This document is **under development**, and contents are partial and subject to future updates.

> ⚠️ 本記録は、1998年当時における**技術移管・立ち上げ業務の実体験に基づく教育資料**です。  
> エプソン社における**DRAMは汎用技術の一部であり、主力製品ではなく**、  
> 本記録には**現在の事業機密や製品設計情報は一切含まれていません**。  
> 本記述はすべて**三溝真一個人の記憶・教育目的による再構成**であり、**技術アーカイブとしての公益的利用**を想定しています。

> ⚠️ This document is based on the **author's actual experience** during a technology transfer and ramp-up operation in 1998.  
> At Epson, **DRAM was not a core product** but a transitional legacy technology.  
> This record **does not include any proprietary or confidential design data** from current or past corporate operations.  
> All contents are **reconstructed from personal memory** for the **sole purpose of educational and archival use**.

---

### 🧭 プロジェクト概要 | Project Overview

| 項目 / Item | 内容 / Details |
|-------------|----------------|
| 製品名 / Product | **64M DRAM（第3世代 / 0.25μm）** |
| 年度 / Year | **1998年** |
| 担当者 / Lead Engineer | **三溝真一（Shinichi Samizo, 26歳）** |
| 移管元 / Transfer Fab | 三菱電機 熊本工場 KD棟（MotherFab）<br>Mitsubishi Electric Kumamoto Fab (KD Building) |
| 立ち上げ工場 / Ramp-up Site | セイコーエプソン 酒田工場 T棟<br>Seiko Epson Sakata Fab (T Building) |

---

### 🏗️ プロセス立ち上げ戦略 | Ramp-up Strategy

- KD棟の**処理条件**（フロッピー2枚）をT棟の**各要素プロセス**に展開  
  → Deploy **process specs** (2 floppy disks) from KD Fab to each **module process** at T Fab  
- **形状確認用ロット5本**を各要素工程に分配し、**条件出し**を実施  
  → Allocate **5 pilot lots** to individual modules for **parameter optimization**  
- **露光量**・**フォーカス**・**成膜条件**などを**パラメトリック展開**  
  → Explore **exposure dose**, **focus offset**, and **film formation** conditions parametrically  
- 処理条件は**電子流動票（Caps-T）**で標準化  
  → Standardize process flow via **Caps-T digital documentation**  
- 各要素プロセスの条件確立後、**信頼性評価用の本番ロット**を投入  
  → After stabilization, launch **production lots for reliability evaluation**

---

### 🔗 プロセスフロー詳細 | Full Process Flow

プロセスフローは以下の別ファイルにて整理されています：  
The full process flow is provided in the following separate documents:

- 📄 [DRAM_Process_Flow_Full.md（日本語版）](DRAM_Process_Flow_Full.md)  
- 📄 [DRAM_Process_Flow_Full_en.md（English Version）](DRAM_Process_Flow_Full_en.md)

> 📝 このフローは筆者の **記憶と記録に基づいて再構成** されたものであり、  
> **完全な正確性を保証するものではありません。教育・教材用途を目的としています。**  
> *This flow was **reconstructed from memory and internal documentation** by the author, and is intended for **educational purposes only**. It **may not reflect complete technical accuracy.***

---

### 🔍 不良解析と改善経緯 | Failure Analysis & Process Fix

| 🧭 フェーズ / Phase | 📄 内容（日本語） / Description (JP) | 🌐 内容（英語） / Description (EN) |
|------------------|----------------------------------|--------------------------------------|
| 🚀 本番ロット投入 / Production Lot | 信頼性評価用に**3ロット投入（Burn-in付き）** | 3 lots submitted for **burn-in and reliability testing** |
| 📉 初回歩留まり / Initial Yield | 初回歩留まり約**65%**、主不良は **ポーズリフレッシュ不良** | Initial yield was **~65%**, main failure: **pause refresh** |
| 🔍 不良解析 / Failure Analysis | **ポーズリフレッシュ不良**の原因調査を実施 | Investigated **pause refresh failure** root cause |
| ⚡ セル容量確認 / Cap Confirmation | **セル容量は正常** → **ストレージノードコンタクト〜N+/P-Well間リーク**を疑う | Capacitance was OK → Suspected **junction leakage** between **storage node contact and N+/P-Well** |
| 🧐 SEM観察 / SEM Observation | **THBストレージノードコンタクト**に、形状に大きな問題なし | No major defect in **THB storage node contact** shape |
| 📌 原因特定 / Root Cause | Gate-OX後の**アッシング工程におけるプラズマダメージ** | **Plasma damage** during **resist ashing after gate oxidation** |
| 🛠️ 改善処置 / Fix Action | Gate-OX後のレジスト剥離を**アッシング → ウエット処理**に変更し、**プラズマダメージを低減** | Changed **resist removal after Gate-OX** from **ashing to wet process** to **reduce plasma damage** |
| 🟢 歩留まり改善 / Final Yield | 歩留まり約**80%**に向上。**信頼性評価クリア → 量産フェーズへ**移行 | Improved to **~80% yield**. Passed reliability → Entered **mass production phase** |

---

### 🧪 ポーズリフレッシュ不良とは | What is Pause Refresh Failure?

📌 **ポーズリフレッシュ（Pause Refresh）**とは、DRAMの自動リフレッシュ動作を一時停止し、手動もしくは外部制御によるリフレッシュを行うモードであり、特に組込み用途や特殊タイミング制御が必要な応用で使われる機能である。  

📉 このモードにおいて**セル電荷が保持できず、リフレッシュ漏れが発生する不良**が報告された。  
主な原因は以下の通りと推定された：

- ストレージノードとN+/P-Well間にリーク電流が存在し、セル電荷保持が困難
- Gate-OX後のアッシングによる**プラズマダメージ**が、接合リークや電界変調を引き起こした可能性
- 特に**Pause状態でリフレッシュ間隔が長くなる**ことにより、微小リークが顕在化

🎯 **通常のリフレッシュでは顕在化せず、Pause Refreshという特殊条件でのみ顕在化**したため、歩留まり解析の難易度が高かった。

---
