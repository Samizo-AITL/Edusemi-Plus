---
layout: default
title: 📡 RF・可変素子 / RF & Tunable Devices
---

---

# 📡 RF・可変素子 / RF & Tunable Devices  
*RF & Tunable Devices*

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../#-ライセンス--license)

---

## 🔗 リンク / Links  

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/rf-devices/) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/applied-devices/rf-devices) |

---

## 📘 概要 / Overview  
*Overview*

本カテゴリでは、**RF通信・高周波回路で利用される可変素子・スイッチングデバイス**を整理します。  
*This category covers tunable devices and switching elements used in RF communication and high-frequency circuits.*

例として：  
- **強誘電体可変キャパシタ（FeVar, HfO₂系など）**  
- **RFスイッチ（FeFET, MEMS, SOI-CMOSベース）**  
- **FBAR / BAWフィルタ（AlN, ScAlN, HfO₂ベース）**  
- **再構成可能RFフロントエンド**  

---

## 🔄 0.18 µm FeRAM からの展開 / Expansion from 0.18 µm FeRAM

本カテゴリは、三溝真一による **教育目的の仮想プロセスモデル**  
「0.18 µm FeRAM プロセス」を基盤として、RF領域へ応用展開されます。  
*This category builds on the **virtual process model for educational purposes** “0.18 µm FeRAM process” proposed by Shinichi Samizo,  
and expands it toward RF devices.*

- **強誘電キャパシタ（Pt/PZT/Ti, HfO₂系）** → RFフロントエンド用の可変キャパシタ（FeVar）  
- **高耐圧MOS + FeRAMキャパシタ統合** → RFスイッチ素子（FeFET, Reconfigurable Switch）  
- **PZT薄膜積層の共振利用** → FBAR/BAWフィルタへ応用  

> ⚠️ **注意 / Note**  
> ここで参照する「0.18 µm FeRAM プロセス」は、教育目的で設計された**仮想プロセス**であり、  
> 実在の製品・企業機密・製造フローとは一切関係ありません。  
> *The “0.18 µm FeRAM process” referenced here is a **virtual process for educational purposes** and is not related to any actual product, proprietary process, or confidential information.*

---

## 🧭 図解：0.18 µm FeRAM → RFデバイス系譜  
*Process lineage from the 0.18 µm FeRAM virtual process to RF devices*

```mermaid
flowchart TB
  subgraph FE["0.18 um FeRAM (Virtual, Educational)"]
    GATE["Front-end (FEOL)\\nDual-VDD CMOS 1.8/3.3 V"] --> SALI["Salicide CoSi2"]
    BEOL["Back-end (BEOL)\\nAlCu M1-3 + W-Plugs"]
    CAP1["FeRAM Stack A\\nPt/PZT/Ti"]
    CAP2["FeRAM Stack B\\nTiN/HfZrO2/TiN (HZO)"]
    GATE --> BEOL --> CAP1
    BEOL --> CAP2
  end

  CAP2 -->|"BEOL integration / ALD-HZO 8-12 nm\\nRTA 400-450 degC"| FeVar{{"FeVar\\nFerroelectric Varactor"}}
  GATE -->|"HV MOS + FeVar gate bias"| RFSW1{{"RF Switch\\n(FET + FeVar Bias)"}}
  GATE -->|"Local HZO gate stack"| RFSW2{{"RF Switch\\n(FeFET-Switch)"}}
  CAP1 -->|"Thin-film piezo resonance use"| BAW(("BAW/FBAR Core"))

  subgraph RF["RF Front-End Integration"]
    MATCH["Reconfigurable Matching\\nCfixed || FeVar"]
    PATHSEL["Band/Path Selection\\nwith RF Switches"]
    FILTER["BAW/FBAR Filters"]
    LNA["PA/LNA I/O Networks"]
  end

  FeVar --> MATCH --> LNA
  RFSW1 --> PATHSEL --> FILTER
  RFSW2 --> PATHSEL
  BAW --> FILTER
```

---

## 📚 サブトピック / Sub-topics  
*Sub-topics*

