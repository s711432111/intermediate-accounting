---
title: 成本與淨變現價值孰低法及存貨估算法 (LCNRV and Inventory Estimation Methods)
standard: IAS 2 / IAS 37 / IAS 41
chapter: Chapter 6
type: concept
tags: [LCNRV, 成本與淨變現價值孰低, 淨變現價值, NRV, 跌價回升上限, 虧損採購合約, 毛利率法, 加價率換算, 傳統零售價法]
last_updated: 2026-11-11
---

# 成本與淨變現價值孰低法及存貨估算法

當存貨因毀損、陳舊、市價下跌或生產成本增加，導致其未來的變現創利能力低於原始歷史成本時，會計上必須放棄歷史成本原則，轉依 **成本與淨變現價值孰低法 (LCNRV)** 計量。此外，在期中報導、盤點查核或天災損失理賠時，**毛利率法** 與 **零售價法** 提供科學的估算機制。

---

## 1. 成本與淨變現價值孰低法 (LCNRV, IAS 2)

### 1.1 淨變現價值 (NRV) 核心定義
$$\text{NRV} = \text{正常營業過程中之估計售價} - \text{至完工尚需投入之估計成本} - \text{完成銷售所必需之估計銷售與運送費用}$$

### 1.2 逐項比較法 (Item-by-Item) 之嚴謹性
IAS 2 規定存貨應優先採「逐項比較法 (Item-by-Item Basis)」。逐項比較法產出的期末存貨評價最為穩健保守，能最即時揭露個別產品的跌價風險。

### 1.3 存貨跌價損失提列與回升限制
* **當期跌價**：當期末 $\text{NRV} < \text{Cost}$ 時，按差額借記「銷貨成本」（或「存貨跌價損失」），貸記「備抵存貨跌價 (Allowance to Reduce Inventory to NRV)」。
* **跌價回升利益 (Recovery / Reversal)**：
  * 若以前年度導致存貨跌價之不利因素消除，使 NRV 回升，應於原提列金額範圍內予以迴轉！
  * **法定回升上限**：**迴轉金額嚴格以「原先認列之跌價損失金額」為限**。換言之，迴轉後的帳面淨額**絕對不得高於原始取得成本**（禁止確認未實現評價增值利益）！

---

## 2. 存貨按公允價值衡量之例外領域

IAS 2 原則上採 LCNRV，但在特定產業中，存貨可例外直接按 **公允價值減出售成本 (Fair Value less costs to sell, 即 NRV)** 衡量：

1. **農業資產與農產品 (IAS 41)**：
   - 生物資產 (Biological Assets，如牲畜、果樹）：在初始認列與期末均按公允價值減出售成本衡量，變動直接計入當期損益。
   - 採收農產品 (Agricultural Produce，如採摘之水果、羊毛）：於採收點以公允價值減出售成本衡量，採收後的該 NRV 即轉為其存貨成本。
2. **大宗商品經紀交易商存貨 (Commodity Broker-Traders)**：
   - 經紀交易商持有農產品、貴金屬或原油等大宗商品，目的在於短期內出售賺取價差，存貨按公允價值減出售成本衡量，公允價值變動列入當期損益。

---

## 3. 不可取消之採購合約（虧損合約, IAS 37）

* 當企業簽訂**重大不可取消之採購承諾 (Purchase Commitments)**，若市場價格劇烈下跌至合約價格以下，企業預期執行合約將蒙受損失：
  * 實質構成 IAS 37 之「**虧損合約 (Onerous Contract)**」。
  * 必須於**市價下跌當期**提前認列損失：
    ```text
    借：採購合約評價損失 (Unrealized Holding Loss on Purchase Commitments)
        貸：採購合約估計負債 (Estimated Liability on Purchase Commitments)
    ```
  * 貫徹保守原則與預期損失即期認列觀點！

---

## 4. 存貨估算法模型

### 4.1 毛利率法 (Gross Profit Method)
1. **估算公式**：
   $$\text{估計銷貨成本} = \text{銷貨淨額} \times (1 - \text{銷貨毛利率})$$
   $$\text{估計期末存貨} = \text{可供銷售商品成本} - \text{估計銷貨成本}$$
2. **毛利率與成本加價率之互換**：
   * 銷貨毛利率 (Gross Profit on Selling Price) $= \frac{\text{毛利}}{\text{售價}}$
   * 成本加價率 (Markup on Cost) $= \frac{\text{毛利}}{\text{成本}}$
   $$\text{銷貨毛利率} = \frac{\text{成本加價率}}{1 + \text{成本加價率}} \quad \Longleftrightarrow \quad \text{成本加價率} = \frac{\text{銷貨毛利率}}{1 - \text{銷貨毛利率}}$$
   *(例如：成本加價 25%，則銷貨毛利率為 $\frac{0.25}{1.25} = 20\%$)*。

### 4.2 傳統零售價法 (Conventional Retail Method)
* **核心技巧（逼近 LCNRV）**：
  $$\text{成本率} = \frac{\text{期初存貨成本} + \text{本期進貨成本}}{\text{期初存貨零售價} + \text{進貨零售價} + \text{淨加價 (Net Markups)}}$$
  * **關鍵設計**：在計算成本率時，**分母計入「淨加價」，但「絕不扣除淨減價 (Net Markdowns)」**！
  * **經濟實質**：人為擴大分母，使成本率偏低；將偏低的成本率乘以期末零售價存貨，得出的期末存貨成本自然逼近保守穩健的「成本與淨變現價值孰低 (LCNRV)」！
