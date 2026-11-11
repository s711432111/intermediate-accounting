---
title: 借款成本資本化 (Capitalization of Borrowing Costs)
standard: IAS 23
chapter: Chapter 7
type: concept
tags: [借款成本, 資本化, IAS 23, 累積支出加權平均數, WAAE, 可避免利息, 專案借款, 一般借款]
last_updated: 2026-11-11
---

# 借款成本資本化 (Capitalization of Borrowing Costs - IAS 23)

## 1. 核心觀念與會計哲學

依據 **IAS 23《借款成本》(Borrowing Costs)**，為使資產達到預定可使用或可銷售狀態所直接歸屬之借款利息，屬於該項資產取得成本之一部分，必須予以**資本化 (Capitalized)**，而非直接認列為當期利息費用。

其理論依據為**成本與收益配合原則**：自建長期資產在建造期間尚未產生任何營運收入，將建造期間必要的資金取得代價資本化為資產帳面金額，可使該資產於未來投入營運並產生經濟效益時，透過折舊方式系統性地分攤轉為費用。

---

## 2. 符合資格之資產 (Qualifying Assets)

並非所有自建或購入之資產皆可將利息資本化：
* **符合資格之資產 (Qualifying Assets)**：必須需要**相當長之期間 (Substantial Period of Time)** 始能達到預定使用或銷售狀態之資產。
  * *例*：自行建造的廠房、辦公大樓、大型特殊重型機械、耗時數年的自製特定存貨。
* **不符合資格之資產 (Non-Qualifying Assets)**：
  1. 取得時已處於可使用或可銷售狀態的資產。
  2. 常態性、短週期、大量重複製造的存貨（IAS 2）。
  3. 未實質進行建造準備作業之閒置土地。

---

## 3. 資本化期間 (Capitalization Period) 之起訖條件

### 3.1 開始資本化（三條件必須「同時」具備）
1. **已產生資產支出 (Expenditures for the asset are being incurred)**：已投入現金、轉移其他資產或承擔附息債務。
2. **為使資產達到預定狀態所必要之活動已在進行 (Activities that are necessary to prepare the asset are in progress)**：包括實體工程、地質勘探、請領建照許可等前期準備。
3. **已產生借款成本 (Borrowing costs are being incurred)**：企業帳上確實承擔有利息負擔。

### 3.2 暫停與停止資本化
* **暫停資本化 (Suspension)**：若非正常情況下實質建造活動**中斷一段較長期間**（如罷工、法律糾紛停工），利息應暫停資本化，轉列為當期利息費用。（但若是建造工程必經之正常程序中斷，如雨季停工，則毋需暫停）。
* **終止資本化 (Cessation)**：當資產實質上已達到**預定可使用或銷售狀態 (Substantially Complete)** 時，利息資本化應立即終止；後續再發生之利息一律列為利息費用。

---

## 4. 資本化金額之衡量模型

IAS 23 規範每一期間資本化之借款成本金額，採「孰低法」：
$$\text{資本化借款成本} = \min(\text{實際借款成本 Actual Interest}, \text{可避免借款成本 Avoidable Interest})$$

### 4.1 步驟一：計算累積支出加權平均數 (WAAE)
**累積支出加權平均數 (Weighted-Average Accumulated Expenditures, WAAE)**：
$$\text{WAAE} = \sum \left( \text{每筆實質支出金額} \times \frac{\text{當年度資本化期間月數}}{12} \right)$$

### 4.2 步驟二：決定資本化利率與計算可避免利息
將 WAAE 依資金來源分層匹配：
1. **專案借款 (Specific Borrowings)**：
   * 為建造該資產專門借入之借款。
   * 若 $\text{WAAE} \le \text{專案借款本金}$：
     $$\text{可避免利息} = \text{WAAE} \times \text{專案借款利率} - \text{專案借款未動用資金之暫時性投資收益}$$
   > [!IMPORTANT]
   > **暫時性投資收益之扣除**：依 IAS 23 規定，專案借款在尚未支用前轉存定存或短期投資所產生之**暫時性投資收益 (Investment Income)**，必須**全數自應資本化利息中扣除**！

2. **一般借款 (General Borrowings)**：
   * 當 $\text{WAAE} > \text{專案借款本金}$ 時，超出部分（超額 WAAE）視為動用企業之一班性借款：
     $$\text{一般借款加權平均利率} = \frac{\sum \text{其他各筆一般借款之年度利息費用}}{\sum \text{其他各筆一般借款之本金總額}}$$
     $$\text{超額 WAAE 之利息} = (\text{WAAE} - \text{專案借款本金}) \times \text{一般借款加權平均利率}$$

### 4.3 步驟三：比較並認列
* 若 $\text{可避免利息} \le \text{實際總利息}$：資本化金額 = 可避免利息，差額列為利息費用。
* 若 $\text{可避免利息} > \text{實際總利息}$：資本化金額以「實際總利息」為上限（不可虛增利息資產化）。

---

## 5. 跨章節關聯與準則參照

* [[wiki/sources/ch07_property_plant_equipment|Chapter 7 來源筆記]]
* [[wiki/concepts/cash_and_receivables|Chapter 5 受限制存款與利息]]
* 後續折舊參照：[[wiki/standards/ias16_ppe|IAS 16 不動產、廠房及設備折舊]]
