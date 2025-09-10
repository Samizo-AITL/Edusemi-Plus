---
layout: default
title: AIツール比較と使い分けガイド（Edusemi-Plus版 / AI Tools Comparison & Usage Guide）
---

---

# 🤖 AIツール比較と使い分けガイド（Edusemi-Plus版）  
**AI Tools Comparison & Usage Guide (Edusemi-Plus Edition)**

Edusemi-Plusでは、半導体技術の教育・設計・調査・教材作成において、生成AIを効果的に活用しています。  
This guide compares the main AI tools and helps you quickly decide **which tool to use in which situation**.  
📌 Update: 2025/09

---

## 🧩 三位一体型AI活用構成（推奨） / Recommended "Trinity" AI Setup

| 役割 / Role | 使用AI / Tool | 得意分野 / Strengths | 主な用途 / Main Uses |
|-------------|---------------|----------------------|----------------------|
| 🧠 **メイン：構成・生成** | [ChatGPT GPT-5](https://chat.openai.com/) | 高度な推論・教材設計・PoC設計・Markdown出力 | 教材化、技術文書、演習生成 |
| 🔍 **補佐①：検索・要点収集** | [Gemini 2.5 Pro / Flash](https://gemini.google.com/) | Web検索、YouTube要約、最新動向、深い推論 | 地政学・企業動向調査、参考情報取得 |
| ✒️ **補佐②：文章推敲・整形** | [Claude 3 Opus](https://claude.ai/) | 丁寧な言い換え、構文整理、長文圧縮 | レポート整形、読みやすさ改善、校正 |

> **Tip:** ChatGPTの構成力 × Geminiの情報力 × Claudeの文章力 を掛け合わせた三位一体モデル。

### 🔗 フロー図
```mermaid
flowchart LR
    Gemini["Gemini 2.5 (Search & Summarize)"]
    ChatGPT["ChatGPT GPT-5 (Structure & Generate)"]
    Claude["Claude 3 Opus (Polish & Edit)"]

    Gemini --> ChatGPT --> Claude
```

---

## ✅ 用途別 推奨AI早見表

| Task | Tool | Notes |
|------|------|-------|
| 教材を構成・生成 | **ChatGPT GPT-5** | Markdownや図解に強い |
| 最新動向調査 | **Gemini 2.5** | Google検索・YouTube解析 |
| レポートを整形 | **Claude 3 Opus** | 長文要約・言い換え |
| YouTube講義 → 教材 | **Gemini → ChatGPT** | 要約→整形 |
| 技術報告書の仕上げ | **ChatGPT → Claude** | 構成→推敲 |
| コード/設計レビュー | **ChatGPT GPT-5** | FSM・PoC対応 |
| 3D教材ビジュアル | **Tencent Hunyuan3D / Runway Gen-3** | 高品質3D・映像 |
| PoC検証をAIエージェント化 | **ChatGPT + Gemini** | 状態遷移・シナリオ探索 |

---

## 🌐 その他AIツール

| Model | Main Use | Notes |
|-------|----------|-------|
| DeepSeek | コーディング・研究 | 中国系で急成長 |
| Perplexity | 検索特化LLM | 出典付き要約 |
| Mistral / LLaMA 3 | OSS研究/ローカル運用 | Ollama等で実行可 |
| Le Chat (Mistral) | エージェント型対話 | 企業利用に拡張中 |
| Quickplay AI Studio | 動画編集・短尺生成 | 放送・マーケ向け |
| Grok | SNS連携 | X(Twitter)連動型 |

---

## 📁 本ディレクトリ構成 / Directory Structure

| ファイル / File | 内容 / Description |
|-----------------|--------------------|
| [README.md](./README.md) | このページ：AIツール比較・使い分けガイド |
| [ai_models_list_2025.md](./ai_models_list_2025.md) | 主要AIモデル一覧と特徴 |
| [ai_selection_guide_2025.md](./ai_selection_guide_2025.md) | 用途別AIツール選択ガイド |
| [prompt_test_cases_2025.md](./prompt_test_cases_2025.md) | AI別プロンプト比較演習ログ |
| [usecase_examples_2025.md](./usecase_examples_2025.md) | 実用事例集（教材・レビュー・分析） |
| [ai_agents_examples.md](./ai_agents_examples.md) | FSM×LLM×PIDエージェント活用事例 |

---

## 👤 著者・ライセンス

| Item | Detail |
|------|--------|
| Author | 三溝 真一（Shinichi Samizo） |
| GitHub | [Samizo-AITL](https://github.com/Samizo-AITL) |
| Email | [shin3t72@gmail.com](mailto:shin3t72@gmail.com) |
| License | MIT License |

---

## 🔙 戻る / Back
- **JP:** [Edusemi-Plus トップへ戻る](../index.md)  
- **EN:** [Return to Edusemi-Plus Top](../index.md)
