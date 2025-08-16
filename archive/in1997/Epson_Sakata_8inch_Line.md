---
layout: default
title: "セイコーエプソン酒田事業所 8インチライン稼働と第2世代DRAM立ち上げ（1997）"
description: "1997年、筆者のセイコーエプソン入社と酒田事業所配属。8インチライン立ち上げ、第2世代（0.35μm）64M DRAM量産化に向けた技術課題と突破の記録。"
tags: ["DRAM", "半導体プロセス", "8インチライン", "歩留まり改善", "技術移管", "0.35μm"]
---

---

# 🏭 セイコーエプソン酒田事業所 8インチライン稼働と第2世代DRAM立ち上げ（1997）  
**Seiko Epson Sakata Fab 8-inch Line Ramp-up & 2nd Gen DRAM Startup (1997)**  

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](https://samizo-aitl.github.io/Edusemi-Plus/archive/#license)

---

⚠️ **免責事項 / Disclaimer**  

| 日本語 | English |
|--------|---------|
| 本記録は1997年当時の業務経験に基づく教育・アーカイブ資料です。企業機密や現行製品情報は含まれていません。 | This document is based on the author's work experience in 1997, reconstructed for educational and archival purposes, and contains no proprietary or current product data. |

---

## 🧭 背景と配属 | Background & Assignment

**日本語**  
1997年、筆者はセイコーエプソンに入社し、ゴールデンウィーク後に山形県の**酒田事業所**へ配属された。  
当時の酒田事業所は、**0.35μm世代ベースの8インチライン立ち上げ**を開始したばかりで、筆者はまず**スパッタ装置 Endura**の導入に関与した。

**English**  
In 1997, the author joined Seiko Epson and was assigned to the **Sakata plant** in Yamagata Prefecture after the Golden Week holiday.  
At that time, Sakata Fab had just begun the **0.35 μm-based 8-inch production line ramp-up**, and the author was initially involved in the introduction of the **Endura sputtering tool**.

---

## 🌏 当時の時代背景（筆者推測）| Industry Context (Author’s Speculation)

**日本語**  
筆者の推測だが、エプソンが8インチラインを立ち上げた背景には、  
**0.35μm以降の先端プロセス技術を導入し、将来的にロジックファンドリや社内製品展開へと応用する狙い**があったと考えられる。  
DRAMはその技術習得のための「足がかり」であり、当時のプロセス水準は世界最先端クラスで、TSMCと同等レベルにあった。  
しかし、その後のTSMCは国策レベルの巨額投資で急成長し、エプソンとの格差は大きく開くことになる。

**English**  
The author speculates that Epson’s motivation for launching the 8-inch line was to  
**adopt sub-0.35 μm advanced process technology as a stepping stone for future logic foundry services and in-house products**.  
DRAM served primarily as a vehicle for process mastery.  
At the time, Epson’s process capabilities were at a world-class level, comparable to TSMC.  
However, in subsequent years, TSMC’s rapid growth—driven by massive state-level investments—widened the gap significantly.

---

## 📦 技術供与と展開計画 | Technology Transfer & Deployment Plan

**日本語**  
立ち上げ方法は、三菱電機 熊本工場（KD棟）からの技術供与に基づき、以下の世代プロセスが順次展開された。

- 0.5μm **16M DRAM**
- 0.35μm **64M DRAM（第2世代）**
- 0.25μm **64M DRAM（第3世代）**

これらの個別要素技術を、**ファンドリ案件**や**社内ロジック製品**にも応用する計画だった。

**English**  
The ramp-up approach was based on a technology transfer from Mitsubishi Electric’s Kumamoto Fab (KD building), with the following process generations to be deployed sequentially:

- 0.5 μm **16M DRAM**
- 0.35 μm **64M DRAM (2nd Generation)**
- 0.25 μm **64M DRAM (3rd Generation)**

These individual process technologies were also planned to be applied to **foundry projects** and **in-house logic products**.

---

## 🚀 第2世代（0.35μm）64M DRAM立ち上げの難航 | Ramp-up Challenges of 2nd Gen (0.35 μm) 64M DRAM

**日本語**  
0.5μm 16M DRAMは順調に立ち上がったが、**0.35μm 64M DRAM（第2世代）**は、  
おそらく16M DRAMと**並行して初期活動を開始**しており、**1997年秋頃から本格的な立ち上げフェーズ**に入った。  

試作ロットは少なくとも**30ロット以上投入**したが、**形状すら満足に形成できず**、  
測長SEMで寸法を測ろうにも形状が崩れており、**どこを測って良いのかわからない状態**が続いた。  

しかも、この立ち上げは**半導体事業部として最重要課題**に位置づけられており、  
現場には**相当な重圧**がのしかかっていた。  
プロセスは熊本工場での実績があり、装置仕様やレシピも同等だったにもかかわらず、原因は不明だった。

**English**  
While the 0.5 μm 16M DRAM ramp-up proceeded smoothly, the **0.35 μm 64M DRAM (2nd Generation)**,  
likely initiated in parallel with the 16M DRAM, entered a **full-scale ramp-up phase around autumn 1997**.  

At least **30 trial lots** were processed, yet **pattern shapes could not be formed properly**.  
Even when attempting to measure dimensions with a CD-SEM, the shapes were so deformed that it was **unclear where to measure**.  

Furthermore, this ramp-up was classified as the **highest-priority task** for the Semiconductor Division,  
placing **tremendous pressure** on the production team.  
Despite having a proven process from the Kumamoto Fab, with identical equipment and recipes, the root cause remained elusive.

---

## 🔍 原因究明：洗浄工程の差異 | Root Cause: Cleaning Process Difference

**日本語**  
詳細調査の結果、唯一異なる工程が判明した。

| 工程比較 | 三菱電機 熊本工場 | セイコーエプソン 酒田工場 |
|----------|------------------|---------------------------|
| 洗浄工程 | 硫酸過水 → アンモニア過水 → 塩酸過水 | アンモニア過水 → 塩酸過水（※硫酸過水なし） |

**硫酸過水工程の欠落**により、成膜前の表面状態がプラズマ処理などで変化し、  
**枚葉処理依存の層間膜厚差**が発生していた。

**English**  
Detailed investigation revealed the only difference in the process:

| Step Comparison | Mitsubishi Kumamoto Fab | Seiko Epson Sakata Fab |
|-----------------|-------------------------|------------------------|
| Cleaning Process | H₂SO₄/H₂O₂ → NH₄OH/H₂O₂ → HCl/H₂O₂ | NH₄OH/H₂O₂ → HCl/H₂O₂ (**No H₂SO₄/H₂O₂ step**) |

The **absence of the sulfuric acid/hydrogen peroxide (H₂SO₄/H₂O₂) step** altered the wafer surface condition before film deposition,  
leading to **plasma-induced surface changes** and **layer thickness variations dependent on single-wafer processing**.

---

## ✅ 解決と成果 | Resolution & Results

**日本語**  
最終的に、熊本工場の工程フローを**酒田工場へ完全移植（鏡写し）**することで問題を解消。  
この対応により、第2世代64M DRAMの量産化への道が開かれた。  

この難航期を通じて、筆者はDRAMプロセス全体を把握し、  
翌年後半からの**0.25μm 第3世代64M DRAM立ち上げ**への準備が整った。

**English**  
Ultimately, the problem was resolved by **fully replicating (mirror copying)** the Kumamoto Fab process flow at the Sakata Fab.  
This measure paved the way for mass production of the 2nd Generation 64M DRAM.  

Through this challenging period, the author gained a comprehensive understanding of the DRAM process,  
preparing for the **0.25 μm 3rd Generation 64M DRAM ramp-up** starting in the latter half of the following year.

---

## 📅 翌年のプロジェクト | Next Year’s Project

**日本語**  
64M DRAM（第2世代・0.35μm）は、**1997年秋頃から1998年前半**にかけて立ち上げが行われた。  
その後、**1998年後半から第3世代（0.25μm）64M DRAM**の立ち上げが開始された。  
この第3世代プロジェクトは、本ページで記した経験と知見を基盤としている。

➡ [1998年：0.25μm 第3世代64M DRAM立ち上げ記録](../in1998/DRAM_Startup_64M_1998.md)

**English**  
The 64M DRAM (2nd Gen, 0.35 μm) ramp-up took place from **autumn 1997 to the first half of 1998**.  
Subsequently, in the latter half of 1998, the **0.25 μm 3rd Generation 64M DRAM** ramp-up began.  
This 3rd Gen project was built on the experience and knowledge described on this page.

➡ [1998: 0.25 μm 3rd Generation 64M DRAM Startup Record](../in1998/DRAM_Startup_64M_1998.md)
