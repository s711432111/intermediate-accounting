---
title: 公允價值衡量與輸入值層級 (Fair Value Measurement and Hierarchy)
standard: IFRS 13 / Conceptual Framework Chapter 6
chapter: Chapter 1
type: concept
tags: [公允價值, FairValue, IFRS13, Level1, Level2, Level3, 輸入值層級]
last_updated: 2026-11-11
---

# 公允價值衡量與輸入值層級 (Fair Value Measurement and Hierarchy)

> **國際準則依據**：IFRS 13 公允價值衡量、觀念架構第六章（衡量）。
> **核心定義**：公允價值係指市場參與者在衡量日之常規交易中，出售資產所能收取或移轉負債所需支付之價格（脫手價格，Exit Price）。

---

## 1. 公允價值的三級輸入值階層 (Fair Value Hierarchy)

為增加公允價值衡量與相關揭露之一致性與可比性，IASB 建立了**三級輸入值優先順序架構 (Fair Value Hierarchy)**。企業於評估公允價值時，應優先使用第一級輸入值，最後才使用第三級輸入值（即最大化使用可觀察輸入值，最小化使用不可觀察輸入值）。

```text
Least Subjective (主觀性最低，客觀驗證性最高)
       ▲
       │  【第一級輸入值 Level 1】
       │  活絡市場中相同資產或負債之未調整公開報價 (Quoted prices in active markets for identical items)
       │  例：交易所收盤價（如台積電股票、倫敦金屬交易所銅期貨現貨價）。
       │
       │  【第二級輸入值 Level 2】
       │  除第一級公開報價外，該資產或負債直接或間接可觀察之輸入值 (Observable inputs other than Level 1)
       │  例：相似資產在活絡市場之報價、相同資產在非活絡市場之報價、可觀察之殖利率曲線、利差模型。
       │
       │  【第三級輸入值 Level 3】
       │  該資產或負債之不可觀察輸入值 (Unobservable inputs)
       │  例：企業依自身資料所作之折現率假設、未公開發行新創股權之現金流折現預測、專有評價模型。
       ▼
Most Subjective (主觀性最高，需大量專業判斷)
```

---

## 2. 三個層級之詳細比較

| 層級 | 輸入值性質 | 市場特徵 | 主觀程度 | 代表性實例 | 審計與資訊品質考量 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Level 1** | 相同項目之活絡市場報價 | 交易頻率與交易量足以持續提供定價資訊 | 最低 (Objective) | 集中交易市場之股票、公債、上市基金 | 可驗證性最高，忠實表述無偏誤，不允許主觀折溢價調整。 |
| **Level 2** | 可觀察之直接或間接市場資訊 | 相似項目活絡市場，或相同項目缺乏活絡市場 | 中等 (Moderate) | 店頭市場衍生性商品（IRS利率交換）、類似商辦大樓每坪實價登錄成交行情 | 需確認調整項目（如成色、地點、流動性）是否客觀合理。 |
| **Level 3** | 不可觀察輸入值（企業自身估計假設） | 無可觀察市場交易數據，需依賴內部評價模型 | 最高 (Subjective) | 私募股權（PE）、無市場報價之複雜結構型債券、未上市櫃無形資產 | 需充分揭露模型敏感度分析（Sensitivity analysis），防止管理階層盈餘操縱。 |

---

## 3. 教學思考與盲點剖析

> [!IMPORTANT]
> **觀念盲點：公允價值層級是針對「輸入值（Inputs）」分類，而非評價技術本身！**
> 許多初學者誤以為 DCF（折現現金流模型）一定就是 Level 3。事實上，如果 DCF 中使用的所有現金流量與折現率皆來自市場公開可觀察資訊（如標準利率交換合約），則其可能屬於 Level 2。只有當模型中採用了重大且無法由市場驗證之內部假設時，該評價才會被歸類為 Level 3。

---

## 4. 相關連結
* [[qualitative_characteristics|品質特性：可驗證性 vs 攸關性之拉鋸]]
* [[conceptual_framework|觀念架構衡量原則：歷史成本 vs 現時價值]]
* [[ch01_environment_and_conceptual_framework|第一章章節來源筆記]]
