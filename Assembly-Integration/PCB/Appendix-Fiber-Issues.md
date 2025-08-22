---
layout: default
title: "Appendix: Fiber Issues | ガラスファイバー由来の構想不具合"
---

---

# 🧩 Appendix: Fiber Issues / ガラスファイバー由来の構想不具合

---

## 🏗 背景 / *Background*
PCB材料の多くは **ガラスファイバー布と樹脂（FR-4系など）** をベースにしており、  
その特性は電気的・機械的な信頼性に大きく影響します。  
*Most PCB materials are based on glass-fiber reinforced resin (e.g., FR-4), and the fibers affect electrical and mechanical reliability.*

---

## ⚡ CAF現象 / *Conductive Anodic Filament (CAF)*
- ガラスファイバーの毛細管経路に沿って、銅イオンがマイグレーションして導電性フィラメントを形成。  
- 高湿・高電圧環境で進行し、絶縁破壊やリークの原因となる。  
*Copper ions migrate along glass fiber bundles, forming conductive filaments under humidity and bias, leading to leakage and breakdown.*

---

## 📌 ビア配置の課題 / *Via Placement Issues*
- **異電位ビアが同一ガラス繊維を介して接触**すると、イオンマイグレーションが促進される。  
- 設計段階で **ビアをガラス繊維方向にオフセット配置**することが推奨される。  
*Misaligned vias across the same fiber can accelerate migration; offset placement is recommended.*

---

## 🛠 一般的対策 / *General Countermeasures*
- ビアのオフセット配置  
  *Offset via placement*  
- CAF耐性材料の採用（低吸湿・改良レジン系）  
  *Use CAF-resistant, low-moisture materials*  
- 基板製造時のベーキング・湿度管理  
  *Baking and humidity control during fabrication*  
- 高電圧用途では**ガラスファイバー方向の設計規則**を追加  
  *Design rules considering fiber orientation for HV PCBs*  

---

## 📚 学習の意義 / *Educational Value*
- ガラスファイバーが**信号品質・絶縁信頼性**に与える影響を理解できる  
- 材料選定とレイアウト設計の関連性を学べる  
- 実装後ではなく、**構想設計段階**での対策の重要性を把握できる  

---

## ⬆️ Back to PCB Materials
| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | PCB Materials ページへ戻る<br>*Back to PCB Materials site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/materials/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to PCB Materials repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/materials.md) |
