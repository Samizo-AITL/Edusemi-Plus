---
layout: default
title: "MLCC付録資料 | Appendix MLCC Characteristics"
---

---

# 📘 MLCC付録資料 / *Appendix: MLCC Characteristics*

---

## 📊 各分類の周波数特性 / *Impedance Characteristics by Dielectric*

各分類ごとに、インピーダンスの周波数依存性を示す。  
*Impedance vs frequency characteristics by dielectric type.*

<p align="center">
  <img src="https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/figures/mlcc_impedance_vs_frequency.png" alt="Impedance vs Frequency" width="70%">
</p>

- **C0G/NPO**  
  高安定・低損失・高周波安定  
  *High stability, low loss, suitable for RF*  

- **X7R**  
  広範囲で使用可能、SRFはMHz帯  
  *Widely used, SRF in MHz range*  

- **Y5V**  
  大容量だが温度・電圧依存が大きい  
  *High capacitance but poor stability under temp/voltage*  

---

## 📉 各分類の容量変化率 / *Capacitance Change by DC Bias*

各分類ごとに、直流バイアス印加による容量劣化を示す。  
*Capacitance degradation under DC bias by dielectric type.*

<p align="center">
  <img src="https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/figures/mlcc_capacitance_vs_bias.png" alt="Capacitance vs DC Bias" width="70%">
</p>

- **C0G/NPO**  
  容量変化ほぼゼロ  
  *Almost no capacitance change*  

- **X7R**  
  20–60%の容量減少  
  *Capacitance drops 20–60%*  

- **Y5V**  
  著しい容量減少（-80%以上）  
  *Severe drop (> -80%)*  

---

## 🧪 誘電材料と分類 / *Dielectric Materials & Classifications*

| 分類 / *Class* | 誘電材料 / *Dielectric* | 特徴 / *Characteristics* | 主な用途 / *Applications* |
|----------------|--------------------------|---------------------------|----------------------------|
| **C0G / NPO** | チタン酸カルシウム系 / *CaTiO₃-based* | 高安定・低損失・低容量<br>*High stability, low loss, low C* | RF回路、クロック、フィルタ<br>*RF, clocks, filters* |
| **X7R** | 修飾バリウムチタン酸系 / *Modified BaTiO₃* | 容量密度高い・広範囲利用<br>*High C density, general purpose* | 電源デカップリング<br>*Decoupling capacitors* |
| **X5R** | バリウムチタン酸系 / *BaTiO₃* | 小型化に適す・温度範囲狭い<br>*Compact but narrower temp range* | モバイル機器<br>*Mobile devices* |
| **Y5V** | 高誘電率型バリウムチタン酸系 / *High-k BaTiO₃* | 超大容量・不安定<br>*Very high C, poor stability* | バイパス・低周波用途<br>*Bypass, low-frequency* |

---

## 🎯 設計ガイドライン / *Design Guidelines*

- **RF用途** → C0G/NPOを選定  
  *For RF: always use C0G/NPO*  
- **電源デカップリング** → X7R/X5Rを容量帯域ごとに並列配置  
  *For decoupling: parallel X7R/X5R across capacitance bands*  
- **大容量重視** → Y5Vは注意（実効容量が大幅に低下）  
  *For bulk: Y5V requires caution due to large drop*  
- **直流バイアス** → 定格電圧の50%以下を推奨  
  *Use <50% rated voltage to ensure stability*  

---

## 📑 学習目標 / *Learning Goals*

- 各分類の **周波数特性とDCバイアス依存性** を理解する  
  *Understand frequency and DC bias dependence by dielectric class*  
- 誘電材料の違いから生じる **特性差と用途の適合性** を説明できる  
  *Explain how dielectric choice impacts performance and applications*  
- **実効容量とSRF** を考慮したボード配置設計ができる  
  *Design PCB placement considering effective C and SRF*  

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Passives全体ページへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
