---
layout: default
title: 📡 0.18µm RFCMOS Capacitor Formation（教育モデル）
---

---

# 📡 0.18µm RFCMOS Capacitor Formation — 教育モデル  
*0.18µm RFCMOS Capacitor Formation — Educational Model*

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](../../../#-ライセンス--license)

---

## 🧭 概要 / Overview  

本資料は **0.18µm FeRAMプロセス**を起点とし、RF応用に焦点を当てて「キャパシタ形成工程」を抽出・再構成した教育モデルです。  
FeRAMの**Pt/PZT/Tiキャパシタ構造**を、RFフロントエンドに応用可能な**HfZrO₂ベースキャパシタ**へと置き換え、CMOS整合性のある形で示しています。  

*This document extracts and restructures the **capacitor formation process** from the 0.18µm FeRAM flow for RF applications.  
The **Pt/PZT/Ti ferroelectric capacitor** is replaced with an **HfZrO₂-based capacitor** suitable for RFCMOS integration.*  

---

## 🔽 RFCMOSキャパシタ形成工程 / *RFCMOS Capacitor Formation Steps*  

| 工程 / Step | 内容 / Description |
|-------------|--------------------|
| **TI1-SP（下部）** | TiNスパッタによる下部電極（バリア兼導電層）。<br>*TiN bottom electrode (barrier + conductive layer).* |
| **HZO-ALD** | HfZrO₂強誘電膜をALDで堆積（厚さ5–10nm）。<br>*HfZrO₂ ferroelectric layer deposition by ALD (5–10nm).* |
| **HZO-ANL** | Rapid Thermal Anneal (400–500℃) により結晶化。<br>*Crystallization of HZO via RTA at 400–500℃.* |
| **TI2-SP（上部）** | TiNスパッタ上部電極。配線バッファ機能を兼ねる。<br>*Top TiN electrode, also serving as wiring buffer.* |
| **RFCAP-PH/ET** | フォト＋RIEによりキャパシタパターニング。<br>*Capacitor patterning by lithography + RIE.* |

📘 **解説 / Explanation**  
- HfZrO₂は**CMOS整合性が高く、水素アニールにも耐性**がある。  
- FeRAM PZTと異なり、**最終水素シンター工程を削除する必要がない**。  
- RF可変容量デバイス（FeVar）やFeFET-Switchの基盤素子として活用可能。  

---

## 🔗 関連教材リンク / *Related Educational Links*  

| リンク / Link | 内容 / Description |
|---|---|
| 📘 [0.18µm FeRAM Process Flow（完全版）](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/doc_FeRAM/feram_full_process_table) | FeRAMプロセスフロー完全版（教育モデル）<br>*Full FeRAM process flow (educational model)* |
| 📘 [Proposal CMOS混載型RFデバイス（教育モデル）](https://samizo-aitl.github.io/Edusemi-v4x/applied-devices/rf-devices/proposal_rfintegration) | CMOS混載型RFデバイス提案（教育モデル）<br>*Proposal of CMOS-integrated RF devices (educational model)* |
| 🔬 [0.18µm CMOSロジックプロセス](https://samizo-aitl.github.io/Edusemi-v4x/chapter3_process_evolution/docs/0.18um_Logic_ProcessFlow) | 0.18µm CMOSロジックプロセス教材<br>*0.18µm CMOS logic process (educational)* |

---

## 👤 Author & License  

| 項目 / Item | 詳細 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 再配布・改変自由（教育目的） / *Free for educational use* <br> 商用利用は別途許可 / *Commercial use requires separate permission* |
