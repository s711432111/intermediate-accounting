# 中級會計學 LLM Wiki 工作日誌

本檔案為 Append-only 變更紀錄，記錄每次簡報攝取 (Ingest)、教學產出 (Query/Presentation)、與庫內體檢 (Lint)。

---

## [2026-11-11] init | 初始化知識庫架構
- 建立 `AGENTS.md`：規範中會 IFRS 5/e 教學與簡報導向維護原則。
- 建立資料夾架構：`raw/textbook/`、`wiki/standards/`、`wiki/concepts/`、`wiki/journal-entries/`、`wiki/presentations/`、`wiki/sources/`、`wiki/comparisons/`。
- 整合 `assets/` 角色貼圖角色設定（教師、助教、學生、審計員）。
- 建立 `wiki/index.md` 與 `wiki/log.md` 基礎骨幹。

## [2026-11-11] ingest | Chapter 1: The Environment and Conceptual Framework for Financial Reporting
- 萃取 Chapter 1 簡報內容，涵蓋全球金融市場、資本配置、IASB 組織、IFRS 層級、正當程序。
- 深度梳理觀念架構三層結構（目標、第二層橋樑品質特性與要素、第三層假設與原則）。
- 新增來源筆記：`wiki/sources/ch01_environment_and_conceptual_framework.md`。
- 新增概念頁面：
  - `wiki/concepts/conceptual_framework.md`
  - `wiki/concepts/qualitative_characteristics.md`
  - `wiki/concepts/fair_value_hierarchy.md`
- 新增分錄與算式頁面：
  - `wiki/journal-entries/cash_to_accrual_conversion.md` (附錄 1A 轉換算式與工作底稿)
  - `wiki/journal-entries/reversing_entries.md` (附錄 1B 迴轉分錄規則與經典對照)
- 新增比較專題：`wiki/comparisons/cash_vs_accrual.md`。
- 新增教學簡報模組：`wiki/presentations/ch01_lecture_deck.md`（包含角色貼圖教學腳本）。
- 更新 `wiki/index.md` 索引總表。

## [2026-11-11] presentation | Chapter 1 互動教學簡報與教材存檔
- 將原始簡報檔案 `Ch01_Kieso_WEB - new.pdf` 存入 `raw/textbook/`。
- 依據知識庫與簡報大綱，生成完整 HTML 互動式簡報：`wiki/presentations/ch01_presentation.html`。
  - 涵蓋 13 頁互動投影片（金字塔架構、品質特性對比、IFRS 13 公允價值層級切換、現金轉權責工作底稿、迴轉分錄對照、課堂互動小測驗）。
  - 完整整合 `assets/` 角色貼圖（教授、助教、提問學生、會計師）。
  - 支援全螢幕 (F)、講者備忘錄 (N)、總覽導航 (O) 與鍵盤/手勢滑動控制。
- 更新 `wiki/index.md`。

## [2026-11-11] presentation | 第一章「日系燕麥奶茶手帳風」HTML 簡報正式定案
- 使用者確定選用「風格 A：日系燕麥奶茶手帳風 (Cozy Milk Tea Journal)」。
- 重新全面生成 `wiki/presentations/ch01_presentation.html`：
  - 13 頁完整投影片架構，全面換上燕麥米白底、溫暖拿鐵棕文字、焦糖奶茶卡片、半透明紙膠帶 (Washi Tape) 與手帳印章。
  - 大量融入 `assets/` 24 款貼圖：封面與結語大立繪、卡片角落探頭貼紙 (Peeking Stickers)、角色漫才對話卡、小測驗答對/答錯動態表情反饋。
  - 保留專業演講功能：全螢幕 (F)、演講備忘錄抽屜 (N)、投影片縮圖總覽導航 (O)、公允價值層級即時切換、李萬醫師工作底稿手帳表格、觸控手勢滑動。

## [2026-11-11] presentation | 投影片字體等比微調放大與排版優化
- 根據使用者反饋，將投影片全域字體進行微調放大（內文與列表由 `0.85rem` 調升至 `0.94rem`，標題由 `1.45rem` 調升至 `1.62rem`）。
- 同步微調對話氣泡字體（`0.94rem`）、頭像尺寸（`62px`）與表格字級（`0.88rem`）。
- 嚴格維持一頁式免滾動（Zero-Scroll）結構，確保文字清晰易讀且版面留白與視覺比重更加飽滿平衡。

