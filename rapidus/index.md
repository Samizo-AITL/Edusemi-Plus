---
layout: default
title: 📘 Rapidusと2nm技術の挑戦 / The Challenge of Rapidus and 2nm Technology
---

---

# 📘 Rapidusと2nm技術の挑戦 / The Challenge of Rapidus and 2nm Technology

---

## 🔗 公式リンク / *Official Links*

| 言語 / Language | GitHub Pages 🌐 | GitHub 💻 |
|-----------------|----------------|-----------|
| 🇯🇵 日本語 / *Japanese* | [![GitHub Pages JP](https://img.shields.io/badge/GitHub%20Pages-日本語版-brightgreen?logo=github)](https://samizo-aitl.github.io/Edusemi-Plus/rapidus/) | [![GitHub Repo JP](https://img.shields.io/badge/GitHub-日本語版-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/rapidus) |

---

## 🏁 概要 / Overview
**🇯🇵 JP:**  
2025年7月、Rapidusは**2nmプロセスによる試作チップが正常に動作**したことを確認しました。  
このチップは、IBMから技術移転を受けた**GAAFET（Gate-All-Around FET）構造**を採用し、  
北海道千歳市の仮設クリーンルームにて**国内製造**されました。  

**🇺🇸 EN:**  
In July 2025, Rapidus confirmed that its **prototype chip manufactured with a 2nm process** operated successfully.  
The chip uses **GAAFET (Gate-All-Around FET) architecture**, transferred from IBM, and was **produced domestically**  
at a temporary cleanroom facility in Chitose, Hokkaido.

---

## 🧪 技術的背景 / Technical Background: 2nm & GAAFET
**🇯🇵 JP:**  
- **GAAFET（ナノシート型MOS）**は、FinFETの後継となる次世代トランジスタ構造  
- チャネルをゲートが全面から包み込み、**電流制御性を飛躍的に向上**  
- IBMが2021年に世界初の2nm GAAFETチップを試作、Rapidusがその技術を導入  

**🇺🇸 EN:**  
- **GAAFET (Nanosheet MOS)** is the next-generation transistor structure replacing FinFET  
- The gate fully surrounds the channel, **significantly improving current control**  
- IBM first demonstrated a 2nm GAAFET chip in 2021, and Rapidus adopted the technology

---

## 📊 先端ノード比較 / Advanced Node Comparison

| ノード / Node | トランジスタ構造 / Structure | 代表企業 / Key Players | 特徴 / Features |
|---------------|-----------------------------|------------------------|-----------------|
| **5nm** | FinFET | TSMC, Samsung, Intel(改良版) | 高性能・成熟プロセスだが、短チャネル効果抑制に限界<br>High-performance & mature, but limited in short-channel control |
| **3nm** | FinFET → 初期GAAFET | TSMC(N3系), Samsung(GAA) | リーク低減・密度向上、製造複雑化<br>Lower leakage, higher density, but more complex fabrication |
| **2nm** | **GAAFET (ナノシート)** | IBM, Rapidus, Samsung, TSMC(N2計画) | 電流制御性飛躍向上、低電圧動作、設計自由度拡大<br>Better current control, low-voltage operation, greater design flexibility |
| **1.4nm** (予定) | GAAFET → CFET | Intel, imec(研究) | 垂直スタック構造、面積効率最大化、熱・配線課題大<br>Vertical stacking, maximum area efficiency, thermal & routing challenges |

📎 **関連教材 / Related Material:**  
- [Edusemi-v4x 特別編：FinFETとGAAFETの構造比較](https://github.com/Samizo-AITL/Edusemi-v4x/tree/main/f_chapter1_finfet_gaa)  
- [CFET構造と課題（appendixf1_04_cfet.md）](https://github.com/Samizo-AITL/Edusemi-v4x/blob/main/f_chapter1_finfet_gaa/appendixf1_04_cfet.md)

---

## 🗓️ 年表 / Timeline

| 年 / Year | 出来事 / Event |
|-----------|----------------|
| **2022** | IBMとRapidusが技術提携を締結 / IBM and Rapidus sign technology partnership |
| **2023–2024** | 千歳にてプロセス移転・パイロットライン構築 / Process transfer and pilot line setup in Chitose |
| **2025年7月** | 国内製造2nmチップの動作確認に成功（ファーストシリコン） / First silicon of domestically produced 2nm chip successfully verified |
| **2025年12月** | AI設計支援基盤「Raads」を発表、2nm向け設計環境の整備方針を明確化 / Announcement of AI-based design support platform “Raads” for 2nm enablement |
| **2026年（予定）** | 2nm向けPDK公開、EDAベンダー（Siemens等）と連携した設計フロー提供開始 / Release of 2nm PDK and launch of EDA-integrated design flow |

---

## 🌏 戦略的意義 / Strategic Significance
**🇯🇵 JP:**  
- 日本の「ポストTSMC」戦略を象徴する国家プロジェクト  
- CHIPS法やLSI Japan構想と連動した**先端製造基盤の確立**  
- 設計（DFM）・パッケージ・人材育成との**垂直統合エコシステム**構想  

**🇺🇸 EN:**  
- A national project symbolizing Japan’s “Post-TSMC” strategy  
- Establishing an **advanced manufacturing base** in connection with CHIPS Act and LSI Japan initiatives  
- Vision of a **vertically integrated ecosystem** linking design (DFM), packaging, and talent development

---

## 🧩 設計環境 / Design Enablement

**🇯🇵 JP:**  
Rapidusは 2nm ファーストシリコン達成後、  
**設計環境（Design Enablement）の整備を次フェーズ** に位置づけています。  
先端ノードでは、**PDK・EDA・設計支援基盤が揃わなければ事業は成立しません**。

- **2025年12月**：AI設計支援基盤 **「Raads」** を発表  
- **2026年（予定）**：2nm GAAFET 向け **PDK公開**、EDA連携設計フロー提供開始  
- Siemens EDA 等と連携し、**設計–製造一体型フロー** を構築中  

これは Rapidus が  
**「技術実証」→「顧客設計フェーズ」**  
へ移行しつつあることを示します。

**🇺🇸 EN:**  
Following first silicon, Rapidus has shifted focus to **design enablement**,  
including AI-assisted design (Raads), high-precision 2nm PDKs, and
EDA-integrated reference flows—marking the transition toward
**customer-driven design activity**.

---

## 🎓 教材としての意義 / Educational Value
**🇯🇵 JP:**  
- ✅ **FinFETとGAAFETの構造比較**（Edusemi 特別編と連動）  
- ✅ **産業戦略×政策×技術**を結ぶ事例分析  
- ✅ **技術移転と製造立ち上げプロセス**のケーススタディ  

**🇺🇸 EN:**  
- ✅ **Comparing FinFET and GAAFET structures** (linked with Edusemi special edition)  
- ✅ Case study connecting **industrial strategy, policy, and technology**  
- ✅ Visualization of **technology transfer and fab ramp-up process**

---

## 🔗 関連リンク / Related Links
- [地政学教材（日本の戦略）](../geopolitics/japan.md) / [Geopolitics: Japan Strategy](../geopolitics/japan.md)  
- [技術ロードマップ編（2nm以降）](../tsmc-insight/roadmap.md) / [Tech Roadmap: Beyond 2nm](../tsmc-insight/roadmap.md)

---

## 👤 **著者・ライセンス | Author & License**

| 📌 項目 / Item | 📄 内容 / Details |
|------|------|
| **著者 / Author** | **三溝 真一**（Shinichi Samizo） |
| **💻 GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-black?logo=github)](https://github.com/Samizo-AITL) |
| **📜 ライセンス / License** |[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](https://samizo-aitl.github.io/Edusemi-Plus/#-ライセンス--license)<br>コード / Code: [MIT](https://opensource.org/licenses/MIT)<br>教材テキスト / Text: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)<br>図表 / Figures: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) 

---

## 🔙 戻る / Back
- **JP:** [Edusemi-Plus トップへ戻る](https://samizo-aitl.github.io/Edusemi-Plus/index.html)  
- **EN:** [Return to Edusemi-Plus Top](https://samizo-aitl.github.io/Edusemi-Plus/index.html)
