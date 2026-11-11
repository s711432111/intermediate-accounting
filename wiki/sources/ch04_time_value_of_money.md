---
title: Chapter 4 來源筆記：會計與貨幣時間價值 (Accounting and the Time Value of Money)
standard: IFRS 9 / IFRS 13 / IFRS 16 / IAS 37
chapter: Chapter 4
type: source
tags: [時間價值, 複利, 普通年金, 到期年金, 遞延年金, 公司債評價, 有效利率法, 期望現金流量法]
last_updated: 2026-11-11
---

# Chapter 4: Accounting and the Time Value of Money 來源筆記

> 依據教材：*Intermediate Accounting: IFRS Edition (5th Edition)*, Kieso, Weygandt, Warfield (Wiley, 2025).

---

## 1. 章節學習目標 (Learning Objectives)

* **LO 1**：指認會計中貨幣時間價值的實務應用，並區分單利 (Simple Interest) 與複利 (Compound Interest)。
* **LO 2**：解決單筆金額 (Single-Sum) 的複利終值 (FV) 與現值 (PV) 問題，並反求期數與利率。
* **LO 3**：解決普通年金 (Ordinary Annuity) 與到期年金 (Annuity Due) 的未來值 (FV) 問題。
* **LO 4**：解決普通年金與到期年金的現值 (PV) 問題。
* **LO 5**：掌握進階時間價值課題：遞延年金 (Deferred Annuities)、長期公司債評價 (Valuation of Bonds)、折溢價之有效利率攤銷法 (Effective-Interest Method)，以及 IFRS 13 現值衡量中的期望現金流量法 (Expected Cash Flow Approach)。

---

## 2. 核心觀念體系

### 2.1 貨幣時間價值的哲學與會計應用
* **核心哲學**：今日之一元價值大於未來之一元（A dollar received today is worth more than a dollar promised at some time in the future）。
* **會計八大應用範疇**：
  1. **應收/應付票據 (Notes)**：不帶息或低於市場利率票據之折現評價與利息認列。
  2. **租賃 (Leases, IFRS 16)**：使用權資產與租賃負債以未來租金現值衡量。
  3. **退職後福利 (Pensions, IAS 19)**：確定福利義務 (DBO) 之折現評估。
  4. **非流動資產減損 (Non-Current Assets, IAS 36)**：使用價值 (Value in Use) 評估之未來現金流量折現。
  5. **股份基礎給付 (Share-Based Compensation, IFRS 2)**：員工認股權公允價值估價模型。
  6. **企業合併 (Business Combinations, IFRS 3)**：或有對價 (Contingent Consideration) 折現。
  7. **金融工具公允價值揭露 (Disclosures)**：估計未具活絡市場工具之公允價值。
  8. **環境負債與除役準備 (Environmental Liabilities, IAS 37)**：除役、復原及環境整治義務現值。

### 2.2 利息計算三變數與複利頻率
* **利息三變數**：
  * 本金 ($p$, Principal)
  * 利率 ($i$, Interest Rate per compounding period)
  * 期間數 ($n$, Number of compounding periods)
* **單利 vs 複利**：
  * 單利：僅原始本金生息，$I = p \times i \times n$。
  * 複利：本金及未支付/未提取之累積利息均生息，利滾利。
* **複利頻率 (Compounding Frequency)**：
  * 每期利率 $i = \text{名目年利率} / m$
  * 總計息期數 $n = \text{年數} \times m$
  * 頻率越高，實質年收益率 (Effective Yield) 越高（如 9% 年息按日複利實質收益率達 9.42%）。

---

## 3. 五大基本利率表與換算因子模型

1. **Table 4.1：複利終值因子 ($FVF_{n,i}$)**：
   $$FVF_{n,i} = (1 + i)^n \quad \Longrightarrow \quad FV = PV \times (1 + i)^n$$
2. **Table 4.2：複利現值因子 ($PVF_{n,i}$)**：
   $$PVF_{n,i} = \frac{1}{(1 + i)^n} \quad \Longrightarrow \quad PV = FV \times \frac{1}{(1 + i)^n}$$
3. **Table 4.3：普通年金終值因子 ($FVF\text{-}OA_{n,i}$)**：
   $$FVF\text{-}OA_{n,i} = \frac{(1 + i)^n - 1}{i} \quad \Longrightarrow \quad FV_{OA} = R \times FVF\text{-}OA_{n,i}$$
4. **Table 4.4：普通年金現值因子 ($PVF\text{-}OA_{n,i}$)**：
   $$PVF\text{-}OA_{n,i} = \frac{1 - (1 + i)^{-n}}{i} \quad \Longrightarrow \quad PV_{OA} = R \times PVF\text{-}OA_{n,i}$$
5. **Table 4.5：到期年金現值因子 ($PVF\text{-}AD_{n,i}$)**：
   * 到期年金（期初收付）各款項多累積 1 期利息：
   $$PV_{AD} = PV_{OA} \times (1 + i) = R \times PVF\text{-}OA_{n,i} \times (1 + i)$$
   * 查表技巧：$PVF\text{-}AD_{n,i} = PVF\text{-}OA_{n-1,i} + 1.0$。

---

## 4. 進階專題

### 4.1 遞延年金 (Deferred Annuities)
* 租金款項在遞延 $k$ 期後才開始發生。
* **現值折現法**：
  * 方法一（兩段式）：先算第 $k$ 期末的普通年金現值，再折現 $k$ 期：
    $$PV = R \times PVF\text{-}OA_{n,i} \times PVF_{k,i}$$
  * 方法二（扣除法）：
    $$PV = R \times (PVF\text{-}OA_{k+n,i} - PVF\text{-}OA_{k,i})$$

### 4.2 長期公司債之評價與有效利率法攤銷
* **公司債發行價格** = 票面利息年金現值 + 面額單筆現值：
  $$\text{Price} = (F \times r) \times PVF\text{-}OA_{n,i} + F \times PVF_{n,i}$$
* **有效利率法 (Effective-Interest Method)**：
  * 當期利息費用 (Interest Expense) = 期初帳面價值 $\times$ 市場有效利率 ($i$)
  * 當期票面利息收付 (Interest Paid) = 面額 ($F$) $\times$ 票面利率 ($r$)
  * 差額 = 折價攤銷數（使帳面價值增加）或 溢價攤銷數（使帳面價值減少）。

### 4.3 IFRS 13 期望現金流量法與利率三要素
* **期望現金流量法 (Expected Cash Flow Approach)**：考量所有可能現金流結果，依機率加權計算期望值，並以無風險利率 (Risk-Free Rate) 進行折現。
* **利率三大成分**：
  1. 純粹利率 (Pure Rate of Interest, 2%–4%)
  2. 預期通貨膨脹率 (Expected Inflation Rate, 0%–?)
  3. 信用風險溢價 (Credit Risk Rate, 0%–5%)
  * 無風險利率 = 純粹利率 + 預期通膨率。