## [2026-11-11] standard | 投影片 Graph 生成工作流定案與規格書沉澱
- 將「全自動端到端教學投影片 Graph 產出工作流 (Automated Presentation Graph Pipeline)」正式寫入 `AGENTS.md`，移除人工審查檢查點，改採自主內部品質防線（Auto-Linters）。
- 更新根目錄首頁入口 `index.html`（日系燕麥奶茶手帳風導航 Portal）。

## [2026-11-11] ingest & presentation | Chapter 3: Statement of Financial Position and Statement of Cash Flows (全自動 Graph 產出)
- 將原始教材 `Ch03_Kieso_Financial_Position_and_Cash_Flows.pdf` 歸檔至 `raw/textbook/`。
- 萃取章節知識，建立來源筆記 `wiki/sources/ch03_financial_position_and_cash_flows.md`。
- 執行全自動 Graph Pipeline：
  - Stage 1：自主提煉 13 頁階層大綱（涵蓋資產負債價值限制、非流動/流動劃分、現金流量表三大活動、間接法推導、Hu Inc. 黑字倒閉案例、重大非現金活動、自由現金流量 FCF 與比率分析）。
  - Stage 2：自主產出規格與角色腳本 `wiki/presentations/ch03_deck_spec.md`（完整規劃四大角色漫才對白、講者備忘錄與版面佈局）。
  - Stage 3：自主編譯產出日系燕麥奶茶手帳風 HTML 簡報 `wiki/presentations/ch03_presentation.html`（嚴格零滾動、防擠壓、貼圖無遮擋、互動小測驗判定與全功能導航）。
- 同步更新專案首頁 `index.html`（點亮 Chapter 3，更新總收錄 3 章 39 頁）與 `wiki/index.md` 總索引。

## [2026-11-11] presentation | 全套投影片與首頁字體全面放大升級 (Enhanced Readability)
- 響應使用者大螢幕與演講投影閱讀需求，對 Chapter 1、Chapter 2、Chapter 3 之 HTML 簡報及專案首頁 `index.html` 進行字級放大與排版調校：
  - **投影片舞台尺度放寬**：`.slide` 最大寬度由 `1320px` 放寬至 `1380px`，高度由 `calc(100vh - 108px)` 優化為 `calc(100vh - 104px)`（最大高度調升至 `890px`），大幅消除大螢幕周邊過多背景死白，讓版面飽滿大器。
  - **層級字級全面顯著調升**：
    - 主標題 `.slide-h1`：`1.48rem ~ 1.62rem` $\rightarrow$ `1.76rem`
    - 副標題 `.slide-subtitle`：`0.88rem ~ 0.94rem` $\rightarrow$ `1.02rem`
    - 卡片標題 `.card-title`：`1.02rem ~ 1.10rem` $\rightarrow$ `1.20rem`
    - 卡片正文 `.card p, .card li`：`0.88rem ~ 0.95rem` $\rightarrow$ `1.04rem`（行高調升至 `1.50`）
    - 角色對話字體 `.dialogue-text`：`0.86rem ~ 0.94rem` $\rightarrow$ `1.02rem`（頭像擴大至 `62px`）
    - 會計算式與分錄 `.code-box`：`0.80rem ~ 0.88rem` $\rightarrow$ `0.94rem ~ 0.96rem`
    - 表格單元格 `.pastel-table td`：`0.84rem ~ 0.90rem` $\rightarrow$ `0.94rem ~ 0.96rem`
    - 課堂測驗選項 `.quiz-btn`：`0.88rem ~ 0.94rem` $\rightarrow$ `1.02rem`
    - 導航與狀態按鈕：`0.80rem ~ 0.84rem` $\rightarrow$ `0.88rem ~ 0.94rem`
  - **嚴格零滾動排版防護 (Zero-Scroll & Anti-Squish)**：清理三個章節中過小的 inline 樣式（`0.76rem ~ 0.84rem` 統整提升至 `0.94rem ~ 0.98rem`），動態調節 padding 與 gap，確保全 39 頁投影片在各解析度下均 100% 絕無垂直滾動條、無文字截斷、貼圖無遮擋。
  - **同步提升首頁 `index.html` 字體層級**：標題升至 `2.3rem`、章節名稱升至 `1.35rem`、描述文字升至 `0.98rem`。