| デバイス / Device | 概要（JP） | *Summary (EN)* | Link |
|---|---|---|---|
| 🧩 **Ferroelectric Varactors** | HfO₂系強誘電体を用いた可変キャパシタ | *HfO₂-based ferroelectric tunable capacitors* | [ferroelectric-varactors](./ferroelectric-varactors.md) |
| 🔀 **RF Switches** | FeFET/MEMS/SOIによるRFスイッチ | *RF switches using FeFET, MEMS, or SOI* | [rf-switches](./rf-switches.md) |
| 📡 **BAW/FBAR Devices** | AlN/ScAlNやHfO₂を用いた高周波フィルタ | *High-frequency filters using AlN/ScAlN or HfO₂* | [baw-fbar](./baw-fbar.md) |

---

## 🧩 市場への展開 / Market Deployment  

### 1) バリューチェーンと供給形態  
*Value chain & deliverables*

```mermaid
flowchart TB
  RnD["概念設計・研究開発 / Concept & R&D (Virtual 0.18 um FeRAM → RF)"] --> PDK["PDK・RF IP提供 / PDK & RF IP (FeVar / Switch / BAW cells)"]
  PDK --> REF["リファレンス設計 / Reference Designs (Front-End modules, eval boards)"]
  REF --> SiP["モジュール・SiPベンダー / Module & SiP Vendors (RF FEM, Antenna-in-Package)"]
  SiP --> OEM["機器メーカー (OEM/ODM) / OEM & ODMs (Handsets, IoT, Automotive)"]
  OEM --> Field["市場導入・認証展開 / Field Deployment (Certification & Rollout)"]
```  

- **教育起点の強み**：仮想プロセス → 実装テンプレ → 参照設計 という流れを一気通貫で提示可能  
- **提供形態**：  
  - RF 可変素子 IP セット（FeVar/スイッチのセル＋モデル）  
  - リファレンス・マッチネット（周波数別テンプレ）  
  - 評価基板（Sパラ測定・P1dB/IIP3実演）

---

### 2) アプリケーション・マップ  
*Application map*

| Segment | Use-case | Goal Specs (目安) | Note |
|---|---|---|---|
| **Smartphone RF FEM** | Band selection, tunable matching | IL ≤ 0.5 dB（switch）, Q@2–6 GHz > 30（FeVar） | 多バンド最適化・小型化 |
| **Wi-Fi (2.4/5/6 GHz)** | Antenna tuning / reconfig | S11 ≤ −10 dB、IIP3高め | 筐体差の補正 |
| **IoT (Sub-GHz/2.4 GHz)** | Antenna trimming | 低電力・不揮発設定保持 | バッテリ寿命重視 |
| **Automotive (V2X/Telematics)** | Harsh temp drift comp. | −40〜125 °Cドリフト補償 | 信頼性・AEC-Q |
| **Infrastructure (Sub-6/FR1)** | Reconfigurable front-end | 高IP3、耐電力 | PA側整合補助 |

---

### 3) TRL（技術成熟度）とロードマップ（教育モデル）
*TRL & roadmap (educational model)*

```mermaid
gantt
    title RF Devices Roadmap (Educational)
    dateFormat  YYYY-MM-DD
    section FeVar (HZO)
    Modeling/PDK            :done,    des1, 2025-01-01, 60d
    Layout Templates        :active,  des2, 2025-03-01, 60d
    Eval Board & S-params   :         des3, 2025-05-01, 90d
    section RF Switch
    FET+FeVar Gate Bias     :done,    sw1,  2025-02-01, 45d
    FeFET-Switch (local HZO):active,  sw2,  2025-03-15, 120d
    section BAW/FBAR
    Resonator Modeling      :         baw1, 2025-04-01, 90d
    Filter Reference        :         baw2, 2025-07-01, 90d
```

- **TRL 目安**：FeVar（5–6） → Switch（4–5） → BAW/FBAR（3–4）  
- **マイルストーン**：PDK公開 → 参照設計 → 評価基板 → 認証支援  

---

## 👤 **著者・ライセンス / Author & License**

| **項目 / Item** | **内容 / Details** |
|-----------------|--------------------|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 再配布・改変自由（教育目的） / *Free for educational use, redistribution, and modification* <br> 商用利用は別途許可が必要 / *Commercial use requires separate permission* |

---

## ⬆️ Applied Devices へ戻る / Back to Applied Devices  

| Link | Badge |
|---|---|
| 🌐 **カテゴリへ戻る / Back to Category** | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Applied--Devices-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/) |
| 📂 **リポジトリへ戻る / Back to Repo** | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/applied-devices) |
