# 中級會計學 (Intermediate Accounting) LLM Wiki - Agent 指南

本知識庫遵循 Andrej Karpathy 的 **LLM Wiki** 模式建構，專門針對**中級會計學（IFRS 準則）**打造，服務於**教學備課、演講闡述及後續自動化生成 HTML 互動簡報**。

---

## 1. 核心設定與參考準則

* **權威教材依據**：
  * 書名：*Intermediate Accounting: IFRS Edition (5th Edition, Wiley Custom Edition)*
  * 作者：Donald E. Kieso, Jerry J. Weygandt, Terry D. Warfield
* **語言風格與命名慣例**：
  * **主語言**：繁體中文（台灣會計專業通用語法與科目名稱）。
  * **關鍵術語保留英文原文**：初次出現或標題處並列英文原文。
    * *例*：攤銷後成本（Amortized Cost, AC）、公允價值（Fair Value, FV）、其他綜合損益（Other Comprehensive Income, OCI）、重大財務組成部分（Significant Financing Component）。
* **核心產出目標**：
  * **教學與演講導向（Presentation-Ready）**：知識頁面必須兼具學術嚴謹性與教學說理邏輯，段落層次清晰，便於直接擷取或轉換為模組化教學講義及 HTML 互動簡報。
  * **教材趣味化（Sticker & Character Avatars）**：善用 `assets/` 中的角色貼圖（`img1_char*.png` ～ `img4_char*.png`），在生成教學簡報或釋例時設計「助教提醒」、「學生提問」或「觀念盲點」之對話框。

---

## 2. 三層架構與目錄規範

```text
LLM Wiki/
├── index.html                 # 專案首頁入口：日系手帳風互動簡報總導航 Portal
├── AGENTS.md                  # 本規範文件
├── assets/                    # 教學角色貼圖與視覺資產 (img1_char*.png 等)
├── raw/
│   └── textbook/              # [不可竄改] 使用者提供的各章節 PDF 原始簡報
└── wiki/                      # [LLM 持久維護] Markdown 知識庫
    ├── index.md               # 知識庫總目錄索引
    ├── log.md                 # 時序變更與工作日誌 (Append-only)
    ├── sources/               # 各章節 PDF 的提取與閱讀筆記 (對應 raw/textbook)
    ├── standards/             # 國際財務報導準則專題 (IFRS 9, IFRS 15, IFRS 16, IAS 36 等)
    ├── concepts/              # 核心觀念與定義詞條 (中英對照)
    ├── journal-entries/       # 經典會計分錄、算式推導、折溢價攤銷表模型
    ├── comparisons/           # 跨章節/跨工具比較專題 (如 FVPL vs FVOCI、租賃雙方對稱性)
    └── presentations/         # 模組化簡報大綱、HTML 簡報草稿與演講腳本
```

---

## 3. 知識庫頁面規範與排版標準

### 3.1 YAML Frontmatter（每頁必備）
所有 `wiki/` 內的 Markdown 檔案頂部均需包含標準 Frontmatter：
```yaml
---
title: 收入認列五步驟 (Five-Step Model for Revenue Recognition)
standard: IFRS 15
chapter: Chapter 18
type: concept # concept | standard | journal-entry | comparison | source | presentation
tags: [IFRS15, 收入認列, 合約負債]
last_updated: 2026-11-11
---
```

### 3.2 雙向連結（Wikilinks）
* 內部關聯一律使用 Obsidian 風格的 `[[檔案名稱|顯示名稱]]`。
* 任何章節提到跨章觀念時，必須主動建立連結，例如：
  > 承租人認列之使用權資產，後續應依 [[IAS 36 資產減損|IAS 36]] 進行減損測試。

### 3.3 會計分錄（Journal Entries）標準格式
分錄統一使用 Markdown 代碼塊或清楚的縮排排版，標記借貸方向、科目（中英對照）與金額說明：
```text
借：現金 (Cash)                                      $100,000
    合約負債折價 (Discount on Contract Liability)       $5,000
    貸：合約負債 (Contract Liability)                              $105,000
    （說明：於合約生效日認列預收保證金及重大財務組成之折價）
```

### 3.4 算式與數學表達式
涉及現值、有效利率法攤銷、每股盈餘（EPS）計算時，一律使用 LaTeX 格式：
$$PV = \sum_{t=1}^{n} \frac{CF_t}{(1 + r)^t}$$

---

## 4. LLM Agent 核心作業流程

