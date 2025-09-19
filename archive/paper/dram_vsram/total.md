# プロローグ / Prologue

---

## 日本語

1990年代、日本の半導体産業は大きな転換期を迎えていた。  
1980年代にDRAM市場を席巻した日本勢は、1990年代に入ると日米半導体協定や韓国・台湾勢の台頭によって急速に競争力を失った。  
それでも国内各社は、最先端技術の導入に果敢に挑み続けた。  

セイコーエプソン酒田工場の8インチラインも、その流れの中で建設された。  
狙いは **DRAMを事業の中心とすることではなく、DRAM技術を戦略的ビークルとして活用し、0.35µm以降の先端プロセスを吸収して自社固有の製品群※へ展開すること** にあった。  
※社内ASICやロジックIC、パネルドライバ、インクジェット駆動ICなどの応用製品  

DRAM技術導入は、三菱電機からの技術移管によって進められ、各世代が明確な役割を担った。  

- **0.5 µm世代 16M DRAM**：量産実績を確保し、Fab稼働を軌道に乗せるための入り口  
- **0.35 µm世代 64M DRAM（第2世代）**：微細化に伴うプロセス導入と、歩留まり課題への挑戦  
- **0.25 µm世代 64M DRAM（第3世代）**：次世代技術の検証と、社内展開の基盤構築  

本論文では、1998年に酒田工場で実施された **0.25 µm DRAM技術移管と立ち上げ** を中心に、  
**プロセス解説、立ち上げ方法、不良解析と歩留まり改善** の取り組みを整理する。  
さらに、その成果が2001年の **モバイル用疑似SRAM（VSRAM）** 量産へとどのように結びついたのかを記録する。  

---

# 📘 0.25µm 64M DRAM (3rd Gen) Startup Record (1998)

---

## 1️⃣ プロセス概要 / Process Overview

- **リソグラフィ**：初の **KrFステッパー** を導入し、0.25µm世代の量産露光技術を確立  
- **デバイス分離**：Semi-recess LOCOS による素子分離  
- **ウェル構成**：Triple-well、Deep N-Well によりセルの耐ノイズ性を強化  
- **ゲート電極（ワードライン）**：**Wシリサイド (WSi, CVD)** を用いた構造。  
  - ゲート上に **BRAC (Barrier Cap) 層** を形成し、エッチング耐性と絶縁性を確保  
  - これにより **ビットラインコンタクトがワードラインと接触しないセルフアライン構造**を実現  
- **ビットライン**：**ビットラインコンタクトとビットラインを同時形成**。WSi-CVD導入により配線抵抗を低減し、高密度配線化を可能にした  
- **ストレージノード（キャパシタ）**：スタック型構造。粗面化処理により容量を 1.5〜1.8 倍に向上  
- **配線・封止**：AlCu/TiN配線、SOG平坦化、SiNまたはPIによるパッシベーション
  
---

## 2️⃣ 立ち上げ方法 / Ramp-up Method

### 1. ベースフロー（SCF → 形状ロット → 本番ロット）

- **SCF（Short Cycle Feedback）**  
  各要素技術部門が立ち上げ仕様書に基づき、短サイクルロットを流して条件を素早く評価・修正し、処理条件を決定。

- **形状ロット（約10ロット）**  
  各要素技術には、**実製品ウエハでなければ評価できない項目**が多い。  
  形状ロットはそれらの部門にウエハを提供すると同時に、以下を並行して確認することを目的とした。  
  - 各フォトのパターン寸法  
  - エッチング後寸法とフォト→エッチの寸法変換差  
  - 各層間膜堆積後の断面観察  
  - 各要素技術担当による評価（拡散、CVD、エッチングなど）  
  → これらの結果を基に、後続ロット用のレシピを作成・更新。

- **本番ロット（信頼性確認）**  
  信頼性確認用に複数ロットを投入し、ウエハテストと長期信頼性試験（Burn-in等）で量産移行可否を判定。

---

### 2. 実務フロー（筆者の担当）

