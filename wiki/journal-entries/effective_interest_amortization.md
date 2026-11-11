---
title: 長期公司債評價與有效利率法攤銷表 (Bond Valuation & Effective-Interest Amortization)
standard: IFRS 9
chapter: Chapter 4
type: journal-entry
tags: [公司債, 有效利率法, 折價發行, 溢價發行, 攤銷表]
last_updated: 2026-11-11
---

# 長期公司債評價與有效利率法攤銷 (Effective-Interest Amortization)

## 1. 公司債之定價模型 (Bond Valuation)
公司債的發行價格由兩股現金流組合而成：
1. **票面利息年金現值**：面額 ($F$) $\times$ 票面利率 ($r$) $\times$ 普通年金現值因子 ($PVF\text{-}OA_{n,i}$)
2. **到期本金單筆現值**：面額 ($F$) $\times$ 複利現值因子 ($PVF_{n,i}$)

$$\text{Issue Price} = (F \times r) \times PVF\text{-}OA_{n,i} + F \times PVF_{n,i}$$

* **平價 (Par)**：票面利率 = 市場有效利率 $\Longrightarrow$ 發行價 = 面額。
* **折價 (Discount)**：票面利率 < 市場有效利率 $\Longrightarrow$ 發行價 < 面額。
* **溢價 (Premium)**：票面利率 > 市場有效利率 $\Longrightarrow$ 發行價 > 面額。

---

## 2. 有效利率法攤銷原理 (Effective-Interest Method)
IFRS 9 規範金融負債與以攤銷後成本衡量的金融資產，必須採用有效利率法進行折溢價攤銷：

$$\text{利息費用 (Interest Expense)} = \text{期初帳面價值 (Carrying Value)} \times \text{市場有效利率 ($i$)}$$
$$\text{應付利息 (Cash Interest)} = \text{面額 ($F$)} \times \text{票面利率 ($r$)}$$
$$\text{當期折溢價攤銷額} = |\text{利息費用} - \text{應付利息}|$$

---

## 3. 經典釋例：Alltech Corporation 折價發行公司債 (Illustration 4.39-4.40)
* **條件**：面額 $\$100,000$，發行時本金現值 $\$74,726$，利息現值 $\$21,061.80$，得款 $\$95,787.80$。
* **應付公司債折價**：$\$100,000 - \$95,787.80 = \$4,212.20$。

### 3.1 發行日會計分錄
```text
借：現金 (Cash)                                      $95,787.80
    應付公司債折價 (Discount on Bonds Payable)         $4,212.20
    貸：應付公司債 (Bonds Payable)                                 $100,000.00
    （說明：發行面額 $100,000 公司債，認列發行折價）
```

### 3.2 期末計息與攤銷分錄
```text
借：利息費用 (Interest Expense, 帳面值 × 市場有效利率)   $XX,XXX
    貸：應付利息 / 現金 (Interest Paid, 面額 × 票面利率)          $XX,XXX
        應付公司債折價 (Discount on Bonds Payable)              $X,XXX
    （說明：依有效利率法認列利息費用並攤銷折價，使公司債帳面價值逐期增加至面額）
```

> **查核核心要點**：折價攤銷會使利息費用大於票面付現利息；溢價攤銷則使利息費用小於票面付現利息。到期日帳面價值必定精確回歸面額！
