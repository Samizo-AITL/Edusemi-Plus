---
layout: default
title: 2. 材料特性の定量比較｜Quantitative Comparison of Si / SiC / GaN / Diamond
---

---

# 📊 2. 材料特性の定量比較｜Quantitative Comparison of Si / SiC / GaN / Diamond

本節では、主要半導体材料 **(Si, SiC, GaN, Diamond)** の**物理特性を定量的に比較**し、  
それぞれの **「強み」** と **「制約」** を明確化します。  
In this section, we **quantitatively compare** the physical properties of **Si, SiC, GaN, and Diamond**,  
clarifying each material’s **strengths** and **limitations**.

---

## 📌 比較視点｜Key Comparison Metrics

| **項目 / Parameter** | **意味 / Meaning** | **重要性 / Importance** |
|----------------------|--------------------|--------------------------|
| **バンドギャップ (Eg)** | 電流を流すために必要な最小エネルギー差 / Minimum energy gap for conduction | 高温特性・耐圧に影響 / Affects high-temp tolerance & breakdown voltage |
| **飽和ドリフト速度 / Saturation Drift Velocity** | 電界印加時のキャリア速度限界 / Max carrier velocity under field | スイッチング速度に影響 / Impacts switching speed |
| **電子移動度 / Electron Mobility** | 電界に対する電子の動きやすさ / Ease of electron movement | 抵抗・高速性に関与 / Relates to resistance & speed |
| **熱伝導率 / Thermal Conductivity** | 発熱を外部へ逃がす能力 / Ability to dissipate heat | パッケージ・冷却設計に関与 / Critical for cooling & packaging |
| **絶縁破壊電界 / Breakdown Field** | 絶縁破壊が起きる限界電界 / Max field before breakdown | 耐圧・小型化に直結 / Directly impacts breakdown voltage & scaling |
| **臨界オン抵抗 / Critical On-Resistance** | 高耐圧FETでの理論的最小オン抵抗 / Theoretical min. on-resistance | 効率・発熱に直結 / Determines efficiency & heat loss |

---

## 📊 主要材料の物性一覧｜Representative Material Properties

| **材料 / Material** | **Eg (eV)** | **電子移動度 / Mobility (cm²/V·s)** | **熱伝導率 / Thermal Conductivity (W/m·K)** | **絶縁破壊電界 / Breakdown Field (MV/cm)** | **臨界オン抵抗 (相対) / Critical R<sub>on</sub> (Rel.)** |
|---------------------|------------|--------------------------------------|---------------------------------------------|----------------------------------------------|----------------------------------------------|
| **Si**              | 1.1  | 1,500  | 150   | 0.3   | 1.0（基準 / Reference） |
| **SiC**             | 3.3  | 900    | 490   | 3.0   | 約1/300 |
| **GaN**             | 3.4  | 2,000  | 130   | 3.3   | 約1/400 |
| **Diamond**         | 5.5  | 2,200  | 2,000 | 10.0+ | 約1/5000 |

💡 **臨界オン抵抗は、同じ耐圧で必要とされる理論的オン抵抗の指標（Siを1とした相対値）**  
💡 **Critical R<sub>on</sub> is the theoretical min. on-resistance for the same breakdown voltage, normalized to Si = 1**

---

## 📊 グラフ化例 | Example Graphs

<!-- Eg vs Mobility -->
<figure>
  <img src="./images/eg_vs_mobility_improved.png" alt="Eg vs Mobility for Si / SiC / GaN / Diamond" width="80%">
  <figcaption>
    **Eg と移動度の関係**：WBG材料は一般に Eg が大きい一方、GaN・Diamond は高い移動度を維持します。SiC は高耐圧寄りで移動度は低め。→ **高周波・高速**は GaN/Diamond、**集積・汎用**は Si が得意。  
    *Relation between Eg and mobility: While WBG materials have larger bandgaps, GaN and diamond keep high mobility. SiC is more HV-oriented with lower mobility. ⇒ GaN/diamond suit high-frequency/high-speed, Si suits general-purpose integration.*
  </figcaption>
</figure>

<!-- Breakdown Field vs Thermal Conductivity -->
<figure>
  <img src="./images/breakdown_vs_thermal_improved.png" alt="Breakdown Field vs Thermal Conductivity" width="80%">
  <figcaption>
    **絶縁破壊電界 × 熱伝導率**：SiC は両方が高く、**高耐圧・高信頼の電力用途**に最適。GaN は電界は高いが熱伝導が低めのため、**基板・放熱設計**が重要（GaN on SiC など）。Diamond は理論的に突出。  
    *Breakdown field vs thermal conductivity: SiC scores high on both → ideal for high-voltage/reliability power. GaN has high field but lower thermal conductivity → thermal management matters (e.g., GaN on SiC). Diamond is outstanding in theory.*
  </figcaption>
</figure>

<!-- Critical Ron vs Breakdown Field (log scale) -->
<figure>
  <img src="./images/criticalRon_vs_breakdown_improved.png" alt="Critical Ron vs Breakdown Field (log scale)" width="80%">
  <figcaption>
    **臨界オン抵抗（相対）**：同じ耐圧なら WBG ほど理論最小 Ron は小さく、**高効率なスイッチング**が可能。SiC/GaN は Si に対して数百分の1、Diamond はさらに低い。  
    *Critical on-resistance (relative): For the same breakdown, WBG materials allow much lower theoretical Ron, enabling high-efficiency switching. SiC/GaN are hundreds of times lower than Si; diamond is lower still.*
  </figcaption>
</figure>

---

## 🧠 材料の使いどころ｜Where Each Material Excels

- **Si** → 標準ロジックLSI・MEMS、低耐圧・低コストが利点  
  **Standard LSI/MEMS, low-voltage & cost advantage**
- **SiC** → 高耐圧・高温・高信頼性、EV・鉄道インバータに最適  
  **High voltage/temp reliability, ideal for EV & railway inverters**
- **GaN** → 高速スイッチング＆小型化、電源・5G・LIDARに有効  
  **High-speed switching & miniaturization, effective for power, 5G, LiDAR**
- **Diamond** → 性能限界を超えるがコスト高、宇宙・核融合応用へ  
  **Ultimate performance but costly, suited for space & nuclear fusion**

---

## 📎 次節への接続｜Next Section

[3. 材料応用マッピング｜Applications Mapping](./3_applications.md) では、  
ここで比較した材料特性が **どのアプリケーションに最適化されるか** を解説します。  
In the next section, we discuss how these material properties map to **specific applications**.

---

## 🔄 ナビゲーション / Navigation
- **◀ 前節 / Previous:** [1. Si・SiC・GaN・ダイヤモンド｜なぜ材料を変える必要があるのか？](./1_si_vs_sic_gan.md)  
- **▶ 次節 / Next:** [3. 材料応用マッピング｜Applications Mapping](./3_applications.md)  
- **🔙 README:** [Materials｜半導体材料の特性と応用選定](./README.md)
