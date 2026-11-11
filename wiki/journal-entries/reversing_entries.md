---
title: 迴轉分錄之規則與經典分錄模型 (Reversing Entries: Rules and Journal Entries)
standard: Accounting Cycle / IAS 1
chapter: Chapter 1 (Appendix 1B)
type: journal-entry
tags: [迴轉分錄, 調整分錄, 應計項目, 遞延項目, 結帳分錄]
last_updated: 2026-11-11
---

# 迴轉分錄之規則與經典分錄模型 (Reversing Entries)

> **所屬章節**：Chapter 1 附錄 1B
> **目的**：迴轉分錄係在次期期初所作的分錄，其借貸科目與金額恰好為前一期末調整分錄之相反。其存在目的在於**簡化次期日常交易之記帳程序**，非屬強制性程序，但為實務記帳之利器。

---

## 1. 迴轉分錄三大判斷黃金準則

實務判斷「期末調整分錄在次期初是否需做迴轉」之規則：

1. **所有應計項目（Accruals）一律應作迴轉**：
   * 包含：應計費用（Accrued Expenses）、應計收入（Accrued Revenues）。
2. **遞延項目（Deferrals）依原始入帳方式而定**：
   * 若原始收支時**記入損益類帳戶（虛帳戶，即費用或收入）**者 $\longrightarrow$ **作迴轉**。
   * 若原始收支時**記入資產負債類帳戶（實帳戶，即預付費用或預收收入）**者 $\longrightarrow$ **不作迴轉**。
3. **估計項目一律不得作迴轉**：
   * 例如：折舊費用、攤銷費用、壞帳（預期信用損失）等調整分錄，**絕不可作迴轉**。

---

## 2. 經典情境對照演練

### 2.1 應計薪資費用 (Accrued Salaries)

* **情境**：
  * 10月24日發放前兩週薪資 \$4,000。
  * 10月31日底結算，員工已工作但尚未發放之應計薪資為 \$1,200。
  * 11月8日發放次期薪資 \$2,500（含10月份之 \$1,200 與11月份之 \$1,300）。

#### A. 採用迴轉分錄 (Reversing Entries Used)
```text
【10/24 原始發薪】
借：薪資費用 (Salaries and Wages Expense)       $4,000
    貸：現金 (Cash)                                      $4,000

【10/31 期末調整分錄】
借：薪資費用 (Salaries and Wages Expense)       $1,200
    貸：應付薪資 (Salaries and Wages Payable)            $1,200

【10/31 結帳分錄】
借：本期損益 (Income Summary)                  $5,200
    貸：薪資費用 (Salaries and Wages Expense)            $5,200

【11/1 次期初迴轉分錄】
借：應付薪資 (Salaries and Wages Payable)       $1,200
    貸：薪資費用 (Salaries and Wages Expense)            $1,200

【11/8 後續日常發薪】(會計人員不需翻查前期應付薪資金額，直接全額計入薪資費用)
借：薪資費用 (Salaries and Wages Expense)       $2,500
    貸：現金 (Cash)                                      $2,500
（效果：11月份薪資費用帳戶餘額自動呈現貸方 $1,200 與借方 $2,500 互抵後的淨額 $1,300，完全正確！）
```

#### B. 不採用迴轉分錄 (Reversing Entries NOT Used)
```text
【11/1 次期初】
不作任何分錄 (No entry)。

【11/8 後續日常發薪】(會計人員必須手動查帳並沖銷前期應付負債)
借：應付薪資 (Salaries and Wages Payable)       $1,200
    薪資費用 (Salaries and Wages Expense)       $1,300
    貸：現金 (Cash)                                      $2,500
```

---

### 2.2 遞延耗材費用（先虛後實 vs 先實後虛）

* **情境**：
  * 12月10日購入文具用品（Supplies）現金 \$20,000。
  * 12月31日盤點尚未使用之用品盤存價值為 \$5,000（當期耗用 \$15,000）。

#### A. 先虛後實法（原始購入記入費用，需迴轉）
```text
【12/10 購入時記為費用】
借：用品盤存費用 (Supplies Expense)             $20,000
    貸：現金 (Cash)                                      $20,000

【12/31 期末調整（轉出未耗用資產）】
借：用品盤存 (Supplies)                         $5,000
    貸：用品盤存費用 (Supplies Expense)                  $5,000

【12/31 結帳】
借：本期損益 (Income Summary)                  $15,000
    貸：用品盤存費用 (Supplies Expense)                  $15,000

【次年 1/1 迴轉分錄】
借：用品盤存費用 (Supplies Expense)              $5,000
    貸：用品盤存 (Supplies)                              $5,000
（效果：未耗用資產自動轉回次期期初費用，次期購入時繼續全額借記費用即可，作業一致化）
```

#### B. 先實後虛法（原始購入記入資產，不迴轉）
```text
【12/10 購入時記為資產】
借：用品盤存 (Supplies)                         $20,000
    貸：現金 (Cash)                                      $20,000

【12/31 期末調整（認列當期耗用）】
借：用品盤存費用 (Supplies Expense)             $15,000
    貸：用品盤存 (Supplies)                             $15,000

【次年 1/1 迴轉分錄】
不作任何分錄 (No entry)。
```

---

## 3. 效益總結
迴轉分錄的唯一目的就是**防錯與提高常態入帳效率**。它確保常態日常會計人員不需要記憶或去查詢前期期末各項負債或資產的應計金額，而可以標準化地以「原始日常分錄」進行登錄。
