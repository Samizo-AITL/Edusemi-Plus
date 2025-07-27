# モバイル用疑似SRAM（VSRAM）技術アーカイブ（2001年）  
*Edusemi-Plus/archive/in2001/VSRAM_2001.md*  
最終更新: 2025-07-27  

---

## 概要 / **Overview**

本ドキュメントは、2001年に量産された**モバイル用疑似SRAM（VSRAM）**の技術アーカイブである。64M DRAM第3世代プロセスを流用し、内部リフレッシュ制御によりSRAM的に動作させた本製品は、**世界初のカメラ付き携帯電話（SHARP製）**に搭載された。

This document archives the technology of a pseudo-SRAM (VSRAM) product mass-produced in 2001. Based on a 64M DRAM 3rd-generation process with internal refresh logic, it was adopted in the world's first camera-equipped mobile phone (by SHARP).

---

## 1. 基本構成と特徴 / **Architecture and Features**

- **プロセス流用 / Process Reuse**：64M DRAM（第3世代, 0.25μm）をそのまま適用  
  → Reused 0.25μm 64M DRAM process as-is

- **内部リフレッシュ制御 / Internal Refresh Logic**：疑似SRAMとして機能  
  → SRAM-like operation through auto-refresh mechanism

- **用途 / Application**：世界初のカメラ付き携帯電話に搭載  
  → Used in SHARP’s first-in-world camera-equipped mobile phone

- **低消費電力 / Low Power**：ポーズリフレッシュ（pause refresh）による待機電力の抑制  
  → Power-saving via extended refresh intervals

- **高温対応 / High-Temperature Operation**：85℃ → **90℃保証へ拡張**  
  → Guaranteed memory operation up to 90°C

---

## 2. 初期量産時の課題と対策 / **Startup Challenges and Solutions**

### ● 歩留まり：**30%台からの立ち上げ**  
→ 筆者（当時29歳）が投入され、プロセス課題の解決に従事  
→ Initial yield was only ~30%. The author (age 29 at the time) was assigned to lead improvement.

---

### 2.1 ポーズリフレッシュによる保持不良  
**Retention failure due to extended pause refresh**

**課題 / Problem**：
- リフレッシュ周期を限界まで延ばし、低消費電力化  
- 90℃保証によって**ジャンクションリークが増加**し、保持時間が不足  
- Pause refresh for low-power → higher temperature → increased junction leakage → data loss

**対策 / Solution**：
- **HF系洗浄回数の最小化**（Gate-OX形成後の膜減り防止）  
  → Reduced HF wet clean steps to preserve gate oxide thickness  
- **バックバイアス Vbs = -1V → -3V**（リーク電流抑制）  
  → Increased back-bias to suppress junction leakage  

---

### 2.2 WSA後のゲート膜残膜確保 / **Preserving Gate Oxide after WSA**

- WSA（Wordline Sidewall After）後、**ソース・ドレイン領域にゲート膜残膜を確保**  
- 特に**ストレージノードコンタクト（SNC）側のドレイン領域でダメージ防止が重要**  
- In contrast to 643rd (64M DRAM Gen3), where dry ashing was replaced by wet clean,  
  今回は**ウエット処理そのものを削減**し、**酸化膜の過剰除去を防止**

---

### 2.3 ディスターブリフレッシュ / **Disturb Refresh Failures**

**課題 / Problem**：
- 0.25μmでのSCE（Short Channel Effect）により、セル反転（disturb）発生  
- Cell inversion due to SCE-related leakage under disturb conditions

**対策 / Solution**：
- **ゲート寸法の中心値管理**を強化  
  → Tightened control of gate CD (Critical Dimension) center values  

---

### 3. 次世代VSRAMの検討と不採用判断（0.18μm世代）

#### 🧪 0.18μm世代VSRAM（NANYA / 東芝プロセス）の検討

次世代VSRAMとして、NANYA製 0.18μm DRAMプロセス（東芝系）の適用を検討したが、以下の技術的課題により採用を断念した。

- **トレンチキャパシタ構造**により、メモリセルの**ソースドレインのジャンクション面積が大きく**、高温時の**リーク電流が増加**  
- 高温90℃保証を要求するモバイル用途において、**保持時間が十分に確保できなかった**
- Pause Refresh条件を満たせず、実装に適さないと判断

---

#### 🧪 Mosys社 1T-SRAMマクロの検討（参考記録）

- **Mosys社の1T-SRAM**を、回路マクロとして0.18μmロジックプロセス上での適用を検討
- DRAMセル不要・リフレッシュ不要の構造により、**簡便なインプリ可能性**が期待された
- しかし、筆者は当時**高耐圧インテグレーション業務**に従事しており、**工数確保できず、本格検討には至らなかった**

> 検討のみで終了したが、SRAMマクロとしての柔軟性と簡易性は今後の参考になりうる構造であった。

---

## 4. 関連リンク / **Related Link**

📂 **64M DRAM立ち上げ技術アーカイブ（1998年）**  
📄 [`DRAM_Startup_64M_1998.md`](../in1998/DRAM_Startup_64M_1998.md)

- **日本語**：64M DRAM（第3世代 / 0.25μm）の量産立ち上げに関する実体験と技術課題を記録。プロセス条件の展開、不良解析（Pause Refresh）、ゲート酸化膜の損傷制御などを詳細に記述。  
- **English**：Technical archive of 64M DRAM (3rd generation / 0.25μm) production startup, including real-world experiences and issues such as pause refresh failures, gate oxide damage control, and yield improvement strategies.

---
