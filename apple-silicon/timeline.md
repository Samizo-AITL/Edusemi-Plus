# Apple Aチップ年表（A4〜A18 Pro）

Appleは2010年のA4チップから、自社設計SoC「Apple Silicon」の展開を開始しました。  
以下は各世代の特徴・搭載製品・製造プロセスなどを時系列で整理した年表です。

---

| 世代     | 発表年 | 主な搭載製品             | プロセス | 製造 | 備考                         |
|----------|--------|--------------------------|----------|------|------------------------------|
| A4       | 2010   | iPhone 4                 | 45nm     | Samsung | 初のApple独自設計SoC         |
| A5       | 2011   | iPhone 4s, iPad 2        | 32nm     | Samsung | デュアルコア化                |
| A6       | 2012   | iPhone 5                 | 32nm     | Samsung | 初のApple内製CPU（Swift）    |
| A7       | 2013   | iPhone 5s                | 28nm     | Samsung | 初の64bit ARMv8              |
| A8       | 2014   | iPhone 6, iPad mini 4    | 20nm     | TSMC   | TSMCへ移行開始               |
| A9       | 2015   | iPhone 6s                | 16nm/14nm| TSMC/Samsung | デュアル供給モデル          |
| A10      | 2016   | iPhone 7                 | 16nm     | TSMC   | TSMC単独へ                   |
| A11 Bionic | 2017 | iPhone 8/X               | 10nm     | TSMC   | Neural Engine初搭載          |
| A12 Bionic | 2018 | iPhone XS, XR            | 7nm      | TSMC   | 第2世代Neural Engine         |
| A13 Bionic | 2019 | iPhone 11                | 7nm+     | TSMC   | AI性能・GPU強化              |
| A14 Bionic | 2020 | iPhone 12, iPad Air 4    | 5nm      | TSMC   | 世界初5nmスマホチップ         |
| A15 Bionic | 2021 | iPhone 13, SE (3rd)      | 5nm      | TSMC   | 電力効率強化                 |
| A16 Bionic | 2022 | iPhone 14 Pro            | 4nm（N4）| TSMC   | Proモデル専用、N4採用         |
| A17 Pro    | 2023 | iPhone 15 Pro            | 3nm（N3B）| TSMC  | Pro向け、GPU刷新              |
| A18 Pro*   | 2024 | iPhone 16 Pro            | 3nm（N3E？）| TSMC | N3E適用見込み、詳細未公開     |

\* A18 Proは予測を含む記載です（執筆時点：2025年6月）

---

## 傾向と考察

- **2014年のA8以降、TSMCが一貫して主要製造パートナーに**
- Proセグメントでは、製造ノードの**先行採用（N4, N3B）**が定着
- Neural EngineやGPU強化により、**SoCが体験を差別化する中核**に
- 製造と設計をAppleが統合的に調整していることが明確化

---

## 関連資料

- [tsmc_relation.md](./tsmc_relation.md)：AppleとTSMCの関係と製造戦略
- [design_policy.md](./design_policy.md)（予定）：Apple設計思想

---

© Shinichi Samizo, 2025