1. **条件データ受領**：移管元（三菱KD工場）から **フロッピー2枚分の処理条件データ** を受領  
2. **条件展開**：各要素技術（拡散・CVD・PVD・エッチング等）へ処理条件を展開  
3. **各工程SCF**：各担当が短サイクルロットで条件を確認し、修正・再投入を繰り返す  
4. **電子流動票作成**：最新条件を集約し、電子流動票へ反映  
5. **形状ロット投入（10ロット）**：  
   - 各部門へ実製品ウエハを提供  
   - フォトレジスト寸法、エッチ寸法、変換差を確認  
   - 各層間膜後の断面観察を実施  
   - 後続ロット用レシピを作成・更新  
6. **形状Fix**：狙い寸法・膜厚の達成を確認し、条件を確定  
7. **本番ロット投入（5ロット・信頼性用）**：  
   - ウエハテストを実施  
   - 信頼性試験結果を確認し、量産移行を判断  

---

## 3️⃣ 運用体制（スケジュール最適化）

通常、ロットはストッカーに入庫し、**リムライナー（リニア搬送レール）**で自動搬送され、次のストッカーから出庫して装置ロードロックにセットされる。  
しかし、この方式では**順番待ちや搬送遅延**が避けられず、初回の重要ロットでは処理開始までに大きな時間を要した。  

そこで、初回立ち上げロットについては、**技術者が各装置まで直接搬送する「手渡し流動」**を採用。  
各装置担当者がロットの到着時刻に合わせて待機し、到着次第すぐに処理を開始することで、搬送待ちによるロスを最小化した。  
それでもフルフローを通すには約2か月を要し、立ち上げ全体は約5か月かかった。  

さらに、初回ロットを**いち早く流して、後続ロットの標準パス（標準流動）を確立できるか**が立ち上げスケジュールを左右した。  
そのため酒田工場では通常の製造部門に加え、**技術側（プロセス開発・要素技術担当・立ち上げチーム）が日勤・夜勤の二交代制で常駐**し、  
24時間体制でモニタリングとフィードバックを行った。  

また、**毎朝の朝会**では以下を実施した：  
- **ラミネートした流動票をホワイトボードに掲示**し、各ロットの進捗を共有  
- 各ロットがオンスケジュールか、遅延がある場合は日数を明示して報告  
- 各要素技術担当者から、立ち上げ状況や課題の進捗を報告  

これにより、部門横断的に進捗を「見える化」し、全体最適の立場で迅速に調整を行うことができた。

---

## 3️⃣ 不良解析と改善プロセス / Failure Analysis and Improvement Process

### ① 現状把握（不良解析 / Failure Analysis）

- **初期歩留まり**  
  - 立ち上げ直後の本番ロットで歩留まりは約65%に留まった。  
- **主不良モード**  
  - ウエハテストでは **Pause Refresh Fail (Bin5)** が支配的。  
- **分布特性**  
  - 不良はウエハ面内に均一に散在する単ビットエラーとして出現。  
  - ライン欠陥やエッジ集中型ではなく、クラスタリング傾向も薄い。  
- **構造・特性評価**  
  - ストレージノード容量は規格内。  
  - 不良セルのコンタクト断面もSEM観察では異常なし。  
  - 他の形状・膜厚・電気特性も規格範囲内で異常なし。  

**まとめ**  
通常の寸法外れや異物混入による欠陥ではなく、**観察上は健全に見えるが保持特性を劣化させる、極めてセンシティブな不具合**が原因と推定された。  

---

### ② 仮説（推定故障モデル / Hypothesized Failure Model）

- **前提確認**  
  - ストレージノード容量やセルプレートリークは正常。  
  - 直接測定可能なリークでは異常を検出できない。  
- **推定モデル**  
  - 問題は **ストレージノードコンタクト n⁺/p⁻ ジャンクションのリーク増大**にあると考えられる。  
- **劣化メカニズム**  
  - ゲートエッチング後、メモリセルS/Dアクティブ上に残存するゲート酸化膜が、  
    LDD形成工程での複数回のレジスト剥離アッシングに曝される。  
  - この繰り返しのプラズマダメージにより酸化膜が**ポーラス状に劣化**。  
  - 酸化膜下の拡散層にもダメージが及び、ジャンクションに微細なリークパスが形成される。  
