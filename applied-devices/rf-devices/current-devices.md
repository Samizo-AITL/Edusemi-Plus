---
layout: default
title: 1️⃣ 現行 & 新興RFデバイス / Current & Emerging RF Devices
---

---

# 1️⃣ 現行 & 新興RFデバイス / *Current & Emerging RF Devices*

---

## 📘 全体概要 / *Overview*  
現行のRF通信モジュールは、**スマートフォン・IoT・車載**を中心に巨大市場を形成しています。  
特に **FBAR/BAWフィルタ** と **SOI RFスイッチ** を中核とする **RFフロントエンドモジュール（FEM）** が標準構成です。  

一方で、**強誘電体可変キャパシタ（FeVar）** や **MEMS可変C** といった **新興技術** も研究開発が進められており、  
今後の **再構成可能RFフロントエンド** に向けた基盤となる可能性があります。  

*Today’s RF communication modules form a huge market in smartphones, IoT, and automotive.  
Mainstream FEMs rely on FBAR/BAW filters and SOI RF switches.  
At the same time, emerging devices such as ferroelectric varactors (FeVar) and MEMS capacitors are under R&D, with potential for reconfigurable RF front-ends.*  

---

## 🔑 構成要素 / *Key Components*  

| デバイス / Device | 技術区分 / Status | 現状技術 / Current Tech | 主なプレーヤー / Major Players | 特徴 / Characteristics | 詳細 / Details |
|---|---|---|---|---|---|
| 📡 **BAW/FBAR Devices** | 商用主流<br>*Mainstream* | AlN, ScAlN薄膜共振子<br>*AlN/ScAlN resonators* | Murata, Broadcom, Qorvo, Skyworks | 高Q・高周波対応・量産実績豊富<br>*High Q, high frequency, proven mass production* | [baw-fbar.md](./baw-fbar.md) |
| 🔀 **RF Switches** | 商用主流<br>*Mainstream* | SOI-CMOSベースFETスイッチ<br>*SOI-CMOS FET switches* | Qorvo, Skyworks, pSemi | 低挿入損失、既に標準化<br>*Low IL, standardized* | [rf-switches.md](./rf-switches.md) |
| 🧩 **Ferroelectric Varactors** | 新興技術<br>*Emerging* | HfO₂系強誘電体を利用<br>*HfO₂-based ferroelectrics* | Niche, university R&D | 可変C素子、再構成可能性向上のポテンシャル<br>*Tunable C for reconfigurable front-ends* | [ferroelectric-varactors.md](./ferroelectric-varactors.md) |
| ⚙️ **MEMS Capacitors** | 新興技術<br>*Emerging* | 可動構造MEMS可変C<br>*Movable MEMS varactors* | niche | 高Qだが歩留まり課題<br>*High Q, but yield issues* | — |

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

- **再構成可能RFへの期待**  
  柔軟性・周波数切替が可能なFeVarやMEMSへの注目度が上昇。  
  *Rising attention to FeVar and MEMS for reconfigurable RF.*  

---

## ⚠️ 現行課題 / *Current Challenges*  

| 課題 / Challenge | 内容 / Details |
|---|---|
| **再構成性の欠如 / Lack of reconfigurability** | デバイス特性が固定されており、周波数再構成が困難。 |
| **部品点数の爆発 / Filter count explosion** | 多バンド化により数十個のフィルタを実装、コスト増大。 |
| **熱信頼性・挿入損失の制約 / Thermal reliability & IL** | 高電力駆動や高温環境での安定性が課題。 |

---

## 🔗 関連リンク / *Related Links*  

- [baw-fbar.md](./baw-fbar.md) — FBAR/BAWフィルタの仕組みと産業動向  
- [rf-switches.md](./rf-switches.md) — RFスイッチ技術の詳細  
- [ferroelectric-varactors.md](./ferroelectric-varactors.md) — 強誘電体可変キャパシタの研究動向  
- [rfcmos_review.md](./rfcmos_review.md) — CMOS混載型RFデバイス検討  
