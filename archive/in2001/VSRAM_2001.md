# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ（2001年）  
*Edusemi-Plus/archive/in2001/VSRAM_2001.md*  
**最終更新: 2025-07-27**

---

## 🧭 概要 / **Overview**

本ドキュメントは、2001年に量産された **モバイル用疑似SRAM（VSRAM）** の技術アーカイブである。  
64M DRAM 第3世代プロセス（0.25μm）をそのまま流用し、内部リフレッシュ制御によってSRAM的に動作。  
世界初の **カメラ付き携帯電話（SHARP製）** に搭載された。

This document archives the technology of a **pseudo-SRAM (VSRAM)** product mass-produced in 2001.  
Based on a **64M DRAM 3rd-generation (0.25μm) process** with internal refresh logic, it was adopted in the **world’s first camera-equipped mobile phone** (by SHARP).

---

## 1️⃣ 基本構成と特徴 / **Architecture and Features**

- **プロセス流用 / Process Reuse**：64M DRAM（第3世代, 0.25μm）をそのまま適用  
  → *Reused 0.25μm 64M DRAM process as-is*

- **内部リフレッシュ制御 / Internal Refresh Logic**：疑似SRAMとして機能  
  → *SRAM-like operation via auto-refresh mechanism*

- **用途 / Application**：世界初のカメラ付き携帯電話に搭載  
  → *Used in SHARP’s world-first camera-equipped mobile phone*

- **低消費電力 / Low Power**：ポーズリフレッシュ（pause refresh）による待機電力の抑制  
  → *Power-saving via extended refresh intervals*

- **高温動作対応 / High-Temperature Operation**：85℃ → **90℃保証へ拡張**  
  → *Extended temperature guarantee from 85°C to 90°C*

---

## 2️⃣ 初期量産の課題と対策 / **Startup Challenges and Solutions**

### 🔸 歩留まり課題：**初期30%台からの立ち上げ**
→ 筆者（当時29歳）が投入され、実行的なプロセス改善を主導  
→ *Initial yield was ~30%; author (age 29) was assigned to drive yield recovery*

---

### 2.1 ポーズリフレッシュ保持不良 / **Pause Refresh Retention Failures**

**問題 / Issue**：
- 内部リフレッシュ周期を限界まで延長 → 消費電力は削減されたが、  
- **90℃保証下でのジャンクションリーク増大**により、**保持時間が不足**

**対策 / Countermeasures**：
- **HF系洗浄回数の最小化**  
  → *Minimized HF cleaning steps to preserve gate oxide integrity*
- **バックバイアス Vbs = -1V → -3V へ強化**  
  → *Applied stronger back-bias to suppress junction leakage*

---

### 2.2 WSA後ゲート膜の残膜確保 / **Preserving Gate Oxide after WSA**

- **WSA（Wordline Sidewall After）後に、ソース・ドレイン領域のゲート膜を保護**  
- 特に **ストレージノードコンタクト（SNC）** 接続部の膜厚確保が重要  
- *Unlike the 643rd (64M DRAM Gen3), where wet clean replaced ashing,  
  in this case, the wet process itself was minimized to avoid over-etching*

---

### 2.3 ディスターブリフレッシュ対策 / **Disturb Refresh Failure Control**

**問題 / Issue**：
- **0.25μm特有のShort Channel Effect（SCE）** により、**セル反転（disturb）現象が発生**

**対策 / Countermeasure**：
- **ゲート寸法（CD）中心値管理を徹底**  
  → *Tightened control of gate length (CD) centering to reduce variation-induced leakage*

---

## 3️⃣ 次世代VSRAMの検討と不採用判断 / **Evaluation and Rejection of Next-Gen VSRAM (0.18μm)**

### 🧪 3.1 0.18μm世代VSRAM（NANYA / 東芝系プロセス）

**検討内容 / Evaluation**：
- 次世代VSRAM候補として、**NANYA製（東芝プロセス）0.18μm DRAM** を評価

**問題点 / Issues Identified**：
- **トレンチキャパシタ構造**により、**ジャンクション面積が増大**  
- **保持力が不足**し、**90℃のPause Refresh要件を満たせなかった**

→ **実装不可と判断 / Rejected for insufficient retention under mobile temperature specs**

---

### 🧪 3.2 Mosys社 1T-SRAMマクロの検討（参考）

- **Mosys社製1T-SRAMマクロ**を、**0.18μmロジックプロセス上**で検討  
- リフレッシュ不要・DRAMセル不要な**高柔軟性構造**  
- しかし当時、筆者は**高耐圧インテグレーション業務に従事しており、工数確保できず**

→ **評価未完了 / Evaluation not completed due to resource constraints**

---

## 4️⃣ 関連リンク / **Related Link**

📂 **64M DRAM 立ち上げ技術アーカイブ（1998年）**  
📄 [`DRAM_Startup_64M_1998.md`](../in1998/DRAM_Startup_64M_1998.md)

- **日本語**：64M DRAM（第3世代 / 0.25μm）の量産立ち上げ記録。プロセス条件展開、不良解析（Pause Refresh）、ゲート酸化膜ダメージ対策などを収録  
- **English**：Technical archive of 64M DRAM (3rd Gen / 0.25μm) startup, including process tuning, pause refresh failures, and gate oxide damage mitigation

---
