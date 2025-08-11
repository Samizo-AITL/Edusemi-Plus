---
layout: default
title: 🏭 4.1 サプライチェーンの基本構造 / 4.1 Basic Supply Chain Structure
---

# 🏭 4.1 サプライチェーンの基本構造  
**4.1 Basic Supply Chain Structure**

---

## 📜 概要 / Overview

**JP:**  
半導体サプライチェーンは、**設計（Design）→製造（Fabrication）→パッケージ（Packaging）→出荷（Shipping）**の大きく4段階に分かれます。  
それぞれの段階で異なるプレイヤー・国・技術が関与し、グローバルな分業体制を形成しています。

**EN:**  
The semiconductor supply chain can be divided into four major stages: **Design → Fabrication → Packaging → Shipping**.  
Each stage involves different players, countries, and technologies, forming a global division of labor.

---

## 🗂 フロー構造 / Process Flow

```mermaid
flowchart LR
    A[設計 / Design] --> B[製造 / Fabrication]
    B --> C[パッケージ / Packaging]
    C --> D[出荷 / Shipping]
```

---

## 📊 各段階の概要 / Stage Overview

| 段階 / Stage | 主な内容 / Key Activities | 主な国・企業 / Main Countries & Companies |
|--------------|---------------------------|-------------------------------------------|
| 設計 / Design | RTL設計、EDA利用、IP統合 / RTL, EDA, IP integration | 米国（Synopsys, Cadence）, 日本, 欧州 |
| 製造 / Fabrication | 前工程（リソ・成膜・エッチング） / Front-end processing | 台湾（TSMC）, 韓国（Samsung）, 米国, 中国 |
| パッケージ / Packaging | 後工程（2.5D/3D, CoWoS, FC-BGA） / Back-end packaging | 台湾（ASE）, 韓国（Amkor）, 日本 |
| 出荷 / Shipping | ロジスティクス・顧客納品 / Logistics, delivery | グローバル物流企業 |

---

## 🧩 分業構造の特徴 / Characteristics of Division of Labor

**JP:**  
各段階は高度に専門化されており、**一国で全工程を完結できる国は極めて限られています**。  
サプライチェーンの強靭化には、複数国間の連携や代替供給源の確保が必須です。

**EN:**  
Each stage is highly specialized, and **very few countries can complete all processes domestically**.  
Strengthening the supply chain requires multi-country collaboration and securing alternative supply sources.

---

## 🔗 関連リンク / Related Links

- [第4章 README](README.md)

---

## 🔙 戻る / Back
- **JP:** [第4章 READMEに戻る](README.md)  
- **EN:** [Return to Chapter 4 README](README.md)
