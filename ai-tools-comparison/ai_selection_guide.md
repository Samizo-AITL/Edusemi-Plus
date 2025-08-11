---
layout: default
title: 🧭 用途別AIツール選択ガイド（Edusemi-Plus版 / AI Tool Selection Guide by Use Case）
---

---

# 🧭 用途別AIツール選択ガイド（Edusemi-Plus版）  
**AI Tool Selection Guide by Use Case (Edusemi-Plus)**

本資料は、Edusemi-Plus における **半導体技術教育・教材作成・設計レビュー・PoC支援** の各シーンで、  
目的別に「どの生成AIツールを使うべきか」を整理した早見表です。  
This guide shows **which AI tool to use for each purpose** in the context of **semiconductor education, material creation, design review, and PoC** in Edusemi-Plus.

---

## ✅ 教育・教材作成 / Education & Material Creation

| 目的 / Purpose | 推奨AI / Recommended AI | 理由・補足 / Reason & Notes |
|----------------|------------------------|-----------------------------|
| 教材の構成設計（章立て・流れ） / Curriculum & flow design | **[ChatGPT](https://chat.openai.com/)** | 論理構成・Markdown・演習問題生成に強い / Strong in logic, Markdown, exercises |
| 授業用スライドの要点抽出 / Key point extraction for slides | ChatGPT → [Claude](https://claude.ai/) | ChatGPTで内容生成 → Claudeで整形 / Generate with ChatGPT, polish with Claude |
| YouTube講義から教材化 / Create materials from lectures | **[Gemini](https://gemini.google.com/) → ChatGPT** | Geminiで動画要約 → ChatGPTで構成 / Gemini summary → ChatGPT structuring |
| 演習問題（選択式・記述式）作成 / Exercise creation | **ChatGPT** | 出力形式とレベル調整が容易 / Flexible format & difficulty |
| 教材の文体・丁寧化 / Polishing style | **Claude** | 冗長→簡潔、柔らかい表現化に適 / Great for concise & polite rephrasing |

---

## 🛠 設計・レビュー・PoC支援 / Design, Review & PoC Support

| 目的 / Purpose | 推奨AI / Recommended AI | 理由・補足 / Reason & Notes |
|----------------|------------------------|-----------------------------|
| FSM／PID制御の設計構成 / FSM & PID design structure | **ChatGPT** | 設計テンプレート生成・構成力◎ / Template generation & strong structure |
| コードの添削・リファクタ / Code review & refactoring | ChatGPT / [DeepSeek](https://deepseek.com/) | ChatGPTは安定、DeepSeekは高速高精度 / ChatGPT stable, DeepSeek fast & accurate |
| 技術資料（報告書）の初稿 / Draft technical reports | **ChatGPT** | 要点→構成→文書化を一貫可能 / Consistent from outline to document |
| 技術資料の仕上げ / Final polish | **Claude** | 丁寧語化・誤解のない表現 / Polite & clear phrasing |
| 外部仕様やAPI仕様確認 / API & spec check | **Gemini / [Perplexity](https://www.perplexity.ai/)** | 最新・公式情報に強い / Strong for up-to-date official info |

---

## 🌍 情報調査・トレンド収集 / Research & Trend Tracking

| 目的 / Purpose | 推奨AI / Recommended AI | 理由・補足 / Reason & Notes |
|----------------|------------------------|-----------------------------|
| 地政学・産業動向の最新調査 / Geopolitical & industry trends | **Gemini** | Google検索＋要約が優秀 / Excellent search + summary |
| 企業戦略・発表会の要点取得 / Corporate strategy briefings | **Gemini（YouTube連携）** | 動画要約・リンク検索に最適 / Best for video summary & link search |
| 技術論文・記事比較 / Compare technical papers | Gemini / Perplexity | 出典提示型LLM / Cited-answer LLM |
| SNS上の技術話題収集 / Social tech topic scraping | **[Grok](https://x.ai/)** | X（旧Twitter）上の動向取得に便利 / Great for X(Twitter) trend scraping |

---

## 📘 文書整形・言語表現 / Document Editing & Language Style

| 目的 / Purpose | 推奨AI / Recommended AI | 理由・補足 / Reason & Notes |
|----------------|------------------------|-----------------------------|
| 冗長文の短縮・圧縮 / Shortening text | **Claude** | 情報保持しつつ短く自然に / Keeps info, makes concise |
| 報告書・論文の推敲 / Report & paper polishing | **Claude** | 丁寧語・論理性・自然文調 / Politeness, logical clarity |
| 外国語文書の構成チェック / Foreign doc structure check | Claude / ChatGPT | Claudeは自然文、ChatGPTは構成力◎ / Claude for natural text, ChatGPT for structure |

---

## 🎓 学習支援・演習 / Learning Support & Exercises

| 目的 / Purpose | 推奨AI / Recommended AI | 理由・補足 / Reason & Notes |
|----------------|------------------------|-----------------------------|
| 用語説明 / Term explanation | ChatGPT / Gemini | ChatGPTは例示豊富、Geminiは出典付き / ChatGPT rich examples, Gemini with sources |
| 課題のヒント・解法導出 / Homework hints | ChatGPT | 段階的誘導が可能 / Step-by-step guidance |
| 自己チェックQ&A作成 / Self-check Q&A | ChatGPT | カスタム問題生成が得意 / Good at custom Q&A generation |

---

## 🔖 備考 / Notes

- 本表は **2025年7月時点** のモデル性能に基づく / Based on July 2025 model performance  
- 教育・研究・PoC用途では **ChatGPT＋Claude＋Gemini** 三位一体構成が最も実用的  
- OSSモデル（LLaMA3, Mistral等）は補助・ローカル運用として別途整理 / OSS models listed separately  

> 詳細は [README.md](./README.md) と [ai_models_list.md](./ai_models_list.md) を参照してください。  
> See also [README.md](./README.md) and [ai_models_list.md](./ai_models_list.md) for more.

---

## 🔙 戻る / Back
- **JP:** [AIツール比較と使い分けガイドへ戻る](./README.md)  
- **EN:** [Return to AI Tools Comparison Guide](./README.md)
