---
layout: default
title: 1. Si・SiC・GaN・ダイヤモンド｜なぜ材料を変える必要があるのか？ / Why Change from Si to SiC, GaN, and Diamond?
---

---

# 🧪 1. Si・SiC・GaN・ダイヤモンド｜なぜ材料を変える必要があるのか？  
**1. Why Change from Si to SiC, GaN, and Diamond?**

---

## 🔍 出発点：シリコンの優位性と限界  
**Starting Point: Advantages and Limitations of Silicon**

| **特性 / Property** | **シリコン（Si）の利点 / Advantages of Si** | **限界（用途による） / Limitations** |
|--------------------|--------------------------------------------|--------------------------------------|
| **製造性 / Manufacturability** | 高結晶性・加工容易 / High crystallinity, easy to process | 300mmウェハが主流 / 300mm wafer dominant |
| **コスト / Cost** | 安価・既存インフラ多数 / Low cost, abundant infrastructure | 高耐圧領域で劣化 / Degrades at high voltages |
| **電子特性 / Electrical Properties** | MOS動作に適した移動度 / Mobility suited for MOS | 熱伝導性やや低い / Relatively low thermal conductivity |
| **応用範囲 / Application Range** | CMOSロジックに最適 / Ideal for CMOS logic | 高電圧・高周波に非効率 / Inefficient for high-voltage & high-frequency |

➡ **これらの用途には「ワイドバンドギャップ材料（WBG）」が必要**  
➡ **Such applications require *Wide Bandgap (WBG)* materials**

---

## ⚡ WBG材料とは？  
**What are Wide Bandgap Materials?**

| **材料 / Material** | **バンドギャップ (eV) / Bandgap (eV)** | **特徴 / Features** | **主な用途 / Main Applications** |
|-------------------|--------------------------------------|---------------------|----------------------------------|
| **Si** | 1.1 | CMOSの基本材料 / Base material for CMOS | LSI, MEMS |
| **SiC** | 3.3 | 高耐圧・高温耐性 / High voltage & high temperature resistance | EV, Power IC, Railways |
| **GaN** | 3.4 | 高周波性能・高速スイッチング / High frequency, fast switching | 5G, Power supply, Satellite comms |
| **Diamond** | 5.5 | 最高熱伝導率・絶縁耐圧 / Highest thermal conductivity, high breakdown | Space, Nuclear fusion, Radiation-hardened devices |

💡 **バンドギャップが広いほど高電圧・高温に強く、オン抵抗を下げられる可能性が高い**  
💡 **Wider bandgap → better high-voltage/high-temperature tolerance, lower on-resistance**

---

## 🧩 Siでは到達できない応用例  
**Applications Beyond Silicon’s Capability**

| **応用例 / Application** | **材料の選定理由 / Reason for Material Choice** |
|-----------------------|--------------------------------------------|
| **EVインバータ / EV Inverter** | 高耐圧＆低損失 → SiC / High voltage & low loss → SiC |
| **5G通信 / 5G Communication** | 高速スイッチング＆小型化 → GaN HEMT / High-speed switching & compact size → GaN HEMT |
| **宇宙用途 / Space Applications** | 放射線耐性＆熱放出性 → ダイヤモンドFET / Radiation resistance & heat dissipation → Diamond FET |

---

## 🔁 CMOSとの違いと接続  
**Differences from and Connections to CMOS**

- GaN・SiCも **MOS構造やHEMT構造** に応用可能  
  GaN and SiC can also be used in **MOS and HEMT structures**
- CMOSロジックとは **電気特性・製造プロセス・基板温度制約** が異なる  
  They differ from CMOS logic in **electrical properties, manufacturing processes, and substrate temperature limits**

---

## 📝 本節のまとめ / Summary

- **Si以外の材料が必要な理由は「限界特性の突破」**  
  **Need for non-Si materials arises from overcoming physical limits**
- **SiC・GaN・ダイヤモンドは高耐圧・高温・高周波・高放射線環境に適応**  
  **SiC, GaN, and Diamond are suited for high-voltage, high-temp, high-frequency, radiation environments**
- **用途と材料はトレードオフで選定**し、「物性」→「応用」への流れが重要  
  **Application and material choice are trade-offs**, making the flow from *physical properties → application* crucial

---

📎 **次節 / Next:** [2. 材料の物性比較｜Material Properties Comparison](./2_material_properties.md) では、  
各材料の **移動度・バンドギャップ・耐圧・オン抵抗** を定量的に比較します。  
In the next section, we will quantitatively compare **mobility, bandgap, breakdown voltage, and on-resistance** of each material.

---

## 🔄 ナビゲーション / Navigation
- **◀ 前節 / Previous:** _(なし / None)_  
- **▶ 次節 / Next:** [2. 材料の物性比較｜Material Properties Comparison](./2_material_properties.md)  
- **🔙 README:** [Materials｜半導体材料の特性と応用選定](./README.md)
