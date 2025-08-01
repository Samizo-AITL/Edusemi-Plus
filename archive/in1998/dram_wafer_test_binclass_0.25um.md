# 0.25µm DRAM ウエハテスト：Bin分類表（日本語・英語併記）

本ドキュメントは、0.25µm世代DRAMにおけるウエハテストのBin分類を、日本語・英語併記で整理したものです。テストはフェイルストップ方式に基づき、致命的な不良から順に評価されます。

This document summarizes the bin classification used in wafer testing of 0.25µm generation DRAM. Tests are executed in a fail-stop manner, prioritizing fatal failures first.

---

## 📘 Bin分類表 / Bin Classification Table

| Bin  | テスト項目（日本語）                     | Test Item (English)              | 内容説明（日本語）                                                                 | Description (English)                                                                |
|------|------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Bin1 | オープン／ショート                        | Open / Short                     | 配線断線やブリッジなど、致命的な導通異常。DC測定で検出される。                       | Critical wiring defects such as opens or shorts. Detected by DC continuity test.       |
| Bin2 | スタンバイ電流異常                        | Standby Current Fail             | スタンバイ状態でのリーク電流が規格を超過。セル・ジャンクションのリークなどが原因。 | Excessive leakage in standby mode. May be due to cell or junction leakage.             |
| Bin3 | アクティブ電流異常                        | Active Current Fail              | 動作中の電流が異常に高い。ロジック暴走やセル破壊などが原因。                         | Abnormally high current during active operation. Caused by logic malfunction or damage. |
| Bin4 | ファンクションチェック不良                | Function Check Fail              | 読み出し／書き込み失敗、パターン化け、アドレスデコード不良など。                     | Read/write failure, data corruption, address decoding issues.                          |
| Bin5 | ポーズリフレッシュ不良                    | Pause Refresh Fail               | スタンバイ中にデータが保持されない。弱セルによるチャージ保持不足。                   | Charge loss during standby due to weak cell retention.                                 |
| Bin6 | ディスターブリフレッシュ不良              | Disturb Refresh Fail             | 他セルのアクセスにより、干渉でリークが誘発され保持力が低下。                         | Cell disturbance due to access to neighboring rows; leads to retention loss.           |
| Bin7 | マージン不良（電圧・タイミング）          | Margin Fail (Voltage/Timing)     | 動作はするが、電圧（Vcc）やタイミング（tRCDなど）の余裕が足りず、設計マージン不足。 | Functional but fails under marginal voltage/timing specs (e.g., Vcc, tRCD).            |

---

## 🔧 テスト実行順と意図 / Test Execution Order and Rationale

- Bin1〜3：**致命的DC不良** → チップが全く動作しないため、最初に判定されます。  
  Bins 1–3: **Fatal DC failures**, which prevent any functionality. Tested first.

- Bin4：**機能チェック** → 最小限のDRAM機能があるかを確認。  
  Bin 4: **Functionality check** for minimal DRAM operation.

- Bin5〜6：**保持特性チェック** → DRAM固有のセル保持力・干渉耐性の評価。  
  Bins 5–6: **Retention behavior**, specific to DRAM cell characteristics.

- Bin7：**設計マージンチェック** → 正常動作するがスペック保証外。軽度の分類。  
  Bin 7: **Margin checks**. Device operates but falls outside design specifications.

---

## 🧪 Bin5・Bin6のテストパターン概要 / Test Pattern Overview for Bin5 and Bin6

**Bin5（ポーズリフレッシュ不良）および Bin6（ディスターブリフレッシュ不良）** は、DRAM特有の保持特性に関するテストです。以下に代表的なウエハテストパターンを示します。

**Bin5 (Pause Refresh Fail)** and **Bin6 (Disturb Refresh Fail)** are specific to DRAM retention behavior. Representative wafer test patterns are outlined below.

---

### 🔹 Bin5：ポーズリフレッシュ不良 / Pause Refresh Fail

| 項目 / Item         | 内容 / Description |
|----------------------|--------------------|
| テスト目的 / Purpose | **リフレッシュを一時停止**し、セルの電荷保持能力（リテンション）を評価する | To pause refresh and evaluate the cell's charge retention ability |
| 手順 / Procedure     |  
1. 任意データ（例：AA55）を書き込み  
2. **一定時間リフレッシュを停止（例：1s, 5s）**  
3. セルを全読み出しし、化けビットを検出  
→ 弱セルはこの間にリークしてエラーを起こす  
<br>  
1. Write data (e.g., AA55 pattern)  
2. **Pause refresh for a fixed time (e.g., 1s, 5s)**  
3. Read out and detect flipped bits  
→ Weak cells leak charge and cause errors |
| テスト条件 / Conditions |  
- データ：0xAA / 0x55 alternating  
- ウェイト時間：1s / 5s / 10s  
- 温度：常温または高温（例：85℃）  
- Fail判定：1bit以上のエラー検出  
<br>  
- Data: 0xAA / 0x55 alternating  
- Wait time: 1s / 5s / 10s  
- Temperature: room or elevated (e.g., 85°C)  
- Fail if any bit error is detected |

---

### 🔸 Bin6：ディスターブリフレッシュ不良 / Disturb Refresh Fail

| 項目 / Item         | 内容 / Description |
|----------------------|--------------------|
| テスト目的 / Purpose | **近隣行の激しいアクセス**によるセル干渉（disturb）による保持劣化を検出する | To detect retention degradation caused by aggressive access to adjacent rows |
| 手順 / Procedure     |  
1. ターゲット行にデータを書き込み  
2. **隣接行を高頻度でアクティブ（例：10万回）**  
3. ターゲット行を再読み出しし、ビット化けを検出  
→ セル間電界干渉によるリークを評価  
<br>  
1. Write data to target row  
2. **Aggressively activate neighboring rows (e.g., 100K times)**  
3. Read target row to detect flipped bits  
→ Evaluate cell-to-cell interference and leakage |
| テスト条件 / Conditions |  
- ターゲット行：Row 100  
- ストレス行：Row 99, 101  
- アクセス回数：100K / 1M  
- 高温条件で実施（例：85〜90℃）  
- Fail判定：1bit以上のエラー  
<br>  
- Target row: Row 100  
- Stress rows: Row 99, 101  
- Access count: 100K / 1M  
- Elevated temperature (e.g., 85–90°C)  
- Fail if any bit error is detected |

---

## 📎 教育的補足 / Educational Notes

- フェイルストップ方式により、**致命的な不良で即Bin振り分けが行われる**。  
  Fail-stop ensures early binning when a fatal error is detected.

- Bin7は**ファンクション通過後にのみ評価**されるため、テストの最後に実施される。  
  Bin 7 is executed **only after passing functional checks**.

- 各Binは、**歩留まり分析・バーンインとの相関・統計分析（Pareto等）**に活用可能。  
  Bins can be used for **yield analysis, burn-in correlation, and Pareto studies**.

---

## 📝 使用例 / Application Example

この分類は、ウエハテスト仕様書、教育資料、工程改善レポート、歩留まりトラブルシュートなどに利用できます。

This classification can be used in wafer test specs, educational documents, process improvement reports, and yield debugging.

---

## 🔗 関連リンク / Related Links

- 📄 [`DRAM_Startup_64M_1998.md`](../in1998/DRAM_Startup_64M_1998.md)  
- 📄 [`VSRAM_2001.md`](../in2001/VSRAM_2001.md)
