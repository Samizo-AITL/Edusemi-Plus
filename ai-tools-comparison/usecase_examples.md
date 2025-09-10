---
layout: default
title: 📘 ChatGPT × Gemini × Claude 活用事例集（Edusemi-Plus版）
---

---

# 📘 ChatGPT × Gemini × Claude 活用事例集（Edusemi-Plus版）  
**Practical Use Cases of ChatGPT × Gemini × Claude (Edusemi-Plus Edition)**

本資料は、Edusemi-Plus における **教材設計・技術支援・調査分析** において、  
ChatGPT（GPT-5）を中心に **Gemini 2.5（検索補佐）**、**Claude 3 Opus（文章整形）** を組み合わせて活用する実例集です。  
This document provides practical examples of combining **ChatGPT (GPT-5)** with **Gemini 2.5 (search assistant)** and **Claude 3 Opus (text refinement)** in **teaching, technical support, and research**.

---

## 🧠 事例01：半導体教材の生成と演習問題作成  
**Case 01: Generating Semiconductor Teaching Material with Exercises**

**タスク概要 / Task Overview:**  
大学生向け「TSMCと先端半導体技術」教材を作成し、演習問題を付加する。  
Create a university-level material on "TSMC and Advanced Semiconductor Technology" with exercises.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 情報収集 / Info Gathering | **Gemini 2.5** | TSMC最新技術・工場戦略・競合状況を検索 |
| 教材構成 / Structure Design | **ChatGPT GPT-5** | 章立て・要点整理・Mermaid図生成 |
| 演習生成 / Exercise Creation | **ChatGPT GPT-5** | 選択式・記述式問題を自動生成 |
| 表現整形 / Refinement | **Claude 3 Opus** | 文体を丁寧化し読みやすく編集 |

---

## 🎛 事例02：FSM制御教材のPoC支援  
**Case 02: PoC Support for FSM Control Teaching Material**

**タスク概要 / Task Overview:**  
自動ドアのFSM教材を構成し、状態遷移図と演習問題を作成する。  
Design an FSM teaching material for automatic doors, including a state diagram and exercises.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 初期設計 / Initial Design | **ChatGPT GPT-5** | 状態一覧・遷移条件を定義しMermaid形式で出力 |
| 検証補助 / Validation Support | **Gemini 2.5** | FSM事例を収集・代表例抽出 |
| 整形 / Polishing | **Claude 3 Opus** | 演習問題と解説を丁寧に編集 |

---

## 🌍 事例03：地政学×半導体の分析レポート作成  
**Case 03: Geopolitics × Semiconductor Analysis Report**

**タスク概要 / Task Overview:**  
「米中半導体摩擦とTSMCの位置づけ」に関する技術調査レポートを作成。  
Create a technical report on "US-China Semiconductor Tensions and TSMC's Position."

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 時事情報収集 / News Gathering | **Gemini 2.5** | 米中規制・CHIPS法・工場動向を検索 |
| 初稿作成 / Draft Creation | **ChatGPT GPT-5** | Markdown構成で要点整理 |
| 文章仕上げ / Final Editing | **Claude 3 Opus** | 論文調に整形 |

---

## 📹 事例04：YouTube講義を教材に変換  
**Case 04: Converting YouTube Lectures into Teaching Material**

**タスク概要 / Task Overview:**  
YouTubeの半導体講義（英語）を日本語教材として再構成。  
Reconstruct an English YouTube semiconductor lecture into Japanese teaching material.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 動画要約 / Video Summary | **Gemini 2.5** | 要点・セクション抽出 |
| 教材構成 / Structure Design | **ChatGPT GPT-5** | 構成案と演習問題生成 |
| 言い換え整形 / Language Simplification | **Claude 3 Opus** | 難解文を平易化 |

---

## 📄 事例05：社内技術報告書の作成と推敲  
**Case 05: Creating and Refining Internal Technical Reports**

**タスク概要 / Task Overview:**  
設計レビュー結果をわかりやすく報告書化。  
Summarize design review results into an easy-to-read report.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 構成下書き / Draft Structure | **ChatGPT GPT-5** | 箇条書き→章構成化 |
| 用語補完 / Term Verification | **Gemini 2.5** | API仕様・規格出典確認 |
| 文体整形 / Style Refinement | **Claude 3 Opus** | 誤解防止・丁寧化 |

---

## 🎨 事例06：生成メディアを用いた教材強化  
**Case 06: Enhancing Teaching Materials with Generative Media**

**タスク概要 / Task Overview:**  
RunwayやHunyuan3Dを使って教材ビジュアルや短尺動画を作成。  
Use Runway or Hunyuan3D to create visuals and short videos for teaching.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| 3Dモデル生成 / 3D Model Generation | **Hunyuan3D-2.0** | 半導体装置やチップの3D教材化 |
| 映像生成 / Video Generation | **Runway Gen-3** | 教材用短尺動画を生成 |
| 構成統合 / Integration | **ChatGPT GPT-5** | 教材テキストと連携、演習と組合せ |

---

## 🛠 事例07：コードPoC生成とレビュー  
**Case 07: Code PoC Generation & Review**

**タスク概要 / Task Overview:**  
FSM×PIDを組み合わせた制御PoCコードを作成・レビュー。  
Generate and review PoC code combining FSM & PID control.

| 工程 / Step | 使用AI / AI Used | 活用内容 / Usage |
|-------------|-----------------|------------------|
| コード生成 / Code Generation | **ChatGPT GPT-5 / DeepSeek Coder V3** | 実行可能なPythonコード生成 |
| 検証 / Validation | **Gemini 2.5** | 仕様・APIの確認 |
| 整形 / Polishing | **Claude 3 Opus** | コメント・可読性改善 |

---

## 🔖 まとめ：三位一体＋拡張活用パターン  
**Summary: Three-in-One + Extended Usage Patterns**

| パターン / Pattern | 主体 / Main AI | 補佐1 / Search Assist | 補佐2 / Refinement | 想定ユースケース / Use Case |
|--------------------|---------------|-----------------------|--------------------|-----------------------------|
| 教材生成型 / Teaching Material | ChatGPT GPT-5 | Gemini 2.5 | Claude 3 Opus | 授業資料・演習教材 |
| 調査報告型 / Research Report | ChatGPT GPT-5 | Gemini 2.5 | Claude 3 Opus | 技術レポート |
| コード支援型 / Code Support | ChatGPT GPT-5 | DeepSeek V3 / Gemini 2.5 | Claude 3 Opus | FSM / PoCレビュー |
| 動画活用型 / Video Utilization | Gemini 2.5 | ChatGPT GPT-5 | Claude 3 Opus | YouTube教材化 |
| メディア生成型 / Media Creation | Hunyuan3D / Runway | ChatGPT GPT-5 | Claude 3 Opus | 3D・動画教材 |
| 推敲改善型 / Text Polishing | ChatGPT GPT-5 | (Optional) | Claude 3 Opus | 報告書整形 |

---

## 📎 関連資料 / Related Docs
- [README.md](./README.md)
- [ai_models_list_2025.md](./ai_models_list_2025.md)
- [ai_selection_guide_2025.md](./ai_selection_guide_2025.md)
- [prompt_test_cases_2025.md](./prompt_test_cases_2025.md)

---

## 🔙 戻る / Back
- **JP:** [AIツール比較と使い分けガイドへ戻る](./README.md)  
- **EN:** [Return to AI Tools Comparison Guide](./README.md)
