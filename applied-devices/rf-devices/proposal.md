---
layout: default
title: 💡 Proposal CMOS混載型RFデバイス
---

---

# 💡 CMOS混載型RFデバイス提案  
*Proposal: CMOS-integrated RF Devices*

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../#-ライセンス--license)

---

## 🔗 リンク / *Links*  

| Link | Badge |
|---|---|
| 🌐 **View Site** | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/rf-devices/proposal) |
| 📂 **View Repo** | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/applied-devices/rf-devices/) |

---

## 📘 概要 / *Overview*  

本提案は、三溝真一による **教育目的の仮想プロセス「0.18 µm FeRAM」** を起点に、  
**CMOS混載型RFデバイス**を実現することを目指すものです。  

*This proposal aims to realize CMOS-integrated RF devices, expanding from the educational virtual process “0.18 µm FeRAM”.*  

👉 実在の製品・企業・製造プロセスとは無関係ですが、実現可能性を追求した設計指針を含みます。  
👉 *This work is independent of actual products or proprietary processes, but explores practical design directions.*  

---

## 🔄 提案デバイス群 / *Proposed Devices*  

| デバイス / Device | 内容 / Description | 特徴 / Differentiation |
|---|---|---|
| **FeVar (Ferroelectric Varactor)** | HfO₂系強誘電体を用いた不揮発可変キャパシタ | 再構成可能・不揮発制御 <br>*Reconfigurable, non-volatile control* |
| **FeFET-Switch** | HZO局所ゲートを利用したCMOS互換RFスイッチ | CMOS整合・低コスト <br>*CMOS-compatible, cost-efficient* |
| **BAW/FBAR (Edu ver.)** | PZT/HfO₂薄膜共振器 | 薄膜積層共振を応用 <br>*Thin-film stack resonance* |

---

## 📚 系譜図 / *Process Lineage*  

```mermaid
flowchart TB
  subgraph FE["0.18 µm FeRAM (Virtual, Educational)"]
    GATE["Front-end (FEOL) / Dual-VDD CMOS 1.8/3.3 V"] --> SALI["Salicide CoSi2"]
    BEOL["Back-end (BEOL) / AlCu M1-3 + W-Plugs"]
    CAP1["FeRAM Stack A / Pt/PZT/Ti"]
    CAP2["FeRAM Stack B / TiN/HfZrO₂/TiN (HZO)"]
    GATE --> BEOL --> CAP1
    BEOL --> CAP2
  end

  CAP2 --> FeVar["FeVar / Ferroelectric Varactor"]
  GATE --> RFSW1["RF Switch / FET + FeVar Bias"]
  GATE --> RFSW2["RF Switch / FeFET-Switch"]
  CAP1 --> BAW["BAW/FBAR Core"]

  subgraph RF["RF Front-End Integration"]
    MATCH["Reconfigurable Matching / Cfixed || FeVar"]
    PATHSEL["Band/Path Selection / with RF Switches"]
    FILTER["BAW/FBAR Filters"]
    LNA["PA/LNA I/O Networks"]
  end

  FeVar --> MATCH --> LNA
  RFSW1 --> PATHSEL --> FILTER
  RFSW2 --> PATHSEL
  BAW --> FILTER
```

---

## 🏭 産業的背景 / *Industrial Background*  

現行のRFフロントエンドは **FBAR/BAW + SOIスイッチ** に依存し、  
**多バンド化による部品点数増大・コスト増**が大きな課題です。  

*Today’s RF front-ends rely on FBAR/BAW + SOI switches, facing issues of component count increase and rising costs due to multi-band expansion.*  

欧州・米国・日本では、**再構成可能RF** が6Gの研究テーマとして進展中。  
CMOS内に可変素子を統合することで、**コスト削減・小型化・低消費電力化**が可能となります。  

---

## ⚖️ 競合技術との比較 / *Comparison with Existing Approaches*  

| 技術 / Technology | 特徴 / Characteristics | 課題 / Challenges |
|---|---|---|
| **SOI-CMOS Switch** | 標準スマホFEMで実績多数 <br>*Proven in smartphone FEM* | 多バンドでチップ肥大・コスト増 <br>*Chip size/cost explosion in multi-band* |
| **GaAs FET** | 高周波特性良好 <br>*Excellent RF performance* | 高コスト・電源制約 <br>*Costly, power supply constraints* |
| **MEMS Switch** | 超低損失・高アイソレーション <br>*Ultra-low loss, high isolation* | 信頼性・寿命課題 <br>*Reliability, lifetime issues* |
| **外付けVaractor** | アンテナチューニングで利用 <br>*Used in antenna tuning* | 実装負荷・集積困難 <br>*Integration challenges* |
| **本提案 (FeVar/FeFET)** | CMOS互換・不揮発制御・小型化 <br>*CMOS-compatible, non-volatile, compact* | 実証・量産性未確立 <br>*Not yet mass-proven* |

