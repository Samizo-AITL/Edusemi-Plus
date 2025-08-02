# 📐 Q値と損失抵抗の数式補足  
##｜Q-Factor and Loss Resistance Formulas for Thin-Film Inductors

本資料は、薄膜インダクタの高周波特性設計におけるQ値および損失要因（直流抵抗、渦電流損失）に関する代表的な数式と設計指針を示す補足資料です。  
This document provides supplemental formulas and design guidelines related to Q-factor and loss mechanisms (DC resistance, eddy current loss) in thin-film inductor design for high-frequency applications.

---

## ✅ Q値の定義｜Definition of Q-Factor

$$
Q = \frac{\omega L}{R_{\text{total}}}
$$

- $Q$：インダクタのQ値（dimensionless, quality factor）  
- $\omega = 2\pi f$：角周波数（angular frequency, rad/s）  
- $L$：インダクタンス（inductance, H）  
- $R_{\text{total}}$：総損失抵抗（total loss resistance, Ω）

> **Q値は、蓄積エネルギーと損失エネルギーの比。Qが高いほど高効率。**  
> The Q-factor represents the ratio of energy stored to energy dissipated. Higher Q means better performance.

---

## ✅ 総損失抵抗の内訳｜Breakdown of Total Loss Resistance

$$
R_{\text{total}} = R_{\text{DC}} + R_{\text{eddy}} + R_{\text{others}}
$$

- $R_{\text{DC}}$：直流抵抗（DC resistance）  
- $R_{\text{eddy}}$：渦電流損失抵抗（eddy current loss resistance）  
- $R_{\text{others}}$：その他損失（誘電体損失、ヒステリシス等）  
  (e.g. dielectric loss, magnetic hysteresis)

---

## ✅ 直流抵抗の式｜Formula for DC Resistance

$$
R_{\text{DC}} = \frac{\rho \cdot l}{A}
$$

- $\rho$：導体材料の抵抗率（resistivity of conductor, Ω·m）  
- $l$：導体長（length of conductor, m）  
- $A$：断面積（cross-sectional area, m²）

> **Cu（銅）は低抵抗であり、低周波域ではQ値向上に有利。**  
> Copper has lower resistivity than aluminum and is favorable in lower frequency ranges.

---

## ✅ 渦電流損失の近似｜Approximation of Eddy Current Loss

$$
R_{\text{eddy}} \propto \frac{1}{\delta}
\quad , \quad
\delta = \sqrt{\frac{2\rho}{\mu \omega}}
$$

- $\delta$：スキン深さ（skin depth, m）  
- $\mu$：透磁率（magnetic permeability, H/m）  
- $\omega = 2\pi f$：角周波数（angular frequency, rad/s）

> **高周波になるほど皮膜に電流が集中（スキン効果）→ 抵抗増加**  
> At higher frequencies, the current flows near the conductor surface (skin effect), increasing effective resistance.

---

## 📊 周波数と導体材料の指針  
###｜Frequency and Conductor Material Selection Guidelines

| 周波数帯域｜Frequency Range | 推奨導体｜Recommended Material | 備考｜Notes |
|------------------------------|-------------------------------|-------------------------------------------|
| ～500 kHz                   | **Cu（銅 / Copper）**           | 低抵抗により直流損失を低減。Low DC loss.  |
| 1 MHz以上                  | **Al（アルミ / Aluminum）**     | スキン効果による渦電流損失が小。Reduced eddy current loss. |

> **材料選定は抵抗率とスキン効果の両立を考慮。**  
> Material selection should balance resistivity and skin effect behavior.

---

## 🔗 関連図（予定）｜Planned Visuals

- Q値 vs 周波数｜Q-factor vs Frequency  
- スキン深さ vs 周波数｜Skin Depth vs Frequency  
- 導体断面の電流分布（低周波／高周波）  
  Current distribution in conductor cross-section (low vs high frequency)

---

## 🧭 関連資料｜Related Material

📘 [Phase 0 薄膜インダクタ研究（1996–1997）](../d_chapter1_memory_technologies/thin_film_inductor_1996.md)  
📘 [5a.5 インダクタのQ値設計｜AMS教材リンク](../d_chapter5a_analog_mixed_signal/5_inductor_q_factor.md)

---
