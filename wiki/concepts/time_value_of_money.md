---
title: 貨幣時間價值與利息概念 (Time Value of Money & Nature of Interest)
standard: IFRS 9 / IFRS 13 / IAS 36 / IAS 37
chapter: Chapter 4
type: concept
tags: [時間價值, 複利, 單利, 實質利率, 折現]
last_updated: 2026-11-11
---

# 貨幣時間價值與利息概念 (Time Value of Money)

## 1. 核心定義與理論基石
貨幣時間價值（Time Value of Money, TVM）建立在一項基本經濟事實上：**今天的一元比未來的一元更有價值**。因為今天獲得的資金可以透過投資或借貸產生利息收益，且未來現金流存在通貨膨脹與不確定性風險。

在會計決策中，比較不同時點的資金流向必須站在相同基準上——即「**同基準比較 (Compare Apples to Apples)**」。

---

## 2. 會計上的八大關鍵實務應用
在現代 IFRS 體系下，時間價值不是純粹的財務數學，而是財報認列與衡量的底層工具：
1. **[[應收與應付票據|Notes Receivable/Payable]]**：長期不附息或低於市場利率票據，依有效利率折現認列利息收入/費用。
2. **[[IFRS 16 租賃|Leases]]**：承租人按未來租賃給付現值認列「使用權資產」與「租賃負債」。
3. **[[IAS 19 員工福利|Pensions]]**：精算確定福利義務（DBO）之現值。
4. **[[IAS 36 資產減損|Impairment of Assets]]**：使用價值（Value in Use）之未來現金流折現。
5. **[[IFRS 2 股份基礎給付|Share-Based Payment]]**：認股權之公允價值評估模型。
6. **[[IFRS 3 企業合併|Business Combinations]]**：或有對價之現值衡量。
7. **財報附註揭露 (Disclosures)**：未具市場活絡報價金融工具之公允價值折現評估。
8. **[[IAS 37 負債準備|Environmental Liabilities]]**：除役、復原及環境整治負債準備之折現。

---

## 3. 單利 vs 複利與複利頻率效應

### 3.1 算式對比
* **單利 (Simple Interest)**：僅依原始本金計息：
  $$I = p \times i \times n$$
* **複利 (Compound Interest)**：對原始本金及前期累積之未提取利息重複計息（利滾利）：
  $$FV = PV \times (1 + i)^n$$

### 3.2 計息頻率與實質年收益率 (Effective Yield)
當一年內複利次數為 $m$ 次時：
* 每期計息利率：$i = \frac{\text{名目年利率}}{m}$
* 總計息期數：$n = \text{年數} \times m$
* 實質收益率公式：
  $$\text{Effective Yield} = \left(1 + \frac{r}{m}\right)^m - 1$$
* **頻率越高，實質收益率越高**：以 9% 年息為例，半年複利實質收益率為 9.20%，按日複利則躍升至 9.42%！