## [2026-11-11] ingest & presentation | Chapter 4: Accounting and the Time Value of Money (全自動 Graph 產出)
- 將原始教材 `Ch04_Kieso_Time_Value_of_Money.pdf` 歸檔至 `raw/textbook/`。
- 萃取章節知識，建立來源筆記 `wiki/sources/ch04_time_value_of_money.md`。
- 擴散更新核心知識庫：
  - 新增概念筆記：`wiki/concepts/time_value_of_money.md`（時間價值八大會計應用、單利 vs 複利、複利頻率與實質年收益率）。
  - 新增概念筆記：`wiki/concepts/annuities.md`（普通年金、到期年金、遞延年金兩段式折現與差額法）。
  - 新增分錄模型：`wiki/journal-entries/effective_interest_amortization.md`（長期公司債雙現金流定價與有效利率法折溢價攤銷表）。
- 執行全自動 Graph Pipeline：
  - **Stage 1**：自主提煉 13 頁階層大綱（涵蓋時間價值哲學、單利 vs 複利、複利頻率效應、單筆終值現值對稱、反求期數與利率、年金三要素、普通年金 vs 到期年金 $(1+i)$、遞延年金、公司債定價、有效利率法攤銷、IFRS 13 期望現金流量法與利率三要素、課堂互動小測驗）。
  - **Stage 2**：自主產出規格與角色腳本 `wiki/presentations/ch04_deck_spec.md`（完整規劃柯教授、兔兔助教、小安同學、張會計師四大角色漫才對白、講者備忘錄與版面佈局）。
  - **Stage 3**：自主編譯產出日系燕麥奶茶手帳風 HTML 簡報 `wiki/presentations/ch04_presentation.html`（採用最新升級的高清晰放大字體規範、嚴格零滾動、防擠壓、貼圖無遮擋、互動小測驗判定、KaTeX 數學公式與全功能導航）。
- **Stage 4**：同步更新專案首頁 `index.html`（點亮 Chapter 4 為 Ready，總收錄投影片擴增為 4 章 52 頁，新增 Chapter 5 為 Upcoming）與 `wiki/index.md` 總索引。

## [2026-11-11] ingest & presentation | Chapter 5: Cash and Receivables (全自動 Graph 產出)
- 將原始教材 `Ch05_Kieso_Cash_and_Receivables.pdf` 歸檔至 `raw/textbook/`。
- 深入萃取章節內容，建立單章來源筆記 `wiki/sources/ch05_cash_and_receivables.md`。
- 擴散更新核心知識庫：
  - 新增概念筆記：`wiki/concepts/cash_and_receivables.md`（現金認定、約當現金 3 個月門檻、受限制現金與補償性餘額分類、銀行透支 IAS 7 抵銷條件、現金折扣總額法 vs 淨額法、IFRS 9 備抵法與帳齡分析表）。
  - 新增概念筆記：`wiki/concepts/receivables_derecognition.md`（質押借款 vs 應收帳款承購 Factoring、無追索權 vs 附有限追索權出售、IFRS 9 金融資產除列三道檢驗決策樹）。
  - 新增分錄模型：`wiki/journal-entries/bank_reconciliation.md`（附錄 5A 銀行存款調節表四象限平衡模型、在途存款與未兌現支票時間差分析、公司端四項必要調整分錄）。
- 執行全自動教學投影片 Graph 流程 (Automated Presentation Graph Pipeline)：
  - **Stage 1 & 2**：自主產出 13 頁完整規格書與逐頁腳本 `wiki/presentations/ch05_deck_spec.md`（流動性判定 $\rightarrow$ 交易價格與折扣 $\rightarrow$ 預期信用損失備抵法 $\rightarrow$ 零息票據折價攤銷 $\rightarrow$ 公允價值階梯 $\rightarrow$ 承購融資 $\rightarrow$ 除列決策樹 $\rightarrow$ Crest Textiles 經典釋例 $\rightarrow$ 報表週轉分析 $\rightarrow$ 銀行存款調節表 $\rightarrow$ 隨堂測驗）。
  - **Stage 3**：自主生成高清晰日系燕麥奶茶手帳風互動簡報 `wiki/presentations/ch05_presentation.html`（嚴格零滾動、防擠壓、採用最新微調放大之高清晰字級規範、角色貼圖底座展示、KaTeX 數學公式、互動測驗即時判定、講者備忘錄抽屜與縮圖總覽導航）。
