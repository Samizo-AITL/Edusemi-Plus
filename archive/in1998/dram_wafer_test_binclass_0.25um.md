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

**🧪 テスト目的 / Purpose**  
リフレッシュを一時停止し、セルの電荷保持能力（リテンション）を評価する。  
To pause refresh and evaluate the cell's charge retention ability.

**🔁 テスト手順 / Procedure**  
1. 任意データ（例：0xAA, 0x55）を全セルに書き込み  
2. リフレッシュを一定時間停止（例：1s, 5s, 10s）  
3. セル内容を全読み出しし、化けビットを検出  
→ 弱セルの保持不良を確認  
<br>
1. Write data (e.g., 0xAA, 0x55) to all cells  
2. Pause refresh for a defined duration (e.g., 1s, 5s, 10s)  
3. Read out all cells and check for bit flips  
→ Detect weak retention cells

**⚙️ テスト条件 / Conditions**  
- パターン：0xAA / 0x55 alternating  
- 温度：25°C または高温（85°C〜90°C）  
- 判定基準：1ビット以上の誤りでFail  
<br>
- Pattern: 0xAA / 0x55 alternating  
- Temperature: Room (25°C) or elevated (85°C–90°C)  
- Fail Criteria: ≥ 1 bit error detected

---

### 🔸 Bin6：ディスターブリフレッシュ不良 / Disturb Refresh Fail

**🧪 テスト目的 / Purpose**  
隣接行の激しいアクセスによって生じるセル干渉（Disturb）による保持劣化を評価する。  
To evaluate retention degradation due to interference from aggressive access to neighboring rows.

**🔁 テスト手順 / Procedure**  
1. ターゲット行（例：Row 100）にデータ書き込み  
2. 隣接行（Row 99, 101）を高頻度アクティブ（例：100K〜1M回）  
3. ターゲット行を再読み出しし、化けビットを検出  
→ 干渉によるリーク発生有無を評価  
<br>
1. Write data to target row (e.g., Row 100)  
2. Repeatedly activate adjacent rows (e.g., Row 99 and 101, 100K–1M times)  
3. Read back target row and detect flipped bits  
→ Evaluate if disturbance-induced leakage occurred

**⚙️ テスト条件 / Conditions**  
- ストレスアクセス数：100K〜1M回  
- 温度：高温条件（85〜90℃）で実施  
- 判定基準：1ビット以上の誤りでFail  
<br>
- Stress count: 100K–1M accesses  
- Temperature: Elevated (85°C–90°C)  
- Fail Criteria: ≥ 1 bit error detected

---

## 🌡️ ウエハテストの温度条件 / Temperature Conditions in Wafer Test

メモリ製品のウエハテストでは、**以下の温度順序でテストが実施される**のが一般的です：

In memory wafer testing, it is common to run tests across the following temperature sequence:

| フェーズ / Phase | 温度条件 / Temperature | 説明 / Description |
|------------------|------------------------|--------------------|
| RT（常温）        | 25 °C                  | 初期ファンクション確認やスクリーニング用途<br>Used for initial function check and screening |
| HT（高温）        | 80 °C（VSRAMは90 °C）   | リーク電流・保持特性の評価に最重要。<br>Pause/Disturb Failが最も発生しやすい領域。<br>Critical for leakage and retention failures |
| LT（低温）        | −25 °C                 | タイミングやリテンションマージンの低温依存性確認<br>Evaluate cold-temp behavior and margin |

> ✅ 特にVSRAMでは、**DRAM標準の80℃保証を超える90℃での安定動作**が求められ、高温ウエハテストが合否を左右します。  
> VSRAM products require stable operation at 90°C, making HT wafer testing essential.

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
