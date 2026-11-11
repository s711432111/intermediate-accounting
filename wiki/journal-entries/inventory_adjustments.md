---
title: 存貨盤存、跌價調整與虧損承諾分錄模型 (Inventory Adjustments and Commitments Journal Entries)
standard: IAS 2 / IAS 37
chapter: Chapter 6
type: journal-entry
tags: [存貨分錄, 永續盤存制, 定期盤存制, 進貨折扣淨額法, 存貨跌價損失, 備抵存貨跌價, 跌價回升利益, 採購承諾, 虧損合約]
last_updated: 2026-11-11
---

# 存貨盤存、跌價調整與虧損承諾分錄模型

本專題彙整存貨交易中最核心的四大類會計分錄：永續 vs 定期盤存制之經典對照、進貨現金折扣淨額法、LCNRV 跌價提列與回升限制，以及虧損採購承諾之會計處理。

---

## 1. 永續盤存制 vs 定期盤存制交易分錄對照 (Illustration 6.3)

假設期初存貨 100 單位 @ $6（總額 $600）：

### 交易 1：賒購商品 900 單位 @ $6（總額 $5,400）
* **永續盤存制**：
  ```text
  借：存貨 (Inventory)                                 $5,400
      貸：應付帳款 (Accounts Payable)                             $5,400
  ```
* **定期盤存制**：
  ```text
  借：進貨 (Purchases)                                 $5,400
      貸：應付帳款 (Accounts Payable)                             $5,400
  ```

### 交易 2：賒銷商品 600 單位 @ $12（總額 $7,200）
* **永續盤存制（雙分錄）**：
  ```text
  (a) 記錄營收：
  借：應收帳款 (Accounts Receivable)                   $7,200
      貸：銷貨收入 (Sales Revenue)                                $7,200

  (b) 記錄成本：
  借：銷貨成本 (Cost of Goods Sold) (600 @ $6)          $3,600
      貸：存貨 (Inventory)                                       $3,600
  ```
* **定期盤存制（單分錄）**：
  ```text
  借：應收帳款 (Accounts Receivable)                   $7,200
      貸：銷貨收入 (Sales Revenue)                                $7,200
  （平時不記錄銷貨成本分錄）
  ```

### 交易 3：期末結算（實地盤點尚餘 400 單位 @ $6 = $2,400）
* **永續盤存制**：平時帳面已即時結存 $2,400，**無需期末結算分錄**！
* **定期盤存制（期末倒扣結算分錄）**：
  ```text
  借：存貨 (期末 Ending Inventory)                     $2,400
      銷貨成本 (Cost of Goods Sold) (倒擠差額)          $3,600
      貸：進貨 (Purchases)                                       $5,400
          存貨 (期初 Beginning Inventory)                            $600
  ```

---

## 2. 進貨現金折扣：總額法 vs 淨額法 (Illustration 6.5)

購入商品 $10,000，信用條件 2/10, n/30。

### 2.1 淨額法 (Net Method, IAS 2 首選)
```text
1. 進貨日（按折後淨額入帳）：
借：存貨 (Inventory)                                 $9,800
    貸：應付帳款 (Accounts Payable)                             $9,800

2. 於 10 天內付款（享折扣，付款 $9,800）：
借：應付帳款 (Accounts Payable)                       $9,800
    貸：現金 (Cash)                                             $9,800

3. 逾期付款（未享折扣，需付全額 $10,000）：
借：應付帳款 (Accounts Payable)                       $9,800
    未享進貨折扣 (Purchase Discounts Lost - 財務費用)    $200
    貸：現金 (Cash)                                            $10,000
```

---

## 3. LCNRV 存貨跌價與回升分錄模型 (Illustration 6.23)

### 情境 A：當期提列存貨跌價損失
期末存貨成本 $188,000，淨變現價值 (NRV) $176,000，需提列跌價 $12,000：
```text
借：銷貨成本 / 存貨跌價損失 (Loss on Inventory Write-down)   $12,000
    貸：備抵存貨跌價 (Allowance to Reduce Inventory to NRV)         $12,000
```

### 情境 B：次期 NRV 部分回升
次年期末成本 $194,000，NRV 回升至 $187,000，應有備抵餘額為 $7,000（調整前備抵貸餘 $12,000，應調減 $5,000）：
```text
借：備抵存貨跌價 (Allowance to Reduce Inventory to NRV)     $5,000
    貸：存貨跌價回升利益 / 銷貨成本 (Recovery of Inventory Loss)      $5,000
```

### 情境 C：次期 NRV 大幅暴漲超過原始成本
設第三年期末成本 $173,000，NRV 暴漲至 $190,000：
* 應有備抵餘額為 $0（已無跌價）。
* 原備抵餘額全部沖轉回升，但**絕對不得將帳面存貨認列超過原始成本 $173,000**！

---

## 4. 虧損性不可取消採購承諾 (Purchase Commitments, IAS 37)

簽訂不可取消合約承諾以每桶 $100 購買 10,000 桶原料（總價 $1,000,000）。期末市價崩跌至每桶 $80，預期採購將虧損 $200,000：

```text
1. 期末市價下跌時提列負債準備：
借：採購合約評價損失 (Unrealized Holding Loss)          $200,000
    貸：採購合約估計負債 (Estimated Liability on Purchase Commitments)   $200,000

2. 實際執行採購並收貨付款時（市價仍為 $80）：
借：存貨 (按市價入帳)                                $800,000
    採購合約估計負債 (沖銷負債)                         $200,000
    貸：現金 (按合約價給付)                                   $1,000,000
```