- **現象との整合性**  
  - 局所的・ランダムに発生するため、ウエハ全体で単ビット不良が均一分布。  
  - SEMでは構造的異常を確認できず、リーク特性のみで歩留まりを低下させる。  

**まとめ**  
**「目に見えないプラズマダメージによるジャンクションリーク」**が真因であるとの仮説を構築した。  

---

### ③ 対策の立案 / Countermeasure Planning

- **重点ポイント**  
  - アッシング工程によるプラズマ曝露を最小化すること。  
- **具体策**  
  - LDD工程のレジスト除去を、従来のプラズマアッシングから  
    **ウェット処理（硫酸系剥離）主体**へ切り替え。  
- **狙い**  
  - プラズマ起因の酸化膜ダメージを根本的に排除。  
  - ジャンクションリークの発生を抑制し、セル保持特性を回復させる。  
- **補足**  
  - 他工程との整合性（後続フォトプロセスのクリーン度確保、残渣リスクの回避）も並行して検討。  

---

### ④ 効果の確認 / Effectiveness Verification

- **歩留まりの改善**  
  - 改善前: 約65%  
  - 改善後: **80%前後**へ向上。  
  - 均一に散在していた単ビット不良が顕著に減少。  
- **信頼性評価**  
  - バーンイン試験を含む高温動作・長期保持試験で規格を満足。  
  - 不良再発率も大幅に低下。  
- **量産適用**  
  - 改善条件をもって最終レシピをFix。  
  - 以後の量産立ち上げで安定した歩留まりを確保。  

**まとめ**  
解析 → 仮説 → 対策 → 効果確認という一連の改善サイクルにより、  
**原因の見えにくいセンシティブ不良を克服し、量産条件を確立**することに成功した。  


---

# 📘 モバイル用疑似SRAM（VSRAM）技術アーカイブ (2001)

---

## 1️⃣ 製品仕様と時代背景 / Product Specification and Historical Context

**日本語**  
2000年前後、半導体市場の主役はPC向け大容量DRAMから、急速に普及し始めた携帯電話向けのモバイルデバイスへと移りつつあった。特にシャープでは、携帯電話にカメラ機能を追加する企画が進み、その実現には **大容量かつ低消費電力のメモリ** が不可欠であった。  

このニーズに応えるため、2001年に0.25 µm世代のDRAMプロセスを流用し、内部リフレッシュ制御を付加することで **疑似SRAM (VSRAM)** が量産化された。これはDRAMセルをベースとしながら、SRAMのように外部からリフレッシュを意識せず使用できる点に特徴があった。さらに動作温度保証を標準の80 °Cから90 °Cへ拡張し、モバイル用途に適合させた。  

ただし、当初の歩留まりは約30%と低かった。それでも、**市場投入を最優先する合理的判断** により量産が開始され、実際にVSRAMは世界初のカメラ付き携帯電話に採用されることでモバイルメモリの歴史に大きな一歩を刻んだ。  

---

**English**  
Around 2000, the focus of the semiconductor market shifted from large-capacity DRAM for PCs to mobile devices driven by the rapid spread of cell phones. At Sharp, a project was underway to add a camera to mobile phones, which required **high-density, low-power memory**.  

To meet this demand, in 2001 a **pseudo-SRAM (VSRAM)** was mass-produced by reusing the 0.25 µm DRAM process and adding internal refresh control. While based on DRAM cells, it allowed seamless SRAM-like operation without external refresh, and its operating temperature range was extended from the standard 80 °C to 90 °C to suit mobile applications.  

The initial yield was only about 30%, but mass production was launched as a **rational decision to prioritize market entry**. VSRAM went on to be adopted in Sharp’s first camera-equipped mobile phone, marking a significant milestone in the history of mobile memory.  

---

## 2️⃣ 初期課題と対策 / Startup Challenges and Solutions

### 課題① Pause Refresh Fail (Bin5)

