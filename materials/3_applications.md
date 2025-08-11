---
layout: default
title: 3. 材料と応用のマッピング｜Application Mapping of Semiconductor Materials
---

---

# 🗺️ 3. 材料と応用のマッピング｜Application Mapping of Semiconductor Materials

本節では、前章で示した**物性データ**をもとに、  
用途ごとに最適な材料選定の**具体例**を示します。  
In this section, based on the **material properties** from the previous chapter,  
we present **examples of optimal material selection** for each application.

---

## 📌 材料選定の基本ロジック｜Basic Selection Logic

| **観点 / Aspect** | **評価軸 / Evaluation Axis** | **優位材料 / Preferred Materials** |
|-------------------|-----------------------------|--------------------------------------|
| **耐圧 / Breakdown Voltage** | スイッチのブロック耐圧 / Voltage blocking capability | **SiC > GaN > Si** |
| **スイッチ速度 / Switching Speed** | 高周波・高速応答性 / High-frequency & fast response | **GaN > SiC > Si** |
| **熱放出性 / Thermal Dissipation** | 熱伝導率・冷却性 / Thermal conductivity & cooling ease | **Diamond > SiC > Si** |
| **放射線耐性 / Radiation Tolerance** | 宇宙・原子力用途 / Space & nuclear environments | **Diamond◎, GaN◯, SiC△** |
| **成熟性・コスト / Maturity & Cost** | 製造インフラ親和性 / Manufacturing readiness | **Si◎, SiC◯, GaN△** |

---

## 🔧 主要応用領域と材料の組み合わせ｜Applications & Material Choices

| **応用領域 / Application** | **特徴・要求 / Key Requirements** | **主な採用材料 / Main Materials** |
|----------------------------|------------------------------------|------------------------------------|
| **電気自動車（EV） / Electric Vehicles** | 高耐圧・高電流・高温・高信頼性 / High V/I, temp, reliability | **SiC MOSFET** |
| **5G・RF電源 / 5G & RF Power** | 高速スイッチ・高効率・小型化 / Fast switching, high efficiency | **GaN HEMT** |
| **データセンター / Data Centers** | 電源効率化・発熱対策 / Power efficiency & thermal mgmt | **GaN FET, Next-gen SiC** |
| **宇宙機器 / Space Equipment** | 放射線耐性・極限環境 / Radiation & extreme environments | **Diamond FET** (R&D) |
| **産業用電源 / Industrial Power** | 高耐圧と堅牢性 / High voltage & ruggedness | **SiC or IGBT** (depends) |
| **レーザー・光デバイス / Laser & Optoelectronics** | 青紫外光対応・高出力 / Blue-UV compatibility & high output | **InGaN, AlGaN** (related tech) |

---

## 🧭 材料選定マトリクス（作成予定）｜Material-Application Matrix (Planned)

| **応用 / Application** → 材料 ↓ | EV | 5G | 宇宙 / Space | DC電源 / DC Power | 光デバイス / Optoelectronics |
|---------------------------------|----|----|--------------|-------------------|------------------------------|
| **Si**       | △  | ×   | ×    | ◯      | ×          |
| **SiC**      | ◎  | △   | △    | ◎      | ×          |
| **GaN**      | △  | ◎   | ◯    | ◎      | △ (LD etc.) |
| **Diamond**  | △ (将来 / future) | × | ◎ (将来 / future) | △ | × |

💡 このマトリクスは `/images/` に後日追加予定  
💡 This matrix will be added later in `/images/`

---

## 🔗 他章・カテゴリとの接続｜Connections

- 📘 次節 / Next: [4. 将来の材料動向｜Future Material Trends](./4_future_trends.md)  
  **将来有望な材料や構造（ダイヤモンドFET、AlN、垂直GaN）**を解説  
  Explains **future materials & structures** (Diamond FET, AlN, Vertical GaN)
- 🤖 関連: [AIと半導体材料](../ai-semiconductor/)  
  GaNのスイッチング特性はAI電源モジュールにも応用  
  GaN switching is also used in AI power modules

---

## 🔄 ナビゲーション / Navigation
- **◀ 前節 / Previous:** [2. 材料特性の定量比較｜Quantitative Comparison](./2_material_properties.md)  
- **▶ 次節 / Next:** [4. 将来の材料動向｜Future Trends](./4_future_trends.md)  
- **🔙 README:** [Materials｜半導体材料の特性と応用選定](./README.md)
