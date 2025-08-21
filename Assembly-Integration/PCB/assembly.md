---
layout: default
title: "PCB Assembly | 部品実装"
---

---

# 🛠 PCB Assembly / 部品実装

---

## 📑 目次 / Table of Contents
1. [🏗 概要 / Overview](#-概要--overview)  
2. [🔑 キートピック / Key Topics](#-キートピック--key-topics)  
3. [⚙️ 実装フロー / Assembly Flow](#️-実装フロー--assembly-flow)  
4. [🧪 はんだ付け技術 / Soldering Technologies](#-はんだ付け技術--soldering-technologies)  
5. [🩺 検査・欠陥と対策 / Inspection & Defects](#-検査欠陥と対策--inspection--defects)  
6. [✅ 学習目標 / Learning Goals](#-学習目標--learning-goals)  
7. [📚 関連資料 / References](#-関連資料--references)  
8. [🔗 関連リンク / Related Links](#-関連リンク--related-links)  
9. [⬆️ Back to PCB](#️-back-to-pcb)  

---

## 🏗 概要 / Overview
部品実装は、プリント基板 (PCB) 上に電子部品を実際に搭載・接続するプロセスです。  
*Assembly is the process of physically mounting and connecting electronic components onto a PCB.*  

この工程は、設計段階でのパッドレイアウトやDFM（Design for Manufacturability）に強く依存し、歩留まり・信頼性・熱特性に直結します。  
*It is highly dependent on pad layout and DFM considerations, directly impacting yield, reliability, and thermal performance.*  

---

## 🔑 キートピック / Key Topics
- **部品配置設計と最適化**  
  *Component placement design and optimization*  

- **表面実装技術 (SMT) とスルーホール実装 (THT)**  
  *Surface Mount Technology (SMT) and Through-Hole Technology (THT)*  

- **はんだ付けプロセス**  
  リフロー、フロー、手付け  
  *Reflow, wave, and manual soldering*  

- **フラックス・ペースト管理**  
  印刷、ディスペンス、特性評価  
  *Paste/flux application, dispensing, and characterization*  

- **実装欠陥の検出と対策**  
  ボイド、はんだ割れ、未接続、ずれなど  
  *Detection and mitigation of voids, solder cracks, opens, misalignment*  

---

## ⚙️ 実装フロー / Assembly Flow

```mermaid
flowchart TD
  A[部品供給・準備<br/>Component Preparation] --> B[印刷工程<br/>Solder Paste Printing]
  B --> C[部品実装 (Pick & Place)<br/>Placement]
  C --> D[リフロー炉<br/>Reflow Soldering]
  D --> E[フローはんだ (必要時)<br/>Wave Soldering]
  E --> F[洗浄・フラックス除去<br/>Cleaning]
  F --> G[検査 (AOI/X-ray)<br/>Inspection]
  G --> H[最終検査・信頼性試験<br/>Final QA & Reliability Tests]
```

---

## 🧪 はんだ付け技術 / Soldering Technologies
- **リフローはんだ付け**: ペーストを印刷後、温度プロファイル制御で加熱。  
  *Reflow soldering with controlled thermal profile after paste printing.*  

- **フローはんだ付け**: 主にTHT部品用。溶融はんだ槽を基板下面に接触。  
  *Wave soldering for THT parts using molten solder bath.*  

- **選択はんだ付け**: 一部エリアのみ局所的にはんだ処理。  
  *Selective soldering for localized solder joints.*  

- **はんだ合金の種類**: Sn-Pb, SAC305 (Sn-Ag-Cu), 無鉛対応。  
  *Common alloys: Sn-Pb, SAC305, lead-free types.*  

---

## 🩺 検査・欠陥と対策 / Inspection & Defects
- **自動光学検査 (AOI)**  
  *Automatic Optical Inspection*  

- **X線検査 (BGA・CSP下の接合確認)**  
  *X-ray inspection for hidden joints (BGA, CSP)*  

- **欠陥例と原因**  
  - ボイド: ペーストガス残留 / *Voids: trapped gases in paste*  
  - ブリッジ: 過多ペースト・ずれ / *Bridges: excessive paste or misalignment*  
  - クラック: 熱衝撃 / *Cracks: thermal shock*  

- **対策**  
  温度プロファイル調整、ペースト管理、DFM改善。  
  *Countermeasures include thermal profiling, paste control, and DFM improvements.*  

---

## ✅ 学習目標 / Learning Goals
- SMTとTHTの実装技術を理解する。  
  *Understand SMT and THT assembly technologies.*  

- 実装工程フローと歩留まり管理の基礎を習得する。  
  *Learn the basics of assembly flow and yield management.*  

- 実装欠陥の検出・対策方法を理解する。  
  *Understand methods for defect detection and countermeasures.*  

---

## 📚 関連資料 / References
- IPC-A-610: *Acceptability of Electronic Assemblies*  
- JIS C 5010: 電子部品の実装信頼性試験規格  
- IPC-J-STD-001: *Requirements for Soldered Electrical and Electronic Assemblies*  
- 専門書: SMT実装技術、リフロー解析論文  

---

## 🔗 関連リンク / Related Links
- [📖 Fabrication](./fabrication.md)  
- [📖 Reliability](./reliability.md)  
- [📖 Simulation](./simulation.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
