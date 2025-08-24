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

## 🏭 産業的背景 / *Industrial Background*  

現行のRFフロントエンドは **FBAR/BAW + SOIスイッチ** に依存しており、  
多バンド化による **部品点数の爆発・コスト増** が大きな課題です。  

*Today’s RF front-ends rely heavily on FBAR/BAW + SOI switches,  
facing major challenges of filter count explosion and cost increase due to multi-band expansion.*  

欧州・米国・日本では、**再構成可能RF（Reconfigurable RF）** が次世代6Gの研究テーマとして進められています。  
CMOS内に可変素子を統合するアプローチは、**コスト削減・小型化・低消費電力化**につながります。  

---

## ⚖️ 競合技術との比較 / *Comparison with Existing Approaches*  

| 技術 / Technology | 特徴 / Characteristics | 課題 / Challenges |
|---|---|---|
| **SOI-CMOS Switch** | 標準スマホFEMで実績多数 | 多バンド化でチップ肥大・コスト増 |
| **GaAs FET** | 高周波特性良好 | 高コスト・電源制約 |
| **MEMS Switch** | 超低損失・高アイソレーション | 信頼性・寿命・応答速度 |
| **外付けVaractor** | アンテナチューニングに利用 | 実装負荷、集積化が難しい |
| **本提案 (FeVar/FeFET)** | CMOS互換・不揮発制御・小型化 | 実証段階、量産性未確立 |

---

## 🗓️ ロードマップ（教育モデル） / *Educational Roadmap (TRL)*  

```mermaid
gantt
    title CMOS-integrated RF Devices (Educational TRL Roadmap)
    dateFormat  YYYY-MM-DD
    section FeVar (HZO)
    Modeling & PDK Templates   :done,    des1, 2025-01-01, 60d
    Layout & Cell Libraries    :active,  des2, 2025-03-01, 90d
    Eval Boards & S-params     :         des3, 2025-06-01, 120d
    section FeFET Switch
    Device Modeling            :done,    sw1,  2025-02-01, 60d
    Test Structures            :active,  sw2,  2025-05-01, 120d
    section BAW/FBAR (Edu ver.)
    Resonator Modeling         :         baw1, 2025-07-01, 90d
    Filter Reference           :         baw2, 2025-10-01, 90d
```

- **TRL目安**  
  - FeVar：TRL 4–5（回路シミュレーション〜基板評価）  
  - FeFET Switch：TRL 3–4（素子モデリング〜試作構造）  
  - BAW/FBAR (Edu ver.)：TRL 3（モデリング段階）  

*Estimated TRL levels: FeVar (4–5), FeFET Switch (3–4), BAW/FBAR Edu (3).*  

---

## 👤 Author & License  

| 項目 / Item | 詳細 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 再配布・改変自由（教育目的） / *Free for educational use* <br> 商用利用は別途許可 / *Commercial use requires separate permission* |