### 流程一：來源攝取 (Ingest Workflow)
當使用者在 `raw/textbook/` 放入新的章節 PDF 簡報時：
1. **讀取與分析**：深入閱讀 PDF 內容，提煉核心考點、準則條文、分錄演繹與經典釋例。
2. **建立單章來源頁**：在 `wiki/sources/` 建立章節萃取筆記（例如 `sources/ch18_revenue_recognition.md`）。
3. **擴散更新知識庫**：
   * 更新或新建 `wiki/standards/`（對應準則重點）。
   * 更新或新建 `wiki/concepts/`（核心名詞與觀念）。
   * 更新或新建 `wiki/journal-entries/`（代表性分錄與計算題型）。
   * 如有跨章關聯，於 `wiki/comparisons/` 建立或修訂比較表。
4. **維護骨幹**：
   * 將新增或修改的頁面編入 `wiki/index.md`。
   * 在 `wiki/log.md` 追加一條紀錄（格式：`## [YYYY-MM-DD] ingest | Chapter XX: Title`）。

### 流程二：全自動教學投影片 Graph 產出工作流 (Automated Presentation Graph Pipeline)
製作任何章節的 HTML 互動教學簡報時，本系統採用 **完全自主且具內部品質防線的全自動化 Graph 流程 (Autonomous Graph Pipeline)**，無需使用者中途手動審查，從教材攝取至 HTML 簡報發布一氣呵成：

```text
[教材 PDF] ──> 【Ingest: 筆記與概念萃取】
                     │
                     └──> 【Stage 1: 結構大綱節點】 ──> [內部大綱 Auto-Linter]
                                  │
                                  └──> 【Stage 2: 逐頁規格與腳本節點】 ──> [內部容量 Auto-Linter]
                                               │
                                               └──> 【Stage 3: HTML 互動工程節點】 ──> [四大品質安全防線 Auto-Linter]
                                                            │   ├─ 1. 舞台架構與零外溢檢查 (Stage & Anti-Leak)
                                                            │   ├─ 2. 角色貼圖兩位數補零檢查 (Avatar Zero-Padding)
                                                            │   ├─ 3. 高可讀大字級標準檢查 (Typography Scale)
                                                            │   └─ 4. 一頁式零滾動與公式檢查 (Zero-Scroll & KaTeX)
                                                            │
                                                            └──> 【Sync: 首頁 index.html & Wiki 總索引同步】
```

* **Stage 1：結構大綱節點 (Autonomous Outline Node)**
  * **產出格式**：自動提煉章節核心主線，形成 **Markdown 條列式階層清單**（建議總頁數 12~14 頁）。
  * **設計專注**：聚焦於知識脈絡與邏輯推演（引發動機 $\rightarrow$ 準則規範 $\rightarrow$ 實務深入 $\rightarrow$ 跨表串接 $\rightarrow$ 課堂測驗）。
  * **內部 Auto-Linter 檢查**：
    * 自動檢核是否完整涵蓋本章核心考點、專有名詞英漢對照、公式與經典附錄。
    * 確認前後頁次之知識相依性與教學節奏。

* **Stage 2：逐頁規格與腳本節點 (Slide Specification & Dialogue Node)**
  * **產出格式**：自動存檔為 `wiki/presentations/chXX_deck_spec.md`。
  * **單頁規格必備五要素**：
    1. **頁面定位**：頁碼、主標題、副標題、手帳印章標籤。
    2. **版面佈局形式**：精準指定版型（`grid-2` 雙欄對稱、`grid-3`/`grid-4` 多欄並列、`pastel-table` 手帳底稿、`quiz-arena` 測驗擂台、`hero-standee-card` 立繪卡座）。
    3. **核心卡片內文**：提煉結構化條列句，嚴格執行**資訊容量控制**（單張卡片 3~4 行為限，拒絕教科書大段落）。
    4. **角色指派與漫才對話**：明確指定此頁出場角色與對白（柯教授專業引導、兔兔助教速記口訣、小安同學盲點提問、張會計師查核實務）。
    5. **演講備忘錄 (Speaker Notes)**：主講人口語化教學重點。
  * **內部 Auto-Linter 檢查**：
    * 嚴格執行「文字總容量與行數安全檢查」，預先防止單頁超載。

