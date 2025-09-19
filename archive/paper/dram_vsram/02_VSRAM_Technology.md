---
layout: default
title: "モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)"
---

---

# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)  
*📘 Mobile Pseudo-SRAM (VSRAM) Technology Archive (2001)*

---

## 1️⃣ 製品仕様と時代背景 / Product Specification & Historical Context

**日本語 🇯🇵**  
2000年前後、市場は **PC向け大容量DRAM** から、急速に普及した **携帯電話向けモバイルデバイス** へと移行した。  
特にシャープでは、携帯電話への **カメラ搭載** を企画し、その実現には **大容量かつ低消費電力のメモリ** が不可欠であった。  

このニーズに応え、2001年に **0.25 µm DRAMプロセスを流用**、**内部リフレッシュ制御を付加** した **疑似SRAM (VSRAM)** を量産化。  
- **特徴**：DRAMセルベースだが、外部リフレッシュ不要でSRAMのように利用可能  
- **拡張**：動作温度保証を **80 °C → 90 °C** に拡張し、モバイル仕様へ適合  

当初歩留まりは **約30%** に過ぎなかったが、**市場投入を最優先** し量産を開始。  
結果、VSRAMは **世界初のカメラ付き携帯電話** に採用され、モバイルメモリ史の転機となった。  

**English 🇺🇸**  
Around 2000, the market shifted from **large-capacity DRAM for PCs** to **mobile devices** driven by the cell phone boom.  
At Sharp, the plan to add **cameras to mobile phones** required **high-density, low-power memory**.  

In 2001, **pseudo-SRAM (VSRAM)** was mass-produced by **reusing the 0.25 µm DRAM process** with **internal refresh control**:  
- **Feature**: DRAM-based cells, but usable like SRAM without external refresh  
- **Extension**: Operating temperature expanded from **80 °C to 90 °C**, tailored for mobile  

Although the initial yield was only **~30%**, production started to **prioritize market entry**.  
VSRAM was adopted in the **world’s first camera phone**, marking a milestone in mobile memory history.  

---

## 2️⃣ 初期課題と対策 / Startup Challenges & Solutions

### 🧪 課題① Pause Refresh Fail (Bin5)  
*🧪 Issue ① Pause Refresh Fail (Bin5)*

| 項目 / Item | 日本語 🇯🇵 | English 🇺🇸 |
|-------------|-----------|-------------|
| **問題 / Problem** | - リフレッシュ周期延長＋90 °C保証によりセル保持限界が顕在化<br>- 高温での **ジャンクションリーク増大** が主因 | - Extended refresh cycle + 90 °C spec exposed retention limit<br>- **Junction leakage at high T** became dominant |
| **対策 / Countermeasure** | 1. **プロセス改善**：プラズマアッシングを回避し、**ウェット剥離（硫酸系）＋HF最小化**<br>2. **電気設計**：バックバイアスを **−1 V → −3 V** に強化 | 1. **Process**: Replace plasma ashing with **wet strip + minimized HF**<br>2. **Design**: Stronger back bias **−1 V → −3 V** |

---

### ⚡ 課題② Disturb Refresh Fail (Bin6)  
*⚡ Issue ② Disturb Refresh Fail (Bin6)*

| 項目 / Item | 日本語 🇯🇵 | English 🇺🇸 |
|-------------|-----------|-------------|
| **問題 / Problem** | - 短チャネル効果により、隣接WLアクセスでセルチャネル擾乱<br>- **90 °C** で顕著に発生 | - Short-channel effects: repeated adjacent WL access disturbed channels<br>- Prominent at **90 °C** |
| **対策 / Countermeasure** | 1. **CD管理強化**：ゲート長ばらつきを低減<br>2. **ドーピング最適化**：Vth上昇でリーク抑制＋性能維持<br>3. **補助策**：−3 V バックバイアス | 1. **CD control**: tighter gate length variation<br>2. **Channel doping**: tuned Vth to suppress leakage while keeping drive<br>3. **Auxiliary**: −3 V back bias helped disturb immunity |

---

### 📈 成果 / Outcome

| 項目 / Item | 日本語 🇯🇵 | English 🇺🇸 |
|-------------|-----------|-------------|
| **量産開始時 Yield** | 約30%（市場投入優先） | ~30% (market entry prioritized) |
| **改善後 Yield** | 継続改善で **80–90%** 達成 | Improved to **80–90%** |
| **信頼性 / Reliability** | 高温保持・バーンイン合格 → 安定生産 | Passed retention/burn-in → stable production |

---

## 3️⃣ 次世代検討と断念 / Next-Generation Evaluation & Abandonment

### 🔬 0.18 µm VSRAM（NANYA/Toshiba） 
*🔬 0.18 µm VSRAM (NANYA/Toshiba)*

| 項目 / Item | 日本語 🇯🇵 | English 🇺🇸 |
|-------------|-----------|-------------|
| **方式 / Type** | トレンチキャパシタ方式 | Trench capacitor |
| **問題 / Problem** | ジャンクション面積が大きく、90 °Cでリーク増大 → 保持不足 | Larger junction → retention fails at 90 °C |
| **結果 / Result** | モバイル仕様不適合、採用断念 | Failed mobile spec, project abandoned |

---

### 🧠 MoSys 1T-SRAM（参考評価）  
*🧠 MoSys 1T-SRAM (Reference)*

| 項目 / Item | 日本語 🇯🇵 | English 🇺🇸 |
|-------------|-----------|-------------|
| **特徴 / Feature** | DRAMセル不要・リフレッシュ不要、ロジック互換 | No DRAM cells, no refresh, logic-compatible |
| **利点 / Pros** | 低消費電力、組み込み適性 | Low power, good for embedded |
| **課題 / Cons** | 設計ノウハウ難、性能レンジが中途半端 → 採用見送り | Hard design know-how, mid-tier specs → not adopted |
| **参考 / Ref.** | [`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md) | same |

---

## 4️⃣ まとめ / Overall Summary

**日本語 🇯🇵**  
0.25 µm VSRAMは **酒田工場の技術移管DRAMを基盤に量産化** され、**世界初のカメラ付き携帯電話** を実現する鍵となった。  
一方、0.18 µmでは **トレンチ型VSRAMが保持特性を満たせず断念**。これは **1T-1Cセルをベースとする擬似SRAMの終焉** を象徴する出来事となった。  

この経験は「**DRAMを事業の柱にせず、先端技術吸収のビークルとして活用し、主力製品（LCDドライバ・ASIC・ロジックIC）へ展開**」という戦略を後押しし、その知見は後続事業の競争力基盤となった。  

**English 🇺🇸**  
The 0.25 µm VSRAM was **successfully mass-produced at Sakata Fab** and enabled the **first camera phone**.  
At 0.18 µm, trench-based VSRAM **failed retention specs**, marking the **end of 1T-1C-based pseudo-SRAMs**.  

This reinforced Epson’s strategy: **use DRAM as a vehicle to absorb advanced process know-how, then redeploy it into core products (LCD drivers, ASICs, logic ICs)**.  
While memory business shrank, the **process, design, and reliability knowledge** became a cornerstone of later competitiveness.  
