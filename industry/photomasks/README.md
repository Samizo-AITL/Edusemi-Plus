# 🖼️ フォトマスク関連｜設計と製造をつなぐ光のブリッジ  
# 🖼️ Photomasks | The Optical Bridge Between Design and Manufacturing

**本ディレクトリでは、フォトマスクに関わる主要技術・企業・工程を整理します。**  
**This directory outlines the key technologies, companies, and processes related to photomasks.**

フォトマスクは、EDAで生成されたレイアウトデータを**光学的にシリコン上に転写するための基盤**です。  
Photomasks serve as the **physical medium that projects layout data onto wafers through lithography**.

---

## 📚 フォトマスク関連の主な領域と企業  
## 📚 Major Domains and Companies in Photomask Industry

| 領域 | 代表企業 | 概要 |
|------|----------|------|
| **マスクブランクス** | **HOYA 🇯🇵**, AGC 🇯🇵 | 石英基板、EUV用多層反射膜形成 |
| **マスク描画・製作** | **DNP 🇯🇵**, Toppan 🇯🇵, Photronics 🇺🇸 | e-beam描画、先端マスク製造 |
| **OPC/ILT最適化** | **Synopsys 🇺🇸**, Siemens EDA 🇺🇸 | 設計データの露光最適化、ILT手法の導入 |
| **欠陥検査・補正** | **NuFlare 🇯🇵**, KLA 🇺🇸 | マスク欠陥の検出と修正、actinic検査対応 |

---

## 🧩 フォトマスクの種類と構造  
## 🧩 Mask Types and Structures

- **ArF透過型マスク**：通常の光透過構造、液浸対応あり  
- **EUV反射型マスク**：極紫外光を反射する多層ミラー構造  
- **レチクル（Reticle）**：1x～4x縮小比で使用、露光縮小光学系と連携  

> EUVマスクは、**極端に高価かつ欠陥検査が困難**なため、歩留まりと開発リスクに大きく影響します。  
> EUV masks are **extremely expensive and hard to inspect**, significantly affecting yield and development cost.

---

## 🔍 教材活用のヒント  
## 🔍 Learning & Exploration Ideas

- **なぜASMLだけがEUV露光を供給できるのか？** → フォトマスク技術と装置の連携構造に注目  
- **OPCとILTの違いと役割** → デザインと製造の相互最適化の本質  
- **HOYAのEUVマスクブランクスの世界シェア**と地政学的意味を探る

---

## 📎 関連カテゴリ  
## 📎 Related Categories

- [🧠 eda-tools/](../eda-tools/)：設計データ生成・OPC連携  
- [⚙️ front-equipments/](../front-equipments/)：露光装置との適合性  
- [🔬 metrology-tools/](../metrology-tools/)：マスク検査・補正との接続

---

## 📄 ライセンス  
## 📄 License

MIT License に基づき、非営利・教育目的での自由な利用・改変・共有を歓迎します。  
This content is released under the MIT License, and is freely available for non-commercial and educational reuse.

---

**フォトマスクは、設計情報を物理世界に写し取る「光のテンプレート」です。構造・材料・検査まで含めて深く学びましょう。**  
**Photomasks are the light-based templates that translate design into reality. Explore their structure, materials, and inspection technologies.**
