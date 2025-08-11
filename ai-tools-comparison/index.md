---
layout: default
title: AIツール比較と使い分けガイド（Edusemi-Plus版 / AI Tools Comparison & Usage Guide）
---

---

# 🤖 AIツール比較と使い分けガイド（Edusemi-Plus版）  
**AI Tools Comparison & Usage Guide (Edusemi-Plus Edition)**

Edusemi-Plusでは、半導体技術の教育・設計・調査・教材作成において、生成AIを効果的に活用しています。  
This guide compares the main AI tools and helps you quickly decide **which tool to use in which situation**.

---

## 🧩 三位一体型AI活用構成（推奨） / Recommended "Trinity" AI Setup

| 役割 / Role | 使用AI / Tool | 得意分野 / Strengths | 主な用途 / Main Uses |
|-------------|---------------|----------------------|----------------------|
| 🧠 **メイン：構成・生成 / Main – Structuring & Generation** | [ChatGPT 4o](https://chat.openai.com/) | 教材設計、論理構成、PoC設計、Markdown出力 / Curriculum design, logical structuring, PoC design, Markdown output | 教材化、技術文書、演習生成 / Educational materials, technical docs, exercises |
| 🔍 **補佐①：検索・要点収集 / Support 1 – Search & Summarization** | [Gemini 1.5 Pro](https://gemini.google.com/) | Web検索、YouTube要約、最新動向把握 / Web search, YouTube summarization, latest trends | 地政学・企業動向調査、参考情報取得 / Geopolitical & corporate research, info gathering |
| ✒️ **補佐②：文章推敲・整形 / Support 2 – Polishing & Editing** | [Claude 3 Opus](https://claude.ai/) | 丁寧な言い換え、構文整理、長文圧縮 / Polite rephrasing, syntax refinement, summarization | レポート整形、読みやすさ改善、校正 / Report polishing, readability improvement, proofreading |

> **運用ポイント / Tip:**  
> この「三位一体構成」は **ChatGPTの構成力 × Geminiの情報力 × Claudeの文章力** を掛け合わせた高効率モデルです。

---

## ✅ 用途別 推奨AI早見表 / Quick Reference by Use Case

| やりたいこと / Task | 推奨AI / Recommended Tool | 補足 / Notes |
|--------------------|---------------------------|--------------|
| 教材を構成・生成したい / Create & structure learning materials | **ChatGPT** | Markdownや図解に強く、構成が安定 / Strong at Markdown & diagrams |
| 最新の技術・地政学動向を調べたい / Research latest tech or geopolitics | **Gemini** | Google検索とYouTube理解が武器 / Leverages Google Search & YouTube parsing |
| 文章を丁寧に直したい / Polish reports | **Claude** | 長文要約・言い換え・丁寧語に強い / Strong in rephrasing & summarizing |
| YouTube講義動画を教材化したい / Convert YouTube lectures to materials | **Gemini → ChatGPT** | Geminiで要約 → ChatGPTで整形 / Summarize with Gemini, format with ChatGPT |
| 技術報告書を提出用に整えたい / Finalize technical reports | **ChatGPT → Claude** | ChatGPTで構成 → Claudeで仕上げ / Structure with ChatGPT, refine with Claude |
| コードや設計レビューをしたい / Review code & designs | **ChatGPT** | PoC構成やFSM生成にも対応可 / Also handles PoC & FSM generation |

---

## 🌐 その他AIツールの位置づけ（補足） / Other AI Tools Overview

| モデル名 / Model | 主な用途 / Main Use | 備考 / Notes |
|------------------|---------------------|--------------|
| [DeepSeek](https://deepseek.com/) | コーディング特化 / Coding-focused | 高精度・中国系モデルとして急成長 / High-accuracy, China-based |
| [Perplexity](https://www.perplexity.ai/) | 検索特化LLM / Search-oriented LLM | 出典付き要約に便利 / Good for sourced summaries |
| [Mistral](https://mistral.ai/) / [LLaMA 3](https://ai.meta.com/llama/) | OSS研究／ローカル運用 / OSS research & local deployment | [Ollama](https://ollama.com/)等で実行可 / Can run locally |
| [Grok](https://x.ai/) | SNS連携・速報性 / Social media integration & speed | X（旧Twitter）連動型 / Integrated with X (Twitter) |

詳細は [`ai_models_list.md`](./ai_models_list.md) を参照 / See [`ai_models_list.md`](./ai_models_list.md) for details.

---

## 📁 本ディレクトリ構成 / Directory Structure

| ファイル / File | 内容 / Description |
|-----------------|--------------------|
| [`README.md`](./README.md) | このページ：AIツールの比較・使い分けガイド / This guide |
| [`ai_models_list.md`](./ai_models_list.md) | 主要LLMモデルの一覧比較（OSS含む） / Main LLM models list |
| [`ai_selection_guide.md`](./ai_selection_guide.md) | 用途別おすすめAIチャート（印刷向け） / AI selection chart |
| [`prompt_test_cases.md`](./prompt_test_cases.md) | AI別の回答比較演習 / AI response comparison |
| [`usecase_examples.md`](./usecase_examples.md) | 実用例集（教材・レビュー・分析） / Practical examples |

---

## 👤 **著者・ライセンス / Author & License**

| **項目 / Item** | **内容 / Details** |
|-----------------|--------------------|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **GitHub** | [Samizo-AITL](https://github.com/Samizo-AITL) |
| **Email** | [shin3t72@gmail.com](mailto:shin3t72@gmail.com) |
| **ライセンス / License** | MIT License（再配布・改変自由） / Redistribution & modification allowed |

---

## 🔙 戻る / Back
- **JP:** [Edusemi-Plus トップへ戻る](../index.md)  
- **EN:** [Return to Edusemi-Plus Top](../index.md)