- **Stage 4**：同步根目錄總導航 `index.html`（點亮 Chapter 5 為 Ready，總投影片躍升至 5 章 65 頁，新增 Chapter 6 存貨為 Upcoming）與總目錄 `wiki/index.md`。

## [2026-11-11] fix | 修正 Chapter 5 簡報角色貼圖檔名補零路徑
- 修正 `wiki/presentations/ch05_presentation.html` 與 `wiki/presentations/ch05_deck_spec.md` 中所有角色貼圖路徑。
- 將 `imgX_charY.png`（遺漏兩位數補零）全面修復為 `imgX_char0Y.png`（如 `img1_char01.png`、`img2_char01.png` 等），確保所有立繪展座與漫才對話頭像完美載入，無破圖問題。

## [2026-11-11] ingest & presentation | Chapter 6: Inventories (全自動 Graph 產出)
- 將原始教材 `Ch06_Kieso_Inventories.pdf` 歸檔至 `raw/textbook/`。
- 深入萃取章節內容，建立單章來源筆記 `wiki/sources/ch06_inventories.md`（涵蓋 LO 1 至 LO 10 全章重點與附錄 6A）。
- 擴散更新核心知識庫：
  - 新增概念筆記：`wiki/concepts/inventory_valuation_and_cost_flows.md`（永續 vs 定期盤存制、FIFO vs 平均成本法、物價上漲下稅負與現金流天秤、IFRS 禁用 LIFO 理由、存貨錯誤兩期自動抵銷）。
  - 新增概念筆記：`wiki/concepts/lcnrv_and_estimation_methods.md`（IAS 2 成本與淨變現價值孰低法 LCNRV、逐項比較法、跌價回升上限歷史成本天花板、生物資產 IAS 41、虧損採購承諾 IAS 37、毛利率法加價率轉換、傳統零售價法排除減價原理）。
  - 新增分錄模型：`wiki/journal-entries/inventory_adjustments.md`（永續 vs 定期盤存制交易分錄對照、進貨現金折扣淨額法、LCNRV 跌價提列與回升限制、虧損採購合約負債準備）。
- 執行全自動教學投影片 Graph 流程 (Automated Presentation Graph Pipeline)：
  - **Stage 1 & 2**：自主產出 13 頁完整規格書與逐頁腳本 `wiki/presentations/ch06_deck_spec.md`（分類與盤存制 $\rightarrow$ 成本歸屬與折扣 $\rightarrow$ FIFO 與平均 $\rightarrow$ 通膨效應與 LIFO 禁制 $\rightarrow$ 存貨錯誤自動抵銷 $\rightarrow$ IAS 2 核心 LCNRV $\rightarrow$ 跌價回升上限 $\rightarrow$ 生物資產與虧損合約 $\rightarrow$ 毛利率法加價率轉換 $\rightarrow$ 傳統零售價法 $\rightarrow$ 隨堂測驗）。
  - **Stage 3**：自主生成高清晰日系燕麥奶茶手帳風互動簡報 `wiki/presentations/ch06_presentation.html`（嚴格零滾動、防擠壓、採用最新微調放大之高清晰字級規範、角色貼圖檔名嚴格兩位數補零無破圖保證、KaTeX 數學公式、互動測驗即時判定、講者備忘錄抽屜與縮圖總覽導航）。
- **Stage 4**：同步根目錄總導航 `index.html`（點亮 Chapter 6 為 Ready，總投影片擴增至 6 章 78 頁，新增 Chapter 7 不動產廠房及設備為 Upcoming）與總目錄 `wiki/index.md`。


