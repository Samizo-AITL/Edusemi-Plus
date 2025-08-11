---
layout: default
title: 第2章：AIの歴史とブームの背景
---

---

# 第2章：AIの歴史とブームの背景  
**Chapter 2: History of AI and the Background of Its Booms**

---

## 2.1 初期のAIとその限界  
**Early AI and Its Limitations**

人工知能（AI）の研究は1950年代に端を発します。  
当初は論理推論やルールベースのエキスパートシステムが主流で、特定分野では実用化も試みられました。

The study of Artificial Intelligence began in the 1950s.  
Early AI was dominated by logic-based reasoning and rule-based expert systems, with some attempts at practical applications.

- **1956年：ダートマス会議 / Dartmouth Conference**  
  「Artificial Intelligence」という用語が初めて提唱される。  
  The term "Artificial Intelligence" was first proposed.

- **1980年代：エキスパートシステムの台頭 / Rise of Expert Systems**  
  医療・製造などへの応用が進むが、運用コストやスケーラビリティの課題が顕在化。  
  Applied in areas like healthcare and manufacturing, but issues with cost and scalability emerged.

- その結果、AIへの過度な期待が失望に転じ、**「AIの冬」**と呼ばれる停滞期が二度訪れた。  
  This led to the so-called **"AI winters"**, periods of stagnation due to unmet expectations.

> **JP:** 初期AIはルール駆動型で柔軟性や学習能力に乏しかった。  
> **EN:** Early AI was rule-driven, lacking flexibility and learning capability.

---

## 2.2 深層学習の登場とGPUの台頭  
**The Emergence of Deep Learning and the Rise of GPUs**

2006年、Hintonらの研究により「深層学習（Deep Learning）」が再評価され始め、  
2012年のImageNetコンペで **AlexNet** が圧倒的な成果を収めたことで新たなAIブームが到来しました。

In 2006, research by Hinton and others revived interest in "Deep Learning,"  
and in 2012, **AlexNet** achieved a breakthrough performance in the ImageNet competition, sparking a new AI boom.

### 🔑 技術的ブレイクスルー / Key Technical Breakthroughs

- **演算性能の壁を打破 / Breaking the Computational Barrier**  
  並列演算に優れた **GPU** が深層学習に活用され始める。  
  Highly parallel **GPUs** began to be used for deep learning.

- **アルゴリズム革新 / Algorithmic Innovations**  
  ReLU, Dropout, BatchNorm などで学習効率が飛躍的に向上。  
  Techniques like ReLU, Dropout, and BatchNorm greatly improved training efficiency.

- **データ×計算×アルゴリズムの三位一体 / Data × Compute × Algorithm Synergy**  
  大量データ・高性能計算・高度なアルゴリズムの組み合わせが成果を生んだ。  
  The combination of large datasets, powerful computing, and advanced algorithms drove results.

> **JP:** GPUはもともとグラフィックス向けだったが、汎用AIアクセラレータへと進化した。  
> **EN:** Originally for graphics, GPUs evolved into general-purpose AI accelerators.

---

## 2.3 現在のブームと大規模言語モデル（LLM）  
**Current Boom and Large Language Models (LLMs)**

2020年代に入り、AIの主戦場は画像認識から自然言語処理へ拡大。  
特に **大規模言語モデル（LLM）** がAIの能力を飛躍的に高めています。

In the 2020s, AI’s focus expanded from image recognition to natural language processing,  
with **Large Language Models (LLMs)** greatly enhancing AI capabilities.

### 🌍 LLMの特徴と要件 / Features and Requirements of LLMs

- 代表例 / Examples: **GPT-4 (OpenAI)**, **Claude (Anthropic)**, **Gemini (Google)**
- パラメータ数は数千億〜数兆規模。  
  Parameter counts range from hundreds of billions to trillions.
- 学習には莫大な演算量・ストレージ・電力が必要。  
  Training requires enormous compute, storage, and power.
- 推論でもレイテンシ・帯域・電力が課題。  
  Inference faces challenges in latency, bandwidth, and power.

### 💡 ハードウェア依存の高まり / Rising Hardware Dependence

- 高性能モデルの実現には専用アクセラレータ（GPU, TPU, ASICなど）が必須。  
  Specialized accelerators (GPUs, TPUs, ASICs) are essential for high-performance models.
- LLMはソフトとハードの共進化の象徴。  
  LLMs symbolize the co-evolution of software and hardware.

---

## 2.4 参入企業の多様化と市場拡大  
**Diversification of Players and Market Expansion**

AI市場の成長に伴い、多くの企業がAI専用ハードウェアの開発に参入しています。

With the growth of the AI market, many companies have entered the AI-specific hardware race.

| 企業 / Company | 戦略・特徴 / Strategy & Features |
|---------------|----------------------------------|
| **NVIDIA** | GPU主導のAI計算市場を確立、CUDAで開発者囲い込み / Established GPU-led AI compute market, locked in developers with CUDA |
| **Google** | TPU開発でクラウドAI処理効率化 / Improved cloud AI efficiency with TPU |
| **Apple** | Neural EngineをSoCに統合 / Integrated Neural Engine into SoC |
| **AMD** | MIシリーズでデータセンターAI市場を狙う / Targeted data center AI with MI series |
| **Intel** | 買収でAI強化（Habana Labs, Nervana） / Strengthened AI via acquisitions |
| **Cerebras, Groq, Tenstorrent** | LLM特化の新興企業 / Startups focusing on LLM-optimized chips |

> **JP:** AIブームは「ハードウェア主導の競争」でもある。  
> **EN:** The AI boom is also a "hardware-driven competition."

---

## ✅ 本章のまとめ / Chapter Summary

- **JP:** AIは1950年代から数度のブームと冬を繰り返し、深層学習とGPUで飛躍を遂げた。  
- **EN:** Since the 1950s, AI has gone through cycles of booms and winters, with deep learning and GPUs driving its recent leap.

- **JP:** 現在はLLMと演算インフラ革新がブームを加速。  
- **EN:** Today, LLMs and innovations in computing infrastructure are accelerating the boom.

- **JP:** 多くの企業がAIハード開発に参入し、半導体が技術・市場の中心となっている。  
- **EN:** Many companies are entering AI hardware, making semiconductors central to technology and markets.

---

## 🔙 前後リンク / Navigation

- **◀ 前節 / Previous:** [第1章：はじめに — AI半導体の重要性と全体像](01_introduction.md)  
- **▶ 次節 / Next:** [第3章：主要企業と市場動向](03_key_players.md)  
- **📄 本シリーズREADME:** [ai-semiconductor README](../README.md)
