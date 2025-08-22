---
layout: default
title: "Embedded Bridge | 埋め込みブリッジ技術"
---

---

# 🧱 Embedded Bridge / 埋め込みブリッジ技術
*Organic bridge technology for chiplet interconnects*

---

## 🔗 リンク / Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 View Site | ページ表示 / *View this page on site* | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Advanced-Packaging/Embedded-Bridge/) |
| 📂 View Repo | GitHubリポジトリ / *View source on GitHub* | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Advanced-Packaging/Embedded-Bridge.md) |

---

## 📑 目次 / Table of Contents
1. [概要 / Overview](#-概要--overview)  
2. [技術コンセプト / Technology Concept](#-技術コンセプト--technology-concept)  
3. [Intel EMIB / Intel’s EMIB](#-intel-emib--intels-emib)  
4. [他社技術との比較 / Comparison with Other Technologies](#-他社技術との比較--comparison-with-other-technologies)  
5. [応用分野 / Applications](#-応用分野--applications)  
6. [関連リンク / Related Links](#-関連リンク--related-links)  
7. [⬆️ Back to Advanced Packaging](#️-back-to-advanced-packaging)  

---

## 🏗 概要 / Overview
**Embedded Bridge (EMIB)** は、シリコンインターポーザの代替として、**有機基板に埋め込まれた小型シリコンブリッジ**でチップレット間を接続する技術です。  
*Embedded Bridge (EMIB) replaces full silicon interposers with localized silicon bridges embedded in organic substrates.*  

- **低コスト化**：全面インターポーザ不要 → シリコン使用量を大幅削減  
- **高帯域化**：短距離のシリコン配線で数百Gbpsクラスの接続が可能  
- **高柔軟性**：大規模SoCに複数ブリッジを配置可能  

---

## 🔧 技術コンセプト / Technology Concept
- 有機基板に「溝」を形成し、シリコンダイを埋め込む  
- チップレットのI/OをRDLを介してシリコンブリッジに接続  
- フルインターポーザに比べ、**基板コストと熱膨張ミスマッチを抑制**  

*Bridges are embedded into organic substrates, enabling local high-density interconnects with reduced cost and thermal mismatch compared to full interposers.*  

---

## 🖇 Intel EMIB / Intel’s EMIB
- Intelが開発した代表的なEmbedded Bridge実装  
- **例**: Stratix 10 FPGA, Ponte Vecchio GPU  
- 複数のロジック/メモリダイを小型シリコンブリッジで接続  
- HBMの高帯域接続にも活用  

---

## ⚖️ 他社技術との比較 / Comparison with Other Technologies

| 特性 / Feature | Embedded Bridge (EMIB) | CoWoS (TSMC) | 2.5D Interposer |
|----------------|------------------------|--------------|-----------------|
| シリコン使用量 | 部分的（小型ブリッジのみ） | 大面積インターポーザ | 大面積インターポーザ |
| コスト | ◎（低い） | △（高い） | △（高い） |
| 帯域 | ○（数百Gbpsクラス） | ◎（HBM直結, 数Tbps） | ◎（広帯域） |
| 熱特性 | ◎ 有機基板に準拠 | △ シリコン膨張差あり | △ 同左 |

---

## 💡 応用分野 / Applications
- **高性能FPGA / GPU**（Intel Stratix, Ponte Vecchio）  
- **チップレットSoC**：CPU + GPU + IO ダイ構成  
- **HBM接続**：高帯域・低レイテンシメモリ統合  

---

## 🔗 関連リンク / Related Links

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🖇 CoWoS / InFO | TSMCの先端実装技術<br>*TSMC’s CoWoS and InFO packaging* | [![Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Advanced-Packaging/CoWoS-InFO/)<br>[![Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Advanced-Packaging/CoWoS-InFO.md) |
| 🧱 2.5D / 3D IC | TSV/インターポーザによる実装<br>*TSV/interposer-based high-density IC packaging* | [![Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Advanced-Packaging/2.5D-3D-IC/)<br>[![Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/blob/main/Assembly-Integration/Advanced-Packaging/2.5D-3D-IC.md) |

---

## ⬆️ Back to Advanced Packaging

| 項目 / Item | 説明 / Description | Links |
|-------------|-------------------|-------|
| 🌐 Back to Site | Advanced Packaging 全体ページへ戻る<br>*Back to Advanced Packaging site* | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/Advanced-Packaging/) |
| 📂 Back to Repo | GitHubリポジトリに戻る<br>*Back to GitHub repo* | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/Advanced-Packaging) |
