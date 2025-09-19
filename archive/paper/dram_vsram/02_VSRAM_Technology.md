---
layout: default
title: "モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)"
---

---

# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)

---

## 1️⃣ 製品仕様と時代背景 / Product Specification & Historical Context

**日本語**  
2000年前後、半導体市場の主役はPC向け大容量DRAMから、急速に普及し始めた携帯電話向けモバイルデバイスへと移行した。とりわけシャープでは携帯電話へのカメラ搭載企画が進み、その実現には **大容量かつ低消費電力のメモリ** が不可欠であった。  
このニーズに応えるため、2001年に **0.25 µm世代のDRAMプロセスを流用** し、**内部リフレッシュ制御** を付加した **疑似SRAM (VSRAM)** を量産化。DRAMセルをベースとしつつ、SRAMのように外部リフレッシュ非依存で動作できる点が特徴である。さらに **動作温度保証を80 °C→90 °Cへ拡張** し、モバイル用途に適合させた。  
当初歩留まりは約 **30%** に留まったが、**市場投入を最優先** する判断で量産を開始。VSRAMは **世界初のカメラ付き携帯電話** に採用され、モバイルメモリ史に大きな一歩を刻んだ。  

*English*  
Around 2000, the industry focus shifted from PC DRAM to mobile devices. At Sharp, adding a camera to phones required **high-density, low-power memory**. In 2001, **pseudo-SRAM (VSRAM)** entered mass production by **reusing the 0.25 µm DRAM process** with **internal refresh control**, enabling SRAM-like operation without external refresh. The operating temperature spec was **expanded from 80 °C to 90 °C** for mobile. Initial yield was about **30%**, yet mass production began to **prioritize time-to-market**, and VSRAM powered the **world’s first camera phone**.

---

## 2️⃣ 初期課題と対策 / Startup Challenges & Solutions

### 🧪 課題①：Pause Refresh Fail (Bin5)

**問題 / Issue**  
- モバイル仕様に合わせ **内部リフレッシュ周期を延長**。  
- 動作温度保証を **80→90 °C** に拡張。  
- 高温での **ジャンクションリーク増大** により Pause Refresh Fail が多数発生。  
*Extending refresh interval and raising max temperature to 90 °C exposed retention limits via junction leakage.*

**対策 / Countermeasures**  
1. **プロセス改善 / Process**  
   - DRAM世代で顕在化した **プラズマアッシング起因ダメージ** を回避するため、レジスト剥離を **ウェット主体（硫酸系）** に切替。  
   - **HF洗浄の最小化** により、残存ゲート酸化膜を保持して拡散層ダメージを抑制、SNコンタクト近傍のリークを低減。  
   *Shift to wet strip and minimize HF to suppress plasma-induced damage and junction leakage.*  
2. **電気設計強化 / Circuit**  
   - **バックバイアスを −1 V → −3 V** に強化し、温度依存性を抑制。  
   *Stronger reverse body bias (−3 V) reduced leakage sensitivity to temperature.*

---

### ⚡ 課題②：Disturb Refresh Fail (Bin6)

**問題 / Issue**  
- 0.25 µm世代の **短チャネル効果** により、隣接ワードライン反復アクセスでセルチャネルが擾乱し、リーク増加。  
- **90 °C** 条件で顕著化し、保持力を制約。  
*Short-channel effects caused access-disturb-induced leakage, especially at 90 °C.*

**対策 / Countermeasures**  
1. **寸法制御 / CD Control**：**ゲートCD中心値管理** を強化し、チャネル長ばらつきを抑制。  
2. **チャネルドーピング最適化 / Channel Doping**：Vth を適度に上げ、**リーク抑制とスイッチング能力の両立**。  
3. **補助策 / Auxiliary**：**−3 V バックバイアス** がディスターブ耐性向上に寄与。  

---

### 📈 成果 / Outcomes

