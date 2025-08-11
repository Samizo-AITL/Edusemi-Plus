---
layout: default
title: Thin-Film Inductor Development (1996–1997)
---

---

# 🧪 Thin-Film Inductor Development (1996–1997)

---

## 【Phase 0：研究初期（〜1997）】  
🧪 **FEM解析による薄膜インダクタ構造設計と高周波DCDCコンバータ向けリアクトル最適化**

- 信州大学にて、**スイッチング電源用DCDCコンバータ向けの薄膜インダクタ**に関する基礎研究を実施。
- 当時は、**携帯電話や携帯情報端末の本格的普及を見据え、小型・高効率な電源回路**のニーズが急速に高まっており、とくに**12V→5V変換を行う降圧型DCDCコンバータ**への実装を想定した**オンチップリアクトルの開発**が技術課題となっていた。
- 本研究では、**フェライト系磁性膜とAlスパイラルコイル**を積層した構造を設計し、**有限要素法（FEM）による電磁界解析**を用いてインダクタの動作特性（インダクタンス、Q値）を評価。
- 駆動周波数500kHz〜1MHzの範囲で、**Q値の低下要因は配線導体内の直流抵抗と高周波渦電流損失の重畳である**ことを示した。
- この結果に基づき、**周波数依存での導体材料選択指針（Al / Cu）**を提案：
  - **低周波（〜数百kHz）では低抵抗のCu**を使用、
  - **高周波（〜MHz）ではAl**を用いることで渦電流損失を低減。
- 本研究成果は、**電気学会 MAG研究会（1997年）にて発表**  
  （CiNii CRID: 15714171125436978432、共著：池田慎治、佐藤篤郎、山沢清人）

---

## 🧩 関連技術補足：半導体RFインダクタとの共通課題

- **半導体集積回路でも、RF回路向けにオンチップ・インダクタが金属配線構造で実装**されている。
- この際のQ値劣化要因として、**シリコン基板内での渦電流損失**が支配的となる。
- これを抑制するため、**高抵抗シリコン基板（High-Resistivity Si：例 10〜100Ω・cm）**の採用が行われている：
  - **P型基板で10Ω・cm程度までは標準プロセス互換**、
  - **100Ω・cm以上はPN接合の反転・リークリスクがあるため設計上の制約が存在**。
- 本研究の**磁性膜／導体構造における渦電流制御**と同様、**材料選択および基板設計により高周波損失を最小化するアプローチ**は、今日のRF集積設計にも通じる普遍的な設計指針となっている。

---

## 🧭 English Summary

**Thin-Film Inductor Design and Q-Factor Optimization for DCDC Converters Using FEM Analysis (1996–1997)**

- Conducted foundational research at **Shinshu University** on thin-film inductors for **switching regulator (DCDC converter)** applications.
- This study assumed use in **buck-type DCDC converters for 12V to 5V power conversion**, which were increasingly in demand for future **portable electronics such as mobile phones**.
- Designed laminated structures consisting of **ferrite-based magnetic films** and **aluminum spiral coil conductors**, and used **finite element method (FEM) electromagnetic simulation** to analyze inductance and Q-factor behavior.
- Demonstrated that **Q-value degradation at 500 kHz–1 MHz** arises from the **superposition of DC resistance and eddy current losses within the conductor**.
- Based on these findings, proposed a **frequency-dependent guideline for conductor material selection (Al or Cu)**:
  - **Cu for lower frequencies (~hundreds of kHz)** due to lower resistivity,  
  - **Al for higher frequencies (~MHz)** due to reduced eddy current losses and skin effect.
- Results presented at the **IEEJ Magnetics Technical Meeting (1997)**  
  (CiNii CRID: 15714171125436978432, co-authors: Shinji Ikeda, Atsuro Sato, Kiyoto Yamazawa)

---

## 🧩 Related Insight: On-Chip Inductors in Semiconductor RF Design

- In **semiconductor RF circuits**, on-chip inductors are fabricated using **metal interconnect structures**, often implemented in top-level metal layers.
- **Q-factor degradation** in these cases is also attributed to **eddy current losses within the low-resistivity silicon substrate**.
- To suppress such losses, **high-resistivity silicon substrates (10–100 Ω·cm)** are adopted:
  - ~10 Ω·cm is compatible with standard P-type CMOS processes,
  - Beyond 100 Ω·cm, **PN junction inversion and leakage risks increase**, limiting further resistivity scaling.
- The **principles of minimizing eddy current loss by material and structural optimization**, as explored in the thin-film reactor study, directly correlate with **modern RF SoC inductor design strategies**.

---

### 📐 補足資料リンク｜Reference Material

薄膜インダクタにおけるQ値と損失要因（直流抵抗・渦電流損失など）の数式表現については、以下の補足資料をご参照ください。  
For detailed formulas related to the Q-factor and associated loss mechanisms (DC resistance, eddy current loss) in thin-film inductors, please refer to the following supplemental document.

📘 [Q値と損失抵抗の数式補足｜Q-Factor and Loss Resistance Formulas](./inductor_q_formula.md)

### 🔗 関連リンク｜Related Link

本研究と関連する**オンチップインダクタのQ値設計技術**について、AMS設計指針として以下の教材にまとめています。

This research is closely related to the design of **on-chip inductor Q-factor optimization**.  
The following resource provides practical AMS design guidelines.

📘 [5a.5 インダクタのQ値改善と配線・基板設計｜Improving Inductor Q-Factor via Wiring and Substrate Design](http://samizo-aitl.github.io/Edusemi-v4x/d_chapter5a_analog_mixed_signal/5_inductor_q_factor.md)  
（オンチップインダクタのQ向上技術：金属・基板・パターン設計とその応用）  
(Practical techniques for improving Q: metal stack, substrate isolation, and layout optimization)

---

<!-- Optionally, insert a future image or graph -->
<!-- ![Thin-Film Inductor Structure](./images/thin_film_inductor_structure.png) -->
<!-- ※ Q値 vs 周波数グラフの追加予定 -->
