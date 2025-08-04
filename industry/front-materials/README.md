# 🧪 前工程：材料メーカー｜ナノスケール構造を支える素材技術  
# 🧪 Front-End Materials | Enabling Materials for Nanoscale Structures

**本ディレクトリでは、半導体前工程に使用される材料と、それを供給する主要メーカーを整理します。**  
**This directory organizes the key materials used in semiconductor front-end processing and their suppliers.**

トランジスタや配線層の形成には、**極めて高純度かつプロセス適合性の高い材料**が必要であり、材料選定が歩留まり・性能・信頼性に直結します。  
Fabrication of transistors and interconnects requires **ultra-pure and highly process-compatible materials**, directly affecting yield, performance, and reliability.

---

## 📚 主な材料領域と企業分類  
## 📚 Key Material Domains and Leading Vendors

| 材料カテゴリ | 代表企業 | 用途例 |
|--------------|----------|--------|
| **シリコンウェーハ** | **SUMCO 🇯🇵**, GlobalWafers 🇹🇼, SK Siltron 🇰🇷** | 基板材料（300mm対応、Epiなど） |
| **レジスト材料** | **JSR 🇯🇵**, TOK 🇯🇵, Shin-Etsu 🇯🇵** | リソグラフィ用感光材料、EUV対応品含む |
| **配線用金属材料** | **Mitsubishi Materials 🇯🇵**, Honeywell 🇺🇸** | Cu, W, Coなどのスパッタターゲット |
| **高k絶縁膜前駆体** | **Air Liquide 🇫🇷**, Entegris 🇺🇸** | HfO₂などALD用材料、ゲート絶縁用途 |
| **CMPスラリー／パッド** | **Cabot Microelectronics 🇺🇸**, Fujimi 🇯🇵** | 平坦化工程に必要な研磨材とパッド |
| **プロセスガス** | **Linde 🇩🇪**, Air Products 🇺🇸**, Showa Denko 🇯🇵** | プラズマ、CVD、エッチング等に使用

---

## 🧩 材料と装置・工程との関係  
## 🧩 Material-Tool Integration in Process Flow

各材料は以下のような**装置・工程と密接に関連**しています：  
Each material is tightly linked to its corresponding equipment and process step:

- **シリコンウェーハ**：成膜・熱処理のベース基板  
- **レジスト・プロセスガス**：リソグラフィやエッチング工程に使用  
- **高k材料・前駆体**：ゲート形成やキャパシタ構造に利用  
- **CMPスラリー**：層間絶縁膜や配線平坦化に不可欠

---

## 🔍 教材活用のヒント  
## 🔍 Learning & Exploration Ideas

- **EUV用レジストと従来レジストの違い**を比較しよう  
- **材料メーカーの国別分布と地政学リスク**を整理してみよう  
- **材料品質が前工程のどこに影響を及ぼすか**をマッピングしてみよう

---

## 🧱 基礎構造・材料カテゴリ / Basic Structures & Materials

- [🧾 Wafer 基板の基礎と実務的注意点](./docs/wafer_basics.md)

---

## 📎 関連カテゴリ  
## 📎 Related Categories

- [⚙️ front-equipments/](../front-equipments/)：材料の使用先となる装置群  
- [🖼️ photomasks/](../photomasks/)：レジスト・OPCとの連携  
- [🔬 metrology-tools/](../metrology-tools/)：材料の厚み・均一性測定との関係

---

## 📄 ライセンス  
## 📄 License

MIT License に基づき、非営利・教育目的での自由な利用・改変・共有を歓迎します。  
This content is released under the MIT License, and is freely available for non-commercial and educational reuse.

---

**前工程材料は、半導体構造を構成する原子レベルの部材です。装置・プロセスとの一体運用を意識して探究しましょう。**  
**Front-end materials are the atomic components of semiconductor structures. Study them with an eye toward process and equipment integration.**
