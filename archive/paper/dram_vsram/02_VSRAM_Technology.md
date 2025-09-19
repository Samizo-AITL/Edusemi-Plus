---
layout: default
title: "モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)"
---

---

# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)

---

## 1️⃣ 製品仕様と時代背景 / Product Specification and Historical Context

**日本語**  
2000年前後、半導体市場の主役はPC向け大容量DRAMから、急速に普及し始めた携帯電話向けのモバイルデバイスへと移りつつあった。特にシャープでは、携帯電話にカメラ機能を追加する企画が進み、その実現には **大容量かつ低消費電力のメモリ** が不可欠であった。  

このニーズに応えるため、2001年に0.25 µm世代のDRAMプロセスを流用し、内部リフレッシュ制御を付加することで **疑似SRAM (VSRAM)** が量産化された。これはDRAMセルをベースとしながら、SRAMのように外部からリフレッシュを意識せず使用できる点に特徴があった。さらに動作温度保証を標準の80 °Cから90 °Cへ拡張し、モバイル用途に適合させた。  

ただし、当初の歩留まりは約30%と低かった。それでも、**市場投入を最優先する合理的判断** により量産が開始され、実際にVSRAMは世界初のカメラ付き携帯電話に採用されることでモバイルメモリの歴史に大きな一歩を刻んだ。  

---

**English**  
Around 2000, the focus of the semiconductor market shifted from large-capacity DRAM for PCs to mobile devices driven by the rapid spread of cell phones. At Sharp, a project was underway to add a camera to mobile phones, which required **high-density, low-power memory**.  

To meet this demand, in 2001 a **pseudo-SRAM (VSRAM)** was mass-produced by reusing the 0.25 µm DRAM process and adding internal refresh control. While based on DRAM cells, it allowed seamless SRAM-like operation without external refresh, and its operating temperature range was extended from the standard 80 °C to 90 °C to suit mobile applications.  

The initial yield was only about 30%, but mass production was launched as a **rational decision to prioritize market entry**. VSRAM went on to be adopted in Sharp’s first camera-equipped mobile phone, marking a significant milestone in the history of mobile memory.  

---

## 2️⃣ 初期課題と対策 / Startup Challenges and Solutions

### 課題① Pause Refresh Fail (Bin5)

- **問題**  
  モバイル仕様に合わせてスタンバイ電流を低減するため、VSRAMでは **内部リフレッシュ周期を従来DRAMより延長**した。  
  さらに標準 80 °C から **90 °C 動作保証**を追加したことで、セル保持能力の限界が顕在化。  
  高温条件での **ジャンクションリーク増大**が主要因となり、Pause Refresh Fail が多数発生した。  

- **対策**  
  1. **プロセス改善**  
     - DRAM世代ではプラズマアッシングによるダメージが主因であり、これを回避するため **レジスト剥離をウエット処理主体へ切替**。  
     - VSRAMではさらに **HF洗浄の最小化**を行い、ゲート酸化膜残膜を保持して拡散層ダメージを抑制し、SNコンタクト周辺のジャンクションリークを低減。  
  2. **電気設計面の強化**  
     - バックバイアスを −1 V から **−3 V へ強化**し、リーク電流の温度依存性を抑制。  

---

### 課題② Disturb Refresh Fail (Bin6)

- **問題**  
  0.25 µm 世代では短チャネル効果により、隣接ワードラインの繰り返しアクセス時にセルチャネルが擾乱され、リークが増加する **Disturb Refresh Fail** が発生。  
  高温（90 °C）条件下で特に顕著となり、セル保持力を制約する要因となった。  

- **対策**  
  1. **寸法制御の徹底**  
     - **ゲートCDの中心値管理を強化**し、チャネル長のばらつきを抑制。  
     - 短チャネル効果によるリーク増大を抑止。  
  2. **チャネルドーピング最適化**  
     - セルチャネルのドーピング条件を最適化し、しきい値電圧 (Vth) を適度に上昇。  
     - **Vth向上によるリーク抑制と、スイッチング能力の維持**を両立。  
  3. **補助的対策**  
     - バックバイアス強化（−3 V）が、ディスターブ耐性の改善に寄与。  

---

### 成果

- **量産開始時点Yield**: 約30%（市場ニーズ対応を優先して出荷開始）  
- **改善後Yield**: 量産を継続しながら対策を適用し、最終的に **80〜90%** へ向上  
- 高温信頼性試験にも合格し、安定生産が可能に  

**まとめ**  
Pause Refresh Fail と Disturb Refresh Fail の双方に対して、  
- プロセス面（ウエット剥離・HF洗浄最小化・CD管理）  
- デバイス設計面（チャネルドープ・バックバイアス）  
の複合的対策を講じることで、**30%歩留まりでの量産スタートを切った後も改善を積み重ね、最終的に高歩留まりを達成**した。  

当初は、歩留まり改善の重圧の中で、筆者は **毎朝、部課長に囲まれながら進捗状況を報告**しなければならず、技術面だけでなく組織的な緊張感も伴う立ち上げであった。  

---

## 3️⃣ 次世代検討と断念 / Next-Generation Evaluation and Abandonment

### 0.18 µm VSRAM（NANYA/Toshibaプロセス）

- **採用技術**: トレンチキャパシタ方式  
- **問題点**:  
  - トレンチ型は、縦方向に深掘りしキャパシタを形成するため、**ジャンクション面積がスタック型に比べて大きい**  
  - その結果、高温（90 °C）動作でリーク電流が増大し、セル保持不足が顕在化  
- **結果**: モバイル仕様（90 °C保証）を満たせず採用を断念  
- **背景補足**:  
  - **スタック型**：高さ方向で容量を稼ぐため、ジャンクション面積が小さくリークに強い  
  - **トレンチ型**：面積方向で容量を稼ぐため、ジャンクションが大きくリークに弱い  
  - この世代で、**1T-1Cセルを用いた擬似SRAMの限界**が露呈した事例となった  

---

### MoSys 1T-SRAM評価（参考）

- **方式**: DRAMセル不要、リフレッシュ不要のロジック互換型  
- **プロセス**: 0.18 µm CMOSプロセスにそのまま適用可能  
- **魅力**:  
  - リフレッシュ不要のため、低消費電力に有利  
  - ロジックプロセス互換性が高く、組み込み用途に適する  
- **課題**:  
  - マクロとしては魅力的であったが、**セルフリフレッシュ機能を組み込む設計ノウハウが難しく**  
  - 高速SRAMや大容量DRAMに比べて「中途半端な特性」と評価された  
  - 結果として、社内での採用は見送りとなった  
- **参考リンク**: [`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md)
  
---

## 4️⃣ まとめ / Summary

**日本語**  
0.25 µm VSRAMは、酒田工場における技術移管DRAMを基盤に成功裏に量産され、世界初のカメラ付き携帯電話を実現する鍵となった。しかし0.18 µm世代では、トレンチキャパシタを用いたVSRAMは保持特性の限界により断念され、**1T-1C DRAMセルをベースにした擬似SRAMの終焉**を象徴する事例となった。  

**English**  
The 0.25 µm VSRAM, successfully mass-produced based on the transferred DRAM process, played a pivotal role in enabling the world’s first camera phone. However, at the 0.18 µm node, trench-capacitor-based VSRAM failed to meet retention requirements at 90 °C, marking the **end of pseudo-SRAMs built on the 1T-1C DRAM cell concept**.  
