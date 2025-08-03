# ⚙️ 前工程：装置メーカー｜原子レベルの加工を支える中核機器  
# ⚙️ Front-End Equipment | Core Tools for Atomic-Scale Fabrication

**本ディレクトリでは、半導体前工程（Front-End）における主要な装置メーカーとプロセス装置の分類を整理します。**  
**This directory categorizes the major front-end equipment vendors and the core processing tools used in semiconductor manufacturing.**

前工程では、**トランジスタ形成や配線層の堆積・微細加工をナノメートル精度で行う**必要があり、各装置の精度と安定性が製品性能に直結します。  
The front-end process requires **nanometer-scale precision for transistor and interconnect fabrication**, where the performance and reliability of each tool critically impact the final chip.

---

## 📚 主な装置領域と企業分類  
## 📚 Key Tool Domains and Leading Vendors

| 工程 | 代表企業 | 概要 |
|------|----------|------|
| **CVD/ALD 成膜** | **Applied Materials 🇺🇸**, Lam Research 🇺🇸, Tokyo Electron 🇯🇵** | 配線・ゲート絶縁膜、EUV用保護膜など |
| **ドライエッチング** | **Lam Research 🇺🇸**, TEL 🇯🇵, Hitachi High-Tech 🇯🇵** | 高アスペクト比加工、ナノ加工対応 |
| **フォトリソグラフィ** | **ASML 🇳🇱**, Nikon 🇯🇵, Canon 🇯🇵** | ArF/EUV露光、ステッパー/スキャナー装置 |
| **アッシング・洗浄** | **SCREEN 🇯🇵**, SEMES 🇰🇷** | 残渣除去、パターン保護、表面改質 |
| **熱処理（アニール）** | **Kokusai Electric 🇯🇵**, Mattson 🇺🇸** | 活性化拡散、ゲート形成後の処理

---

## 🧩 前工程装置と製造プロセスの関係  
## 🧩 Role of Front-End Equipment in the Process Flow

前工程装置は、以下のようなステップで連携して使用されます：  
Front-end tools are sequentially applied in steps such as:

1. **成膜（絶縁膜・金属膜の堆積）**  
2. **レジスト塗布 → 露光 → 現像（リソグラフィ）**  
3. **ドライエッチングによる微細加工**  
4. **アッシング、洗浄によるレジスト除去と表面整備**  
5. **熱処理（アニール）での活性化処理や不純物拡散制御**

---

## 🔍 教材活用のヒント  
## 🔍 Learning & Exploration Ideas

- **EUV露光装置とドライエッチング装置の連携構造**を調べてみよう  
- **日本と米国の装置競争力の違い**を企業ごとに比較してみよう  
- **成膜→エッチング→洗浄の工程順と制約条件**を明確にしよう

---

## 📎 関連カテゴリ  
## 📎 Related Categories

- [🧪 front-materials/](../front-materials/)：各装置で使用される材料の視点  
- [🖼️ photomasks/](../photomasks/)：露光装置との協調関係  
- [🔬 metrology-tools/](../metrology-tools/)：前工程後の検査・フィードバック

---

## 📄 ライセンス  
## 📄 License

MIT License に基づき、非営利・教育目的での自由な利用・改変・共有を歓迎します。  
This content is released under the MIT License, and is freely available for non-commercial and educational reuse.

---

**前工程装置は、原子レベルの精度でトランジスタを構築するための中核技術です。技術的制約と装置連携に注目して学びましょう。**  
**Front-end tools are central to atomic-level precision in chipmaking. Study the process integration and technical constraints carefully.**
