# 📘 64M DRAM 第3世代（0.25μm）フルプロセスフロー

---

| 工程 | 内容 | 備考 |
|------|------|------|
| FS-DP| SiON酸窒化膜堆積 | 界面保護 |
| FSN-DP| LOCOS用窒化膜 | Field Mask |
| F-PH | Field Photo | Semi-recessパターン |
| F-ET | Field Etch | SIN + SION開口 |
| F-OX | LOCOS酸化 | 鳥くちばし抑制あり |
| PRE-OX | 犠牲酸化膜形成 | チャネル保護 |
| NWLA-PH/ION | Deep N-Well | MV、セル領域、耐α線強化 |
| NWLB-PH/ION | N-Well | ペリフェラル領域（HC） |
| PWL-PH/ION | P-Well | NMOS領域＋Isolation Stopper |
| G-OX | ゲート酸化膜形成 | 80Å |
| PLYA-DP | ドープポリ堆積 | LPCVD、ゲートポリ |
| WSA-DP | WSi CVD | 
| BRAC-DP | バリアキャップ堆積 | SiO2系、WSA専用 |
| WSA-PH | ゲートパターン形成 | KrF |
| WSA-ET | ゲートパターン形成 |  |
| THA-DP | TEOS堆積 | V1下地、良好Step coverage |
| THA-PH/ET | V1コンタクト開口 | WSAに干渉しないよう配置 |
| PLYB-DP | ドープポリ堆積 | LPCVD |
| WSB-DP | WSi堆積 | CVD方式（0.25μm以降） |
| WSB-PH| ビットライン形成 | KrF |
| WSB-ET | ビットライン形成 | WSAと絶縁維持（BRAC効果） |
| THB-DP | TEOS堆積 | ストレージノード絶縁層 |
| THB-PH/ET | V2開口 | AR ≒ 8、高AR対応 |
| PLYC-DP | ポリSi堆積 | 下部電極、厚膜（約8000Å） |
| PLYC-PH/ET | 下部電極パターン | 残渣あるとノード間ショート |
| PLYC2-DP | 粗面化処理　表面積拡大処理 | 容量1.5〜1.8倍向上 |
| SIN-DP | 誘電体膜形成 | LPCVD SiN |
| SIN-OX| SiN酸化 | ONO構造（Oxide-Nitride-Oxide） |
| PLYD-DP | 上部電極（セルプレート） | PolysiliconまたはTiN等 |
| PLYD-PH/ET | 上部電極パターン形成 | ノード絶縁維持 |
| F2-DP | BPSG堆積 | セル段差緩和 |
| F2-ANL | BPSGリフロー | 平坦化処理 |
| CNT-PH/ET | Tungstenコンタクト開口 | N+/P+領域接続 |
| TIN-SP | TiNバリアスパッタ | ロングスロー（LTスパッタ）方式 |
| LAMP-ANL | LAMPアニール | TiN活性化・接合安定化 |
| W-DP/ET | W堆積 / エッチバック | CMP無し、Wプラグ形成 |
| ALA-SP | Ti/AlCu/TiN M1スパッタ | 第一層配線 |
| HL1-DP | ILD1堆積 | SOG等含む |
| HL-SOG | SOGコート | Spin On Glass |
| HL2-DP | ILD2堆積 | 多層絶縁形成 |
| HL-PH/ET | ビア形成 | M1→M2接続開口 |
| ALB-SP | Ti/AlCu/TiN M2スパッタ | 第二層配線 |
| ALB-PH/ET | M2パターン形成 | 配線完了 |
| PAD-DP | パッシベーション膜堆積 | SiN（窒化シリコン）使用 |
| PAD-PH/ET | パッド開口 | 外部ボンディング端子 |
| AL-SNT | 水素シンター処理 | 金属間リーク低減 |
| POP-PH/CUR | PI塗布・キュア処理 | Package耐熱層、光PIあり |
| E-TEST | 電気特性評価 | IDDQ、セルリーク、AC特性 |

---
