---
layout: default
title: 🔀 RF Switches
---

---

# 🔀 RF Switches  

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../../#-ライセンス--license)

---

## 📘 概要 / *Overview*  

本ページでは、**FeFET / MEMS / SOI をベースとした RF スイッチ技術**について整理します。  
*This page covers RF switch technologies based on FeFET, MEMS, and SOI.*

---

## 🕰️ 歴史的背景 / *Historical Background*  

- **GaAs FET スイッチ（1980–1990年代）**  
  - 携帯電話初期に利用、高周波特性は良好だが高コスト・高電圧駆動が課題。  
  - *Used in early mobile phones; good RF performance but costly and voltage-limited.*  

- **SOI-CMOS スイッチ（2000年代〜現在）**  
  - CMOS互換・低コストで普及。スマートフォンFEMに標準化。  
  - *Became mainstream in the 2000s, cost-effective and CMOS-compatible.*  

- **MEMS スイッチ（2000年代後半〜R&D）**  
  - 超低損失・高アイソレーションを実現。ただし寿命・信頼性が課題。  
  - *Offer ultra-low loss and high isolation, but limited by lifetime/reliability issues.*  

- **FeFET スイッチ（2020年代〜研究開発中）**  
  - 強誘電体HfO₂を用いた **不揮発ON/OFF制御** が可能。  
  - 6Gに向けた「再構成可能RFフロントエンド」の候補技術。  
  - *Enable non-volatile ON/OFF with HfO₂ ferroelectrics; promising for 6G reconfigurable RF.*  

---

## 📊 性能比較 / *Performance Comparison*  

| 指標 / Metric | SOI-CMOS | MEMS | FeFET (R&D) |
|---|---|---|---|
| **挿入損失 / Insertion Loss (@2–6 GHz)** | 0.3–0.5 dB | 0.1–0.3 dB | 0.2–0.4 dB (予測) |
| **アイソレーション / Isolation** | 25–35 dB | 40–60 dB | 30–40 dB |
| **電力ハンドリング / Power Handling** | 中 (数W) | 高 (数十W) | 中 (数W, CMOS互換) |
| **動作速度 / Switching Speed** | ns オーダー | μs オーダー | ns オーダー (予測) |
| **信頼性 / Lifetime** | 高 (10¹⁰ cycles) | 中 (10⁸–10⁹ cycles) | 未確立 (研究段階) |
| **市場導入 / Market Use** | スマホFEM標準 | インフラ・研究用途 | 大学・R&Dレベル |

---

## 📡 応用分野 / *Applications*  

| 分野 / Field | 用途 / Application | 要求特性 / Requirements |
|---|---|---|
| **スマートフォン / Smartphones** | バンド選択、アンテナ切替 | 低IL、小型、高信頼性 |
| **Wi-Fi / IoT** | チューニング、経路切替 | 低電力、コスト効率 |
| **自動車 / Automotive (V2X, Telematics)** | 車載通信モジュール | 高耐性 (−40〜125°C)、長寿命 |
| **基盤技術 / Infrastructure (5G–6G)** | 高周波スイッチング | mmWave対応、高直線性、高電力処理 |

---

## ⚠️ 課題と展望 / *Challenges & Outlook*  

- **SOIスイッチ**  
  - 成熟技術だが、多バンド化によりチップサイズ・コストが増大。  
  - *Mature, but multi-band growth increases cost and die area.*  

- **MEMSスイッチ**  
  - 超低損失だが、寿命・速度・信頼性が課題。  
  - *Excellent IL and isolation, but lifetime and reliability remain issues.*  

- **FeFETスイッチ**  
  - 不揮発制御とCMOS互換性を兼備。6G時代における候補。  
  - *Non-volatile control, CMOS-compatible; strong candidate for 6G reconfigurable RF.*  

**将来展望 / Future Outlook**  
- 6Gでは再構成可能RFフロントエンドが必須。  
- 鍵は「低損失・高アイソレーション・高信頼性・不揮発性」を同時に満たすこと。  

---

## 👤 著者・ライセンス / *Author & License*  

| 項目 / Item | 詳細 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../../#-ライセンス--license) |

---

## ⬆️ 戻る / *Back*  

| Link | Badge |
|---|---|
| 📡 Back to RF Devices | [![Back Site](https://img.shields.io/badge/⬆️%20Back-RF--Devices-brightgreen?style=for-the-badge&logo=githubpages)](../) |
| 🔬 Back to Applied Devices | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Applied--Devices-blue?style=for-the-badge&logo=githubpages)](../../) |
