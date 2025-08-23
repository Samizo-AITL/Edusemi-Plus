---
layout: default
title: 1️⃣ 現行RFデバイス / Current RF Devices
---

---

# 1️⃣ 現行RFデバイス / *Current RF Devices*

---

## 📘 全体概要 / *Overview*  
現行のRF通信モジュールは、**スマートフォン・IoT・車載**を中心に巨大市場を形成しています。  
特に **FBAR/BAWフィルタ** と **SOI RFスイッチ** を中核とする **RFフロントエンドモジュール（FEM）** が標準構成です。  
また、チューナブル素子（可変キャパシタやMEMS）は一部で研究開発が進んでいますが、量産市場では限定的です。  

*Today’s RF communication modules form a huge market in smartphones, IoT, and automotive.  
Standard RF front-end modules (FEMs) are built around FBAR/BAW filters and SOI RF switches.  
Tunable devices such as varactors or MEMS are still in limited commercial use, mainly in R&D.*  

---

## 🔑 構成要素 / *Key Components*  

| デバイス / Device | 現状技術 / Current Tech | 主要プレーヤー / Major Players | 特徴 / Characteristics | 詳細 / Details |
|---|---|---|---|---|
| 🧩 **Ferroelectric Varactors** | 一部で研究開発段階、商用は限定的<br>*Mostly R&D stage, limited in products* | Niche, university R&D | 可変C素子、再構成可能性向上のポテンシャル<br>*Tunable C for reconfigurable front-ends* | [ferroelectric-varactors.md](./ferroelectric-varactors.md) |
| 🔀 **RF Switches** | SOI-CMOSベースが主流<br>*SOI-CMOS dominates* | Qorvo, Skyworks, pSemi | 低挿入損失、既に標準化<br>*Low IL, standardized* | [rf-switches.md](./rf-switches.md) |
| 📡 **BAW/FBAR Devices** | AlN, ScAlNベース薄膜共振子<br>*AlN, ScAlN-based resonators* | Murata, Broadcom, Qorvo, Skyworks | 高Q・高周波対応・量産実績豊富<br>*High Q, high-frequency, proven mass production* | [baw-fbar.md](./baw-fbar.md) |

---

## 📈 市場トレンド / *Market Trends*  

- **多バンド化によるフィルタ爆発**  
  スマートフォンは数十個のBAW/FBARフィルタを搭載。  
  *Smartphones now integrate dozens of BAW/FBAR filters.*  

- **高周波化 (5G FR1/FR2, 6G準備)**  
  3–6 GHz帯から mmWave 帯へ拡張。  
  *Expanding from 3–6 GHz into mmWave ranges.*  

- **小型・低コスト化**  
  アンテナ直結のSiP、Antenna-in-Package化が進展。  
  *Shift toward SiP and Antenna-in-Package (AiP).*  

---

## ⚠️ 現行課題 / *Current Challenges*  

| 課題 / Challenge | 内容 / Details |
|---|---|
| **再構成性の欠如 / Lack of reconfigurability** | デバイス特性が固定されており、周波数再構成が困難。 |
| **部品点数の爆発 / Filter count explosion** | 多バンド化により数十個のフィルタを実装、コスト増大。 |
| **熱信頼性・挿入損失の制約 / Thermal reliability & IL** | 高電力駆動や高温環境での安定性が課題。 |

---

## 🔗 関連リンク / *Related Links*  

- [rf-switches.md](./rf-switches.md) — RFスイッチ技術の詳細  
- [baw-fbar.md](./baw-fbar.md) — FBAR/BAWフィルタの仕組みと産業動向  
- [ferroelectric-varactors.md](./ferroelectric-varactors.md) — 強誘電体可変キャパシタの研究動向  
- [proposal.md](./proposal.md) — 次世代提案（CMOS混載型RFデバイス）
