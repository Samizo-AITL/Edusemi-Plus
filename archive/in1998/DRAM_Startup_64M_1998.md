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
| SION | 酸窒化膜 / SiON film | プロセス安定化・界面保護<br>Start-up baseline layer |
| SIN | LOCOS窒化膜 / Si₃N₄ | Isolation mask |
| F-PH | Field Photo | Semi-recess pattern |
| F-ET | Field Etch | SIN + SION開口 / Openings |
| F-OX | フィールド酸化 / LOCOS | 鳥くちばし抑制あり / Bird's beak control applied |

---

## 🧬 ウェル・チャネル形成工程 | Well & Channel Formation

```plaintext
→ HF → Pre-OX → NWLA-PH/ION（Deep Well）→ NWLB-PH/ION（PMOS）→ PWL-PH/ION（NMOS）
```

| 工程 | 内容 | 備考 |
|------|------|------|
| HF | LOCOS酸化膜除去 | Pre-OX準備 |
| Pre-OX | 前処理酸化（仮酸化膜） | チャネル保護・損傷緩和 |
| NWLA | Deep N-Well Implant（MVインプラ） | メモリセル深部、α線耐性 |
| NWLB | Peripheral N-Well（HC） | ペリフェラルPMOS用 |
| PWL | P-Well（HC） | セル/周辺NMOS用、ストッパー兼用 |

---

## ⚙️ ゲート形成工程 | Gate Stack Formation

```plaintext
→ HF → G-OX（80Å）→ WSADP（ゲート膜堆積）→ BRACDP（Barrier Cap）→ WSA-PH/ET
```

| 工程 / Step | 内容 / Description | 備考 / Note |
|-------------|--------------------|-------------|
| HF | チャネル酸化膜除去 | イオン注入ダメージ除去 |
| G-OX | ゲート酸化膜（80Å） | 高精度酸化、均一性重視 |
| WSADP | Gate Poly堆積 | LPCVDによるドープポリ |
| BRACDP | Barrier Cap堆積 | SiNなどによるCap層、**バーク（BRAC）**と呼称 |
| WSA-PH/ET | ゲートパターン | パターン形成、**WSAマスク**

---

## 🌀 マスクフロー | Mask Flow Overview

```plaintext
F, NWLA, NWLB, PWL, WSA, THA, WSB, THB, PLYC, PLYD, BPSG, CNT, ALA, HOL, ALB, PAD
```

| マスク | 工程 | 説明 |
|--------|------|------|
| F | Field Isolation | LOCOS（セミリセス） |
| NWLA | N-Well A | Deep Well（MVインプラ） |
| NWLB | N-Well B | PMOSペリフェラル用（HC） |
| PWL | P-Well | NMOSセル＋分離兼用（HC） |
| WSA | Gate Patterning | G-OX, WSADP, BRACを含む |
| THA | Contact to Bit Line | V1（コンタクト1）形成 |
| WSB | Bit Line Poly | ポリビットライン形成 |
| THB | Contact to Storage | コンデンサ下コンタクト |
| PLYC | Storage Node | ポリコンデンサ、粗面化含む |
| PLYD | Cell Plate | コンデンサ上部電極 |
| BPSG | Passivation | BPSG層形成、Planarization |
| CNT | Contact | Wコンタクト、Etch-back構造 |
| ALA | Metal1 | 一次配線 |
| HOL | Via | メタル間ビア形成 |
| ALB | Metal2 | 二次配線 |
| PAD | Pad Opening | 外部接続端子開口 |

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

> 🔜 この続き（THA〜PAD）については今後の記録で追記予定です。  
> 🔜 Continuation (THA to PAD) will be added in the next update.
