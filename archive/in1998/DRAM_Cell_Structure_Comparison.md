---
layout: default
title: DRAMセル構造比較（トレンチ vs スタック）
---

---

# 🧬 DRAMセル構造比較（トレンチ vs スタック）  
**🧬 DRAM Cell Structure Comparison (Trench vs Stacked)**

DRAMセル構造には主に「トレンチ型（Trench）」と「スタック型（Stacked）」の2種類が存在し、それぞれに長所・短所があります。  
There are two major DRAM cell types: Trench and Stacked, each with distinct strengths and weaknesses.

| 項目 / Item | トレンチセル / Trench Cell | スタックセル / Stacked Cell |
|-------------|-----------------------------|-------------------------------|
| 構造 / Structure | 基板内に縦穴を掘ってコンデンサを形成<br>Capacitor formed by deep trench in substrate | 基板上にコンデンサを積層<br>Capacitor stacked above substrate |
| 面積効率 / Area Efficiency | 非常に高い / Very high | 高いがトレンチに劣る / High but lower than trench |
| リテンション特性 / Retention | 優れる / Excellent | 劣るが設計で補完可 / Weaker but improvable via design |
| 製造難易度 / Process Difficulty | 高（深掘・トレンチ形状）<br>High (deep etching, trench shape) | 中（成膜と積層形成）<br>Moderate (film deposition, stacking) |
| プラズマダメージ感受性 / Plasma Sensitivity | 高 / High | 中 / Moderate |
| 微細化適性 / Scaling Capability | 難あり / Limited | 高い / Excellent |
| 採用企業 / Adopted by | 東芝・IBM など / Toshiba, IBM | NEC・日立・三菱・Samsung 他 / NEC, Hitachi, Mitsubishi, Samsung, etc. |

> 🔍 トレンチ型はIBM由来の技術で、微細化に課題があるが高密度・高リテンション。  
> Stacked型は1990年代後半以降、業界標準構造として定着。  
>  
> Trench cells originated from IBM technology and excel in density and retention but struggle with scaling.  
> Stacked cells became industry standard in the late 1990s due to easier scaling.
