# 0.25μm 64M DRAM (3rd Generation) Process Flow

> ⚠️ **注記 / Note**  
> 本工程表は、三溝真一による1990年代末の製造経験と記憶をもとに再構成された技術記録です。内容は当時の知識と状況に基づくものであり、現在の技術資料や実データとは一部異なる可能性があります。正確性を保証するものではなく、教育・技術アーカイブ目的での参考情報としてご利用ください。  
>  
> This process table is a technical reconstruction based on Shinichi Samizo's manufacturing experience and memory from the late 1990s. The content reflects knowledge and conditions of that time and may differ from current technical documents or actual data. It is not guaranteed to be accurate and should be used as reference information for educational or archival purposes only.

---

## 🔹 特徴 / Key Features

| 項目 / Item | 内容 / Description |
|------------|---------------------|
| **電源電圧 / Supply Voltage** | 3.3V（メモリセル・周辺・I/O）<br>*3.3V for Memory Cell, Peripheral, and I/O* |
| **セルキャパシタ構造 / Cell Capacitor Structure** | スタック型キャパシタ<br>*Stacked capacitor structure* |
| **ウェル構成 / Well Structure** | メモリセルにトリプルウェル構造を採用<br>*Triple-well adopted in memory cell region* |
| **ワードライン構造 / Word Line** | デバイデッドWL構造、WSA-ALA接続<br>*Divided word-line structure with WSA-ALA connection* |
| **ビットライン形成 / Bit Line** | WSB-CVDにより、BLとBLコンタクトを同時形成<br>*Bit line and bit line contact formed simultaneously by WSB-CVD* |
| **ストレージノード処理 / Storage Node Surface Treatment** | 粗面化処理により容量値1.5〜1.8倍向上<br>*Surface roughening improved capacitance by 1.5–1.8×* |

---

## 🟫 素子分離形成 / Device Isolation Formation

| 工程名 / Step | 処理内容 / Process Description | 対象領域 / Target Area | 主目的 / Purpose | 処理条件 / Conditions | 備考 / Notes |
|---------------|----------------------------------|-------------------------|--------------------|------------------------|----------------|
| **FS-DP**     | SiON酸窒化膜堆積<br>*SiON deposition* | 全体基板<br>*Whole wafer* | LOCOS前の界面保護<br>*Pre-LOCOS interface protection* | 200Å @ 700℃ | 膜質改善のための初期積層<br>*Improved interface quality* |
| **FSN-DP**    | LOCOS用窒化膜堆積<br>*Field Nitride deposition* | Field領域<br>*Field area* | LOCOS酸化マスク<br>*LOCOS oxidation mask* | 1500Å @ 750℃ | LOCOS酸化前の主保護膜<br>*Main hard mask before oxidation* |
| **F-PH**      | Fieldフォトリソ（KrF）<br>*Field lithography (KrF)* | Field領域<br>*Field area* | LOCOSパターン定義<br>*Patterning LOCOS region* | 0.35μm | Semi-recess対応パターン<br>*Semi-recess LOCOS layout* |
| **F-ET**      | SIN + SiON開口（エッチング）<br>*Etching SIN + SiON* | Field領域<br>*Field area* | LOCOS開口形成<br>*Open field oxide region* | - | 多層保護膜の選択除去<br>*Selective removal of multilayer mask* |
| **F-OX**      | LOCOS熱酸化<br>*Thermal field oxidation (LOCOS)* | Field領域<br>*Field area* | フィールド酸化膜形成<br>*Field oxide isolation* | 4500Å @ 1000℃ | 鳥くちばし抑制プロファイル<br>*Bird’s beak minimization* |
| **PRE-OX**    | 犠牲酸化膜形成<br>*Sacrificial oxidation* | チャネル領域<br>*Channel region* | ゲート酸化前の表面処理<br>*Channel surface protection* | 200Å @ 900℃ | 汚染除去および表面平坦化<br>*Cleaning and surface smoothing* |

---

## 🧪 ウエル・CD形成 / Well & Channel Doping (Deep/N/P-Well, Channel Doping)

