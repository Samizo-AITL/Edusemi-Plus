---
layout: default
title: "0.25µm 64M DRAM (3rd Gen) Startup Record (1998)"
---

# 📘 0.25µm 64M DRAM (3rd Gen) Startup Record (1998)

## 1️⃣ 背景 / Background

**日本語**  
1998年、三菱電機KD工場（熊本）で確立された0.25µm 64M DRAMプロセスが、セイコーエプソン酒田工場へ技術移管された。酒田工場ではこれを単なる製品量産目的ではなく、**先端技術を吸収し、社内他製品へ展開するための戦略的ビークル**として活用した。  
初めて **KrFリソグラフィ** を導入し、工場全体が動員される大規模な立ち上げイベントとなった。エンジニアは4班2直体制で夜勤にも対応し、防塵ノートを介して条件変更や解析結果を綿密に引き継いだ。  

**English**  
In 1998, the 0.25 µm 64M DRAM process established at Mitsubishi’s Kumamoto KD Fab was transferred to Seiko Epson’s Sakata Fab. This was not pursued merely for product mass production but served as a **strategic vehicle to absorb cutting-edge technology and deploy it into Epson’s in-house products**.  
It marked the first introduction of **KrF lithography** at the site, and the entire fab was mobilized for the ramp-up. Engineers worked in a four-team, two-shift system with night duty, using cleanroom notebooks for precise handovers of process changes and analysis results.

---

## 2️⃣ プロセス概要 / Process Overview

- **素子分離 / Device Isolation**: Semi-recess LOCOS  
- **ウェル構成 / Well Structure**: Triple-well, Deep N-Well  
- **ゲート電極 / Gate Electrode**: Poly/WSi stacked, with WSA-ET process  
- **キャパシタ / Capacitor**: Stacked type, roughened surface for 1.5–1.8× capacitance boost  
- **ビットライン / Bit Line**: WSB-CVD simultaneous BL + contact formation  
- **配線・封止 / Interconnects & Passivation**: AlCu/TiN metallization, SOG planarization, SiN/PI passivation

---

## 3️⃣ 立ち上げ方法 / Ramp-up Methodology

- **SCF (Short Cycle Feedback)** による短サイクル最適化  
- 母工場からの **フロッピー2枚分の条件データ** を電子流動票に展開  
- **形式ロット10本投入 → 本番ロット3本（信頼性用）＋マージンロット同時投入**

*Adopted SCF methodology for rapid process optimization, transferring two floppy disks of recipe data into the e-traveler, running 10 pilot lots, followed by 3 production lots (for reliability) in parallel with margin lots.*

---

## 4️⃣ 不良解析 / Failure Analysis

- **初期歩留まり**: 約65%  
- **主不良モード**: Pause Refresh Fail (Bin5)  
- **解析経過**:  
  - セル容量は正常  
  - SEM観察では構造欠陥なし  
  - 工程解析で **WSA-ET後、LDD複数アッシング → プラズマダメージ蓄積** と判明  
- STEM等の観察でも検出困難な領域に存在する不良であった

---

## 5️⃣ 改善と成果 / Improvements and Results

- ドライ剥離中心 → **Wet処理主体へ工程変更**  
- プラズマ曝露を最小化  
- **歩留まり改善: 65% → 80%**  
- 信頼性試験クリア、量産条件Fix  

---

👉 この章では、酒田工場がDRAMを **「製品」ではなく「技術習得のビークル」** として活用したことが特徴的である。  
