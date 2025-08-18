---
layout: default
title: "セイコーエプソン酒田事業所 8インチライン稼働と第2世代DRAM立ち上げ（1997）"
description: "1997年、筆者のセイコーエプソン入社と酒田事業所配属。8インチライン立ち上げ、第2世代（0.35μm）64M DRAM量産化に向けた技術課題と突破、そして巨額投資の戦略的意義。"
tags: ["DRAM", "半導体プロセス", "8インチライン", "歩留まり改善", "技術移管", "0.35μm", "ロジック配線", "ファンドリ", "フラッシュメモリ", "投資意義"]
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
当時の酒田事業所は、**0.35μm世代ベースの8インチライン立ち上げ**を開始したばかりで、筆者はまず**スパッタ装置 Endura**の導入に関与し、その後すぐに**0.35μmロジック配線モジュールの立ち上げ**にも携わった。  

この8インチラインの技術導入戦略は、単なるDRAM量産だけでなく、複数の先端技術を同時に吸収する多角的なものであった。  
- **DRAM**：0.35μm以降のプロセス技術導入（第2世代〜第3世代64M DRAM）  
- **先端ロジック**：Xilinxロジック製品のファンドリ受託による最新ロジックプロセス導入  
- **社内ロジック製品展開**：獲得した配線モジュールやプロセス技術を社内ASIC・ロジックICへ展開  
- **フラッシュメモリ**：Lattice案件やSST社とのファンドリ契約によるフラッシュメモリ技術の並行導入  

**English**  
In 1997, the author joined Seiko Epson and was assigned to the **Sakata plant** in Yamagata Prefecture after the Golden Week holiday.  
At that time, Sakata Fab had just begun the **0.35 μm-based 8-inch production line ramp-up**, and the author was first involved in the installation of the **Endura sputtering system**, then quickly engaged in the **ramp-up of the 0.35 μm logic interconnect module**.  

The technology acquisition strategy for the 8-inch line was multifaceted, aiming to absorb multiple advanced technologies in parallel:  
- **DRAM**: Introduction of 0.35 μm and beyond process technologies (2nd to 3rd Gen 64M DRAM)  
- **Advanced logic**: Adoption of latest logic processes via foundry production for Xilinx  
- **In-house logic products**: Application of acquired interconnect module and process know-how to internal ASIC and logic IC development  
- **Flash memory**: Parallel introduction of flash memory processes through foundry collaborations with Lattice and SST  

> 💡 **筆者の推測**：DRAMはあくまで0.35µm以降のプロセス技術導入が目的で、事業の主眼はロジック製品やファンドリ展開にあったと考えられる。当時は世界最先端の技術水準で、TSMCと同等レベルだったが、後に国策レベルの投資差で大きく差が開いた。

---

## 🌐 セイコーエプソン8インチ立ち上げの意義 | Strategic Significance & Investment Rationale

1980年代、日本は世界半導体市場のトップに立ち、DRAMシェアで米国を凌駕していた。  
しかし1990年代に入ると、日米半導体協定や韓国・台湾勢の台頭により、日本のDRAM事業は急速に衰退していった。  
その衰退期に、あえてセイコーエプソンは**巨額投資で8インチラインを立ち上げ**、業界最先端を目指した。  

その意義は「単なるDRAM量産」ではなく、**DRAMを通じて最先端プロセス技術を吸収し、自社強みに展開すること**にあった。  

```mermaid
flowchart LR
    A[DRAM技術導入<br>0.35µm/0.25µm] --> B[先端ロジック協業<br>Xilinxなど]
    B --> C[自前ロジック開発<br>PDK構築]
    C --> D[社内展開<br>ASIC・ロジックIC]
    D --> E[高耐圧/混載CMOS<br>パネルドライバ・IJヘッド]
    
    classDef focus fill=#f9f,stroke=#333,stroke-width=2px;
    A:::focus
    E:::focus
```

- **DRAM技術導入**：三菱からの技術供与をベースに0.35→0.25µm世代を習得  
- **先端ロジック吸収**：Xilinx等のファブレスと協業し、配線だけでなくトランジスタ技術まで獲得  
- **自前PDK構築**：プロセス設計キットを内製化し、社内ASIC展開へ  
- **混載高耐圧デバイス**：携帯向けパネルドライバやインクジェットヘッド駆動ICなど、差別化製品に応用  

👉 投資の本質は「DRAM事業」ではなく、**先端技術を自前化して独自デバイスへ展開する戦略的布石**であった。  

---

## 📦 技術供与と展開計画 | Technology Transfer & Deployment Plan

立ち上げ方法は、三菱電機 熊本工場（KD棟）からの技術供与に基づき、以下の世代プロセスが順次展開された。

- 0.5μm **16M DRAM**
- 0.35μm **64M DRAM（第2世代）**
- 0.25μm **64M DRAM（第3世代）**

---

## 🚀 第2世代（0.35μm）64M DRAM立ち上げの難航 | Ramp-up Challenges

0.5μm 16M DRAMは順調に立ち上がったが、**0.35μm 64M DRAM（第2世代）**は、  
おそらく16M DRAMと**並行して初期活動を開始**しており、**1997年秋頃から本格的な立ち上げフェーズ**に入った。  

試作ロットは少なくとも**30ロット以上投入**したが、**形状すら満足に形成できず**、  
測長SEMで寸法を測ろうにも形状が崩れており、**どこを測って良いのかわからない状態**が続いた。  

しかも、この立ち上げは**半導体事業部として最重要課題**に位置づけられており、  
現場には**相当な重圧**がのしかかっていた。  
プロセスは熊本工場での実績があり、装置仕様やレシピも同等だったにもかかわらず、原因は不明だった。

---

## 🔍 原因究明と解決 | Root Cause & Resolution

詳細調査の結果、唯一異なる工程が判明した。

| 工程比較 | 三菱電機 熊本工場 | セイコーエプソン 酒田工場 |
|----------|------------------|---------------------------|
| 洗浄工程 | 硫酸過水 → アンモニア過水 → 塩酸過水 | アンモニア過水 → 塩酸過水（※硫酸過水なし） |

**硫酸過水工程の欠落**により、成膜前の表面状態がプラズマ処理などで変化し、  
**枚葉処理依存の層間膜厚差**が発生していた。  

最終的に、熊本工場の工程フローを**酒田工場へ完全移植（鏡写し）**することで問題を解消。  
この対応により、第2世代64M DRAMの量産化への道が開かれた。  

---

## ✅ 成果と次世代への布石 | Results & Next Steps

この難航期を通じて、筆者はDRAMプロセス全体を把握し、  
翌年後半からの**0.25μm 第3世代64M DRAM立ち上げ**への準備が整った。  

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
