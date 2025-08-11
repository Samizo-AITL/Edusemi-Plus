---
layout: default
title: 📘 ChatGPT × Gemini × Claude 活用事例集（Edusemi-Plus版）
---

---

# 📘 ChatGPT × Gemini × Claude 活用事例集（Edusemi-Plus版）  
**Practical Use Cases of ChatGPT × Gemini × Claude (Edusemi-Plus Edition)**

本資料は、Edusemi-Plus における **教材設計・技術支援・調査分析** において、  
ChatGPT（GPT-4o）を中心に **Gemini（検索補佐）**、**Claude（文章整形）** を組み合わせて活用する実例集です。  
This document provides practical examples of combining ChatGPT (GPT-4o) with Gemini (search assistant) and Claude (text refinement) in **teaching, technical support, and research**.

---

## 🧠 事例01：半導体教材の生成と演習問題作成  
**Case 01: Generating Semiconductor Teaching Material with Exercises**

**タスク概要 / Task Overview:**  
大学生向け「TSMCと先端半導体技術」教材を作成し、演習問題を付加する。  
Create a university-level material on "TSMC and Advanced Semiconductor Technology" with exercises.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 情報収集 / Info Gathering | **Gemini** | TSMC最新技術・工場戦略・競合状況を検索 / Search latest tech, fab strategies, competitors |
| 教材構成 / Structure Design | **ChatGPT** | 章立て・要点整理・Mermaid図生成 / Chapter outline, key points, Mermaid diagrams |
| 演習生成 / Exercise Creation | **ChatGPT** | 選択式・記述式問題を自動生成 / Auto-generate MCQs and descriptive questions |
| 表現整形 / Refinement | **Claude** | 文体を丁寧化し読みやすく編集 / Make text polite and readable |

---

## 🎛 事例02：FSM制御教材のPoC支援  
**Case 02: PoC Support for FSM Control Teaching Material**

**タスク概要 / Task Overview:**  
自動ドアのFSM教材を構成し、状態遷移図と演習問題を作成する。  
Design an FSM teaching material for automatic doors, including a state diagram and exercises.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 初期設計 / Initial Design | **ChatGPT** | 状態一覧・遷移条件を定義しMermaid形式で出力 / Define states & transitions in Mermaid format |
| 検証補助 / Validation Support | **Gemini** | FSM事例を収集・代表例抽出 / Collect & extract representative FSM cases |
| 整形 / Polishing | **Claude** | 演習問題と解説を丁寧に編集 / Edit exercises & explanations in polite language |

---

## 🌍 事例03：地政学×半導体の分析レポート作成  
**Case 03: Geopolitics × Semiconductor Analysis Report**

**タスク概要 / Task Overview:**  
「米中半導体摩擦とTSMCの位置づけ」に関する技術調査レポートを作成。  
Create a technical report on "US-China Semiconductor Tensions and TSMC's Position."

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 時事情報収集 / News Gathering | **Gemini** | 米中規制・CHIPS法・工場動向を検索 / Search US-China regulations, CHIPS Act, fab updates |
| 初稿作成 / Draft Creation | **ChatGPT** | Markdown構成で要点整理 / Summarize in Markdown |
| 文章仕上げ / Final Editing | **Claude** | 論文調に整形 / Refine into academic style |

---

## 📹 事例04：YouTube講義を教材に変換  
**Case 04: Converting YouTube Lectures into Teaching Material**

**タスク概要 / Task Overview:**  
YouTubeの半導体講義（英語）を日本語教材として再構成。  
Reconstruct an English YouTube semiconductor lecture into Japanese teaching material.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 動画要約 / Video Summary | **Gemini** | 要点・セクション抽出 / Extract key points & sections |
| 教材構成 / Structure Design | **ChatGPT** | 構成案と演習問題生成 / Create outline & exercises |
| 言い換え整形 / Language Simplification | **Claude** | 難解文を平易化 / Simplify complex sentences |

---

## 📄 事例05：社内技術報告書の作成と推敲  
**Case 05: Creating and Refining Internal Technical Reports**

**タスク概要 / Task Overview:**  
設計レビュー結果をわかりやすく報告書化。  
Summarize design review results into an easy-to-read report.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 構成下書き / Draft Structure | **ChatGPT** | 箇条書き→章構成化 / Convert bullet points to chapter structure |
| 用語補完 / Term Verification | **Gemini** | API仕様・規格出典確認 / Verify API specs & standards |
| 文体整形 / Style Refinement | **Claude** | 誤解防止・丁寧化 / Avoid ambiguity, make polite |

---

## 🔖 まとめ：三位一体の活用パターン  
**Summary: Three-in-One Usage Patterns**

| パターン / Pattern | 主体 / Main AI | 補佐1 / Search Assist | 補佐2 / Refinement | 想定ユースケース / Use Case |
|--------------------|---------------|-----------------------|--------------------|-----------------------------|
| 教材生成型 / Teaching Material | ChatGPT | Gemini | Claude | 授業資料・演習教材 / Class materials |
| 調査報告型 / Research Report | ChatGPT | Gemini | Claude | 技術レポート / Technical reports |
| コード支援型 / Code Support | ChatGPT | DeepSeek / Gemini | Claude | FSM / PoCレビュー / FSM & PoC reviews |
| 動画活用型 / Video Utilization | Gemini | ChatGPT | Claude | YouTube教材化 / YouTube-to-material |
| 推敲改善型 / Text Polishing | ChatGPT | (Optional) | Claude | 報告書整形 / Report polishing |

---

## 📎 関連資料 / Related Docs
- [README.md](./README.md)
- [ai_models_list.md](./ai_models_list.md)
- [ai_selection_guide.md](./ai_selection_guide.md)
- [ai_prompt_log.md](./ai_prompt_log.md)

---

## 🔙 戻る / Back
- **JP:** [AIツール比較と使い分けガイドへ戻る](./README.md)  
- **EN:** [Return to AI Tools Comparison Guide](./README.md)
