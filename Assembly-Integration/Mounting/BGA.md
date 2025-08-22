---
layout: default
title: "BGA | ボールグリッドアレイ"
---

---

# 🟦 BGA / ボールグリッドアレイ
*Ball Grid Array (BGA)*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/BGA/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/BGA.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [BGAの種類 / Types of BGA](#-bgaの種類--types-of-bga)  
3. [特徴と利点 / Features & Advantages](#-特徴と利点--features--advantages)  
4. [課題 / Challenges](#-課題--challenges)  
5. [実装と検査 / Mounting & Inspection](#-実装と検査--mounting--inspection)  
6. [関連リンク / Related Links](#-関連リンク--related-links)  
7. [⬆️ Back to Mounting](#️-back-to-mounting)  

---

## 🏗 概要 / Overview
BGA（Ball Grid Array）は、**端子をパッケージ下面にボール状に配列**したパッケージ形態で、高I/O数・高性能デバイスに多用されます。  
*The Ball Grid Array is a package type with solder balls arranged on the underside, widely used in high I/O and high-performance devices.*  

- 高ピン数対応（数百〜数千ピン）  
- 高周波・高速信号向け  
- 放熱性能に優れる  

---

## 🧩 BGAの種類 / Types of BGA
| 種類 / Type | 構造 / Structure | 特徴 / Characteristics |
|-------------|------------------|-------------------------|
| **PBGA (Plastic BGA)** | 樹脂封止 | 低コスト、一般用途 |
| **CBGA (Ceramic BGA)** | セラミック基板 | 高信頼性、耐熱性高い |
| **FC-BGA (Flip-Chip BGA)** | ダイをフリップチップ接続 | 高速・低インダクタンス |
| **LGA (Land Grid Array)** | メタルランド接触 | リフロー不要、ソケット実装可 |
| **μBGA / WLCSP** | 微細ピッチBGA | モバイル用途、小型化特化 |

---

## ⚖️ 特徴と利点 / Features & Advantages
- **高I/O数対応**：リードフレームパッケージに比べ圧倒的に多端子  
  *Supports very high pin counts compared to leaded packages*  
- **優れた電気特性**：短配線でインダクタンス低減  
  *Reduced inductance with short interconnects*  
- **放熱性**：基板経由での放熱に有利  
  *Good thermal dissipation through PCB*  
- **小型化**：実装面積の効率化  
  *Efficient use of PCB area*  

---

## ⚠️ 課題 / Challenges
- **リフロー後のボイド・ソルダークラック**  
  *Voids and solder cracks after reflow*  
- **隠れた接合部の検査困難**（X線必須）  
  *Hidden joints require X-ray inspection*  
- **リワーク性が低い**（CSPより困難）  
  *More difficult to rework compared to CSP*  
- **熱サイクルによる疲労**  
  *Thermal cycling can cause solder fatigue*  

---

## 🛠 実装と検査 / Mounting & Inspection
- **パッド設計**：NSMD（Non-Solder Mask Defined）が主流  
  *NSMD pad design preferred for solder reliability*  
- **基板反り対策**：大サイズBGAでは基板厚・補強を検討  
  *Board warpage mitigation critical for large BGAs*  
- **リフロープロファイル**：急熱によるボイド・クラックを防ぐ  
  *Optimized reflow profile prevents defects*  
- **検査**：X線・超音波による接合部確認が必須  
  *X-ray and acoustic microscopy required for inspection*  

---

## 🔗 関連リンク / Related Links
| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📦 CSP | チップスケールパッケージ<br>*Chip Scale Package* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/CSP/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/CSP.md) |
| 🔧 SMT | 表面実装技術<br>*Surface Mount Technology* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/SMT/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Mounting/SMT.md) |

---

## ⬆️ Back to Mounting
| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Mounting 全体ページへ戻る<br>*Back to Mounting site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Mounting/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Mounting) |
