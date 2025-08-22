---
layout: default
title: "EMC Analysis | EMC解析"
---

---

# 📡 EMC Analysis / EMC解析
*Electromagnetic Compatibility analysis for compliance and system reliability*

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Analysis-Validation/EMC-Analysis/) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Analysis-Validation/EMC-Analysis.md) |

---

## 📖 概要 / Overview
EMC（Electromagnetic Compatibility, 電磁両立性）は、電子機器が**不要な電磁妨害を発生せず、外部ノイズにも耐性を持つ**能力を評価する分野です。  
*EMC analysis ensures that electronic systems do not emit excessive interference and remain immune to external noise.*  

国際規格（CISPR, FCC, VCCI, IEC61000 など）への適合が求められます。  

---

## ⚡ 主な課題 / Key Issues
- **EMI（Electromagnetic Interference, 電磁妨害）**  
  *Unwanted radiation or conduction affecting other systems*  
- **EMS（Electromagnetic Susceptibility, 電磁感受性）**  
  *System’s vulnerability to external electromagnetic fields*  
- **放射エミッション / Radiated Emission**  
  *Noise radiated via PCB traces, cables, enclosures*  
- **伝導エミッション / Conducted Emission**  
  *Noise conducted through power lines and ground*  
- **ESD, EFT, Surge 耐性**  
  *Electrostatic discharge, fast transients, surge immunity*  

---

## 🧮 代表的な解析手法 / Common Analysis Methods
- **スペクトラム解析 / Spectrum Analysis**  
  EMCアンテナ・プローブで電磁放射を測定  
  *Measure radiated noise using spectrum analyzers and EMC antennas*  
- **近傍界プロービング / Near-Field Probing**  
  PCB・ケーブル周辺のノイズ源特定  
  *Identify localized EMI sources on PCB/cables*  
- **伝導ノイズ測定 / Conducted Noise Testing**  
  LISNを用いて電源ラインノイズを測定  
  *Use LISN for conducted emission measurement on power lines*  
- **シミュレーション / Simulation**  
  3D-EM解析、シグナル/パワーインテグリティ連成解析  
  *3D EM solvers and SI/PI co-simulation for EMC prediction*  

---

## 🧱 設計指針 / Design Guidelines
- **グラウンド設計 / Grounding**  
  広面積GNDプレーン、スターブリッジ接続  
  *Large ground planes, star-point connections*  
- **シールド / Shielding**  
  メタル筐体・シールドケースで電磁漏洩を抑制  
  *Metal enclosures and shielding cans to suppress radiation*  
- **フィルタ / Filtering**  
  フェライトビーズ、LCフィルタによる伝導ノイズ低減  
  *Ferrite beads and LC filters for conducted noise suppression*  
- **レイアウト / Layout**  
  差動ペアのループ面積縮小、クロストーク抑制  
  *Minimize loop area of differential pairs, reduce crosstalk*  
- **ESD保護 / ESD Protection**  
  TVSダイオード、ガードリング配置  
  *Use TVS diodes and guard rings for ESD robustness*  

---

## 📑 説明 / Description
EMC対策は**後付けでは困難**であり、設計初期から考慮することが重要です。  
PCBスタックアップ、電源分配、シールド構造、フィルタリングを含めた**システム全体設計**が必要です。  
*EMC mitigation is difficult as a retrofit; it must be addressed from early design with PCB stackup, power distribution, shielding, and filtering strategies.*  

---

## 👤 著者・ライセンス / Author & License

| 項目 / Item | 内容 / Details |
|---|---|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=for-the-badge&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=for-the-badge&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge)](LICENSE) <br> 再配布・改変自由 / Redistribution and modification allowed |

---

## ⬆️ Back to Analysis & Validation

| Link | Badge |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Analysis-Validation/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Analysis-Validation) |
