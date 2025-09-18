---
layout: default
title: "0.25µm 64M DRAM (3rd Gen) Startup Record (1998)"
---

# 📘 0.25µm 64M DRAM (3rd Gen) Startup Record (1998)

## 2️⃣ プロセス概要 / Process Overview

- **リソグラフィ**：初の **KrFステッパー** を導入し、0.25µm世代の量産露光技術を確立  
- **デバイス分離**：Semi-recess LOCOS による素子分離  
- **ウェル構成**：Triple-well、Deep N-Well によりセルの耐ノイズ性を強化  
- **ゲート電極（ワードライン）**：**Wシリサイド (WSi, CVD)** を用いた構造で、低抵抗化と微細化対応  
- **ビットライン**：**ビットラインコンタクトとビットラインを同時形成**、WSi-CVD導入により配線抵抗を低減し高密度配線化  
- **ストレージノード（キャパシタ）**：スタック型構造、粗面化処理により容量を 1.5〜1.8 倍に向上  
- **配線・封止**：AlCu/TiN配線、SOG平坦化、SiNまたはPIによるパッシベーション
  
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
