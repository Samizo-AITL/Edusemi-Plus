---
layout: default
title: "SMT | 表面実装技術"
---

---

# 🔧 SMT / 表面実装技術
*Surface Mount Technology (SMT)*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/SMT/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/SMT.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [SMTプロセス / SMT Process](#-smtプロセス--smt-process)  
3. [利点と課題 / Advantages & Challenges](#-利点と課題--advantages--challenges)  
4. [主要パラメータ / Key Parameters](#-主要パラメータ--key-parameters)  
5. [信頼性と不具合 / Reliability & Failures](#-信頼性と不具合--reliability--failures)  
6. [関連リンク / Related Links](#-関連リンク--related-links)  
7. [⬆️ Back to Mounting](#️-back-to-mounting)  

---

## 🏗 概要 / Overview
SMT（Surface Mount Technology）は、電子部品を**リードを介さず直接基板表面に実装**する技術です。  
*SMT mounts components directly onto the PCB surface without through-hole leads.*  

- 高密度実装により小型・軽量化を実現  
- 自動実装機に対応し生産効率向上  
- 部品：抵抗、コンデンサ、IC、コネクタなど多様  

---

## 🔄 SMTプロセス / SMT Process
1. **はんだ印刷**：ステンシルを用いたクリームはんだ印刷  
   *Solder paste printing using stencil*  
2. **部品搭載**：チップマウンタによる高速配置  
   *Component placement via pick-and-place machines*  
3. **リフローはんだ付け**：赤外線・熱風で加熱  
   *Reflow soldering using IR or convection*  
4. **検査**：AOI（自動外観検査）、X線でBGA確認  
   *AOI inspection and X-ray for BGAs*  

---

## ⚖️ 利点と課題 / Advantages & Challenges

### ✅ 利点 / Advantages
- 小型化・高密度化  
  *Miniaturization and high-density design*  
- 自動化による低コスト化  
  *Lower cost with automation*  
- 高周波特性良好（寄生要素低減）  
  *Good high-frequency performance due to reduced parasitics*  

### ⚠️ 課題 / Challenges
- はんだ接合部の熱疲労・クラック  
  *Solder joint fatigue and cracking*  
- リワーク難易度が高い  
  *Difficult rework compared to through-hole*  
- BGAなどはX線検査必須  
  *X-ray inspection mandatory for BGAs*  

---

## 📏 主要パラメータ / Key Parameters
| パラメータ / Parameter | 意味 / Meaning |
|----------------|-------------------------------|
| パッド設計 / Pad Design | 接合信頼性・はんだ濡れ性に影響 / *Affects solderability & joint reliability* |
| はんだペースト量 / Solder Paste Volume | 過不足が不良原因に直結 / *Directly linked to defects* |
| リフロープロファイル / Reflow Profile | 熱応力・クラック防止に重要 / *Critical for thermal stress management* |
| 部品配置精度 / Placement Accuracy | 高密度基板では±25 µm以下必要 / *±25 µm accuracy needed for dense PCBs* |

---

## 🛡 信頼性と不具合 / Reliability & Failures
- **オープン不良**：はんだ不足や印刷欠け  
  *Open defects from insufficient solder*  
- **ブリッジ不良**：はんだ過多や位置ずれ  
  *Bridging defects from excess solder or misalignment*  
- **ボイド**：熱サイクルでの応力集中  
  *Voids causing stress during thermal cycling*  
- **クラック**：熱疲労や基板曲げによる割れ  
  *Cracks from thermal fatigue or board flexing*  

---

## 🔗 関連リンク / Related Links
| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📦 CSP | 小型パッケージ実装<br>*Chip Scale Package mounting* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/CSP/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/CSP.md) |
| 🟦 BGA | 多端子・高信頼パッケージ実装<br>*Ball Grid Array mounting* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/BGA/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/BGA.md) |

---

## ⬆️ Back to Mounting
| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Mounting 全体ページへ戻る<br>*Back to Mounting site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Mounting) |
