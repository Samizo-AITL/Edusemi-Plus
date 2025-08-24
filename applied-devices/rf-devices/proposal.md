---
layout: default
title: 💡 Proposal CMOS混載型RFデバイス
---

---

# 💡 CMOS混載型RFデバイス提案  
*Proposal: CMOS-integrated RF Devices*

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../#-ライセンス--license)

---

## 📘 概要 / Overview  

本提案は、三溝真一による **教育目的の仮想プロセス**「0.18 µm FeRAM」を起点に、  
**CMOS混載型RFデバイス**を応用展開するものです。  

*This proposal expands the virtual educational 0.18 µm FeRAM process into CMOS-integrated RF devices.*

---

## 🔄 提案デバイス群 / Proposed Devices  

| デバイス / Device | 提案内容 / Proposal | 差別化ポイント / Differentiation |
|---|---|---|
| **FeVar (Ferroelectric Varactor)** | HfO₂系強誘電体を用いた不揮発可変キャパシタ | 再構成可能, 不揮発設定保持 |
| **FeFET-Switch** | HZO局所ゲートスタックを利用したRFスイッチ | CMOS互換, 低コスト集積 |
| **BAW/FBAR (Edu ver.)** | PZT/HfO₂薄膜共振器を用いた教育モデル | 薄膜積層の共振利用, 教育起点の簡易設計 |

---

## 📚 系譜図 / Process Lineage  

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

  CAP2 --> FeVar{{"FeVar / Ferroelectric Varactor"}}
  GATE --> RFSW1{{"RF Switch / FET + FeVar Bias"}}
  GATE --> RFSW2{{"RF Switch / FeFET-Switch"}}
  CAP1 --> BAW(("BAW/FBAR Core"))

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

## 📊 市場展開シナリオ / Market Deployment  

- **ターゲット応用**  
  - IoT：アンテナ自動調整・不揮発設定保持  
  - Automotive：V2X・高温補償RF  
  - 6G：再構成可能RFフロントエンド  
- **提供形態**  
  - RF IPセル（FeVar, Switch, FilterのPDK）  
  - リファレンス回路（Matching, Path Select）  
  - 教育評価基板（Sパラ測定, 実演）  

---

## 👤 Author & License  

| 項目 / Item | 詳細 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 再配布・改変自由（教育目的） / *Free for educational use* <br> 商用利用は別途許可 / *Commercial use requires separate permission* |
