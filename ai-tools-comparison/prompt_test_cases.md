---
layout: default
title: 🧪 AI別プロンプト比較演習ログ（ChatGPT / Gemini / Claude）
---

---

# 🧪 AI別プロンプト比較演習ログ（ChatGPT / Gemini / Claude）  
**Prompt Comparison Exercises by AI (ChatGPT / Gemini / Claude)**

本資料は、同一プロンプトを複数の生成AIに入力し、**出力内容・傾向・強み／弱み** を比較した記録です。  
Edusemi-Plus における **教材作成・PoC設計・情報調査** において、最適なAI選定の参考となります。  
This document compares **responses, tendencies, strengths, and weaknesses** of multiple AI models for the same prompts.

---

## 🧠 テストケース 01：TSMCの地政学的位置づけ / Geopolitical Importance of TSMC

> **プロンプト / Prompt:**  
> 「TSMCがなぜ地政学的に重要な企業とされているのか、半導体供給網との関連で説明してください。」  
> "Explain why TSMC is considered geopolitically important, in relation to the semiconductor supply chain."

| AI | 回答要点 / Key Points | 傾向・評価 / Trend & Evaluation |
|----|----------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 台湾・米中対立・先端ノード供給拠点・米国/日本進出・リスク集中 | ◎ 論理構成と説明力が高く教材化に最適 |
| **Gemini (2.5 Pro / Flash)** | 米中関係・CHIPS法・海外拠点・NVIDIA関連・Deep Thinkで因果整理 | ◎ 最新動向＋因果推論に強い |
| **Claude (3 Opus)** | 経済安全保障・リスク分散・外交的影響 | ◎ 丁寧で読みやすい要約文 |

---

## 💡 テストケース 02：教材構成案の改善 / Improve Teaching Material Outline

> **入力構成（省略） / Input outline omitted**

| AI | 出力傾向 / Output Trend | 傾向・評価 / Trend & Evaluation |
|----|------------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 見出し構造と論理展開が優秀、図解も提案 | ◎ 教材構成力に優れる |
| **Gemini (2.5)** | Markdown可能だが構造が不安定、情報は最新 | ◯ 最新性補完に有用 |
| **Claude (3 Opus)** | 文が丁寧だが構成力控えめ | ◯ 整形に最適 |

---

## 📘 テストケース 03：技術資料の200字要約 / 200-Character Technical Summary

> **技術資料例（省略） / Technical doc omitted**

| AI | 出力傾向 / Output Trend | 傾向・評価 / Trend & Evaluation |
|----|------------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 要点抽出は得意だが削りすぎる場合あり | ◯ 安定だが調整必要 |
| **Gemini (2.5)** | 自然な表現だが情報過多傾向 | ◯ 短縮にはやや不向き |
| **Claude (3 Opus)** | 自然かつ指定字数内で要約 | ◎ 圧縮と丁寧さを両立 |

---

## 🎓 テストケース 04：FSM制御教材設計 / FSM Control Teaching Material

> **プロンプト / Prompt:**  
> 「FSM制御とは何か、自動ドアを例に教育教材を構成してください。」  
> "Explain FSM control with an example (automatic door) and structure it as teaching material."

| AI | 出力傾向 / Output Trend | 傾向・評価 / Trend & Evaluation |
|----|------------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 見出し＋例＋図解を含む教材 | ◎ 教育設計に最適 |
| **Gemini (2.5)** | 概要説明＋例だが浅め | △ 深掘り不足 |
| **Claude (3 Opus)** | 長文説明で優しい文体 | ◯ 読みやすさ◎ |

---

## 📰 テストケース 05：最新ニュース要約 / Latest News Summary

> **プロンプト / Prompt:**  
> 「最新の半導体業界ニュースを200字で要約してください。」  
> "Summarize the latest semiconductor industry news in 200 characters."

| AI | 出力傾向 / Output Trend | 傾向・評価 / Trend & Evaluation |
|----|------------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 構成は明快だが最新性に限界 | ◯ 背景解説に有用 |
| **Gemini (2.5)** | 最新記事を参照、Deep Thinkで要点整理 | ◎ 最新ニュース要約に最適 |
| **Claude (3 Opus)** | ニュース文調で要約、安定 | ◯ 報告文として適切 |

---

## 🛠 テストケース 06：コード生成（FSM/PID PoC） / Code Generation (FSM/PID PoC)

> **プロンプト / Prompt:**  
> 「FSM＋PID制御を組み合わせたPoC用のPythonコードを生成してください。」  
> "Generate Python code for a PoC combining FSM and PID control."

| AI | 出力傾向 / Output Trend | 傾向・評価 / Trend & Evaluation |
|----|------------------------|----------------------------------|
| **ChatGPT (GPT-5)** | 全体構造＋コメント充実、実行可能性高い | ◎ PoC設計に最適 |
| **Gemini (2.5)** | コードは出るが細部不安定 | △ 簡易検証向き |
| **Claude (3 Opus)** | 説明丁寧、コードはシンプル | ◯ 学習用に最適 |
| **DeepSeek Coder V3** | 高速かつ高精度のコード生成 | ◎ 実装検証に最適 |

---

## 📝 備考と活用法 / Notes & Usage

- **評価軸 / Evaluation axes:** 構成力 / 丁寧さ / 情報量 / 応答安定性 / 最新性  
- 授業・研修・PoC評価教材として活用可能  
- 新しいプロンプトを追加する際は形式統一  
- OSSモデルやエージェント連携（ChatGPT＋Gemini）も今後検証対象に追加予定

> 本演習ログは **2025年9月時点** のモデル性能に基づく  
> 詳細は [README.md](./README.md) および [ai_selection_guide.md](./ai_selection_guide.md) を参照

---

## 🔙 戻る / Back
- **JP:** [AIツール比較と使い分けガイドへ戻る](./README.md)  
- **EN:** [Return to AI Tools Comparison Guide](./README.md)
