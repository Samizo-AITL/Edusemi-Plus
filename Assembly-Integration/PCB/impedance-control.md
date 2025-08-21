---
layout: default
title: "PCB Impedance Control | プリント基板のインピーダンス制御"
---

---

# 📏 PCB Impedance Control / プリント基板のインピーダンス制御

---

## 🏗 概要 / Overview

高速信号伝送において、伝送線路のインピーダンス制御は必須です。  
*In high-speed signal transmission, impedance control of transmission lines is essential.*

特に差動ペア配線やクロックラインにおける特性インピーダンスは、SI（Signal Integrity）を確保するための基本設計要件です。  
*Characteristic impedance of differential pairs and clock lines is a fundamental design requirement for ensuring signal integrity (SI).*

---

## 🔑 キートピック / Key Topics

- マイクロストリップラインとストリップラインの違い  
  *Differences between microstrip and stripline*  
- 50Ω・100Ωのインピーダンス設計例  
  *Design examples for 50Ω and 100Ω impedance*  
- スタックアップ構成との依存関係  
  *Dependence on stack-up configuration*  
- シミュレーションによる事前検証  
  *Pre-verification using simulation*  

---

## 📊 計算式 / Calculation Formula

特性インピーダンスの一般式（近似式）：  
*General formula (approximation) for characteristic impedance:*  

\[
Z_0 = \frac{60}{\sqrt{\varepsilon_r}} \ln \left( \frac{8h}{w + t} \right)
\]

- \( \varepsilon_r \) : 誘電率 / Dielectric constant  
- \( h \) : 信号線とリファレンス層間距離 / Height between trace and reference plane  
- \( w \) : 配線幅 / Trace width  
- \( t \) : 配線厚み / Trace thickness  

---

## ✅ 学習目標 / Learning Goals

- 高速設計で重要なインピーダンス制御の基本を理解する。  
  *Understand the fundamentals of impedance control in high-speed design.*  
- スタックアップ・配線パラメータとの関係を把握する。  
  *Grasp the relationship with stack-up and trace parameters.*  
- シミュレーションと実測を組み合わせた設計フローを習得する。  
  *Learn a design flow combining simulation and measurement.*  

---

## 🔗 関連リンク / Related Links

- [📖 Stack-up](./stackup.md)  
- [📖 Via Design](./via-design.md)  
- [📖 Simulation](./simulation.md)  

---

## ⬆️ Back to PCB

[![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/)  
[![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB)
