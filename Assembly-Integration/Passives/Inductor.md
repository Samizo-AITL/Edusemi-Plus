---
layout: default
title: "Inductor | インダクタ"
---

---

# 🌀 Inductor / インダクタ

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Inductor/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Inductor.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [用途 / Applications](#-用途--applications)  
3. [種類 / Types](#-種類--types)  
4. [特性パラメータ / Key Parameters](#-特性パラメータ--key-parameters)  
5. [材料と構造 / Materials & Structures](#-材料と構造--materials--structures)  
6. [信頼性と実装 / Reliability & Mounting](#-信頼性と実装--reliability--mounting)  
7. [設計指針 / Design Guidelines](#-設計指針--design-guidelines)  
8. [関連リンク / Related Links](#-関連リンク--related-links)  
9. [⬆️ Back to Passives](#️-back-to-passives)  

---

## 🏗 概要 / Overview
インダクタは電流変化に対して逆起電力を発生させる受動部品で、**エネルギー蓄積・フィルタリング・インピーダンス変換**に用いられます。  
*Inductors generate counter electromotive force against current variation, used for energy storage, filtering, and impedance transformation.*  

---

## 🎯 用途 / Applications
- **電源回路**: DC-DC コンバータのエネルギー蓄積  
  *Energy storage in DC-DC converters*  
- **フィルタ**: LC フィルタ、EMI/RFI フィルタ  
  *LC filters, EMI/RFI suppression*  
- **RF 回路**: インピーダンス整合、チューニング回路  
  *Impedance matching and tuning in RF circuits*  
- **エネルギー変換**: モータドライブ、無線給電  
  *Motor drive and wireless power transfer*  

---

## 🧩 種類 / Types
| 種類 / Type | 構造 / Structure | 特徴 / Characteristics |
|-------------|------------------|-------------------------|
| **ワイヤ巻線型 / Wire-wound** | 導線をコアに巻線<br>*Winding conductor on a magnetic core* | 高Q、高電流対応、サイズ大<br>*High Q, supports large current, relatively large size* |
| **積層セラミック型 / Multilayer** | セラミック基板に印刷導体<br>*Printed conductor layers in ceramic substrate* | 小型、量産安定、Q値低め<br>*Compact, stable in mass production, lower Q value* |
| **チップフェライトビーズ / Ferrite Beads** | フェライトを通す導体<br>*Conductor passing through ferrite material* | ノイズ吸収、広帯域損失<br>*Noise absorption, broadband loss characteristics* |
| **空芯コイル / Air-core** | コアなし巻線<br>*Winding without magnetic core* | 高周波向け、損失低い、インダクタンス小<br>*Suitable for high frequency, low loss, small inductance* |
| **トロイダルコイル / Toroidal** | 環状コアに巻線<br>*Winding on a toroidal (ring-shaped) core* | 磁束漏れ少、効率高<br>*Low flux leakage, high efficiency* |

---

## 📊 特性パラメータ / Key Parameters
- **インダクタンス L [H]**: 磁束結合能力  
  *Ability to store magnetic flux*  
- **直流抵抗 DCR [Ω]**: 導体抵抗、損失要因  
  *Conductor resistance, main loss factor*  
- **定格電流 [A]**: 飽和電流、許容電流  
  *Saturation current and allowable current*  
- **Q値 (品質係数)**: エネルギー損失の少なさ  
  *Quality factor, indicates low energy loss*  
- **自己共振周波数 (SRF)**: インダクタとして動作する限界周波数  
  *Frequency limit where inductor behaves as pure inductance*  
- **温度係数**: 材料依存の特性変動  
  *Temperature dependence of inductance based on material*  

---

## 🧱 材料と構造 / Materials & Structures
- **磁性体コア / Magnetic Core**: フェライト（Mn-Zn, Ni-Zn）、鉄粉コア  
  *Ferrite (Mn-Zn, Ni-Zn), powdered iron cores*  
- **樹脂モールド / Resin Molded**: パワーインダクタ用、機械強度・放熱性向上  
  *For power inductors, enhances mechanical strength and thermal dissipation*  
- **セラミック / Ceramic**: 高周波対応、安定した特性  
  *For high-frequency applications, stable characteristics*  
- **空芯 / Air-core**: RF、GHz帯で利用  
  *Used for RF and GHz range applications*  

---

## 🛡 信頼性と実装 / Reliability & Mounting
- **熱設計 / Thermal Design**: コア飽和と温度上昇を考慮  
  *Consider core saturation and temperature rise*  
- **機械強度 / Mechanical Strength**: BGA/LGA基板への実装時はリフロー耐性必須  
  *Reflow soldering tolerance required for BGA/LGA mounting*  
- **経年劣化 / Aging**: 磁性体の特性変動、絶縁劣化  
  *Variation of magnetic properties, insulation degradation over time*  
- **実装 / Mounting**: SMT対応チップ型が主流、大型はスルーホールも残存  
  *SMT chip inductors are mainstream; large ones still use through-hole*  

---

## 📝 設計指針 / Design Guidelines
- 高速DC-DCでは **低DCR・高飽和電流**品を選定  
  *Choose inductors with low DCR and high saturation current for high-speed DC-DC converters*  
- EMI対策では **フェライトビーズ**をノイズ源ごとに配置  
  *Place ferrite beads at each noise source for EMI suppression*  
- RF用途では **空芯・高Qインダクタ**を利用  
  *Use air-core or high-Q inductors for RF applications*  
- インダクタンス値は **シミュレーションと実測**で最終確認  
  *Always verify inductance value through both simulation and measurement*  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📘 Resistors | 抵抗器の種類と特性<br>*Types and characteristics of resistors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Resistors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Resistors.md) |
| ⚡ Capacitors | アルミ/タンタル/フィルム<br>*Aluminum/Tantalum/Film capacitors* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Capacitors/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Capacitors.md) |
| 🛠 Passive Design | 受動部品設計ガイドライン<br>*Design guidelines for passive components* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/Passive-Design/)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Passives/Passive-Design.md) |

---

## ⬆️ Back to Passives

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | 受動部品カテゴリトップへ戻る<br>*Back to Passives site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Passives/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to Passives repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Passives) |