- **問題**  
  モバイル仕様に合わせてスタンバイ電流を低減するため、VSRAMでは **内部リフレッシュ周期を従来DRAMより延長**した。  
  さらに標準 80 °C から **90 °C 動作保証**を追加したことで、セル保持能力の限界が顕在化。  
  高温条件での **ジャンクションリーク増大**が主要因となり、Pause Refresh Fail が多数発生した。  

- **対策**  
  1. **プロセス改善**  
     - DRAM世代ではプラズマアッシングによるダメージが主因であり、これを回避するため **レジスト剥離をウエット処理主体へ切替**。  
     - VSRAMではさらに **HF洗浄の最小化**を行い、ゲート酸化膜残膜を保持して拡散層ダメージを抑制し、SNコンタクト周辺のジャンクションリークを低減。  
  2. **電気設計面の強化**  
     - バックバイアスを −1 V から **−3 V へ強化**し、リーク電流の温度依存性を抑制。  

---

### 課題② Disturb Refresh Fail (Bin6)

- **問題**  
  0.25 µm 世代では短チャネル効果により、隣接ワードラインの繰り返しアクセス時にセルチャネルが擾乱され、リークが増加する **Disturb Refresh Fail** が発生。  
  高温（90 °C）条件下で特に顕著となり、セル保持力を制約する要因となった。  

- **対策**  
  1. **寸法制御の徹底**  
     - **ゲートCDの中心値管理を強化**し、チャネル長のばらつきを抑制。  
     - 短チャネル効果によるリーク増大を抑止。  
  2. **チャネルドーピング最適化**  
     - セルチャネルのドーピング条件を最適化し、しきい値電圧 (Vth) を適度に上昇。  
     - **Vth向上によるリーク抑制と、スイッチング能力の維持**を両立。  
  3. **補助的対策**  
     - バックバイアス強化（−3 V）が、ディスターブ耐性の改善に寄与。  

---

### 成果

- **量産開始時点Yield**: 約30%（市場ニーズ対応を優先して出荷開始）  
- **改善後Yield**: 量産を継続しながら対策を適用し、最終的に **80〜90%** へ向上  
- 高温信頼性試験にも合格し、安定生産が可能に  

**まとめ**  
Pause Refresh Fail と Disturb Refresh Fail の双方に対して、  
- プロセス面（ウエット剥離・HF洗浄最小化・CD管理）  
- デバイス設計面（チャネルドープ・バックバイアス）  
の複合的対策を講じることで、**30%歩留まりでの量産スタートを切った後も改善を積み重ね、最終的に高歩留まりを達成**した。  

当初は、歩留まり改善の重圧の中で、筆者は **毎朝、部課長に囲まれながら進捗状況を報告**しなければならず、技術面だけでなく組織的な緊張感も伴う立ち上げであった。  

---

## 3️⃣ 次世代検討と断念 / Next-Generation Evaluation and Abandonment

### 0.18 µm VSRAM（NANYA/Toshibaプロセス）

- **採用技術**: トレンチキャパシタ方式  
- **問題点**:  
  - トレンチ型は、縦方向に深掘りしキャパシタを形成するため、**ジャンクション面積がスタック型に比べて大きい**  
  - その結果、高温（90 °C）動作でリーク電流が増大し、セル保持不足が顕在化  
- **結果**: モバイル仕様（90 °C保証）を満たせず採用を断念  
- **背景補足**:  
  - **スタック型**：高さ方向で容量を稼ぐため、ジャンクション面積が小さくリークに強い  
  - **トレンチ型**：面積方向で容量を稼ぐため、ジャンクションが大きくリークに弱い  
  - この世代で、**1T-1Cセルを用いた擬似SRAMの限界**が露呈した事例となった  

---

### MoSys 1T-SRAM評価（参考）

- **方式**: DRAMセル不要、リフレッシュ不要のロジック互換型  
- **プロセス**: 0.18 µm CMOSプロセスにそのまま適用可能  
- **魅力**:  
  - リフレッシュ不要のため、低消費電力に有利  
  - ロジックプロセス互換性が高く、組み込み用途に適する  
