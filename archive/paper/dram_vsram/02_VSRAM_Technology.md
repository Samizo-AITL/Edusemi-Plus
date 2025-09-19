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

- **問題**: 高温（90 °C）動作時に保持不足が発生、主因は **ジャンクションリークの増大**  
- **対策**:  
  - プロセス面：HF洗浄回数を削減し、WSA後の酸化膜保持 → SNコンタクトリーク低減  
  - 設計面：バックバイアス強化（Vbs −1 V → −3 V）でリーク抑制  

### 課題② Disturb Refresh Fail (Bin6)

- **問題**: 0.25 µm短チャネル効果によるセル間リーク増大、特に90 °Cで顕著  
- **対策**: ゲートCD中心値管理を強化し、リークばらつきを抑制  

### 成果

- **初期Yield**: 約30%  
- **改善後Yield**: 80〜90%  
- 信頼性試験合格、量産移行に成功  

---

## 3️⃣ 次世代検討と断念 / Next-Generation Evaluation and Abandonment

### 0.18 µm VSRAM（NANYA/Toshibaプロセス）

- トレンチキャパシタ採用によりジャンクション面積が増大  
- 90 °C動作で保持不足が顕在化  
- 結果：モバイル仕様を満たせず採用を断念  

### MoSys 1T-SRAM評価（参考）

- 0.18 µm ロジックプロセスで動作、リフレッシュ不要  
- 外部マクロとして評価対象に挙がるも、筆者の業務転換により評価未完  
- 参考リンク: [`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md)  

---

## 4️⃣ まとめ / Summary

**日本語**  
0.25 µm VSRAMは、酒田工場における技術移管DRAMを基盤に成功裏に量産され、世界初のカメラ付き携帯電話を実現する鍵となった。しかし0.18 µm世代では、トレンチキャパシタを用いたVSRAMは保持特性の限界により断念され、**1T-1C DRAMセルをベースにした擬似SRAMの終焉**を象徴する事例となった。  

**English**  
The 0.25 µm VSRAM, successfully mass-produced based on the transferred DRAM process, played a pivotal role in enabling the world’s first camera phone. However, at the 0.18 µm node, trench-capacitor-based VSRAM failed to meet retention requirements at 90 °C, marking the **end of pseudo-SRAMs built on the 1T-1C DRAM cell concept**.  
