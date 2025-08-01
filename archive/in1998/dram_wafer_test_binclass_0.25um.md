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
