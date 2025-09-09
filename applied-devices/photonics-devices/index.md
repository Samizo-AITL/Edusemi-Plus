---
layout: default
title: 💡 光デバイス / Photonics Devices
---

---

# 💡 光デバイス / Photonics Devices  
*Photonics Devices*

---

## 🔗 リンク / Links  

| Link | Badge |
|---|---|
| 🌐 **View Site** | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/photonics-devices/) |
| 📂 **View Repo** | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/applied-devices/photonics-devices) |

---

> **概要 / Overview**  
> 光デバイスは、**発光・受光・光制御を担う半導体素子群**であり、光通信・センシング・AI加速・量子情報において不可欠です。  
> *Photonics devices are semiconductor components for emission, detection, and modulation of light, essential for communication, sensing, AI acceleration, and quantum information.*

---

## 📖 節構成 / Chapter Structure  

### 1️⃣ 基礎光デバイス / *Fundamental Devices*

- **💡 LED / µLED**  
  - 発光原理：**直接遷移半導体**（GaAs, InGaN）  
  - *Principle: Direct bandgap semiconductors*  
  - 応用：**照明、ディスプレイ、光インジケータ**  
  - *Applications: Lighting, display, optical indicators*

```mermaid
graph TD
  A[価電子帯 Valence Band] -->|電子励起 Excitation| B[伝導帯 Conduction Band]
  B -->|再結合・光子放出 Recombination| C[光 Photon 🟡]
```

> **図：** LEDにおける価電子帯から伝導帯への励起と再結合による光子放出  
> *Band-to-band excitation and photon emission in LEDs*

---

- **🔦 半導体レーザ（LD, VCSEL, QD-LD） / Semiconductor Lasers**  
  - キャビティ構造と**しきい値条件**  
  - *Cavity structure and threshold condition*  
  - 応用：**通信、LiDAR、ストレージ、プロジェクタ**  
  - *Applications: Communication, LiDAR, storage, projectors*

---

- **📡 フォトダイオード（PIN, APD） / Photodiodes**  
  - 特徴：**高速応答性、内部増倍機構**  
  - *Features: High-speed response, internal gain*  
  - 応用：**光通信、センシング、イメージング**  
  - *Applications: Optical communication, sensing, imaging*

```mermaid
flowchart TB
  A[光入射<br>Incident Light] --> B[半導体<br>P層]
  B --> C[空乏層<br>I層 Depletion Region]
  C --> D[半導体<br>N層]
  C -->|電子 e⁻| E[外部回路<br>External Circuit]
  C -->|正孔 h⁺| E
  style C fill:#e6f2ff,stroke:#000,stroke-width:1px
```

> **図：** PINフォトダイオードの構造と光電流生成  
> *PIN photodiode structure and photocurrent generation*

```mermaid
flowchart TB
  A[光入射<br>Incident Light] --> B[半導体<br>P層]
  B --> C[空乏層<br>I層 Depletion Region]
  C --> D[増倍領域<br>Multiplication Region]
  D --> E[半導体<br>N層]
  D -->|電子雪崩 e⁻ avalanche| F[外部回路<br>External Circuit]
  style C fill:#e6f2ff,stroke:#000,stroke-width:1px
  style D fill:#ffe6e6,stroke:#000,stroke-width:1px
```

> **図：** APDの内部雪崩増倍機構  
> *Avalanche multiplication in APD*

---

### 2️⃣ シリコンフォトニクス / *Silicon Photonics*

- **導波路（Si, SiN, SOI） / Waveguides**  
- **変調器（キャリア注入型、EO型） / Modulators**  
- **光トランシーバ集積 / Optical Transceivers**  
  - 応用：**データセンター用高速リンク、AIチップ内光インターコネクト**  
  - *Applications: High-speed data links, AI chip interconnects*

```mermaid
flowchart TD
  A[光入力 Input Light] -->|入射 Coupling| B[(Si 導波路 Waveguide)]
  B -->|伝搬 Propagation| C[(変調器 Modulator)]
  C -->|変調後光| D[(SiN/Si 出力導波路 Output)]
  D -->|出射 Out-coupling| E[光出力 Output Light]
```

> **図：** シリコンフォトニクス導波路と変調器  
> *Silicon photonics waveguide and modulation flow*

---

### 3️⃣ 先端フォトニクス / *Advanced Photonics*

- 🌐 **フォトニック結晶レーザ / Photonic Crystal Lasers**  
- 🔬 **量子ドットレーザ / Quantum Dot Lasers**  
- 🖧 **光子集積回路（PIC） / Photonic Integrated Circuits**  
- ⚡ **光AIアクセラレータ、光量子計算素子 / Photonic AI accelerators, quantum devices**

```mermaid
flowchart LR
  A[光源<br>Laser Source] --> B[導波路<br>Waveguide]
  B --> C[変調器<br>Modulator]
  C --> D[分岐導波路<br>Splitter]
  D --> E1[検出器 PD1<br>Photodetector]
  D --> E2[検出器 PD2<br>Photodetector]
  B --> F[リング共振器<br>Resonator]
  F --> G[フィルタリングされた光<br>Filtered Output]
```

> **図：** 光子集積回路 (PIC) の基本構成  
> *Basic architecture of a Photonic Integrated Circuit (PIC)*

---

## 📌 今後の拡張 / *Future Expansion*
- 🚘 **LiDAR 向け光デバイス / LiDAR photonics**  
- 💾 **光メモリ素子 / Photonic memories (e.g., phase-change)**  
- 🔀 **光スイッチ／光演算素子 / Optical switches & computing devices**  
- 🧪 **材料クロスリンク / Materials (InP, GaAs, SiC, GaN, 2D materials)**  

---

## 👤 **著者・ライセンス / Author & License**

| **項目 / Item** | **内容 / Details** |
|-----------------|--------------------|
| **著者 / Author** | **三溝 真一**（Shinichi Samizo） |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![Hybrid License](https://img.shields.io/badge/license-Hybrid-blueviolet?style=for-the-badge)](../../../#-ライセンス--license) <br> 📖 **再配布・改変自由（教育目的）** / *Free for educational use, redistribution, and modification* <br> 💼 **商用利用は別途許可が必要** / *Commercial use requires separate permission* |

---

## ⬆️ 応用デバイスへ戻る / *Back to Applied Devices*

| Link | Badge |
|---|---|
| 🌐 **Back to Applied Devices** | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Applied%20Devices-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/applied-devices/) |
| 📂 **Back to Repo** | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/applied-devices) |
