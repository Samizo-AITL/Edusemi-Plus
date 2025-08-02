---
layout: default
title: Q-Factor and Loss Resistance Formulas
---

<!-- ✅ MathJax support for both block & inline math -->
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']]
    }
  };
</script>
<script type="text/javascript"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

# 📐 Q値と損失抵抗の数式補足  
##｜Q-Factor and Loss Resistance Formulas for Thin-Film Inductors

本資料は、薄膜インダクタの高周波特性設計におけるQ値および主な損失要因（直流抵抗、渦電流損失）に関する代表的な数式と設計指針を示す補足資料です。  
This document provides supplemental formulas and design guidelines related to the Q-factor and major loss mechanisms (DC resistance, eddy current loss) in thin-film inductor design for high-frequency applications.

---

## ✅ Q値の定義｜Definition of Q-Factor

$$
Q = \frac{\omega L}{R_{\text{total}}}
$$

- \( Q \)：Q値（無次元, quality factor）  
- \( \omega = 2\pi f \)：角周波数（angular frequency, rad/s）  
- \( L \)：インダクタンス（inductance, H）  
- \( R_{\text{total}} \)：総損失抵抗（total loss resistance, Ω）

> **Q値は蓄積エネルギーと損失エネルギーの比を示し、値が高いほど高効率。**  
> The Q-factor represents the ratio of stored to dissipated energy. Higher Q means better efficiency.

---

## ✅ 総損失抵抗の構成｜Components of Total Loss Resistance

$$
R_{\text{total}} = R_{\text{DC}} + R_{\text{eddy}} + R_{\text{others}}
$$

- \( R_{\text{DC}} \)：直流抵抗（DC resistance）  
- \( R_{\text{eddy}} \)：渦電流損失抵抗（eddy current loss resistance）  
- \( R_{\text{others}} \)：その他損失（誘電体損失、磁気ヒステリシスなど）  
  (e.g., dielectric loss, magnetic hysteresis)

---

## ✅ 直流抵抗の式｜Formula for DC Resistance

$$
R_{\text{DC}} = \frac{\rho \cdot l}{A}
$$

- \( \rho \)：導体材料の抵抗率（resistivity, Ω·m）  
- \( l \)：導体長（conductor length, m）  
- \( A \)：断面積（cross-sectional area, m²）

> **低周波域ではCu（銅）の低抵抗性がQ値の向上に寄与。**  
> Copper's low resistivity improves Q-factor in lower frequency ranges.

---

## ✅ 渦電流損失の近似｜Approximation of Eddy Current Loss

$$
R_{\text{eddy}} \propto \frac{1}{\delta}, \quad
\delta = \sqrt{\frac{2\rho}{\mu \omega}}
$$

- \( \delta \)：スキン深さ（skin depth, m）  
- \( \mu \)：透磁率（magnetic permeability, H/m）  
- \( \omega = 2\pi f \)：角周波数（angular frequency, rad/s）

> **高周波ではスキン効果により導通面積が減少し、実効抵抗が増加。**  
> At high frequencies, current flows near the surface (skin effect), increasing effective resistance.

---

## 📊 周波数と導体材料の指針  
###｜Frequency and Conductor Material Selection Guidelines

| 周波数帯域｜Frequency Range | 推奨導体｜Recommended Material | 備考｜Remarks |
|------------------------------|-------------------------------|---------------------------------------------------|
| ～500 kHz                   | **Cu（銅 / Copper）**           | 低抵抗による直流損失低減｜Low DC resistance |
| 1 MHz以上                  | **Al（アルミ / Aluminum）**     | スキン効果に強く高周波損失が小さい｜Lower eddy current loss |

> **材料選定は抵抗率と高周波損失のバランスが重要。**  
> Material selection should consider both resistivity and high-frequency behavior.

---

## 🔗 関連図（予定）｜Planned Visuals

- Q値 vs 周波数｜Q-Factor vs Frequency  
- スキン深さ vs 周波数｜Skin Depth vs Frequency  
- 導体断面の電流分布（低周波／高周波）｜Current distribution in cross-section (LF/HF)

---