- **量産開始時 Yield**：≈ **30%**（市場ニーズ優先で出荷開始）  
- **改善後 Yield**：継続的対策で **80–90%** に向上  
- **信頼性**：高温保持・高温動作・バーンインに合格、安定生産へ  

**まとめ / Summary**  
**Pause** と **Disturb** の両不良に対し、  
- *Process*: ウェット剥離、HF最小化、厳密CD管理  
- *Design*: チャネルドープ最適化、強化バックバイアス（−3 V）  
を複合投入し、**30%スタートから高歩留まりへ収束**。技術面に加え、**毎朝の進捗報告と強い組織的プレッシャー** の中で改善を加速した。  

---

## 3️⃣ 次世代検討と断念 / Next-Generation Evaluation & Abandonment

### 🔬 0.18 µm VSRAM（NANYA/Toshibaプロセス）

- **採用技術 / Tech**：**トレンチキャパシタ** 方式  
- **問題 / Pain Point**：トレンチは縦深構造で **ジャンクション面積が大きく**、**90 °C** でリーク増大 → 保持不足  
- **結果 / Result**：モバイル仕様（90 °C保証）を満たせず **不採用**  
- **背景 / Context**：  
  - **スタック型**：高さ方向で容量確保 → ジャンクション小、リークに強い  
  - **トレンチ型**：深掘りで容量確保 → ジャンクション大、リーク弱い  
  → **1T-1Cベースの擬似SRAMの限界** が露呈  

### 🧠 MoSys 1T-SRAM（参考評価）

- **方式 / Concept**：DRAMセル不要・**リフレッシュ不要**、ロジック互換  
- **プロセス / Process**：0.18 µm **CMOS** にそのまま適用可  
- **魅力 / Pros**：低消費電力に有利、組み込み適性が高い  
- **課題 / Cons**：セルフリフレッシュ相当の **制御設計ノウハウが難**。性能レンジが **「中間的」** と評価され、**社内採用見送り**  
- **参考リンク / Ref.**：[`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md)

---

## 4️⃣ まとめ / Overall Summary

**日本語**  
0.25 µm VSRAMは、酒田工場での技術移管DRAMを土台に **量産へ成功** し、**世界初のカメラ付き携帯電話** を実現する鍵となった。一方、0.18 µm世代では **トレンチキャパシタVSRAMが90 °C保持要件を満たせず断念**。これは **1T-1Cセル起点の擬似SRAMの終焉** を象徴する事例となった。  
この経験はエプソンにおける「メモリを恒久事業化するのではなく、**先端技術を吸収して主力製品（LCDドライバ、ASIC、ロジックIC等）へ展開**」という戦略を後押しし、プロセス・設計・信頼性の知見は後続事業の競争力基盤となった。  

*English*  
The 0.25 µm VSRAM achieved **successful mass production** and enabled the **first camera phone**. At 0.18 µm, trench-capacitor VSRAM failed to meet **90 °C** retention, effectively marking the **end of pseudo-SRAMs built on 1T-1C DRAM cells**. The experience reinforced Epson’s strategy to use DRAM as a **vehicle for absorbing advanced technologies** and redeploy them into core products (LCD drivers, ASICs, logic ICs), with the accumulated know-how becoming a foundation for later competitiveness.

---

## 📊 付録：課題と対策の要約 / Appendix: Challenges vs. Countermeasures

| 不良モード / Failure | 主因 / Root Cause | 主対策 / Key Countermeasures | 効果 / Effect |
|---|---|---|---|
| **Pause Refresh (Bin5)** | 高温でのジャンクションリーク増大（延長リフレッシュ＋90 °C拡張の影響） | ウェット剥離（硫酸系）・HF最小化・**−3 V**バックバイアス | 単ビット保持不良の顕著低減、Yield↑ |
| **Disturb Refresh (Bin6)** | 短チャネル効果によるアクセス擾乱リーク（90 °Cで顕著） | ゲートCD中心値管理強化・チャネルドーピング最適化・**−3 V**バックバイアス | ディスターブ耐性向上、保持特性安定 |
