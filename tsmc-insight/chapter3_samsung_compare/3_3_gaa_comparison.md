---
layout: default
title: 🏗️ 3.3 GAA対応：サムスン3nm先行 vs TSMC N2 / 3.3 GAA Implementation: Samsung 3nm Lead vs TSMC N2
---

---

# 🏗️ 3.3 GAA対応：サムスン3nm先行 vs TSMC N2  
**3.3 GAA Implementation: Samsung 3nm Lead vs TSMC N2**

---

## 📜 概要 / Overview

**JP:**  
GAA（Gate-All-Around）はFinFETの後継となるトランジスタ構造で、チャネル全周をゲートで囲むことにより、リーク電流低減と駆動能力向上を実現します。  
サムスンは2022年に**3GAE**世代でGAAを世界初商用化し、先行者利益を狙いました。一方TSMCは、**N2世代（2025年予定）**でGAAを導入する方針を採り、量産歩留まりの確保を優先しています。

**EN:**  
GAA (Gate-All-Around) is the successor to FinFET, surrounding the channel entirely with the gate, reducing leakage current and improving drive strength.  
Samsung was the first to commercialize GAA in its **3GAE** generation in 2022, aiming for first-mover advantage.  
TSMC plans to introduce GAA in its **N2 node (2025)**, prioritizing stable yield before deployment.

---

## ⚖️ アプローチ比較 / Approach Comparison

| 項目 / Item | サムスン / Samsung | TSMC |
|-------------|--------------------|------|
| **導入時期 / Introduction Timing** | 2022（3GAE） | 2025（N2） |
| **構造タイプ / Structure Type** | MBCFET™（Multi-Bridge Channel FET） | Nanosheet GAA |
| **主な顧客 / Key Customers** | Qualcomm, IBM（試作） | Apple, NVIDIA（予定） |
| **初期課題 / Initial Challenges** | 歩留まりの安定化、設計IP不足 | EUV層数調整、EDA対応 |
| **設計支援 / Design Support** | SAFETM GAA PDK提供 | OIP対応GAA PDK提供 |

---

## 🧩 設計と製造の相互作用 / Design–Manufacturing Interplay

**JP:**  
GAA世代ではチャネル幅調整やマルチブリッジ構造による最適化が可能ですが、配線抵抗・寄生容量の影響を抑えるためのEDA対応が重要です。  
サムスンは早期導入に伴い、IPエコシステムの成熟が追いつかない面がありました。  
TSMCはこの経験を踏まえ、EDAベンダーやIPプロバイダとの事前調整を強化しています。

**EN:**  
In the GAA era, channel width tuning and multi-bridge structures enable optimization, but EDA support is essential to mitigate wiring resistance and parasitic capacitance.  
Samsung’s early adoption meant its IP ecosystem was not fully mature.  
TSMC has taken note of this, strengthening pre-launch coordination with EDA vendors and IP providers.

---

## 🔍 補足キーワード / Key Terms

- **MBCFET™** — SamsungのGAA商標 / Samsung's trademarked GAA structure  
- **Nanosheet GAA** — TSMC採用予定のチャネル構造 / TSMC’s planned channel structure  
- **PDK (Process Design Kit)** — 設計ルールやデバイスモデルを含むEDA用データセット  
- **Parasitic Capacitance / 寄生容量**

---

## 🔗 関連リンク / Related Links

- [3.2 EUV導入戦略と層数](3_2_euv_strategy.md)  
- [3.4 歩留まり・顧客数・ファブレス連携の違い](3_4_yield_customer_collab.md)  
- [第3章 README](README.md)

---

## 🔙 戻る / Back
- **JP:** [第3章 READMEに戻る](README.md)  
- **EN:** [Return to Chapter 3 README](README.md)
