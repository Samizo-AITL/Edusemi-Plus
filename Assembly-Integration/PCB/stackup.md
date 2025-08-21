---
layout: default
title: "PCB Stack-up | プリント基板の層構成"
---

---

# 📐 PCB Stack-up / プリント基板の層構成

---

## 🏗 概要 / Overview
層構成（スタックアップ）は、SI/PI/EMC/熱/コストの“出発点”です。設計初期に確定し、全ブロックで共有すべき基本仕様になります。  
*The stack-up is the starting point for SI/PI/EMC/thermal/cost. It should be fixed early and shared across all blocks.*

適切なリファレンスプレーン近接、均衡した銅分布、材料選定により、高速化と歩留まりを同時に実現します。  
*Proper reference-plane proximity, balanced copper distribution, and material choices enable both high speed and manufacturability.*

---

## 🎯 設計ゴール / Design Targets
- 代表インピーダンス目標（例）  
  *Representative impedance targets (examples)*  
  - 単端 50 Ω（±10%） / *Single-ended 50 Ω (±10%)*  
  - 差動 100 Ω（Ethernet/HDMI 等） / *Differential 100 Ω (Ethernet/HDMI, etc.)*  
  - 差動 90 Ω（USB 2.0 HS） / *Differential 90 Ω (USB 2.0 HS)*  
  - 差動 85 Ω（PCIe 系） / *Differential 85 Ω (PCIe)*  

> プロトコル仕様が最優先です。製造公差（銅厚/樹脂収縮/エッチング）を見込んだ **設計値の微調整** を行います。  
> *Follow protocol specs first. Adjust design values accounting for fab tolerances (copper, resin, etch).*

---

## 🧱 層の役割と基本原則 / Layer Roles & Principles
- 信号層は**直下（直上）に連続プレーン**（GND優先）を持たせる。  
  *Each signal layer should have a continuous adjacent plane (prefer GND).*
- 高速差動は**サンドイッチ（Stripline）**を優先、外層は**Microstrip**用途に限定。  
  *Prefer stripline for high-speed pairs; reserve outer microstrips for less critical nets.*
- **スリット分断/プレーン分割跨ぎ**を禁止、やむを得ない場合は**スティッチングビア**でリターンを確保。  
  *Avoid crossing plane splits; use stitching vias to maintain return paths if unavoidable.*
- 銅面の**左右対称と総銅量バランス**で反り/ねじれを抑制。  
  *Maintain symmetry and copper balance to reduce warp/twist.*

---

## 📊 代表スタックアップ例 / Example Stack-ups

### 4-Layer（汎用・低中速） / *4-Layer (General/Low-Mid Speed)*
| 層 / Layer | 推奨用途 / Use | 典型構成 / Typical Build |
|---|---|---|
| L1 | Signal (Microstrip) | Cu 1 oz / Dielectric 0.18 mm to GND |
| L2 | GND Plane | Core 0.8 mm |
| L3 | PWR Plane（分割可） | Prepreg 0.18 mm |
| L4 | Signal (Microstrip) | Cu 1 oz |

### 6-Layer（高速I/O混在） / *6-Layer (Mixed High-Speed)*
| 層 | 用途 | 典型構成 |
|---|---|---|
| L1 | Signal (Microstrip, 低速/制御) | 0.12–0.18 mm→L2 |
| L2 | GND Plane | Core 0.2–0.3 mm |
| L3 | High-Speed Signal (Stripline) | 0.1–0.15 mm→L4 |
| L4 | PWR Plane（可能ならGND優先） | Core 0.2–0.3 mm |
| L5 | High-Speed Signal (Stripline) | 0.1–0.15 mm→L6 |
| L6 | GND Plane or Signal | — |

### 8-Layer（更に高密度） / *8-Layer (Higher Density)*
Signal–GND–Signal–PWR–PWR–Signal–GND–Signal  
*Center dual-PWR for PI; decouple splits properly.*

---

## 🧮 インピーダンス設計の近似式 / Impedance Quick Formulas

- **Microstrip（外層）**  
  *Microstrip (outer)*  

  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{8h}{w+t}\right)
  $$