* **Stage 3：HTML 互動工程節點 (Presentation Engine Node)**
  * **實作依據**：以 Stage 2 規格書為藍本，自動產出 `wiki/presentations/chXX_presentation.html`。
  * **工程設計守則與四大品質安全防線 (Crucial Defense Lines)**：
    1. **舞台架構與零外溢防線 (Stage & Anti-Leak Architecture)**：
       * 必須採用成熟穩健之舞台架構：外層容器為 `<main id="slide-stage">`。
       * 投影片默認隱藏 `.slide { display: none; }`，僅當前頁啟用 `.slide.active { display: flex; animation: slideIn 0.25s ease-out; }`。
       * **嚴格禁止橫向 Carousel 容器**（如 `display: flex; transform: translateX`），徹底消除「下一頁邊緣露出於螢幕右側」的破版缺陷！
    2. **角色貼圖兩位數補零防線 (Avatar Zero-Padding Rule)**：
       * 貼圖檔名一律**強制嚴格補零至兩位數**（`../../assets/imgX_char01.png` ～ `char06.png`），**嚴禁使用無補零檔名**（如 `img1_char1.png`），避免瀏覽器 404 破圖！
       * 貼圖一律放置於**專屬立繪卡座**或**對話框左側 62px 圓形頭像座**，**嚴禁以 `position: absolute` 懸浮於內容上方遮擋文字**。
    3. **高可讀大字級標準 (High-Readability Typography Standard)**：
       * 全面套用微調放大字級規格：
         * 主標題 `.slide-h1`：`1.76rem`（字重 900）
         * 副標題 `.slide-subtitle`：`1.02rem`
         * 卡片標題 `.card-title`：`1.20rem`（字重 800）
         * 卡片內文 `.card p, .card li`：`1.04rem`（行高 1.50）
         * 角色對話 `.dialogue-text`：`1.02rem`（頭像直徑 `62px`）
         * 代碼分錄 `.code-box`：`0.95rem`
         * 表格內文 `.pastel-table td`：`0.94rem`
         * 測驗按鈕 `.quiz-btn`：`1.02rem`
    4. **一頁式零滾動與手帳質感組件 (Zero-Scroll & UI Components)**：
       * 投影片本體 `.slide` 設定 `width: min(1380px, calc(100vw - 32px)); height: calc(100vh - 104px); max-height: 890px; min-height: 520px; overflow: hidden;`，在 650px~900px 常見螢幕下 100% 絕無垂直滾動條。
       * 必備手帳視覺組件：頂部進度條 `#progress-bar`、和紙膠帶 `.washi-tape`、日系戳印 `.sticker-stamp`、對話框 `.dialogue-box`、底部導航列 `<footer>`（含膠囊計數器與快捷鍵提示）。
       * 全功能互動支援：全螢幕 (`F`)、講者備忘錄 (`N`)、縮圖總覽 (`O`)、鍵盤方向鍵/Space 切換、小測驗互動判定、URL Hash 雙向綁定（`#1` ~ `#N`）。
  * **內部 Auto-Linter 檢查**：
    * 逐頁檢測零滾動適配、舞台架構防外溢、貼圖補零路徑、大字級高可讀性與 KaTeX 算式完整性。

* **Stage 4：入口總導航與知識庫同步 (Sync Node)**
  * 自動更新專案根目錄的 `index.html`（點亮章節卡片為 Ready、更新投影片總頁數、啟用開啟連結、排程下一章為 Upcoming）。
  * 同步更新 `wiki/index.md` 與 `wiki/log.md`。

### 流程三：健康體檢 (Lint Workflow)
定期或應使用者要求執行知識庫檢查：
* **孤立頁面檢查**：是否存在無任何入鏈（Inbound links）的孤島筆記。
* **術語一致性**：確保完全採用 Kieso IFRS 5/e 體系，無殘留過時準則（如 IAS 39、舊租賃準則）。
* **未解析連結**：修復指向不存在頁面的無效雙向連結。
* **記錄體檢**：在 `wiki/log.md` 記載體檢結果與修復事項。

---

## 5. 角色貼圖運用守則（Assets Guidelines）

`assets/` 存放之人物圖片為教學演講簡報專用視覺素材：
* **嚴格檔名命名規則**：所有貼圖一律為**兩位數補零命名**（`imgX_char01.png` ～ `imgX_char06.png`，絕無 `imgX_char1.png`），引用路徑統一為 `../../assets/imgX_char0Y.png`。
* `img1_char0*.png`：通常指派為「主講教師 / 教授」形象（專業、引導思考）。
* `img2_char0*.png`：指派為「學習助教」（提示考點、解題秘訣、準則條款參照）。
* `img3_char0*.png`：指派為「提問學生」（拋出常見盲點、初學者直覺誤區）。
* `img4_char0*.png`：指派為「審計員 / 業界專家」（探討實務財報揭露與經濟實質）。

在撰寫 `wiki/presentations/` 的教學模組時，可利用 Markdown 區塊或 HTML 標籤結構將角色圖融入，以便後續一鍵轉換為 HTML 簡報！
