# 第1章：量子半導体の基礎と原理

## 1.1 なぜ量子半導体なのか

現在の半導体スケーリング（微細化）は物理的限界に近づいており、  
**「新たな計算パラダイム」**として量子コンピューティングへの関心が高まっています。

量子半導体とは、**量子力学的な原理を利用して情報処理を行う素子**を対象にした技術領域であり、  
これまでのCMOSロジックとは異なる計算原理・設計思想が必要になります。

---

## 1.2 古典ビットと量子ビット（Qubit）の違い

| 項目 | 古典ビット | 量子ビット (Qubit) |
|------|-------------|---------------------|
| 値の状態 | 0 または 1 | 0と1の重ね合わせ（superposition） |
| 同時性 | 無 | 並列状態を一度に処理可能 |
| 代表的実装 | CMOS, トランジスタ | 超伝導回路, イオントラップ, 半導体量子ドット など |
| 計算特性 | 決定論的 | 非決定論的、確率的出力 |

---

## 1.3 量子力学的な3つの基礎原理

- **重ね合わせ (Superposition)**  
  ビットが「0」と「1」の状態を同時に持つことができる

- **量子もつれ (Entanglement)**  
  複数の量子ビットが強く相関した状態をとり、非局所的に影響し合う

- **量子干渉 (Interference)**  
  波としての振幅が干渉し、望ましい計算結果を強める・望ましくない結果を打ち消す

これらは従来のデジタル回路設計とは根本的に異なる情報処理体系です。

---

## 1.4 半導体との接点：なぜCMOS技術者にも関係があるのか

- CMOS・配線・低温冷却など、**既存の半導体製造・設計ノウハウ**が量子でも重要
- IntelやIBM、Googleなどは、**CMOSとの共存を意識した量子チップの開発**を推進中
- また、将来的には「量子アクセラレータ」がSoCに組み込まれる可能性も視野に

---

## 1.5 本章まとめ

- 量子半導体とは「量子力学に基づく計算素子」
- 原理的には古典と異なり、重ね合わせ・もつれ・干渉を活用
- 技術者として理解すべき理由は、**半導体製造・回路技術との融合が始まっているから**

---

🔗 次章 → [第2章：代表的な量子デバイス](02_devices.md)