## [2026-11-11] ingest & presentation | Chapter 7: Property, Plant, and Equipment (全自動 Graph 產出)
- 將原始教材 `Ch07_Kieso_PP&E_Acquisition_and_Disposition.pdf` 歸檔至 `raw/textbook/`。
- 深入研讀章節內容，建立單章來源筆記 `wiki/sources/ch07_property_plant_equipment.md`（涵蓋 LO 1 至 LO 6 與附錄 7A）。
- 擴散更新知識庫：
  - 新增概念筆記：`wiki/concepts/borrowing_costs_capitalization.md`（IAS 23 借款成本資本化、符合資格資產、資本化起訖期、累積支出加權平均數 WAAE、可避免借款成本上限、專案借款閒置資金暫時投資收益沖減利息）。
  - 新增概念筆記：`wiki/concepts/nonmonetary_asset_exchanges.md`（IAS 16 非貨幣性資產交換、商業實質判定條件、現金流量顯著改變、損益認列核心矩陣：具商業實質全額認列、不具商業實質損失立即認、利得全額遞延入換入資產帳面）。
  - 新增概念筆記：`wiki/concepts/investment_property_ias40.md`（IAS 40 投資性不動產定義與排除範圍、成本模式 vs 公允價值模式：公允價值模式完全不提列折舊且變動全額認列當期損益 P&L、嚴格區別 IAS 16 重估價模式 OCI）。
  - 新增分錄模型：`wiki/journal-entries/ppe_acquisition_and_disposition.md`（包裹購買相對比例分攤、長期不附息票據遞延付款重大財務組成折價攤銷、自建在建工程利息資本化分錄、資產交換利得認列與遞延對照分錄、IAS 20 政府補助遞延收益法與資產減除法、資產除列與火災保險非自願轉換損益認列）。
- 執行全自動教學投影片 Graph 流程 (Automated Presentation Graph Pipeline)：
  - **Stage 1 & 2**：自主產出 13 頁規格書與逐頁腳本 `wiki/presentations/ch07_deck_spec.md`（取得成本四大類別劃分 $\rightarrow$ 自建製造費用正常產能分攤 $\rightarrow$ IAS 23 資本化三要件 $\rightarrow$ WAAE 演算與借款配對 $\rightarrow$ 包裹購買與遞延付款 $\rightarrow$ 非貨幣交換商業實質 $\rightarrow$ 交換分錄對照 $\rightarrow$ IAS 20 政府補助 $\rightarrow$ 取得後支出組件會計 $\rightarrow$ 處分與非自願轉換 $\rightarrow$ IAS 40 投資性不動產 $\rightarrow$ 隨堂測驗小擂台）。
  - **Stage 3**：自主編譯高清晰日系燕麥奶茶手帳風互動簡報 `wiki/presentations/ch07_presentation.html`（嚴格零滾動、防擠壓、採用最新微調放大之高可讀字級規範、角色貼圖檔名兩位數補零無遮擋保證、KaTeX 數學公式、小測驗即時判定、講者備忘錄抽屜、縮圖總覽導航）。
  - **Stage 4**：同步根目錄總導航 `index.html`（點亮 Chapter 7 為 Ready，總投影片擴增至 7 章 91 頁，新增 Chapter 8 折舊、減損與折耗為 Upcoming）與總目錄 `wiki/index.md`。


## [2026-11-11] ingest & presentation | Chapter 8: Depreciation, Impairments, and Depletion (全自動 Graph 產出)
- 將原始教材 `Ch08_Kieso_Depreciation_Impairments_Depletion.pdf` 歸檔至 `raw/textbook/`。
- 深入研讀章節內容，建立單章來源筆記 `wiki/sources/ch08_depreciation_impairments_depletion.md`（涵蓋 LO 1 至 LO 7 與附錄 8A）。
- 擴散更新知識庫：
  - 新增概念筆記：`wiki/concepts/depreciation_methods_and_component.md`（折舊為成本分攤本質、實體 vs 經濟壽命、四大折舊方法公式與經濟適用模式、IAS 16 組件折舊強制規範、年中購置不滿一年服務年跨期拆解、IAS 8 估計變動推延法）。
  - 新增概念筆記：`wiki/concepts/asset_impairment_ias36.md`（IAS 36 減損兩步驟、可回收金額取公允價值減出售成本與使用價值孰高、現金產生單位 CGU 與商譽優先沖銷防線、減損後新折舊與迴轉法定天花板限制、商譽絕對禁止迴轉、IFRS 5 待處分資產終止折舊）。
  - 新增概念筆記：`wiki/concepts/depletion_and_mineral_resources.md`（天然資源折耗基礎四要素、IFRS 6 探勘評估資產、生產數量法折耗計量、開採時資本化入存貨、清算股利資本返還性質）。
  - 新增概念筆記：`wiki/concepts/revaluation_model_ias16.md`（附錄 8A IAS 16 重估價模式、整類資產一致性、重估增值入 OCI、重估下跌入 P&L、先跌後漲回升沖補損益、處分時 AOCI 直轉保留盈餘嚴禁重分類至損益 No Recycling、對照 IAS 40 公允價值模式）。
  - 新增分錄模型：`wiki/journal-entries/depreciation_impairment_revaluation.md`（年數合計法年中購置不滿一年跨期拆解分錄、IAS 36 減損認列與迴轉法定天花板數值演練、天然資源開採存貨與銷貨轉銷分錄、附錄 8A 重估價土地三年漲跌回升完整分錄歷程與處分轉保留盈餘）。
