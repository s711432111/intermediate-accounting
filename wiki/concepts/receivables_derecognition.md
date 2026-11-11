---
title: 應收款項移轉、承購與 IFRS 9 除列決策樹 (Transfers of Receivables and Derecognition)
standard: IFRS 9
chapter: Chapter 5
type: concept
tags: [應收帳款承購, 質押借款, 無追索權出售, 附追索權出售, 追索權負債, 金融資產除列, 實質所有風險與報酬, 控制權]
last_updated: 2026-11-11
---

# 應收款項移轉、承購與 IFRS 9 除列決策樹

企業為加速資金回籠、降低信用風險或避免收款行政成本，常將應收帳款向金融機構融資或出售。然而，**在會計上何時能將應收帳款從資產負債表「除列 (Derecognize)」？何時必須視為「擔保借款 (Secured Borrowing)」？** 這是 IFRS 9 核心考點。

---

## 1. 應收款項融資之兩大模式

### 1.1 質押借款 (Secured Borrowing)
* **實質**：企業以應收帳款作為抵押品，向銀行或財務公司申請借款。
* **會計處理**：
  * **不除列應收帳款**。
  * 認列應付票據/借款負債 (Notes Payable)。
  * 支付銀行之初期融資手續費認列為融資費用 (Finance Expense)。
  * 若客戶直接向銀行還款，企業再同步沖轉借款負債與應收帳款。

### 1.2 應收帳款承購 / 出售 (Factoring / Sale of Receivables)
* **實質**：將應收帳款出售給承購商 (Factor)。
* **關鍵權利義務拆解**：
  1. **融資手續費 (Finance Charge / Factoring Fee)**：承購商按帳款總額抽取一定比率（例如 2%~3%）作為手續費。
  2. **留置款 / 保證金 (Due from Factor / Factor's Retainage)**：承購商為防範後續可能發生的「銷貨退回、銷貨折讓」或合約爭議，通常扣留一定比率（如 4%~6%），待客戶款項完全結清後退還給賣方。

---

## 2. 無追索權 vs 附追索權出售

### 2.1 無追索權出售 (Sale without Guarantee / Recourse)
* **風險歸屬**：承購商承擔所有的客戶違約與信用壞帳損失。
* **會計處理**：
  * 符合除列條件，直接自帳上除列應收帳款。
  * 借記現金、借記應收承購款 (Due from Factor)、借記出售應收款項損失 (Loss on Sale of Receivables)，貸記應收帳款。

### 2.2 附追索權出售 (Sale with Guarantee / Recourse)
* **風險歸屬**：若客戶到期未付款，出售方承諾向承購商購回帳款或償還款項。
* **IFRS 9 關鍵判斷**：
  * **若全額保證 (Full Guarantee)**：賣方保留了應收帳款實質上所有之信用違約風險與報酬 $\rightarrow$ **實質為擔保借款 (Failed Sale)**，不得除列應收帳款！
  * **若符合除列或僅保留有限追索 (Limited Recourse)**：在滿足風險報酬實質移轉或喪失控制時除列，但賣方必須按公允價值額外認列一筆「追索權負債 / 財務保證負債 (Recourse Liability / Financial Guarantee)」，這會使當期的出售損失擴大。

---

## 3. IFRS 9 金融資產除列決策樹 (Illustration 5.15)

在評估應收款項移轉能否自財務狀況表中除列時，必須依序通過以下三道嚴格關卡：

```text
[企業移轉應收帳款]
       │
       ▼
【關卡 1：合約現金流量權利是否終止？】
 ├── 是 ───────────────────────────────> 【除列資產 (Derecognize)】
 └── 否
       │
       ▼
【關卡 2：是否實質移轉所有風險與報酬？】
 ├── 是 (例如：無追索權全額出售) ───────> 【除列資產 (Derecognize)】
 ├── 否 (例如：全額壞帳保證之融資) ─────> 【禁止除列！視為擔保借款認列金融負債】
 └── 既未移轉、亦未保留所有風險報酬
       │
       ▼
【關卡 3：是否保留對該資產之控制權 (Control)？】
 ├── 否 (買方有能力獨立處分該資產) ───> 【除列資產 (Derecognize)】
 └── 是 (買方無處分自由) ───────────────> 【按「持續參與 (Continuing Involvement)」程度認列】
```

---

## 4. 經典釋例：Crest Textiles 出售分錄演算

假設 Crest Textiles 向 Commercial Factors 出售面額 $\$500,000$ 應收帳款。Commercial Factors 抽取 $3\%$ 融資手續費，並扣留 $5\%$ 保證金以防退貨。

### 情況 A：無追索權出售 (Without Guarantee)
* 手續費 $= \$500,000 \times 3\% = \$15,000$
* 保證金 $= \$500,000 \times 5\% = \$25,000$
* 實收現金 $= \$500,000 - 15,000 - 25,000 = \$460,000$

```text
借：現金 (Cash)                                      $460,000
    應收承購款 (Due from Factor)                        $25,000
    出售應收帳款損失 (Loss on Sale of Receivables)      $15,000
    貸：應收帳款 (Accounts Receivable)                             $500,000
```

### 情況 B：附有限追索權出售且符合除列 (With Limited Guarantee)
假設 Crest Textiles 提供有限擔保，估計該追索權之公允價值為 $\$8,000$：

* 實收現金依舊為 $\$460,000$
* 總出售損失 $= \text{手續費 } \$15,000 + \text{追索權負債 } \$8,000 = \$23,000$

```text
借：現金 (Cash)                                      $460,000
    應收承購款 (Due from Factor)                        $25,000
    出售應收帳款損失 (Loss on Sale of Receivables)      $23,000
    貸：應收帳款 (Accounts Receivable)                             $500,000
        追索權負債 (Recourse Liability)                               $8,000
```