| 工程名 / Step | 処理内容 / Process Description | 対象領域 / Target Area | 注入目的 / Purpose | 条件 / Conditions | 備考 / Notes |
|---------------|-------------------------------|-------------------------|----------------------|--------------------|----------------|
| **NWLA-PH**   | Deep N-Wellフォトリソ<br>*Deep N-Well lithography* | メモリセル領域<br>*Memory cell region* | Deep N-Well定義<br>*Define Deep N-Well* | 1.5μm | α線耐性向上のための深打ち領域<br>*Deep region for α-particle immunity* |
| **NWLA-ION**  | Deep N-Well注入（MeV）<br>*Deep N-Well implantation (MeV)* | メモリセル領域<br>*Memory cell region* | 高耐性N-Well形成<br>*Form high-resistance N-Well* | 1e13/cm² @ 1.2 MeV (P⁺) | メモリセル専用の深層注入<br>*Exclusive to memory cell area* |
| **NWLB-PH**   | N-Wellフォトリソ<br>*N-Well lithography* | ペリフェラル領域<br>*Peripheral region* | N-Well定義<br>*Define N-Well* | 1.2μm | 周辺PMOSトランジスタ領域に適用<br>*For peripheral PMOS devices* |
| **NWLB-ION**  | N-Well注入（HC）<br>*N-Well implantation (HC)* | ペリフェラル領域<br>*Peripheral region* | ① N-Well形成<br>② PMOSチャネル形成<br>*① Form N-Well<br>② PMOS channel doping* | 1e13/cm² @ 300 keV (P⁺) | 二重機能を1工程で集約<br>*Combines two functions in one step* |
| **PWL-PH**    | P-Wellフォトリソ<br>*P-Well lithography* | メモリセル・周辺領域<br>*Cell + Peripheral* | P-Well定義<br>*Define P-Well* | 1.0μm | Field Stopper領域を含む複合エリア<br>*Includes Field Stopper region* |
| **PWL-ION**   | P-Well注入（HC）<br>*P-Well implantation (HC)* | 同上<br>*Same as above* | ① P-Well形成<br>② Field Stopper形成<br>③ NMOSチャネル形成<br>*① Form P-Well<br>② Field Stopper<br>③ NMOS channel doping* | 1e13/cm² @ 150 keV (B⁺) | 3機能を統合した高効率注入<br>*Three functions integrated into one step* |

---

## 🟦 ゲート膜・ゲート電極形成 / Gate Oxide & Gate Electrode Formation (Word Line WSA)

| 工程名 / Step | 処理内容 / Process Description | 膜厚 / Thickness | 寸法 / CD | 温度 / Temp | 備考 / Notes |
|---------------|----------------------------------|-------------------|-------------|---------------|----------------|
| **G-OX**      | ゲート酸化膜形成<br>*Gate oxide formation* | 80Å | - | 800℃ | 高品質な熱酸化膜（LPCVD）<br>*High-quality thermal oxide by LPCVD* |
| **PLYA-DP**   | ドープポリ堆積<br>*Doped poly-Si deposition* | 2000Å | - | 620℃ | ゲート電極用ポリシリコン<br>*Poly-Si for gate electrode* |
| **WSA-DP**    | WSi堆積（CVD）<br>*WSi deposition (CVD)* | 1500Å | - | 450℃ | ポリ上にタングステンサイリサイド<br>*Tungsten silicide on poly-Si* |
| **BRAC-DP**   | バリアキャップ堆積（SiO₂）<br>*Barrier cap deposition (SiO₂)* | 800Å | - | 400℃ | エッチング保護と絶縁層形成<br>*Etch protection and insulation* |
| **WSA-PH**    | ゲートパターンフォト（KrF）<br>*Gate lithography (KrF)* | - | 0.25μm | - | 高解像度パターン形成<br>*High-resolution patterning* |
| **WSA-ET**    | ゲートエッチング<br>*Gate etching* | - | - | 室温 / RT | BRAC層を残して絶縁性維持<br>*Keeps BRAC layer for insulation* |

---

