---
layout: default
title: 主要AIモデル一覧と特徴（2025年版 / Major AI Models & Features - 2025 Edition）
---

---

# 🌐 主要AIモデル一覧と特徴（2025年版）  
**Major AI Models & Features (2025 Edition)**

本資料は、Edusemi-Plus における技術教育・設計・調査に活用可能な主要生成AIモデル・チャットツールを一覧化したものです。  
This document lists the main generative AI models and chat tools that can be used in **Edusemi-Plus** for technical education, design, and research.  
商用モデル／OSSモデル／補助ツールを含めて比較します。  
It covers **commercial models, OSS models, and supplementary tools**.

---

## ✅ 商用主要モデル（主力3ツール） / Key Commercial Models (Core 3 Tools)

| モデル名 / Model | 提供元 / Provider | 特徴 / Features | 無料枠 / Free Tier | Edusemi-Plusとの相性 / Fit with Edusemi-Plus |
|------------------|-------------------|-----------------|--------------------|----------------------------------------------|
| **[ChatGPT (GPT-5)](https://chat.openai.com/)** | OpenAI | 高度推論・教材生成・長文安定 / Advanced reasoning, material generation, long text stability | △（制限付き） | ◎ 教材構成・PoC設計支援の主軸 |
| **[Gemini 2.5 Pro / Flash](https://gemini.google.com/)** | Google | Web検索・YouTube要約・推論強化 / Web search, YouTube summarization, deep reasoning | ◯（Flash版） | ◯ 動画教材・最新情報補完 |
| **[Claude 3 Opus](https://claude.ai/)** | Anthropic | 丁寧な言語表現・要約・校正に強い / Polite expressions, summarization, proofreading | ◯（Sonnet版） | ◎ 報告書・教材整形 |

---

## 🔧 コーディング・設計支援向けモデル / Coding & Design Support Models

| モデル名 / Model | 提供元 / Provider | 特徴 / Features | OSS | 備考 / Notes |
|------------------|-------------------|-----------------|-----|--------------|
| **[DeepSeek Coder V3](https://deepseek.com/)** | DeepSeek（中国） | 高精度コード生成、推論速度◎ / High-accuracy code, fast inference | △（一部OSS） | 教育コードやPoCスケルトン生成に最適 |
| **[Command R 2025](https://cohere.com/)** | Cohere | Retrieval-augmented（RAG）特化 / RAG-focused | △ | 資料検索型AI構築に有望 |
| **[Yi-34B](https://01.ai/)** | 01.AI（中国） | 多言語高性能OSSモデル / Multilingual, high-performance OSS | ◎ | GPT-3.5並の構成力あり |

---

## 🧪 OSS・軽量モデル（ローカル実行可） / OSS & Lightweight Models (Local Execution Capable)

| モデル名 / Model | 提供元 / Provider | 特徴 / Features | ローカル実行 / Local Run | 備考 / Notes |
|------------------|-------------------|-----------------|--------------------------|--------------|
| **[LLaMA 3.1 (8B / 70B)](https://ai.meta.com/llama/)** | Meta | 高性能OSSモデルの本命 / Flagship OSS model | ◎（Ollama対応） | 教育機関向けにも注目 |
| **[Mixtral 8x22B](https://mistral.ai/)** | Mistral AI | 大規模Mixture-of-Experts、高速推論 / Large MoE, fast inference | ◎（Ollama, LM Studio） | 大規模教育・研究用途 |
| **[Mistral 7B / Mixtral 8x7B](https://mistral.ai/)** | Mistral AI | 小型・高精度・推論高速 / Small, accurate, fast | ◎ | 教育現場のローカルAI構築に有用 |
| **OpenChat / Dolphin / MythoMax** | コミュニティ | 調整済みLLM / Fine-tuned LLMs | ◎ | GPT代替モデル検証に適 |
| **[Open Assistant (OASST)](https://open-assistant.io/)** | LAION | OSS対話型AI開発プロジェクト / OSS conversational AI | ◎ | 商用不可制限あり |

---

## 🎨 生成メディア系モデル / Generative Media Models

| モデル名 / Model | 提供元 / Provider | 特徴 / Features | 用途例 / Example Uses |
|------------------|-------------------|-----------------|-----------------------|
| **[Tencent Hunyuan3D-2.0](https://www.tencent.com/)** | Tencent | 高速3D生成、30秒以内 / Fast 3D generation under 30s | 教材ビジュアル・設計3D |
| **[Runway Gen-3](https://runwayml.com/)** | Runway | 高品質動画生成 / High-quality video generation | 教育動画・研究発表 |
| **[Pika Labs](https://pika.art/)** | Pika Labs | スタートアップ型動画生成 / Startup-style video generation | 短尺教材・SNS用映像 |

---

## 🔍 情報検索・速報性特化モデル / Search & Real-time Focused Models

| モデル名 / Model | 提供元 / Provider | 特徴 / Features | 用途例 / Example Uses |
|------------------|-------------------|-----------------|-----------------------|
| **[Perplexity AI](https://www.perplexity.ai/)** | Perplexity | 高速検索、出典付き回答 / Fast search, cited answers | 技術調査・資料収集 |
| **[Grok 1.5](https://x.ai/)** | xAI（Elon Musk） | X（旧Twitter）統合型 / Integrated with X (Twitter) | SNS動向・速報収集 |

---

## 🔗 備考とライセンス / Notes & License

- 本リストは **2025年9月時点** の情報に基づく / Based on September 2025 info  
- OSSモデル実行には [Ollama](https://ollama.com/)、[LM Studio](https://lmstudio.ai/)、[Hugging Face Transformers](https://huggingface.co/docs) などの環境が必要  
- 各ツールのライセンス条件（商用利用可否、API連携可否）は個別確認が必要 / Check license terms individually  
- ハードウェア面では **NVIDIA Rubin CPX**（2026予定）が生成AI向けに発表済み

> Edusemi-Plusでは、**ChatGPT（構成）＋ Gemini（検索）＋ Claude（整形）** を中核とし、他モデルは補助・実験・教育現場向けに活用しています。

---

## 🔙 戻る / Back
- **JP:** [AIツール比較と使い分けガイドへ戻る](./README.md)  
- **EN:** [Return to AI Tools Comparison Guide](./README.md)