- **課題**:  
  - マクロとしては魅力的であったが、**セルフリフレッシュ機能を組み込む設計ノウハウが難しく**  
  - 高速SRAMや大容量DRAMに比べて「中途半端な特性」と評価された  
  - 結果として、社内での採用は見送りとなった  
- **参考リンク**: [`MoSys_1T_SRAM_Links.md`](./MoSys_1T_SRAM_Links.md)
  
---

## 4️⃣ まとめ / Summary

**日本語**  
0.25 µm VSRAMは、酒田工場における技術移管DRAMを基盤に成功裏に量産され、世界初のカメラ付き携帯電話を実現する鍵となった。  
しかし0.18 µm世代では、トレンチキャパシタを用いたVSRAMは保持特性の限界により断念され、**1T-1C DRAMセルをベースにした擬似SRAMの終焉**を象徴する事例となった。  

この経験は、エプソンにとって「メモリ製品を長期的に事業化するのではなく、先端技術を吸収し、社内の主力製品（LCDドライバ、ASIC、ロジックICなど）に展開する」戦略を後押しすることとなった。  
結果として、メモリ事業そのものは縮小したが、得られたプロセス・設計・信頼性の知見は、その後の事業競争力を支える基盤となった。  

**English**  
The 0.25 µm VSRAM, successfully mass-produced based on the transferred DRAM process, played a pivotal role in enabling the world’s first camera phone.  
At the 0.18 µm node, however, trench-capacitor-based VSRAM could not meet retention requirements at 90 °C, marking the **end of pseudo-SRAMs built on the 1T-1C DRAM cell concept**.  

For Epson, this experience reinforced the strategy of using DRAM not as a long-term business, but as a **vehicle to absorb advanced technologies and redeploy them into core products such as LCD drivers, ASICs, and logic ICs**.  
Thus, while the memory business itself diminished, the knowledge gained in process, design, and reliability engineering became a cornerstone of Epson’s later product competitiveness.  

# 📎 Appendix: 補足資料 / Supplementary Materials

---

## 1️⃣ 0.25µm DRAM プロセスフロー（概要版）

**日本語**  
1998年立ち上げ時に用いられた、0.25 µm 64M DRAM（第3世代）の代表的なプロセスフロー。  
詳細は [`DRAM_Process_Flow_Full.md`](../in1998/DRAM_Process_Flow_Full.md) を参照。  

**English**  
Representative process flow of 0.25 µm 64M DRAM (3rd Generation) during the 1998 startup.  
See [`DRAM_Process_Flow_Full.md`](../in1998/DRAM_Process_Flow_Full.md) for full details.  

- Semi-recess LOCOS isolation  
- Triple-well, Deep N-Well  
- Poly/WSi stacked gate electrode (WSA-ET process)  
- Stacked capacitor with roughened surface (1.5–1.8× capacitance boost)  
- WSB-CVD simultaneous bit line & contact formation  
- AlCu/TiN metallization, SOG planarization, SiN/PI passivation  

---

## 2️⃣ 0.25µm DRAM ウエハテスト Bin分類表

**日本語**  
ウエハテストはフェイルストップ方式で実施され、致命的不良から順にBin分類される。  
詳細は [`dram_wafer_test_binclass_0.25um.md`](../in1998/dram_wafer_test_binclass_0.25um.md) を参照。  

**English**  
Wafer tests followed a fail-stop scheme, classifying chips into bins in order of fatality.  
See [`dram_wafer_test_binclass_0.25um.md`](../in1998/dram_wafer_test_binclass_0.25um.md) for details.  

| Bin | 日本語テスト項目 | Test Item (English) | 内容概要 |
|-----|----------------|----------------------|-----------|
| 1   | オープン／ショート | Open / Short | 配線断線・短絡 |
| 2   | スタンバイ電流異常 | Standby Current Fail | リーク過大 |
| 3   | アクティブ電流異常 | Active Current Fail | 動作中電流異常 |
| 4   | ファンクション不良 | Function Check Fail | 読書き失敗・デコード異常 |
| 5   | ポーズリフレッシュ不良 | Pause Refresh Fail | セル保持不足 |
| 6   | ディスターブリフレッシュ不良 | Disturb Refresh Fail | 隣接セル干渉による保持低下 |
| 7   | マージン不良 | Margin Fail | 電圧・タイミング余裕不足 |