## ⚙️ ソース・ドレイン形成 / Source & Drain Formation

| 工程名 / Step | 処理内容 / Process Description | 対象領域 / Target Area | 注入目的 / Purpose | 処理条件 / Conditions | 備考 / Notes |
|---------------|-------------------------------|-------------------------|----------------------|------------------------|----------------|
| **NLD-PH**    | NMOS LDDフォト<br>*NMOS LDD lithography* | ペリフェラル領域<br>*Peripheral* | LDD位置定義<br>*Define LDD region* | 0.35μm | 高精度パターン必要 |
| **NLD-ION**   | NMOS LDD注入<br>*NMOS LDD implantation* | ペリフェラル領域<br>*Peripheral* | 浅層N⁻拡散形成<br>*Form shallow N⁻ diffusion* | 5e13/cm² @ 40 keV (As⁺) | LDD：低電界化設計 |
| **NLDC-PH**   | NMOSセルLDDフォト<br>*NMOS Cell LDD lithography* | メモリセル領域<br>*Cell* | セル部LDD定義<br>*Define LDD for cell* | 0.3μm | WSA干渉に注意 |
| **NLDC-ION**  | NMOSセルLDD注入<br>*NMOS Cell LDD implantation* | メモリセル領域<br>*Cell* | 浅層N⁻形成（セル）<br>*Shallow N⁻ in memory cell* | 5e13/cm² @ 30 keV (As⁺) | 小電流制御型 |
| **PLD-PH**    | PMOS LDDフォト<br>*PMOS LDD lithography* | ペリフェラル領域<br>*Peripheral* | PMOS LDD位置定義<br>*Define LDD region for PMOS* | 0.35μm | |
| **PLD-ION**   | PMOS LDD注入<br>*PMOS LDD implantation* | ペリフェラル領域<br>*Peripheral* | P⁻浅層拡散形成<br>*Form shallow P⁻ diffusion* | 3e13/cm² @ 30 keV (BF₂⁺) | |
| **SW-DP**     | スペーサー堆積（酸化膜/窒化膜）<br>*Spacer deposition (oxide/nitride)* | 全体<br>*Global* | スペーサー積層<br>*Spacer stack for S/D mask* | SiO₂: 600Å, SiN: 400Å | CVD積層 |
| **SW-ET**     | スペーサーエッチング<br>*Spacer etching* | 全体<br>*Global* | スペーサー形成<br>*Form oxide/nitride spacers* | ドライエッチ @ RT | SiO₂/SiN選択 |
| **NLD2-PH**   | NMOS深拡散フォト<br>*NMOS deep S/D lithography* | ペリフェラル領域<br>*Peripheral* | N⁺ソース・ドレイン定義<br>*Define N⁺ S/D* | 0.35μm | |
| **NLD2-ION**  | NMOS深拡散注入<br>*NMOS deep S/D implantation* | ペリフェラル領域<br>*Peripheral* | N⁺深拡散形成<br>*Form deep N⁺ S/D* | 5e15/cm² @ 60 keV (As⁺) | アニールにより活性化 |
| **NLDC2-PH**  | NMOSセル深拡散フォト<br>*NMOS Cell deep S/D lithography* | メモリセル領域<br>*Cell* | セルN⁺定義<br>*Define N⁺ S/D in memory cell* | 0.3μm | |
| **NLDC2-ION** | NMOSセル深拡散注入<br>*NMOS Cell deep S/D implantation* | メモリセル領域<br>*Cell* | N⁺深拡散形成（セル）<br>*Deep N⁺ in memory cell* | 5e15/cm² @ 50 keV (As⁺) | |
| **PLD2-PH**   | PMOS深拡散フォト<br>*PMOS deep S/D lithography* | ペリフェラル領域<br>*Peripheral* | PMOS P⁺定義<br>*Define P⁺ S/D* | 0.35μm | |
| **PLD2-ION**  | PMOS深拡散注入<br>*PMOS deep S/D implantation* | ペリフェラル領域<br>*Peripheral* | P⁺深拡散形成<br>*Form deep P⁺ S/D* | 3e15/cm² @ 50 keV (BF₂⁺) | |