- 執行全自動教學投影片 Graph 流程 (Automated Presentation Graph Pipeline)：
  - **Stage 1 & 2**：自主產出 13 頁規格書與逐頁腳本 `wiki/presentations/ch08_deck_spec.md`（折舊本質 $\rightarrow$ 四大經典折舊方法 $\rightarrow$ 組件折舊與部分期間拆分 $\rightarrow$ IAS 8 估計變動推延 $\rightarrow$ IAS 36 減損兩步驟決策 $\rightarrow$ CGU 與商譽分攤順序 $\rightarrow$ 減損後折舊與迴轉天花板 $\rightarrow$ IFRS 5 待處分資產 $\rightarrow$ 天然資源折耗與存貨流轉 $\rightarrow$ 附錄 8A 重估價機制 $\rightarrow$ AOCI 直轉保留盈餘 No Recycling $\rightarrow$ 隨堂測驗小擂台）。
  - **Stage 3**：自主編譯高清晰日系燕麥奶茶手帳風互動簡報 `wiki/presentations/ch08_presentation.html`（100% 對齊成熟穩健之 `#slide-stage` 舞台架構、嚴格零滾動、防擠壓、採用最新微調放大之高可讀字級規範、角色貼圖檔名兩位數補零無遮擋保證、KaTeX 數學公式、小測驗即時判定、講者備忘錄抽屜、縮圖總覽導航）。
  - **Stage 4**：同步根目錄總導航 `index.html`（點亮 Chapter 8 為 Ready，全站總投影片擴增至 8 章 104 頁，新增 Chapter 9 無形資產與商譽為 Upcoming）與總目錄 `wiki/index.md`。


## [2026-11-11] standard & fix | 全自動 Graph Pipeline 架構升級與缺陷防線覆盤
- **覆盤問題一：角色貼圖檔名遺漏補零（圖片 404 破圖）**：
  - *問題成因*：早期規格書與生成模組誤用 `imgX_char1.png`，而資產庫檔案為兩位數補零命名（`imgX_char01.png`），導致瀏覽器解析圖片路徑失敗。
  - *根本防禦*：在 `AGENTS.md` 規範與 Stage 3 內部 Auto-Linter 明確納入「貼圖兩位數補零檢查（Avatar Zero-Padding Rule）」，強制全面採用 `char01` 至 `char06`，路徑統一為 `../../assets/imgX_char0Y.png`。
- **覆盤問題二：投影片橫向 Carousel 容器導致頁面外溢（右側露出下一頁邊緣）**：
  - *問題成因*：Chapter 7 曾一度嘗試使用 Flex 橫向排版容器（`display: flex; transform: translateX`），在特定螢幕解析度或縮放下，右側邊緣會露出下一頁投影片內容。
  - *根本防禦*：在 `AGENTS.md` 確立「嚴格舞台架構規範（Stage & Anti-Leak Architecture）」，強制採用成熟的 `<main id="slide-stage">` 舞台結構，全體卡片預設 `.slide { display: none; }`，僅當前頁啟用 `.slide.active { display: flex; animation: slideIn 0.25s ease-out; }`，徹底杜絕相鄰頁面內容外溢。
- **覆盤問題三：字體可讀性與手帳視覺組件一致性**：
  - *根本防禦*：將微調放大之高可讀大字級標準（主標 `1.76rem`、卡片標題 `1.20rem`、內文 `1.04rem`、行高 `1.50`、對話 `1.02rem`、頭像 `62px`）以及全套手帳經典組件（進度條、和紙膠帶、戳印標籤、對話框、膠囊導航列）正式收錄為 Stage 3 標準設計守則。
- **狀態檢核**：
  - Chapter 1 至 Chapter 8 全體 8 份 HTML 簡報均符合最新四大防線規範。
  - 專案首頁 `index.html` 正確顯示「已收錄 8 章 · 104 頁投影片」，下一章 Chapter 9 已排程待命。
  - 知識庫總索引 `wiki/index.md` 與工作日誌 `wiki/log.md` 均維持 100% 同步。
