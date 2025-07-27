# 📈 DRAMセル技術の年代別進化（1M〜256M）  
# 📈 DRAM Cell Technology Evolution by Generation (1M–256M)

本資料は、1Mから256M世代までのDRAMセル構造およびプロセス技術の進化を年表形式で示したものです。  
This document outlines the evolution of DRAM cell structures and process technology from the 1M to 256M generation.

---

## 📊 世代・プロセス対応マトリクス / Generation & Process Matrix

| 世代 / Gen | 年代 / Years | 容量 / Density | ノード / Node | セル構造 / Cell Type | 備考 / Notes |
|------------|---------------|----------------|----------------|------------------------|--------------|
| 1st | 1985–1987 | 1M | 1.2–1.0μm | プレーナ / Planar | 初期平面型セル / Early planar cell |
| 2nd | 1988–1990 | 4M | 0.8–0.7μm | トレンチ or プレーナ / Trench or Planar | トレンチ導入期 / Trench begins |
| 3rd | 1991–1993 | 16M | 0.6–0.5μm | トレンチ / Trench | 高密度と高リテンション重視 / Density + retention |
| 4th | 1994–1996 | 64M | 0.4–0.35μm | トレンチ or スタック / Trench or Stacked | 技術分岐点 / Fork point |
| 5th | 1997–1999 | 128M | 0.3–0.25μm | スタック / Stacked | スタック主流化 / Stacked dominant |
| 6th | 1999–2001 | 256M | 0.22–0.18μm | スタック / Stacked | 標準構造化 / Industry standard |

---

## 🔁 セル構造の変遷 / Cell Structure Transition

```
1985      1990      1995      2000
│         │         │         │
│ 1M      │ 4M      │ 16M     │ 64M     128M    256M
│ プレーナ│ トレンチ│ トレンチ│ ↘︎       ↘︎        ↓
│         │         │         │ スタック  スタック  スタック（標準構造化）
```

---

## 🔍 技術転換点 / Key Technological Transitions

| 年代 / Year | 転換点 / Transition | 内容 / Content | 影響 / Impact |
|-------------|----------------------|----------------|----------------|
| 1991–1993 | スタック型の登場 / Emergence of Stacked | 積層による高密度化 / High-density stacking | 工程自由度と装置適応性向上 / Greater process flexibility |
| 1995–1997 | スタック vs トレンチ競争 / Trench vs Stacked | スタック型が台頭 / Stacked gaining ground | 多層配線との親和性向上 / Better with multilayer wiring |
| 1998–2000 | スタック型の標準化 / Standardization of Stacked | 全メーカーがスタック化 / Universal adoption | 製造装置の共通化進行 / Equipment standardization |

---

## 🧰 技術キーワード解説 / Key Terms

- **トレンチセル / Trench Cell**：基板内部に縦穴を掘る高密度構造。  
  Deep etched capacitor inside silicon. High density, hard to scale.

- **スタックセル / Stacked Cell**：コンデンサを基板上に積層する構造。  
  Capacitor stacked on transistor. Scalable, dominant since late 90s.

- **HOC（High Oxide Cap）**：高誘電酸化膜。積層セルの容量確保に利用。  
  High-k dielectric for increased capacitance in stacked cells.

- **CMP**：Chemical Mechanical Polishing（化学機械研磨）。多層配線に不可欠。  
  Critical for planarization in multilevel processes.
