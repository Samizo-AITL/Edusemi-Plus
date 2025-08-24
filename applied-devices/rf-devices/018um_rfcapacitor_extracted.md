---
layout: default
title: 🔽 Capacitor Formation for RF Devices (FeVar / FeFET / BAW) — 抜粋版
---

---

# 🔽 Capacitor Formation for RF Devices — 抜粋版  
*Capacitor Formation for RF Devices (FeVar / FeFET / BAW/FBAR) — Extracted Version*

[![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet)](https://samizo-aitl.github.io/Edusemi-v4x/#-ライセンス--license)

---

## 📘 本ドキュメントの位置づけ / *Scope of This Document*

本資料は、**0.18µm FeRAM Process Flow（教育モデル, 完全版）**を大元とし、  
そこから **RF向けキャパシタ形成工程（FeVar / FeFET / BAW/FBAR）**に関わる部分のみを抜粋・派生解説したものです。  

*This document originates from the **0.18µm FeRAM Process Flow (educational, full version)**,  
and extracts only the capacitor formation steps relevant to RF devices (FeVar / FeFET / BAW/FBAR).*

👉 **大元のプロセスフローはこちら → [0.18µm FeRAM Process Flow — 完全版](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/doc_FeRAM/feram_full_process_table.md)**

---

## 🔽 FeVar / Ferroelectric Varactor  

| 工程 / Step | 内容 / Description |
|-------------|--------------------|
| **TiN-BOT** | TiN下部電極形成。CMOS BEOL互換。<br>*Bottom electrode with TiN, CMOS-compatible.* |
| **HZO-DP/ANL** | HfZrO₂堆積＋アニール。不揮発キャパシタ特性を付与。<br>*HfZrO₂ deposition + anneal; enables nonvolatile capacitance.* |
| **TiN-TOP** | 上部電極TiN形成。再構成可能バラクタセル完成。<br>*Top TiN electrode; completes reconfigurable varactor cell.* |

---

## 🔽 FeFET-Switch Integration  

| 工程 / Step | 内容 / Description |
|-------------|--------------------|
| **Gate-Stack HZO** | CMOSゲートに局所HZO層を導入。<br>*Introduce local HZO stack in gate region.* |
| **Pattern & Etch** | FeFETスイッチ領域のみ選択形成。<br>*Patterned only in switch region.* |
| **Integration** | 通常FET配線と接続し、RFスイッチ機能を実現。<br>*Integrated with CMOS FET routing for RF switch.* |

---

## 🔽 BAW/FBAR (Educational Version)  

| 工程 / Step | 内容 / Description |
|-------------|--------------------|
| **Bottom Electrode** | PtまたはMo下部電極形成。<br>*Bottom electrode with Pt or Mo.* |
| **Piezo Layer** | PZTまたはAlN/HfO₂薄膜堆積。<br>*Deposition of PZT or AlN/HfO₂ thin film.* |
| **Top Electrode** | 上部電極形成。<br>*Top electrode formation.* |
| **Resonator Pattern** | フォトリソ＋エッチングで共振器定義。<br>*Lithography + etching to define resonator.* |

---

## 📝 補足 / *Notes*  

- FeVar/FeFETは **CMOS BEOL互換材料（TiN/HZO/TiN）**を採用。  
  *FeVar/FeFET use CMOS-BEOL compatible TiN/HZO/TiN stacks.*  

- BAW/FBARは **教育版モデル**として簡略化した構成を示す。  
  *BAW/FBAR shown here as simplified educational structure.*  

---

## 🔗 関連フローリンク / *Related Full Flows*  

| リンク / Link | 内容 / Description |
|---------------|--------------------|
| 📘 [0.18µm FeRAM Process Flow — 完全版](https://samizo-aitl.github.io/Edusemi-v4x/d_chapter1_memory_technologies/doc_FeRAM/feram_full_process_table.md) | 大元となるFeRAMプロセスフロー（教育モデル, 完全版）<br>*Root FeRAM process flow (educational, full version)* |
| 📘 [CMOS混載型RFデバイス提案](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/rf-devices/proposal/018um_rfcmos_rfproposal.md) | CMOS混載型RFデバイス提案<br>*Proposal: CMOS-integrated RF Devices* |

---

## 👤 **執筆者 / Author**

| 項目 / Item | 内容 / Details |
|-------------|----------------|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **GitHub** | [Samizo-AITL](https://github.com/Samizo-AITL) |
