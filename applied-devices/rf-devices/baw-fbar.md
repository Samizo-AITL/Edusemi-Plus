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
これらはスマートフォンや無線通信の **RFフロントエンドモジュール（FEM）** の中核を担う技術です。  

*This page covers BAW/FBAR devices using thin-film piezoelectric materials such as AlN, ScAlN, HfO₂, and PZT.  
These devices form the backbone of RF front-end modules (FEMs) in smartphones and wireless systems.*  

---

## 🕰️ 歴史的背景 / *Historical Background*  

- **1990年代後半**：GaAs FETやLCフィルタからの置き換えとして、AlN系FBARが登場。  
- **2000年代**：3G携帯電話の普及に伴い、BroadcomやAgilentがBAW技術を製品化。  
- **2010年代**：スマートフォンの多バンド化により、Murata・Qorvo・Broadcomが市場を独占。  
- **現在**：ハイエンドスマホ1台に **50個以上のBAW/FBARフィルタ** が搭載される。  

*From GaAs FETs and LC filters to thin-film resonators, FBAR/BAW technology became the mainstream in 3G/4G/5G front-ends, with today’s smartphones integrating 50+ filters per device.*  

---

## 🏗️ 構造と動作原理 / *Structure & Principle*  

- **FBAR (Film Bulk Acoustic Resonator)**  
  - 薄膜圧電層を上下電極で挟み、厚み方向に音響波を励起する構造。  
  - サスペンション膜またはBragg反射鏡により、基板からの音響損失を遮断。  

- **BAW (Bulk Acoustic Wave Filter)**  
  - FBARをフィルタ構造に組み合わせたもので、狭帯域・広帯域の両方に対応可能。  
  - ダイプレクサやマルチプレクサに発展し、**複数周波数バンドを同時に処理可能**。  

*FBAR uses thickness-mode acoustic waves in thin films, while BAW filters combine resonators into multiplexers for multi-band operation.*  

---

## 🧪 材料技術 / *Material Technologies*  

| 材料 / Material | 特徴 / Characteristics | 利点 / Advantages | 課題 / Challenges |
|---|---|---|---|
| **AlN** | 高音速・安定性良好 | 高Q, CMOS互換 | 結合係数が小さい |
| **ScAlN** | AlNにScを添加 | 高結合係数, 5G帯向け | 結晶欠陥による歩留まり低下 |
| **PZT** | 強誘電体圧電 | 大きな結合係数, 教育用に有用 | CMOS互換性低, 鉛フリー課題 |
| **HfO₂** | 強誘電特性を持つ新興材料 | CMOS互換性, 将来のRF応用候補 | 実用化は初期段階 |

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

## 📊 産業動向 / *Industry Trends*  

- **Murata**：世界シェアNo.1、スマホ向けBAW/FBARの大量供給。  
- **Broadcom**：高性能マルチプレクサでAppleなど大手OEMに採用。  
- **Qorvo / Skyworks**：米国勢、PAと統合したSiP構成に強み。  
- **新興研究**：ScAlNベースで6GHz超帯域に対応、研究室レベルでHfO₂圧電も模索。  

*Murata leads global share, Broadcom dominates in premium smartphones, and U.S. vendors focus on SiP with PA integration. Emerging research targets ScAlN and HfO₂-based devices.*  

---

## ⚠️ 課題と展望 / *Challenges & Outlook*  

- **多バンド爆発**：スマホ1台に50+フィルタ、さらなる小型化が必要。  
- **材料課題**：ScAlNの歩留まり改善、PZTの鉛フリー化。  
- **6Gへの拡張**：7–20 GHz帯でのQ維持と低損失化。  
- **再構成可能RF**：FeVarやFeFETスイッチと組み合わせ、動的フィルタ実現の可能性。  

---

## 👨‍🏫 教育的視点 / *Educational Note*  

- BAW/FBARは **「電気 → 音響 → 電気」へのエネルギー変換デバイス** である。  
- FeRAMのキャパシタ積層と似ており、教育モデルでは **キャパシタ設計から音響共振への発展** を示せる。  
- 半導体教育において「電気-機械連成」を理解する最適教材。  

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
