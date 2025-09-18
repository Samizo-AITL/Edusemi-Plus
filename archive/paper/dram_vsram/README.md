---
layout: default
title: "歴史的ケーススタディ：DRAMからVSRAMへ (1997–2001)"
description: "0.5µm 16M DRAMから始まり、0.35µm 64M DRAM第2世代、0.25µm DRAM第3世代立ち上げ、そしてモバイル用VSRAMの挑戦と断念までを追う歴史的アーカイブ。"
tags: ["DRAM", "VSRAM", "半導体プロセス", "歩留まり改善", "技術史", "1T-1C"]
---

# 📘 歴史的ケーススタディ：DRAMからVSRAMへ (1997–2001)

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../README.md#著者・ライセンス--author--license)

---

⚠️ **免責事項 / Disclaimer**  
本ドキュメントは1997〜2001年にかけての筆者の実体験を教育・アーカイブ目的で再構成したものです。  
現行の企業機密や製品設計情報は含まれていません。  

This document is based on the author’s work experience between 1997–2001, reconstructed for educational and archival purposes.  
No current proprietary or product data is included.

---

## 📖 プロローグ (1997まで)

### 0.5 µm 16M DRAM
- 酒田Fabの最初の本格量産品。比較的順調に立ち上げ。  
- DRAM技術を通じてFab稼働を確立。  

### 0.35 µm 64M DRAM (2nd Gen, 1997)
- 三菱熊本工場からの技術移管。  
- 初期は30ロット以上失敗 → SEM測定すら困難。  
- 原因：洗浄フロー差異（硫酸過水省略）。  
- 解決：熊本プロセスを酒田へ完全移植 → 量産化に成功。  

➡ この経験を踏まえて **0.25 µm 3rd Gen DRAM (1998)** に挑む。  

---

## 📘 パート1 (1998年)  
### 0.25 µm 64M DRAM (3rd Gen) 立ち上げ記録

- **立ち上げ方式**：SCF（Short Cycle Feedback）。  
- **技術要素**：初めてのKrF露光導入。  
- **データ受領**：フロッピー2枚分の条件からスタート。  
- **工場総動員体制**：4班2直、夜勤対応、防塵ノートでの引き継ぎ。  

#### 初期不良と解析
- 初期Yield：約65%。  
- 主不良：**ポーズリフレッシュ (Bin5)**。  
- SEM観察：構造異常なし、容量正常。  
- 工程解析：WSA-ET後や複数LDDのアッシング工程でプラズマダメージ蓄積。  

#### 改善対策
- レジスト剥離を **ドライアッシング → ウェット処理主体** へ変更。  
- 結果：**Yield 80%へ改善、信頼性クリア**。  

➡ DRAM固有課題「Pause Refresh」を克服し量産化。  

---

## 📗 パート2 (2001年)  
### モバイル用 VSRAM 技術アーカイブ

#### 0.25 µm VSRAM (Mitsubishiプロセス × Epson設計)
- DRAMセル流用、内部リフレッシュ制御でSRAM化。  
- 世界初カメラ付き携帯電話（Epson VSRAM + Sharp Flash）に採用。  
- 初期Yield：**30%**。  
- 課題：Pause Refresh / Disturb Refresh（90℃保証で顕著）。  
- 対策：  
  - HF洗浄最小化、酸化膜保持。  
  - Back-bias −1V → −3V。  
  - ゲートCD中心値管理。  
- 結果：**Yield 80〜90%へ回復**。  

#### 0.18 µm VSRAM (Toshibaプロセス × Epson設計, NANYA製造)
- トレンチキャパシタ構造。  
- ジャンクション面積増大 → リーク悪化。  
- 90℃保持不足 → **採用断念**。  

---

## 🔎 考察 / Discussion

- **1T-1C DRAM/VSRAMの宿命**：セルフリフレッシュ＋高温保証を課すと歩留まり劣化が顕在化。  
- **DRAM立ち上げ**は工場全体の総力戦。技術だけでなく、組織力・現場力を鍛える場だった。  
- **VSRAM**は短命だったが、携帯電話の歴史を変える「カメラ付き携帯」の実現に貢献。  
- 技術的には2001年以降限界を迎えるが、**1T-1Cの特性を理解する上で象徴的な事例**となった。  

---

## 📅 タイムライン / Timeline

- 1997年：0.35 µm 64M DRAM (2nd Gen) 立ち上げ  
- 1998年：0.25 µm 64M DRAM (3rd Gen) 立ち上げ → Pause Refresh対策成功  
- 2001年：0.25 µm VSRAM 量産化 → 携帯電話採用  
- 2001年：0.18 µm VSRAM（トレンチキャパ） → 保持力不足で断念  

---