- **Stripline（内層）**  
  *Stripline (inner)*  

  $$
  Z_0 \approx \frac{60}{\sqrt{\varepsilon_r}} \ln\!\left(\frac{4h}{0.67(\pi(w+t))}\right)
  $$

ここで $h$=誘電体厚, $w$=導体幅, $t$=銅厚, $\varepsilon_r$=比誘電率。実務ではファブの**フィールドソルバ**/スタックアップ表を基準に最終調整します。  
*Use solver/fab tables for final tuning; these are starting approximations only.*

---

## 🧪 材料・銅厚・誘電体 / Materials & Thickness
- FR-4: Dk≈4.2, Df≈0.02（汎用） / *General purpose*  
- 低損失材（Megtron/Rogers/Nelco 等）: Dk≈3.2–3.6, Df≤0.004（10 Gbps+）  
  *Low-loss materials for 10 Gbps+ links.*  
- 銅厚目安: 0.5 oz≈17 µm, 1 oz≈35 µm（高速層は**薄銅優先**）  
  *Prefer thin copper for controlled impedance/high-speed.*

---

## 🧵 ビア戦略 / Via Strategy
- スルーホールは**スタブ短縮**（必要に応じ**バックドリル**）  
  *Minimize stubs; use backdrill if needed.*  
- ブラインド/ベリード/マイクロビアで**リターン/密度/歩留まり**のバランス最適化  
  *Balance return path, density, and yield with blind/buried/microvias.*  
- 差動ペア貫通時は**ペア間スタブ差**を最小化  
  *Minimize differential stub mismatch.*

---

## 🔌 PI/EMC の要点 / PI & EMC Essentials
- **GND優先**でプレーン構成、PWRは必要域のみ分割。  
  *Prefer GND planes; split PWR only where needed.*  
- デカップリングは**MLCCをサイズ混在**（例 100 nF/1 µF/10 µF）で共振分散、**ビア直近配置**。  
  *Mix MLCC sizes to spread resonances; place near vias/pins.*  
- 外層は**リターン確保のためGNDビア・シールド**を要所に配置。  
  *Use GND stitching/shielding vias to secure return paths.*  

---

## 🧩 DFM/製造公差 / DFM & Tolerances
- エッチング・レジスト・積層の**公差表**をファブから取得し、w/h調整に反映。  
  *Obtain fab tolerance tables and adjust w/h accordingly.*  
- **銅バランス**不足は反り/ボイドの原因、パターン充填で均し。  
  *Copper imbalance causes warp/voids—use copper thieving/fill.*  
- **面付け/パネル化**と一体で議論（V-cut/ルータの影響）。  
  *Discuss panelization (V-cut/router effects) with the fab.*

---

## ✅ チェックリスト / Checklist
- すべての高速層に**連続GND近接**があるか？  
  *Does every high-speed layer have an adjacent continuous GND?*  
- 差動/単端インピーダンスは**公差込みで合格**か？  
  *Are impedances within spec including tolerances?*  
- **分割跨ぎ/リターン断絶**はないか？  
  *No plane-split crossings/return discontinuities?*  
- 熱/EMC要件に対して**材料と層数**は妥当か？  
  *Are material and layer count appropriate for thermal/EMC?*  

---

## 🧭 ドキュメント雛形 / Handoff Template
| 項目 / Item | 指定 / Spec |
|---|---|
| ボード厚 / Board Thickness | 1.6 mm（例） |
| 材料 / Material | FR-4 Tg170（例） |
| 銅厚 / Copper | 外層 1 oz / 内層 0.5 oz |
| 目標Z0 / Target Impedance | SE 50 Ω, Diff 100 Ω |
| レイヤ構成 / Layer Stack | 6L（Signal–GND–Sig–PWR–Sig–GND） |
| 最小線幅/間隔 / Min W/S | 4/4 mil（例） |
| 最小ビア / Min Via | 0.2 mm（例） |
| 特殊処理 / Special | バックドリル適用（必要Nets） |

---

## 🔗 関連リンク / Related Links
- [📖 Impedance Control](./impedance-control.md)  
- [📖 Via Design](./via-design.md)  
- [📖 Materials](./materials.md)

---

## ⬆️ Back to PCB
[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
