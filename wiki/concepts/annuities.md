---
title: 年金觀念模型：普通年金、到期年金與遞延年金 (Annuities: Ordinary, Due, and Deferred)
standard: IFRS 9 / IFRS 16
chapter: Chapter 4
type: concept
tags: [普通年金, 到期年金, 遞延年金, 年金現值, 年金終值]
last_updated: 2026-11-11
---

# 年金觀念模型 (Annuities)

## 1. 年金的三大核心構成要件
一組現金流量要構成「年金 (Annuity)」，必須同時具備以下三項條件：
1. **等額性**：各期收付款項（稱為 Rent, $R$）金額完全相同。
2. **等距性**：各期收付款項之間隔期間長度相同（如每月、每季、每年）。
3. **等頻計息**：每一間隔期間內複利計息一次。

---

## 2. 普通年金 vs 到期年金

| 特性比較 | 普通年金 (Ordinary Annuity) | 到期年金 (Annuity Due) |
| :--- | :--- | :--- |
| **收付時點** | 每期**期末** (End of Period) | 每期**期初** (Beginning of Period) |
| **第一期利息** | 第一筆款項無利息累積 | 第一筆款項即刻起算利息 |
| **終值因子** | $FVF\text{-}OA_{n,i} = \frac{(1+i)^n - 1}{i}$ | $FVF\text{-}AD_{n,i} = FVF\text{-}OA_{n,i} \times (1 + i)$ |
| **現值因子** | $PVF\text{-}OA_{n,i} = \frac{1 - (1+i)^{-n}}{i}$ | $PVF\text{-}AD_{n,i} = PVF\text{-}OA_{n,i} \times (1 + i)$ |
| **查表速算法** | 查普通年金表第 $n$ 期 | 查普通年金表第 $(n-1)$ 期因子再 $+1.0$ |

> **記憶秘訣**：到期年金每一筆錢都比普通年金**早進出一個期間**，因此無論終值或現值，到期年金剛好都是普通年金乘上 $(1 + i)$！

---

## 3. 遞延年金 (Deferred Annuities)
遞延年金係指租金款項在經過 $k$ 個遞延期間後，才開始定期收付。

### 3.1 終值計算
遞延年金的終值與一般未遞延的普通年金終值完全相同（因為遞延期間根本沒有現金流，無款項可滾利）。

### 3.2 現值計算（兩大經典解法）
假設款項在第 $k$ 期末之後才開始發生，連續支付 $n$ 期：
* **解法一：兩段式折現法 (Two-Step Discounting)**
  1. 將 $n$ 期年金折現至年金發生起點（第 $k$ 期期末）：$PV_k = R \times PVF\text{-}OA_{n,i}$
  2. 再將 $PV_k$ 當成單筆款項，以單筆現值因子折現 $k$ 期回到 $t=0$：
     $$PV_0 = PV_k \times PVF_{k,i} = R \times PVF\text{-}OA_{n,i} \times PVF_{k,i}$$
* **解法二：差額法 (Difference Method)**
  1. 假定全部 $(k+n)$ 期均有付款，算出全期年金現值。
  2. 扣除前 $k$ 期並未實際付款之虛擬年金現值：
     $$PV_0 = R \times (PVF\text{-}OA_{k+n,i} - PVF\text{-}OA_{k,i})$$
