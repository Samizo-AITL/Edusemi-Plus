---
layout: default
title: "Appendix: 0.25µm DRAM / VSRAM 補足資料"
---

---

# 📎 Appendix: 補足資料 / Supplementary Materials

---

## 1️⃣ 0.25µm DRAM プロセスフロー（概要版）

**日本語**  
1998年立ち上げ時に用いられた、0.25 µm 64M DRAM（第3世代）の代表的なプロセスフロー。  
詳細は [`DRAM_Process_Flow_Full.md`](../../in1998/DRAM_Process_Flow_Full.md) を参照。  

**English**  
Representative process flow of 0.25 µm 64M DRAM (3rd Generation) during the 1998 startup.  
See [`DRAM_Process_Flow_Full.md`](../../in1998/DRAM_Process_Flow_Full.md) for full details.  

- Semi-recess LOCOS isolation  
- Triple-well, Deep N-Well  
- Poly/WSi stacked gate electrode (WSA-ET process)  
- Stacked capacitor with roughened surface (1.5–1.8× capacitance boost)  
- WSB-CVD simultaneous bit line & contact formation  
- AlCu/TiN metallization, SOG planarization, SiN/PI passivation  

---

## 2️⃣ 0.25µm DRAM ウエハテスト Bin分類表

**日本語**  
ウエハテストはフェイルストップ方式で実施され、致命的不良から順にBin分類される。  
詳細は [`dram_wafer_test_binclass_0.25um.md`](../../in1998/dram_wafer_test_binclass_0.25um.md) を参照。  

**English**  
Wafer tests followed a fail-stop scheme, classifying chips into bins in order of fatality.  
See [`dram_wafer_test_binclass_0.25um.md`](../../in1998/dram_wafer_test_binclass_0.25um.md) for details.  

| Bin | 日本語テスト項目 | Test Item (English) | 内容概要 |
|-----|----------------|----------------------|-----------|
| 1   | オープン／ショート | Open / Short | 配線断線・短絡 |
| 2   | スタンバイ電流異常 | Standby Current Fail | リーク過大 |
| 3   | アクティブ電流異常 | Active Current Fail | 動作中電流異常 |
| 4   | ファンクション不良 | Function Check Fail | 読書き失敗・デコード異常 |
| 5   | ポーズリフレッシュ不良 | Pause Refresh Fail | セル保持不足 |
| 6   | ディスターブリフレッシュ不良 | Disturb Refresh Fail | 隣接セル干渉による保持低下 |
| 7   | マージン不良 | Margin Fail | 電圧・タイミング余裕不足 |

---

## 3️⃣ VSRAM / DRAM / トレンチVSRAM 比較表

| 項目 / Item | 0.25 µm DRAM (3rd Gen) | 0.25 µm VSRAM | 0.18 µm VSRAM (Trench) |
|-------------|------------------------|---------------|-------------------------|
| セル構造 | スタックキャパシタ | スタックキャパシタ（流用） | トレンチキャパシタ |
| リフレッシュ | 外部制御必須 | 内部制御（疑似SRAM動作） | 内部制御（疑似SRAM動作） |
| 温度保証 | 80 °C | 90 °C（モバイル仕様） | 90 °C目標（未達成） |
| 特徴 | 量産立ち上げ成功 | 世界初カメラ付き携帯に採用 | 保持不足で断念 |
| 意義 | 先端技術吸収のビークル | モバイル応用成功事例 | 1T-1C限界を示す事例 |

---

## 4️⃣ 教育的意義 / Educational Significance

- DRAM量産を **目的そのものではなく「先端技術吸収と社内展開の戦略的ビークル」** と位置づけた点が特徴的。  
- プロセス解析・不良対策・歩留まり改善の実体験が、後続製品（VSRAMなど）に直結。  
- 0.25 µm世代の事例は、**微細化移行期における企業戦略と技術継承** の教材として有用。  

---

📘 本Appendixは、論文本文を補完する参考資料集であり、詳細なプロセス表やテスト条件を収録した。  