---

## 🟩 ビットライン形成 / Bit Line Formation (Through Hole THA to Bit Line WSB)

| 工程名 / Step | 処理内容 / Process Description | 備考 / Notes |
|---------------|----------------------------------|----------------|
| **THA-DP**     | TEOS堆積（THA下地）<br>*TEOS deposition (THA base layer)* | 4000Å @ 650℃ |
| **THA-PH**     | スルーホールフォトリソ（KrF）<br>*Through-hole lithography (KrF)* | アスペクト比 AR=2、WSA干渉を回避するレイアウト<br>*AR=2, layout avoiding interference with WSA* |
| **THA-ET**     | スルーホール開口エッチング<br>*THA contact hole etching* | ビットライン用コンタクトホール形成<br>*Contact hole for BL contact* |
| **PLYB-DP**    | ドープポリ堆積（ビットライン下地）<br>*Doped poly-Si deposition (BL base)* | 2500Å @ 620℃ |
| **WSB-DP**     | タングステンサイリサイド堆積（CVD）<br>*WSi deposition (CVD)* | 1800Å @ 450℃ |
| **WSB-PH**     | ビットラインフォトリソ（KrF）<br>*Bit line lithography (KrF)* | 0.25μm L/S 高密度配線対応<br>*0.25μm L/S for high-density interconnect* |
| **WSB-ET**     | ビットラインエッチング<br>*Bit line etching* | BRACキャップ効果で下層絶縁性を維持<br>*Maintains insulation using BRAC cap* |

---

## 🟥 キャパシタ形成 / Capacitor Formation (THB to PLYD)

| 工程名 / Step | 処理内容 / Process Description | 備考 / Notes |
|---------------|----------------------------------|----------------|
| **THB-DP**     | TEOS堆積（V2下地）<br>*TEOS deposition (V2 base layer)* | 6000Å |
| **THB-PH**     | V2フォトリソ（KrF）<br>*V2 lithography (KrF)* | アスペクト比 AR=8 深コンタクト対応<br>*AR=8 for deep contact* |
| **THB-ET**     | V2開口エッチング<br>*V2 contact etching* | キャパシタ下部コンタクトホール形成<br>*Contact hole to bottom capacitor electrode* |
| **PLYC-DP**    | 厚膜ポリSi堆積（下部電極）<br>*Thick poly-Si deposition (bottom electrode)* | 8000Å @ 620℃ |
| **PLYC-PH**    | 下部電極パターンフォト<br>*Bottom electrode lithography* | 0.25μm |
| **PLYC-ET**    | 下部電極エッチング<br>*Bottom electrode etching* | 残渣によるショートを避ける<br>*Residue can cause shorts* |
| **PLYC2-DP**   | 粗面化処理（容量向上）<br>*Surface roughening (capacitance boost)* | 700℃, 容量1.5〜1.8倍向上<br>*Capacitance boosted 1.5–1.8×* |
| **SIN-DP**     | SiN堆積（ONO誘電体）<br>*SiN deposition for ONO dielectric* | 150Å @ 750℃ |
| **SIN-OX**     | SiN酸化（ONO形成）<br>*SiN oxidation (ONO structure)* | 800℃, ONO構造完成<br>*Completes ONO dielectric* |
| **PLYD-DP**    | 上部電極堆積（ポリSi）<br>*Top electrode deposition (poly-Si)* | 2000Å |
| **PLYD-PH**    | 上部電極フォトリソ<br>*Top electrode lithography* | 0.3μm, ノード絶縁確保<br>*Ensures node isolation* |
| **PLYD-ET**    | 上部電極エッチング<br>*Top electrode etching* | セルプレート形成<br>*Forms cell plate* |

---

## ⬜ 層間絶縁・Wプラグ形成 / Interlayer Dielectric & W Plug Formation