---

## 3️⃣ VSRAM / DRAM / トレンチVSRAM 比較表

| 項目 / Item | 0.25 µm DRAM (3rd Gen) | 0.25 µm VSRAM | 0.18 µm VSRAM (Trench) |
|-------------|------------------------|---------------|-------------------------|
| セル構造 | スタックキャパシタ | スタックキャパシタ（流用） | トレンチキャパシタ |
| リフレッシュ | 外部制御必須 | 内部制御（疑似SRAM動作） | 内部制御（疑似SRAM動作） |
| 温度保証 | 80 °C | 90 °C（モバイル仕様） | 90 °C目標（未達成） |
| 特徴 | 量産立ち上げ成功 | 世界初カメラ付き携帯に採用 | 保持不足で断念 |
| 意義 | 先端技術吸収のビークル | モバイル応用成功事例 | 1T-1C限界を示す事例 |

---

## 4️⃣ 教育的意義 / Educational Significance

- DRAM量産を **目的そのものではなく「先端技術吸収と社内展開の戦略的ビークル」** と位置づけた点が特徴的。  
- プロセス解析・不良対策・歩留まり改善の実体験が、後続製品（VSRAMなど）に直結。  
- 0.25 µm世代の事例は、**微細化移行期における企業戦略と技術継承** の教材として有用。  

---

📘 本Appendixは、論文本文を補完する参考資料集であり、詳細なプロセス表やテスト条件を収録した。  

# 📝 結論 / Conclusion

---

## 日本語

本研究では、**0.25 µm 64M DRAM立ち上げ（1998）** と、それを基盤とした **モバイル用疑似SRAM (VSRAM, 2001)** の量産事例を整理した。  

エプソン酒田工場におけるDRAMは、最終製品ビジネスとしての展開ではなく、**先端プロセス技術を吸収し、社内製品群へ展開するための戦略的ビークル** として活用された点が特筆される。SCF方式による迅速な立ち上げ、不良解析と歩留まり改善、そして信頼性確保は、DRAM自体の事業化以上に **「技術継承と応用展開」** に大きな意義を持った。  

2001年に量産されたVSRAMは、その成果を直接反映したものであり、世界初のカメラ付き携帯電話を実現する原動力となった。しかし、0.18 µm世代では保持特性の限界によりVSRAMは断念され、1T-1Cセルを用いた擬似SRAMの進化はここで終止符を打った。  

この一連の事例は、**微細化移行期における「製品」よりも「技術獲得と活用」を優先する戦略的アプローチ** の成功例であり、半導体アーカイブおよび教育資料としての価値を持つ。さらに、**現代の技術移管やプロセス立ち上げにおける示唆** を与える事例として位置づけられる。  

---

## English

This study reviewed the **startup of 0.25 µm 64M DRAM (1998)** and the subsequent **mass production of mobile pseudo-SRAM (VSRAM, 2001)**.  

At Epson’s Sakata Fab, DRAM was not pursued as a long-term product business, but rather as a **strategic vehicle for absorbing advanced process technologies and deploying them across in-house product lines**. Rapid SCF-based ramp-up, defect analysis, yield improvement, and reliability validation proved more valuable for **technology transfer and application** than for DRAM commercialization itself.  

The VSRAM mass-produced in 2001 embodied these achievements and enabled the world’s first camera phone. Yet, at the 0.18 µm node, retention limitations forced the abandonment of trench-capacitor-based VSRAM, marking the end of pseudo-SRAM evolution based on the 1T-1C DRAM cell.  

This case exemplifies a **strategic approach prioritizing technology acquisition and utilization over direct product success during process scaling transitions**, making it a valuable archive and educational resource. Moreover, it **provides insights for today’s technology transfer and ramp-up strategies**.  