---

## 📉 部品点数削減の効果 / *Effect of Component Reduction*  

- スマホFEMでは数十〜百個のフィルタ・スイッチが必要。  
  *Current FEMs require tens to over 100 filters/switches.*  
- **可変キャパシタ（FeVar）**と**不揮発RFスイッチ（FeFET-SW）**を導入することで、  
  フィルタバンクとスイッチ数を半減可能。  
  *By introducing FeVar and FeFET-SW, filter banks and switches could be halved.*  
- **小型化・低コスト化・低損失**が期待される。  
  *Expected results: reduced size, lower cost, and lower insertion loss.*  

---

## ⚖️ RFCMOSのメリット・デメリット / *Pros & Cons of RFCMOS*  

### ✅ メリット / *Advantages*  
- CMOS互換：SoC集積可能  
  *CMOS-compatible, enabling SoC integration*  
- コスト削減：GaAs, SOIより低コスト  
  *Cheaper than GaAs and SOI*  
- 低消費電力：不揮発制御により待機電力削減  
  *Non-volatile control reduces standby power*  

### ❌ デメリット / *Disadvantages*  
- 高周波特性：GaAs, MEMSに劣る  
  *Weaker RF performance compared to GaAs, MEMS*  
- 電力耐性：PA用途に制約  
  *Limited for PA applications*  
- プロセス未成熟：量産実証不足  
  *Immature process, not yet mass-proven*  

### 🔧 改善方法 / *Improvements*  
- **HfZrO₂導入**：水素耐性強化、CMOS整合性改善  
  *HfZrO₂ for better hydrogen resistance and CMOS compatibility*  
- **3D構造導入**：GAA/FinFETベースで高周波特性強化  
  *3D GAA/FinFET structures to enhance RF performance*  
- **ハイブリッド材料**：高Q誘電体＋強誘電体の組合せ  
  *Hybrid dielectrics for higher Q-factor and reconfigurability*  

---

## 🗓️ 実現型ロードマップ / *Implementation Roadmap*  

```mermaid
gantt
    title CMOS-integrated RF Devices (Implementation Roadmap)
    dateFormat  YYYY-MM-DD
    section FeVar (HZO)
    Device Modeling & TCAD     :done,    des1, 2025-01-01, 90d
    Compact Models & PDK       :active,  des2, 2025-04-01, 120d
    Small-scale Integration    :         des3, 2025-09-01, 180d
    section FeFET Switch
    Test Chips & Evaluation    :done,    sw1,  2025-03-01, 90d
    Reliability Improvements   :active,  sw2,  2025-07-01, 120d
    Integration with RF Frontend:        sw3,  2026-01-01, 180d
    section BAW/FBAR (Edu→Proto)
    Resonator Pilot Structures :         baw1, 2025-10-01, 120d
    Integrated Filter Modules  :         baw2, 2026-04-01, 180d
```

- **FeVar**: TRL 4–6 （デバイスモデリング→小規模集積）  
- **FeFET-Switch**: TRL 3–5 （試作→信頼性改善→RF統合）  
- **BAW/FBAR**: TRL 3–4 （教育モデル→試作共振器）  

---

## 🔗 関連教材リンク / *Related Links*  

| リンク / Link | 内容 / Description |
|---|---|
| 📘 [0.18µm FeRAM Process Flow — 完全版](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/doc_FeRAM/feram_full_process_table) | FeRAMプロセスフロー完全版（教育モデル）<br>*Full FeRAM process flow (educational model)* |
| 📘 [FeRAM特有工程の詳細解説](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/doc_FeRAM/0.18um_FeRAM_ProcessFlow) | PZTキャパシタ・AlOx保護膜・水素還元対策<br>*FeRAM-specific steps: capacitor, AlOx, H₂ mitigation* |
| 📘 [0.18µm RFCMOS Process Flow（派生版）](./018um_rfcapacitor_extracted.md) | RFCMOS派生プロセスフロー<br>*Derived RFCMOS process flow* |
| 🔬 [0.18µm CMOSロジックプロセス](https://samizo-aitl.github.io/Edusemi-v4x/chapter3_process_evolution/docs/0.18um_Logic_ProcessFlow) | 0.18µm CMOSロジックプロセス教材<br>*0.18µm CMOS logic process (educational)* |
| 📐 [MOSトランジスタの特性と信頼性](https://samizo-aitl.github.io/Edusemi-v4x/chapter4_mos_characteristics/) | MOS特性と信頼性教材<br>*MOS transistor characteristics and reliability* |
| 💾 [メモリ技術教材集](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/) | SRAM / DRAM / FeRAM / MRAM / 3DNAND 教材<br>*Memory technologies* |

---

## 👤 Author & License  

| 項目 / Item | 詳細 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 再配布・改変自由（教育目的） / *Free for educational use* <br> 商用利用は別途許可 / *Commercial use requires separate permission* |
