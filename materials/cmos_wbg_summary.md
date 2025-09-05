---
title: "📘 CMOS適用限界とWBGへの分岐まとめ"
layout: default
---

# 📘 CMOS適用限界とWBGへの分岐まとめ  
*Where CMOS ends and WBG (SiC / GaN / Diamond) begins*

---

## ✅ 電圧・用途の棲み分け | Voltage & Application Mapping

| 技術 / Technology | 耐圧レンジ（目安） / *Voltage Range* | 集積度 / *Integration* | 主な強み / *Strengths* | 適用分野 / *Applications* |
|------|----------------------|------------|-------------------|----------------|
| **CMOS** | 1–5 V（ロジック回路）<br>*Logic level* | ⭐⭐⭐⭐⭐ 高 / *High* | **高集積・低消費電力**<br>*High density, low power* | CPU, GPU, DRAM, SoC |
| **BCD** | 5–200 V | ⭐⭐⭐ 中 / *Medium* | **デジタル＋アナログ＋中耐圧を1チップ化**<br>*Mixed-signal + power integration* | PMIC, 車載IC, モータードライバ |
| **LDMOS** | 20–200+ V | ⭐⭐ 低 / *Low* | **中耐圧・高出力・RF対応**<br>*Medium voltage, high power, RF capable* | 基地局PA, 車載電源 |
| **SiC** | 600–1200 V+ | ⭐ 低 / *Low* | **高耐圧・高温・高効率**<br>*High voltage, high temperature, efficiency* | EVインバータ, 産業電源 |
| **GaN** | 100–650 V（RF:〜100 GHz） | ⭐⭐ 低 / *Low* | **高速スイッチング・高周波・小型化**<br>*Fast switching, RF, compact* | 充電器, サーバ電源, 5G基地局, レーダー |
| **Diamond** | kV〜10kV級（研究段階） | ☆ 非常に低 / *Very low* | **超高熱伝導・超高耐圧（理論最強）**<br>*Ultra-high thermal & breakdown* | 宇宙, 核融合, 将来応用 |

---

## 📊 適用領域イメージ | Application Landscape

```mermaid
graph TD
    A[CMOS 適用領域<br>*Low voltage, high integration*] --> B[BCD<br>*5–200 V mixed-signal power*]
    B --> C[LDMOS<br>*20–200+ V RF/PA*]
    B --> D[GaN<br>*100–650 V fast switching/RF*]
    D --> E[SiC<br>*600–1200 V high power*]
    E --> F[Diamond<br>*kV extreme future use*]
```

---

## 🔀 選定フロー | Selection Flow

1. **SoC集積が必須？**  
   *Is SoC integration required?*  
   → はい → **CMOS / BCD**

2. **耐圧 > 200 V 必要？**  
   *Need >200 V blocking voltage?*  
   → はい → **LDMOS / GaN / SiC**

3. **> 600 V必要？**  
   *Need >600 V?*  
   → はい → **SiC**（さらにkV級なら Diamond / Ga₂O₃）

4. **高周波・RF用途？**  
   *RF or high-frequency application?*  
   → はい → **GaN**（特に *GaN on SiC*）

---

## 🎯 まとめ | Summary

- **CMOSの限界 = 数十V以下、SoCやロジック領域**  
  *CMOS limit ≈ under tens of volts, for logic/SoC*  
- **数十V〜200V → BCD / LDMOS** が適用範囲  
  *Medium voltage handled by BCD/LDMOS*  
- **200〜650V → GaN** が有利（電源小型化・RF高効率）  
  *GaN dominates mid-voltage & RF power*  
- **600V超 → SiC** が本命  
  *SiC leads in high-voltage & power electronics*  
- **kV級・極限環境 → Diamond（研究段階）**  
  *Diamond for extreme and future applications*
