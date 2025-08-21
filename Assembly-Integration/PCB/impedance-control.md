---
layout: default
title: "PCB Impedance Control | プリント基板のインピーダンス制御"
---

---

# 📏 PCB Impedance Control / プリント基板のインピーダンス制御

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/impedance-control) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/impedance-control.md) |

---

## 📑 目次 / Table of Contents
- [🏗 概要 / Overview](#-概要--overview)
- [🎯 設計ゴール / Design-Targets](#-設計ゴール--design-targets)
- [🔑 基本概念 / Fundamentals](#-基本概念--fundamentals)
- [📊 計算式 / Calculation-Formulas](#-計算式--calculation-formulas)
- [🧮 差動インピーダンス / Differential-Impedance](#-差動インピーダンス--differential-impedance)
- [🧪 実測とシミュレーション / Measurement--Simulation](#-実測とシミュレーション--measurement--simulation)
- [🧩 DFM/製造公差 / DFM--Tolerances](#-dfm製造公差--dfm--tolerances)
- [✅ チェックリスト / Checklist](#-チェックリスト--checklist)
- [🧭 ドキュメント雛形 / Handoff-Template](#-ドキュメント雛形--handoff-template)
- [🔗 関連リンク / Related-Links](#-関連リンク--related-links)
- [⬆️ Back to PCB](#️-back-to-pcb)

---

## 🏗 概要 / Overview
高速信号伝送において、伝送線路の**インピーダンス制御**は必須です。  
*In high-speed transmission, impedance control for transmission lines is essential.*

特に**クロック・差動ペア・高速バス**では、インピーダンス乱れが反射・クロストーク・ジッタの主因になります。  
*For clocks, differential pairs, and high-speed buses, mismatch drives reflection, crosstalk, and jitter.*

---

## 🎯 設計ゴール / Design Targets

| 種類 / Type | 代表値 / Target | 用途 / Use |
|---|---|---|
| 単端 / Single-ended | 50 Ω (±10%) | 汎用高速信号 |
| 差動 / Differential | 100 Ω | Ethernet / HDMI |
| 差動 / Differential | 90 Ω | USB 2.0 HS |
| 差動 / Differential | 85 Ω | PCIe |

> プロトコル仕様を最優先し、**銅厚・誘電体・エッチング**などの製造公差を見込んで線幅/間隔を微調整します。  
> *Follow protocol specs first; tune width/spacing with fab tolerances (copper, dielectric, etch).*

---

## 🔑 基本概念 / Fundamentals
- **マイクロストリップ（外層）**：空気境界の影響で実効比誘電率が下がり、Z0は高めに出やすい。  
  *Microstrip (outer): air boundary lowers effective εr → higher Z0 tendency.*
- **ストリップライン（内層）**：誘電体にサンドイッチされ均一性が高く、クロストーク抑制に有利。  
  *Stripline (inner): sandwiched in dielectric → better uniformity and lower crosstalk.*
- **差動ペア**：ペア間隔 $s$ と線幅 $w$ の比 $s/w$ が支配的。  
  *Differential pairs: spacing-to-width ratio $s/w$ dominates behavior.*

---

## 📊 計算式 / Calculation Formulas

- **Microstrip（外層）**

$$
Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{8h}{w+t}\right)
$$

- **Stripline（内層）**

$$
Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{4h}{0.67\pi(w+t)}\right)
$$

ここで：$h$=誘電体厚, $w$=線幅, $t$=銅厚, $\varepsilon_r$=比誘電率。  
*Where $h$=dielectric thickness, $w$=trace width, $t$=copper thickness, $\varepsilon_r$=relative permittivity.*

---

## 🧮 差動インピーダンス / Differential Impedance

$$
Z_{diff} \approx 2 Z_0 \!\left( 1 - k \frac{w}{s+w} \right)
$$

- $Z_0$: 単端インピーダンス / single-ended impedance  
- $s$: ペア間隔 / pair spacing  
- $k$: 構造依存係数（目安 0.48–0.52） / structure factor (~0.5)

> 実務では**2D/3D フィールドソルバ**やファブの**スタックアップ表**を基準に最終決定します。  
> *Finalize geometry with a field solver or the fab’s stack-up tables.*

---

## 🧪 実測とシミュレーション / Measurement & Simulation
- **TDR**：実ボードでインピーダンスプロファイルを実測。  
  *Time-Domain Reflectometry on actual boards.*
- **Field Solver**：線幅・間隔・層間距離を事前同定。  
  *Use a field solver to pre-determine width/spacing/heights.*
- **SPICE/IBIS-AMI**：反射・減衰・ジッタを系統評価。  
  *Model reflections/attenuation/jitter in SI analysis.*

---

## 🧩 DFM/製造公差 / DFM & Tolerances
- **エッチング公差**：線幅 ±10% 程度 → 実効Z0に直結。  
- **誘電体厚公差**：±10% 程度 → Z0・Zdiff の主要変動源。  
- **銅厚バラつき**：メッキ条件に依存 → 仕上がり線幅/表面粗さにも影響。  
*Etch, dielectric, and copper tolerances each shift impedance; account for them up front.*

---

## ✅ チェックリスト / Checklist
- 設計した線幅/間隔は**公差込み**で規定Z0/Zdiff内？  
- 差動は**等長・等間隔**・**ビア通過数の均等**を満たす？  
- リターンは**連続GNDプレーン**で確保？（分割跨ぎなし）  
- **TDR実測**はシミュレーション結果と整合？  

---

## 🧭 ドキュメント雛形 / Handoff Template

| 項目 / Item | 指定 / Spec |
|---|---|
| ターゲットZ0 / Target Z0 | SE 50 Ω, Diff 100 Ω |
| レイヤ / Layer | L3 Stripline, L5 Stripline |
| 誘電率 / Dielectric | 3.8（FR-4） |
| 配線幅 / Trace Width | 4 mil |
| 配線間隔 / Spacing | 6 mil（Diff Pair） |
| 銅厚 / Copper Thickness | 0.5 oz |
| 公差 / Tolerance | ±10% |

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 📐 Stack-up | 層構成の役割と代表例<br>*Layer stack-up roles & examples* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./stackup.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/stackup) |
| 🕳 Via Design | スルーホール/マイクロビア/バックドリル設計<br>*Through/microvia/backdrill design* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./via-design.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/via-design) |
| 🧪 Materials | FR-4/低損失材の特性比較<br>*FR-4 vs low-loss materials* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](./materials.md)<br>[![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](../PCB/materials) |

---

## ⬆️ Back to PCB

| Link | Badge |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |
