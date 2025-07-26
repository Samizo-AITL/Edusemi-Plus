# 📘 64M DRAM 第3世代（0.25μm）立ち上げ記録 – 三溝真一（1998）  
📘 64M DRAM 3rd Gen (0.25μm) Startup Record – Shinichi Samizo (1998)

> 📝 本文書は現在 **記録中** の技術資料です。内容は中途段階であり、今後追記・整理・補完予定です。  
> 📝 This document is **under development**, and contents are partial and subject to future updates.

---

## 🧭 プロジェクト概要 | Project Overview

| 項目 / Item | 内容 / Details |
|-------------|----------------|
| 製品名 / Product | 64M DRAM（第3世代 / 0.25μm） |
| 年度 / Year | 1998年 |
| 担当者 / Lead Engineer | 三溝真一（Shinichi Samizo, 26歳） |
| 移管元 / Transfer Fab | 三菱電機 熊本工場 KD棟（MotherFab）<br>Mitsubishi Electric Kumamoto Fab (KD Building) |
| 立ち上げ工場 / Ramp-up Site | セイコーエプソン 酒田工場 T棟<br>Seiko Epson Sakata Fab (T Building) |

---

## 🏗️ プロセス立ち上げ戦略 | Ramp-up Strategy

- **プロセスの道を開通させてから本番投入**  
  All process steps must be validated before production wafers.

- **条件出しロット：5ロット（要素技術分散）**  
  5 pilot lots were used to optimize different process modules.

- **露光・フォーカス・成膜条件などパラメータ展開**  
  Matrix testing for exposure dose, focus offset, and film formation.

- **電子流動票（Caps-T）でKD棟→T棟条件移行**  
  Process specs were transferred via Caps-T flow documents.

---

## 🧪 初期Isolation工程 | Initial Isolation Flow

```plaintext
SION → SIN → F-PH / F-ET（セミリセス）→ F-OX（LOCOS）
```

| 工程 / Step | 内容 / Description | 備考 / Note |
|-------------|--------------------|-------------|
| SION | 酸窒化膜 / SiON film | プロセス安定化・界面保護 |
| SIN | LOCOS窒化膜 / Si₃N₄ | Isolation mask |
| F-PH | Field Photo | Semi-recess pattern |
| F-ET | Field Etch | SIN + SION開口 |
| F-OX | フィールド酸化 / LOCOS | 鳥くちばし抑制あり（Bird's beak control） |

---

## 🧬 ウェル・チャネル形成工程 | Well & Channel Formation

```plaintext
→ HF → Pre-OX → NWLA-PH/ION（Deep Well）→ NWLB-PH/ION（PMOS）→ PWL-PH/ION（NMOS）
```

| 工程 | 内容 | 備考 |
|------|------|------|
| HF | LOCOS酸化膜除去 | Pre-OX準備 |
| Pre-OX | 前処理酸化（仮酸化膜） | チャネル保護・損傷緩和 |
| NWLA | Deep N-Well Implant（MV） | α線耐性向上 / セル領域深部 |
| NWLB | N-Well for PMOS（HC） | ペリフェラル領域用 |
| PWL | P-Well for NMOS（HC） | セルNMOS＋分離ストッパー |

---

## ⚙️ ゲート形成工程 | Gate Stack Formation

```plaintext
→ HF → G-OX（80Å）→ WSADP（ドープポリ）→ BRACDP（Cap）→ WSA-PH/ET
```

| 工程 | 内容 | 備考 |
|------|------|------|
| G-OX | Gate Oxide | 80Å、均一酸化 |
| WSADP | Gate Poly | LPCVDドープポリ |
| BRACDP | Barrier Cap | SiN系、WSA専用の“バーク” |
| WSA-PH/ET | ゲートパターン | ノックオン防止に注意 |

---

## 🧱 ポリ以降：ビットライン形成前段 | WSA → THA → WSB

```plaintext
WSA-PH/ET → THA-DP（TEOS）→ THA-PH/ET → WSB-DP（WSi-CVD）→ WSB-PH/ET
```

| 工程 | 内容 | 備考 |
|------|------|------|
| THA-DP | Interlayer TEOS堆積 | コンタクト用下地、Step coverage良好 |
| THA-PH/ET | V1 Contact開口 | WSA上に被らないよう配置 |
| WSB-DP | Bit Line WSi堆積 | 0.25μm世代より**WSi-CVD**方式 |
| WSB-PH/ET | Bit Lineパターン | THA後に形成。WSAと絶縁構造を維持（BRAC含む） |

---

## 🧱 ストレージノード構造形成工程 | Storage Node Stack Formation (THB → PLYD)

```plaintext
WSB-PH/ET → THB-DP → THB-PH/ET → PLYC-DP → PLYC-ET → 粗面化 → SiN堆積 → 酸化処理 → PLYD堆積
```

| 工程 | 内容 | 備考 |
|------|------|------|
| THB-DP | ILD堆積（TEOS） | ストレージノードコンタクト絶縁層 |
| THB-PH/ET | V2開口（高AR） | AR ≒ 8、開口不良・オープンリスクあり |
| PLYC-DP | ポリSi下部電極堆積 | 粗面化前処理に適した厚膜（約8000Å） |
| PLYC-ET | 下部電極パターン | 残渣あると**ノード間ショート（共通電位）** → バーンイン検出不可 |
| 粗面化 | 表面積拡大処理 | セル容量 **1.5〜1.8倍**に向上 |
| SiN堆積 | 誘電体膜形成 | 窒化膜（LPCVD）。リーク抑制 |
| 酸化処理 | SiN酸化 | **ONO（Oxide-Nitride-Oxide）**構成へ |
| PLYD堆積 | 上部電極（セルプレート） | PolysiliconまたはTiNなど。共通電位形成 |

---

## 🌐 マスクフロー | Mask Flow Overview

```plaintext
F, NWLA, NWLB, PWL, WSA, THA, WSB, THB, PLYC, PLYD, BPSG, CNT, ALA, HOL, ALB, PAD
```

| マスク | 工程 | 概要 |
|--------|------|------|
| F | Isolation | LOCOS (セミリセス) |
| NWLA | Deep N-Well | セル領域、MV |
| NWLB | N-Well | ペリフェラル、HC |
| PWL | P-Well | チャネル制御、ストッパー |
| WSA | Gate | Gate Poly＋BRAC形成 |
| THA | V1 Contact | Bit Line接続コンタクト |
| WSB | Bit Line Poly | セル側配線 |
| THB | Storage Node Contact | Capacitor Bottom |
| PLYC | Storage Node | 粗面化あり |
| PLYD | Cell Plate | コンデンサ上部電極 |
| BPSG | Planarization | セル・周辺段差緩和、リフロー |
| CNT | W Contact | Tungsten埋込＋エッチバック |
| ALA | Metal1 | 第一層メタル |
| HOL | Via | M1→M2ビア |
| ALB | Metal2 | 第二層メタル |
| PAD | Pad開口 | 外部接続端子 |

---

## 🔍 不良解析と改善経緯 | Failure Analysis & Process Fix

| フェーズ / Phase | 内容 / Description |
|------------------|---------------------|
| 本番ロット投入 / Production Lot | 信頼性評価用3ロット投入 / 3 lots for reliability burn-in |
| 歩留まり初回 / Initial Yield | 65% – Pause Refresh failure observed |
| セル容量確認 / Cap OK | ストレージノードコンタクト～N+間リーク疑い / Suspected junction leakage |
| SEM観察 / SEM Cross-section | THA, THB, CNT形状良好 / No structural defect |
| 原因特定 / Root Cause | **WSA後のアッシング→洗浄切替時のプラズマダメージ**<br>Plasma-induced damage during resist ashing |
| 改善処置 / Fix | ノックオン対策、洗浄順序最適化 / Knock-on prevention, cleaning sequence tune |
| 歩留改善 / Final Yield | 80%、信頼性クリア → 量産フェーズへ移行 / Stable for volume production |

---

> 🔜 この続き（THB → PLYC → BPSG → CNT → AL）以降は、今後の記録で追記予定です。  
> 🔜 Continuation (THB to AL) will be added in the next update.
