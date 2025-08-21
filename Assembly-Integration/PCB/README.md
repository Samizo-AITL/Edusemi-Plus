---
layout: default
title: "PCB | プリント基板"
---

---

# 📐 PCB / プリント基板  
*Printed Circuit Boards (PCB)*  

---

## 🔗 リンク / Links
| | |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |

---

## 📖 概要 / Overview
PCB（Printed Circuit Board）は、電子部品を実装する基板であり、**電気的接続**と**機械的支持**を同時に担います。  
*PCBs serve as the foundation for mounting semiconductors, passives, and connectors, supporting signal integrity, power delivery, and thermal management.*  

---

## 📂 ファイル一覧 / File List
| 📘 ファイル / File | 📑 内容 / Content | 🔗 リンク |
|--------------------|------------------|-----------|
| **Stack-up（層構成）** | 層構成設計、信号層・電源層の最適化。<br>*Design of PCB layer stack-ups, optimization of signal/power planes.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/stackup)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/stackup.md)</li></ul> |
| **Impedance Control（インピーダンス制御）** | 特性インピーダンスの設計と制御。<br>*Design and control of characteristic impedance in transmission lines.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/impedance-control)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/impedance-control.md)</li></ul> |
| **Via Design（ビア設計）** | スルーホール、マイクロビア、バックドリルの設計指針。<br>*Design guidelines for through-holes, microvias, and back-drills.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/via-design)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/via-design.md)</li></ul> |
| **Materials（材料）** | 基板材料（FR-4, BT, セラミック）の特性比較。<br>*Comparison of substrate materials such as FR-4, BT, and ceramics.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/materials)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/materials.md)</li></ul> |
| **Fabrication（製造プロセス）** | 製造工程：露光、エッチング、積層。<br>*Fabrication processes such as photolithography, etching, and lamination.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/fabrication)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/fabrication.md)</li></ul> |
| **Assembly（部品実装）** | SMT, THT, BGA, CSP などの実装手法。<br>*Mounting techniques such as SMT, THT, BGA, and CSP.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/assembly)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/assembly.md)</li></ul> |
| **Design Rules（設計ルール）** | トレース幅、クリアランス、ビア径、ランド設計。<br>*Trace width, clearance, via size, and pad design rules.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/design_rules)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/design_rules.md)</li></ul> |
| **Routing（配線）** | 差動配線、クロストーク対策、電源/グラウンド設計。<br>*Differential routing, crosstalk mitigation, power/ground design.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/routing)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/routing.md)</li></ul> |
| **Reliability（信頼性）** | 熱サイクル、はんだ疲労、信頼性試験。<br>*Reliability testing including thermal cycling and solder fatigue.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/reliability)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/reliability.md)</li></ul> |
| **Validation（検証）** | SI/PI/EMC/熱解析、DFMによる製造性検証。<br>*Design validation including SI/PI/EMC, thermal analysis, and manufacturability checks.* | <ul><li>[📖 Site](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/validation)</li><li>[📂 Repo](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/validation.md)</li></ul> |

---

## 📑 説明 / Description
PCBは、**信号品質（SI）**、**電源供給（PI）**、**熱設計**を支える重要要素であり、電子システム全体の信頼性・性能に直結します。  
*PCBs are critical to ensuring signal integrity, power delivery, and thermal management, directly impacting the reliability and performance of electronic systems.*  

---

## 👤 著者・ライセンス / Author & License
| 項目 / Item | 内容 / Details |
|-------------|----------------|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=flat&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=flat&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=flat&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) <br> 再配布・改変自由 / Redistribution and modification allowed |

---

## ⬆️ Back to Assembly & Integration
| | |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration) |
