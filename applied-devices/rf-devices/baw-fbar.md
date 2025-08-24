---
layout: default
title: 📡 BAW / FBAR Devices
---

---

# 📡 BAW / FBAR Devices  

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../../#-ライセンス--license)

---

## 📘 概要 / *Overview*  

本ページでは、**薄膜圧電材料（AlN, ScAlN, HfO₂, PZT など）を用いた BAW/FBAR デバイス**について解説します。  
*This page covers BAW/FBAR devices using thin-film piezoelectric materials such as AlN, ScAlN, HfO₂, and PZT.*  

---

## 🏗️ 構造と動作原理 / *Structure & Principle*  

- **FBAR (Film Bulk Acoustic Resonator)**  
  - 薄膜圧電層を上下電極で挟み、厚み方向に音響波を励起する構造。  
  - 高Q特性と小型化が可能。  

- **BAW (Bulk Acoustic Wave filter)**  
  - FBARをフィルタ構造に組み合わせたもの。  
  - ダイプレクサ・マルチプレクサ構成に展開され、スマートフォンFEMの基幹要素となっている。  

*FBAR excites acoustic waves in the thickness direction of piezoelectric films, while BAW filters combine multiple resonators into duplexers or multiplexers.*  

---

## 🔄 0.18 µm FeRAM からの関連性 / *Relation to 0.18 µm FeRAM*  

- **PZT 薄膜の積層・結晶化プロセス**は、  
  RF フィルタ（FBAR/BAW）の共振子形成に展開可能。  
- 教育モデルとして、**FeRAM キャパシタ形成工程 → RF 共振素子**という流れを提示できる。  

> ⚠️ **注意 / Note**  
> 「0.18 µm FeRAM プロセス」は教育目的の仮想モデルであり、実在の製品・企業機密・製造フローとは無関係です。  
> *The “0.18 µm FeRAM process” is a virtual model for educational purposes, unrelated to any actual product or proprietary flow.*  

---

## 📡 応用分野 / *Applications*  

| 分野 / Field | 用途 / Application | 目標仕様 / Key Specs |
|---|---|---|
| **スマートフォン** | フィルタ / マルチプレクサ | Q > 1000, f = 2–6 GHz |
| **Wi-Fi (2.4/5/6 GHz)** | フィルタ / チューナブル構成 | 高選択度, 小型化 |
| **IoT** | アンテナ整合 / 簡易フィルタ | 低電力, 低コスト |
| **自動車 (V2X/Telematics)** | 耐環境RFフィルタ | −40〜125°C動作 |
| **インフラ (5G/6G Sub-6, FR2)** | 高周波・広帯域フィルタ | mmWave帯対応, 高信頼性 |

---

## ⚠️ 課題と展望 / *Challenges & Outlook*  

- **ScAlN** の採用による高性能化（高結合係数・高周波対応）。  
- **HfO₂・PZT 薄膜**の研究的適用により、新しい材料プラットフォームの可能性。  
- **6G帯 (7–20 GHz) への拡張**において、共振Qの維持と低損失化が課題。  

*Future challenges include high-k piezoelectric films (ScAlN, HfO₂, PZT), maintaining high Q in mmWave ranges, and enabling reconfigurable RF front-ends for 6G.*  

---

## 👤 **著者・ライセンス / Author & License**

| **項目 / Item** | **内容 / Details** |
|-----------------|--------------------|
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
