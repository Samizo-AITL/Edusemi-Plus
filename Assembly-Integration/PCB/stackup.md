---
layout: default
title: "PCB Stack-up | プリント基板の層構成"
---

---

# 📐 PCB Stack-up / プリント基板の層構成

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/stackup) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/PCB/stackup.md) |

---

## 🏗 概要 / Overview
層構成（スタックアップ）は、SI/PI/EMC/熱/コストの“出発点”です。設計初期に確定し、全ブロックで共有すべき基本仕様になります。  
*The stack-up is the starting point for SI/PI/EMC/thermal/cost. It should be fixed early and shared across all blocks.*

適切なリファレンスプレーン近接、均衡した銅分布、材料選定により、高速化と歩留まりを同時に実現します。  
*Proper reference-plane proximity, balanced copper distribution, and material choices enable both high speed and manufacturability.*

---

## 🎯 設計ゴール / Design Targets

| 種類 / Type | 代表値 / Target | 用途 / Use |
|---|---|---|
| 単端 / Single-ended | 50 Ω (±10%) | 一般高速信号 |
| 差動 / Differential | 100 Ω | Ethernet / HDMI |
| 差動 / Differential | 90 Ω | USB 2.0 HS |
| 差動 / Differential | 85 Ω | PCIe |

> プロトコル仕様が最優先。製造公差を見込んで設計値を微調整。  
> *Follow protocol specs first, then adjust for fab tolerances.*

---

## 📊 代表スタックアップ例 / Example Stack-ups

### 4-Layer
| Layer | Use | Typical Build |
|---|---|---|
| L1 | Signal (Microstrip) | Cu 1 oz / 0.18 mm to GND |
| L2 | GND Plane | Core 0.8 mm |
| L3 | PWR Plane | Prepreg 0.18 mm |
| L4 | Signal (Microstrip) | Cu 1 oz |

### 6-Layer
| Layer | Use | Typical Build |
|---|---|---|
| L1 | Signal (Microstrip, 低速) | 0.12–0.18 mm → L2 |
| L2 | GND Plane | Core 0.2–0.3 mm |
| L3 | High-Speed Signal (Stripline) | 0.1–0.15 mm → L4 |
| L4 | PWR Plane (or GND) | Core 0.2–0.3 mm |
| L5 | High-Speed Signal (Stripline) | 0.1–0.15 mm → L6 |
| L6 | GND Plane or Signal | — |

### 8-Layer
Signal – GND – Signal – PWR – PWR – Signal – GND – Signal

---

## 🧮 インピーダンス設計の近似式 / Impedance Quick Formulas

- **Microstrip（外層）**  
  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{8h}{w+t}\right)
  $$

- **Stripline（内層）**  
  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{4h}{0.67\pi(w+t)}\right)
  $$

> $h$=誘電体厚, $w$=導体幅, $t$=銅厚, $\varepsilon_r$=比誘電率

---

## 🧪 材料・銅厚・誘電体 / Materials & Thickness

| 材料 / Material | Dk | Df | 用途 / Use |
|---|---|---|---|
| FR-4 | ≈4.2 | ≈0.02 | 汎用 |
| Megtron / Rogers / Nelco | 3.2–3.6 | ≤0.004 | 10 Gbps+ |

銅厚: 0.5 oz ≈ 17 µm, 1 oz ≈ 35 µm（高速層は薄銅優先）

---

## 🧵 ビア戦略 / Via Strategy
- スルーホールはスタブ短縮（バックドリル推奨）  
- ブラインド/ベリード/マイクロビアの最適化  
- 差動ペア通過時はスタブ差を最小化  

---

## 🔌 PI/EMC Essentials
- GND優先でプレーン構成  
- デカップリングは MLCC サイズ混在で共振分散  
- 外層にGNDスティッチング配置  

---

## 🧩 DFM & Tolerances
- ファブの公差表を反映  
- 銅バランス確保で反り防止  
- 面付け/パネル化と一体で検討  

---

## ✅ チェックリスト / Checklist
- 各高速層に連続GND近接があるか？  
- インピーダンスは公差込みで合格か？  
- プレーン分割跨ぎはないか？  
- 熱/EMC要件に層数・材料は妥当か？  

---

## 🧭 ドキュメント雛形 / Handoff Template

| Item | Spec (例) |
|---|---|
| Board Thickness | 1.6 mm |
| Material | FR-4 Tg170 |
| Copper | Outer 1 oz / Inner 0.5 oz |
| Target Impedance | SE 50 Ω, Diff 100 Ω |
| Layer Stack | 6L (Sig–GND–Sig–PWR–Sig–GND) |
| Min W/S | 4/4 mil |
| Min Via | 0.2 mm |
| Special | Backdrill (必要Nets) |

---

## 🔗 関連リンク / Related Links
| Link | Badge |
|---|---|
| 📖 Impedance Control | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./impedance-control.md) |
| 📖 Via Design | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./via-design.md) |
| 📖 Materials | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?logo=githubpages)](./materials.md) |

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
