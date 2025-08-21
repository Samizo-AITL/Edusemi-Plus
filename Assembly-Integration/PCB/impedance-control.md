---
layout: default
title: "PCB Impedance Control | プリント基板のインピーダンス制御"
---

---

# 📏 PCB Impedance Control / プリント基板のインピーダンス制御

---

## 📑 目次 / Table of Contents
- [🏗 概要 / Overview](#-概要--overview)
- [🎯 設計ゴール / Design-Targets](#-設計ゴール--design-targets)
- [🔑 基本概念 / Fundamentals](#-基本概念--fundamentals)
- [📊 計算式 / Calculation Formulas](#-計算式--calculation-formulas)
- [🧮 差動インピーダンス / Differential Impedance](#-差動インピーダンス--differential-impedance)
- [🧪 実測とシミュレーション / Measurement & Simulation](#-実測とシミュレーション--measurement--simulation)
- [🧩 DFM/製造公差 / DFM & Tolerances](#-dfm製造公差--dfm--tolerances)
- [✅ チェックリスト / Checklist](#-チェックリスト--checklist)
- [🧭 ドキュメント雛形 / Handoff Template](#-ドキュメント雛形--handoff-template)
- [🔗 関連リンク / Related Links](#-関連リンク--related-links)
- [⬆️ Back to PCB](#️-back-to-pcb)

---

## 🏗 概要 / Overview
高速信号伝送において、伝送線路の**インピーダンス制御**は必須です。  
*In high-speed transmission, impedance control is essential for transmission lines.*

特に**クロックライン・差動ペア・高速バス**などでは、インピーダンスの乱れがリフレクション・クロストーク・ジッタの原因となります。  
*For clocks, differential pairs, and high-speed buses, impedance mismatch causes reflection, crosstalk, and jitter.*

---

## 🎯 設計ゴール / Design Targets
- 単端信号： $50\ \Omega \pm 10\%$  
  *Single-ended:  $50\ \Omega \pm 10\%$*  
- 差動信号： $100\ \Omega \pm 10\%$ （Ethernet/HDMI 等）  
  *Differential:  $100\ \Omega \pm 10\%$  (Ethernet/HDMI, etc.)*  
- USB2.0 HS:  $90\ \Omega$  
- PCIe Genx:  $85\ \Omega$  

---

## 🔑 基本概念 / Fundamentals
- **マイクロストリップ**（外層配線）：配線と空気の境界を含む → 比誘電率が低下し、Z0が上昇しやすい。  
  *Microstrip (outer layer): boundary with air lowers effective permittivity, tends to increase Z0.*
- **ストリップライン**（内層配線）：上下を誘電体に挟まれる → 均一性が高く、クロストーク抑制に有利。  
  *Stripline (inner layer): sandwiched in dielectric, better uniformity and crosstalk suppression.*
- **差動ペア**：ペア間の距離 $s$ と幅 $w$ の比 $s/w$ が支配的。  
  *Differential pairs: spacing-to-width ratio ($s/w$) dominates impedance.*

---

## 📊 計算式 / Calculation Formulas

- **Microstrip（外層）**  
  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{8h}{w+t}\right)
  $$

- **Stripline（内層）**  
  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{4h}{0.67(\pi(w+t))}\right)
  $$

ここで：  
- $h$ = 誘電体厚 / dielectric thickness  
- $w$ = 配線幅 / trace width  
- $t$ = 銅厚 / copper thickness  
- $\varepsilon_r$ = 比誘電率 / dielectric constant  

---

## 🧮 差動インピーダンス / Differential Impedance
差動ペアの特性インピーダンス $Z_{diff}$ は以下の近似式で表されます：  

$$
Z_{diff} \approx 2 Z_0 \left( 1 - k \frac{w}{s+w} \right)
$$

- $Z_0$ : 単端インピーダンス / single-ended impedance  
- $s$ : 差動ペア間隔 / pair spacing  
- $k$ : 構造依存の係数（0.48〜0.52 程度） / structure-dependent factor (~0.5)  

> 実務では **フィールドソルバ** やファブの「スタックアップ表」に基づき、配線幅・間隔を最終決定します。  
> *In practice, finalize with field solvers or fab-provided stack-up tables.*

---

## 🧪 実測とシミュレーション / Measurement & Simulation
- **TDR（Time Domain Reflectometry）**：実ボードのインピーダンスプロファイルを測定。  
  *TDR: measures impedance profile on actual boards.*  
- **2D/3D フィールドソルバ**：シミュレーションで事前に線幅・間隔を決定。  
  *2D/3D field solver: pre-determines width/spacing by simulation.*  
- **SPICE モデル**：配線を伝送線路モデル化し、SI解析に統合。  
  *SPICE modeling for SI analysis.*

---

## 🧩 DFM/製造公差 / DFM & Tolerances
- ファブの**エッチング公差**：±10% 程度 → 線幅の実効値に直結。  
  *Etching tolerance ±10%, directly impacts effective width.*  
- **積層誤差**：誘電体厚 ±10% → インピーダンス変動要因。  
  *Dielectric thickness tolerance ±10% → affects impedance.*  
- **銅厚ばらつき**：メッキ・エッチング条件に依存。  
  *Copper thickness variation by plating/etching.*

---

## ✅ チェックリスト / Checklist
- 配線幅・間隔は**fab公差込み**で規定インピーダンス内か？  
  *Are width/spacing within spec including fab tolerances?*  
- 差動ペアは**等長・等間隔**が維持されているか？  
  *Are pairs length- and spacing-matched?*  
- リターンパスは**連続プレーン**で確保されているか？  
  *Is the return path ensured with a continuous plane?*  
- 実測（TDR）が**シミュレーションと一致**しているか？  
  *Do TDR results match simulation?*  

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
- [📖 Stack-up](./stackup.md)  
- [📖 Via Design](./via-design.md)  
- [📖 Simulation](./simulation.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
