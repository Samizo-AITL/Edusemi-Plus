---
layout: default
title: "PCB Via Design | ビア設計"
---

---

# 🕳 PCB Via Design / ビア設計

---

## 📑 目次 / Table of Contents
- [🏗 概要 / Overview](#-概要--overview)
- [🎯 設計ゴール / Design Targets](#-設計ゴール--design-targets)
- [🔑 基本概念 / Fundamentals](#-基本概念--fundamentals)
- [📊 ビア構造 / Via Structures](#-ビア構造--via-structures)
- [🧮 等価回路と数式 / Equivalent Circuits & Formulas](#-等価回路と数式--equivalent-circuits--formulas)
- [🧵 スタブと対策 / Stubs & Countermeasures](#-スタブと対策--stubs--countermeasures)
- [🧪 HDI・マイクロビア設計 / HDI & Microvia Design](#-hdiマイクロビア設計--hdi--microvia-design)
- [🧩 DFM/製造公差 / DFM & Tolerances](#-dfm製造公差--dfm--tolerances)
- [✅ チェックリスト / Checklist](#-チェックリスト--checklist)
- [🧭 ドキュメント雛形 / Handoff Template](#-ドキュメント雛形--handoff-template)
- [🔗 関連リンク / Related Links](#-関連リンク--related-links)
- [⬆️ Back to PCB](#️-back-to-pcb)

---

## 🏗 概要 / Overview
ビア（Via）は基板層間の導通を担い、**SI/PI/熱/信頼性/コスト**に直結します。  
*Vias connect PCB layers, directly impacting SI, PI, thermal performance, reliability, and cost.*

ビアの形状・寸法・スタブ長は高周波信号の損失・反射・遅延に強く影響します。  
*Via geometry, dimensions, and stub length strongly affect high-frequency signal loss, reflection, and delay.*

---

## 🎯 設計ゴール / Design Targets
- **スタブ長**を最小化する（必要に応じバックドリル採用）。  
  *Minimize stub length; use backdrill if necessary.*  
- **差動ペア貫通ビア**のスタブ差を抑制。  
  *Reduce stub mismatch in differential pairs.*  
- **電源・GNDビア**は十分な本数を確保。  
  *Ensure sufficient power/ground vias.*  
- **HDI/マイクロビア**を適切に組み合わせ、高密度配線を実現。  
  *Use HDI/microvias for dense routing.*

---

## 🔑 基本概念 / Fundamentals
- **スルーホールビア（Through-hole via）**：低コストだがスタブ長が大きい。  
  *Through-hole: low cost but long stubs.*  
- **ブラインドビア（Blind via）**：片面→内層。高密度設計に有効。  
  *Blind via: surface-to-inner; effective for dense design.*  
- **ベリードビア（Buried via）**：内層間接続で表面を塞がない。  
  *Buried via: inner-to-inner; does not occupy surface space.*  
- **マイクロビア（Microvia, レーザ加工）**：HDI向け。直径 50–100 µm。  
  *Microvia: laser-drilled; diameter ~50–100 µm; HDI use.*

---

## 📊 ビア構造 / Via Structures
| 種類 / Type | 概要 / Description | 特徴 / Characteristics |
|---|---|---|
| Through-hole | 表→裏を貫通 | 低コスト、SI不利、スタブ発生 |
| Blind | 表→内層のみ | 高密度、加工追加コスト |
| Buried | 内層間接続 | 表面自由度UP、加工複雑 |
| Microvia | レーザ加工、1層深さ | HDI必須、高信頼性、歩留まり依存 |

---

## 🧮 等価回路と数式 / Equivalent Circuits & Formulas
ビアは**インダクタンス + キャパシタンス**を持つ伝送要素としてモデル化できます。  
*A via is modeled as inductance + capacitance element.*

- **ビアインダクタンス近似式**  
  $$
  L_{via} \approx 5.08 h \left[ \ln\!\left(\frac{4h}{d}\right) + 1 \right] \ [\text{nH}]
  $$
  - $h$ : ビア長 [mm] / via length  
  - $d$ : ビア径 [mm] / via diameter  

- **ビアキャパシタンス近似式**  
  $$
  C_{via} \approx 1.41 \varepsilon_r \frac{D_1 D_2}{h}
  $$
  - $D_1, D_2$ : アンチパッド径 [mm] / antipad diameters  
  - $\varepsilon_r$ : 誘電率 / dielectric constant  

これらがSIに与える影響は数百 MHz〜数 GHz で顕著です。  
*These parasitics significantly affect SI at 100s MHz–GHz.*

---

## 🧵 スタブと対策 / Stubs & Countermeasures
- **スタブ**は高周波で λ/4 共振 → リフレクション源に。  
  *Stubs resonate at λ/4, causing reflections.*  
- 対策：  
  - バックドリルで未使用部分を除去  
    *Use backdrill to remove unused portion*  
  - ビアを**キャプドビア**として処理  
    *Cap vias with resin*  
  - **ブラインド/ベリードビア**活用  
    *Use blind/buried vias*

---

## 🧪 HDI・マイクロビア設計 / HDI & Microvia Design
- **マイクロビア直列積層**（stacked microvias）：高密度・高コスト・信頼性課題。  
  *Stacked microvias: high density, costly, reliability issues.*  
- **オフセット積層（staggered）**：応力分散で信頼性向上。  
  *Staggered microvias: better stress distribution, higher reliability.*  
- **フィルド＆キャプド**：銅埋め＋平滑化で実装面のBGA対応。  
  *Filled & capped: copper-filled, planarized for BGA pads.*  

---

## 🧩 DFM/製造公差 / DFM & Tolerances
- **最小ビア径**：レーザ加工で ~75 µm、機械ドリルで ~200 µm。  
  *Min diameter: ~75 µm (laser), ~200 µm (mechanical).*  
- **アスペクト比**：$h/d \leq 10$ が一般的限界。  
  *Aspect ratio $h/d \leq 10$ is typical limit.*  
- **バックドリル精度**：残 stub 長 ±5–10% が実用範囲。  
  *Backdrill tolerance ±5–10% stub length.*  

---

## ✅ チェックリスト / Checklist
- 高速信号ビアの**スタブ長**は λ/4 以下か？  
  *Is stub length < λ/4 for high-speed nets?*  
- 差動ペアビアの**左右対称性**は確保されているか？  
  *Are differential vias symmetric?*  
- 電源・GNDビアは**十分な密度**で配置されているか？  
  *Are power/GND vias adequately distributed?*  
- HDI/マイクロビアは**信頼性検証**済みか？  
  *Are HDI/microvias validated for reliability?*  

---

## 🧭 ドキュメント雛形 / Handoff Template
| 項目 / Item | 指定 / Spec |
|---|---|
| ビア種類 / Via Type | Through / Blind / Buried / Microvia |
| ビア径 / Diameter | 0.2 mm（機械ドリル） |
| アスペクト比 / Aspect Ratio | ≤10 |
| スタブ処理 / Stub Handling | Backdrill（必要Nets） |
| ビア充填 / Filling | Resin filled（BGA領域） |
| 配置密度 / Density | GND via 1 per 3–5 mm |

---

## 🔗 関連リンク / Related Links
- [📖 Impedance Control](./impedance-control.md)  
- [📖 Simulation](./simulation.md)  
- [📖 Reliability](./reliability.md)  

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
