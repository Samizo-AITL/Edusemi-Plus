---
layout: default
title: "PCB | プリント基板"
---

---

# 📐 PCB / プリント基板  
*Printed Circuit Boards (PCB)*  

---

## 🔗 リンク / Links

| Link | Badge |
|---|---|
| 🌐 View Site | [![View Site](https://img.shields.io/badge/View-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/PCB/) |
| 📂 View Repo | [![View Repo](https://img.shields.io/badge/View-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration/PCB) |

---

## 📖 概要 / Overview
PCBは電子部品を実装する基板で、電気的・機械的な統合を担う。  
*PCBs are the platform for mounting components, enabling electrical and mechanical integration.*  

---

## 📂 ファイル一覧 / File List (Auto on GitHub Pages)
> この一覧は **GitHub Pages でビルド時に自動生成** されます（GitHub上のREADMEではLiquidは展開されません）。

{% assign dir = "Assembly-Integration/PCB/" %}

<!-- ページ（Markdown等） -->
{% for page in site.pages %}
  {% if page.path contains dir and page.name != "README.md" %}
- [{{ page.title | default: page.name }}]({{ site.url }}{{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}

<!-- 静的ファイル（画像・PDF等） -->
{% for file in site.static_files %}
  {% if file.path contains dir and file.name != "README.md" %}
- [{{ file.name }}]({{ site.url }}{{ site.baseurl }}{{ file.path }})
  {% endif %}
{% endfor %}

---

## 👤 著者・ライセンス / Author & License

| **項目 / Item** | **内容 / Details** |
|-----------------|--------------------|
| **著者 / Author** | 三溝 真一（Shinichi Samizo） |
| **Email** | [![Email](https://img.shields.io/badge/Email-shin3t72%40gmail.com-red?style=flat&logo=gmail)](mailto:shin3t72@gmail.com) |
| **X** | [![X](https://img.shields.io/badge/X-@shin3t72-black?style=flat&logo=x)](https://x.com/shin3t72) |
| **GitHub** | [![GitHub](https://img.shields.io/badge/GitHub-Samizo--AITL-blue?style=flat&logo=github)](https://github.com/Samizo-AITL) |
| **ライセンス / License** | [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE) <br> 再配布・改変自由 / Redistribution and modification allowed |

---

## ⬆️ Back to Assembly & Integration

| Link | Badge |
|---|---|
| 🌐 Back to Site | [![Back Site](https://img.shields.io/badge/⬆️%20Back-Site-brightgreen?style=for-the-badge&logo=githubpages)](https://samizo-aitl.github.io/Edusemi-Plus/Assembly-Integration/) |
| 📂 Back to Repo | [![Back Repo](https://img.shields.io/badge/⬆️%20Back-Repo-blue?style=for-the-badge&logo=github)](https://github.com/Samizo-AITL/Edusemi-Plus/tree/main/Assembly-Integration) |
