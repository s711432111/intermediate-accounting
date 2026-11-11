# 📘 中級會計學 (Intermediate Accounting) LLM Wiki & 互動教學簡報

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-brightgreen?style=for-the-badge&logo=github)](https://pages.github.com/)
[![IFRS Standard](https://img.shields.io/badge/Standard-IFRS%20Edition%205%2Fe-blue?style=for-the-badge)](https://www.wiley.com/)
[![Style](https://img.shields.io/badge/Style-Cozy%20Milk%20Tea%20Journal-orange?style=for-the-badge)](#)

本專案遵循 **LLM Wiki** 模式建構，依據權威教材 **Donald E. Kieso, Jerry J. Weygandt, Terry D. Warfield 所著之《Intermediate Accounting: IFRS Edition (5th Edition, Wiley)》**，融合台灣中級會計學繁體中文專業術語與全自動化生成技術，打造兼具學術嚴謹性與教學說理邏輯的 **日系燕麥奶茶手帳風 (Cozy Milk Tea Journal)** 互動教學簡報系統與知識庫。

---

## 🌟 核心特色 (Key Features)

* **📖 8 大章節 · 104 頁高畫質互動投影片**：從財務報導觀念架構貫穿至不動產折舊、減損與天然資源折耗。
* **🎨 日系燕麥奶茶手帳風 (Cozy Milk Tea Journal)**：高溫潤配色、細膩和紙膠帶 (`washi-tape`)、日系戳印標籤、獨立人物立繪展示卡與師生漫才對話框。
* **🛡️ 嚴格一頁式零滾動 (Zero-Scroll & Anti-Squish)**：
  * 成熟穩健之舞台架構（`<main id="slide-stage">` + `.slide.active`），徹底消除「下一頁漏邊」的破版缺陷。
  * 視窗自適應高度（`calc(100vh - 104px)`，在 650px~900px 螢幕下 100% 絕無垂直滾動條）。
* **👁️ 高可讀放大字級標竿 (High-Readability Typography)**：
  * 主標題 `1.76rem`（字重 900）、副標題 `1.02rem`、卡片標題 `1.20rem`、卡片內文 `1.04rem`（行高 1.50）、角色對話 `1.02rem`（頭像直徑 `62px`）、代碼分錄 `0.95rem`。
* **⚡ 完整互動操控支援**：
  * 鍵盤切換（`Space` / `左右方向鍵` / 觸控滑動）。
  * 全螢幕模式（快捷鍵 `F`）。
  * 講者備忘錄與演講腳本抽屜（快捷鍵 `N`）。
  * 投影片縮圖總覽導航（快捷鍵 `O`）。
  * 課堂隨堂小測驗（即時正誤反饋與詳盡剖析）。
  * URL Hash 雙向綁定（`#1` ～ `#13` 直達指定頁）。
* **📐 KaTeX 專業數學公式與會計分錄模型**：現值折現、有效利率法攤銷、WAAE 計算、減損迴轉天花板。

---

## 📚 已收錄章節全覽 (Chapter Directory)

點擊專案首頁 `index.html` 即可進入日系手帳導航入口，開啟各章全功能互動簡報：

| 章節 | 中文名稱 | 英文名稱 / 準則規範 | 頁數 | 核心焦點 |
| :---: | :--- | :--- | :---: | :--- |
| **Ch 01** | **財務報導之環境與觀念架構** | The Environment & Conceptual Framework | 13 頁 | IASB 架構、觀念架構八章全覽、品質特性、權責基礎轉換 |
| **Ch 02** | **綜合損益表與相關資訊** | Income Statement & Related Information | 13 頁 | 多步驟獲利階梯、IFRS 5 停業單位稅後拆分、IAS 8 會計變動、OCI |
| **Ch 03** | **財務狀況表與現金流量表** | Statement of Financial Position & Cash Flows | 13 頁 | 資產負債三性、IAS 7 現金流三大活動、黑字倒閉診斷、FCF |
| **Ch 04** | **會計與貨幣時間價值** | Accounting & Time Value of Money | 13 頁 | 複利現值、普通/到期年金、長期公司債有效利率法攤銷、期望現金流 |
| **Ch 05** | **現金與應收款項** | Cash & Receivables | 13 頁 | 約當現金判定、受限制現金、IFRS 15 淨額法、IFRS 9 除列決策樹、調節表 |
| **Ch 06** | **存貨之衡量與評價** | Inventories | 13 頁 | 永續 vs 定期盤存、FIFO vs 平均法、LCNRV 孰低法、生物資產、零售價法 |
| **Ch 07** | **不動產、廠房及設備取得與處分** | PP&E: Acquisition & Disposition | 13 頁 | 取得成本界線、自建資產費用分攤、IAS 23 借款資本化、商業實質、IAS 40 |
| **Ch 08** | **折舊、減損與天然資源折耗** | Depreciation, Impairments, & Depletion | 13 頁 | 四大折舊法、組件折舊、IAS 36 減損與迴轉天花板、折耗存貨流轉、重估價 |

---

## 🚀 如何部署至 GitHub Pages (Deployment Guide)

只需簡單 3 步驟，即可將本專案發布為可在線瀏覽的互動網站：

### 步驟 1：上傳程式碼至 GitHub Repository
```bash
git init
git add .
git commit -m "feat: 初次發布中級會計學 LLM Wiki 互動簡報系統 (Ch01~Ch08)"
git branch -M main
git remote add origin https://github.com/<你的使用者名稱>/<你的儲存庫名稱>.git
git push -u origin main
```

### 步驟 2：開啟 GitHub Pages
1. 前往 GitHub 儲存庫頁面，點選右上角 **Settings**。
2. 在左側選單點選 **Pages**。
3. 在 **Build and deployment** 區塊：
   * **Source** 選擇 `Deploy from a branch`。
   * **Branch** 選擇 `main` 分支，資料夾選擇 `/ (root)`。
4. 點擊 **Save**。

### 步驟 3：開始線上瀏覽！
約 1~2 分鐘後，GitHub Pages 將提供專屬網址：
`https://<你的使用者名稱>.github.io/<你的儲存庫名稱>/`
點擊即可開啟手帳風總導航首頁，自由切換各章節教學投影片！

---

## 📂 專案檔案結構 (Project Structure)

```text
├── index.html                 # 專案入口首頁：日系燕麥奶茶手帳風導航 Portal
├── README.md                  # 專案說明文件（本檔）
├── .nojekyll                  # 確保 GitHub Pages 正常載入所有資產與 Markdown
├── .gitignore                 # Git 忽略設定
├── AGENTS.md                  # LLM Wiki 規範與全自動 Graph 產出工作流準則
├── assets/                    # 角色貼圖視覺資產 (img1_char01.png ~ img4_char06.png)
├── raw/
│   └── textbook/              # [原始教材] Kieso 各章節 PDF
└── wiki/                      # Markdown 知識庫與互動簡報
    ├── index.md               # 知識庫總目錄索引
    ├── log.md                 # 時序變更與工作日誌 (Append-only)
    ├── sources/               # 各章節 PDF 深入提煉閱讀筆記
    ├── concepts/              # 核心觀念與定義詞條 (中英對照)
    ├── journal-entries/       # 經典會計分錄模型與算式推導
    ├── comparisons/           # 跨章節比較專題
    └── presentations/         # 各章 HTML 互動簡報 (ch01 ~ ch08) 與規格書
```

---

## 👥 登場教學角色形象 (Character Avatars)

* 👨‍🏫 **柯教授** (`img1_char*.png`)：主講教師，專業嚴謹，負責觀念引導與準則核心闡釋。
* 🐰 **兔兔助教** (`img2_char*.png`)：解題助教，提示高頻考點、速記口訣與準則條款對照。
* 🎒 **小安同學** (`img3_char*.png`)：提問學生，代表初學者直覺誤區、盲點提問與實務疑惑。
* 💼 **張會計師** (`img4_char*.png`)：業界專家，探討審計查核實務、財務報表揭露與經濟實質。

---

## 📜 版權與參考準則 (License & Reference)

* **教科書依據**：*Intermediate Accounting: IFRS Edition (5th Edition)* - Donald E. Kieso, Jerry J. Weygandt, Terry D. Warfield (Wiley)
* 本專案僅供學術研究、教學備課與生成式 AI 輔助教學展示使用。