| 工程名 / Step | 処理内容 / Process Description | 備考 / Notes |
|---------------|----------------------------------|----------------|
| **F2-DP**      | BPSG堆積<br>*BPSG deposition* | 1.0μm @ 750℃ / セル段差緩和<br>*Step coverage for memory cell* |
| **F2-ANL**     | BPSGリフロー<br>*BPSG reflow* | 850℃ 平坦化処理<br>*Planarization by reflow* |
| **CNT-PH**     | コンポーネントフォト（KrF）<br>*Contact lithography (KrF)* | ハーフトーンマスク / AR=6<br>*Half-tone mask for high AR contact* |
| **CNT-ET**     | コンポーネント開口エッチング<br>*Contact hole etching* | N+/P+拡散層接続ホール形成<br>*Open contact to N+/P+ regions* |
| **CNT-ION**    | N+/P+イオン注入<br>*Contact ion implantation* | 3e15/cm² @ 30 keV（As⁺/BF₂⁺）<br>*Shallow doping for contact* |
| **TIN-SP**     | Ti/TiNバリアスパッタ<br>*Barrier metal sputtering* | 300Å 低温スパッタ<br>*Low-temp Ti/TiN stack* |
| **LAMP-ANL**   | LAMPアニール<br>*LAMP annealing* | 400℃ / TiN活性化・接合安定化<br>*Contact stabilization* |
| **CW-DP**      | Wプラグ形成（CVD）<br>*Tungsten plug deposition (CVD)* | 4000Å, WF₆-CVD |
| **CW-ET**      | Wプラグエッチバック<br>*W plug etch-back* | CMPなし / 非選択ドライ方式<br>*No CMP used* |

---

## 🟨 M1/M2配線・パッド・封止形成 / Metal Interconnects, Pad, and Final Passivation

| 工程名 / Step | 処理内容 / Process Description | 備考 / Notes |
|---------------|----------------------------------|----------------|
| **ALA-SP**     | M1スパッタ（Ti/AlCu/TiN）<br>*M1 sputtering (Ti/AlCu/TiN)* | 6000Å / 0.4μm L/S |
| **HL1-DP**     | ILD1堆積<br>*ILD1 deposition* | 7000Å |
| **HL-SOG**     | SOGコート<br>*SOG coating* | 5000Å スピンオンガラスによる平坦化<br>*Spin-on-glass planarization* |
| **HL2-DP**     | ILD2堆積<br>*ILD2 deposition* | 7000Å |
| **HL-PH**      | ビアフォトリソ<br>*Via lithography* | AR=4, M1→M2接続用<br>*For M1-M2 via connection* |
| **HL-ET**      | ビア開口エッチング<br>*Via hole etching* | M1露出・接続用ホール形成<br>*Via hole to expose M1* |
| **ALB-SP**     | M2スパッタ（Ti/AlCu/TiN）<br>*M2 sputtering (Ti/AlCu/TiN)* | 6000Å / 0.4μm L/S |
| **ALB-PH**     | M2フォトリソ<br>*M2 lithography* | 0.35μm |
| **ALB-ET**     | M2パターンエッチング<br>*M2 etching* | アルCu金属パターン形成<br>*AlCu interconnect patterning* |
| **PAD-DP**     | パッシベーション膜堆積<br>*Passivation layer deposition* | 5000Å / SiNまたはPI |
| **PAD-PH**     | パッドフォトリソ<br>*Pad opening lithography* | 60μm 外部I/O接続開口<br>*I/O pad access window* |
| **PAD-ET**     | パッド開口エッチング<br>*Pad etching* | アルミPad露出処理<br>*Expose Al pads* |
| **AL-SNT**     | 水素シンター処理<br>*Hydrogen sintering* | 450℃ / 金属リーク低減<br>*Leakage suppression* |
| **POP-PH**     | PI塗布フォトリソ<br>*Photo-PI coating lithography* | 60μm, 光PI対応<br>*Photo-defined PI opening* |
| **POP-CUR**    | PIキュア処理<br>*PI curing* | 300℃ / 封止膜硬化<br>*Cure polymer sealing layer* |
| **E-TEST**     | 電気特性評価<br>*Electrical Testing* | RT, TEG測定<br>*Room temp parametric test on TEG* |

---
