---
title: 天然資源折耗與 IFRS 6 探勘評估 (Depletion of Mineral Resources)
standard: IAS 16 / IFRS 6
chapter: Chapter 8
type: concept
tags: [天然資源, 折耗, IFRS 6, 探勘與評估, 生產數量法, 蘊藏量變動, 清算股利]
last_updated: 2026-11-11
---

# 天然資源折耗與 IFRS 6 探勘評估 (Depletion of Mineral Resources)

## 1. 天然資源之特徵與折耗本質

天然資源（Natural Resources，包括石油、天然氣、各類金屬礦藏）在會計上具備兩大根本物理特徵：
1. **實體完全消耗 (Complete Removal)**：隨開採進程，資產實體被逐步採掘移出。
2. **大自然力量始能再生 (Replaced Only by an Act of Nature)**：資產無法如機器設備般由人為製造重置。

**折耗 (Depletion)**：係指將天然資源之取得、探勘與開發成本，隨開採進度系統性分攤計入開採出礦產成本之會計程序。

---

## 2. 折耗基礎 (Depletion Base) 之四大組成成本

企業建立天然資源折耗基礎時，包含下列四類成本：
1. **取得成本 (Acquisition Costs)**：購買礦區土地所有權或租賃開採特許權之代價。若開採完畢後土地仍具剩餘價值，應扣除殘值。
2. **探勘前成本 (Pre-exploratory Costs)**：在尚未取得合法勘探權利前發生之支出，依 IFRS 6 原則列為當期費用。
3. **探勘與評估成本 (Exploration and Evaluation, E&E Costs - IFRS 6)**：取得合法探勘權後，進行地質鑽探、採樣、評估商業可行性之支出。企業可依其會計政策予以資本化為 E&E 資產。
4. **開發成本 (Development Costs)**：
   * **有形設備 (Tangible Equipment)**：可移動之採礦重機械，依其自身壽命提列折舊；若僅能專用於該礦區且無法移作他用，其折舊年限以礦區開採期為限。
   * **無形開發成本 (Intangible Development Costs)**：鑽井、開挖豎井、坑道支架等無實體殘值之工程支出，全數計入折耗基礎。
   * **除役與環境復原義務 (Restoration Costs - IAS 37)**：開採完畢後依法律或合約必須承擔之土地環境復原義務，應以其**折現後之現值 (Present Value)** 計入折耗基礎，並貸記「除役負債準備」。

---

## 3. 折耗之計量方法：生產數量法 (Units-of-Production)

天然資源通常採用**生產數量法 (Activity / Units-of-Production Method)** 計算折耗：
$$\text{每單位折耗額} = \frac{\text{總折耗基礎} - \text{估計殘值}}{\text{估計總可開採蘊藏量 (Total Estimated Recoverable Units)}}$$
$$\text{當期折耗總額} = \text{每單位折耗額} \times \text{當期實際開採數量}$$

### 會計分錄演繹：
當期開採出之礦石屬於待售商品，因此折耗金額**先資本化為存貨**，而非直接列為當期費用：
```text
【開採時】
借：存貨－礦產 (Inventory - Minerals)
    貸：累計折耗 (Accumulated Depletion)

【出售時】
借：銷貨成本 (Cost of Goods Sold)
    貸：存貨－礦產 (Inventory - Minerals)
```

---

## 4. 估計蘊藏量之修正 (Revisions of Estimates)

* 隨開採深度的推進與探勘技術升級，地質學家常會修正剩餘可開採蘊藏量。
* **會計處置**：依 **IAS 8** 屬於**會計估計變動**，採**推延處理 (Prospective Basis)**：
  $$\text{修正後每單位折耗額} = \frac{\text{變動當期期初剩餘未折耗成本} - \text{殘值}}{\text{變動當期期初重新估計之剩餘可開採總數量}}$$
* 不得追溯調整以往各期已計提之折耗費用。

---

## 5. 清算股利 (Liquidating Dividends)

採礦型企業之營業生命週期隨礦藏耗竭而步入終點。法規通常允許採礦企業向股東發放超過累積營業淨利的股利：
* **清算股利定義**：股利發放總額**超過**企業歷年累積獲利（保留盈餘）之部分。
* **經濟實質**：並非盈餘分派，而是將股東原始投入之**資本逐步退還 (Return of Capital)**。
* **分錄處理**：
  ```text
  借：保留盈餘 (Retained Earnings - 既有獲利範圍內)
      資本公積－清算股利 (Share Premium - 資本返還部分)
      貸：應付股利 (Dividends Payable)
  ```
