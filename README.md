# Financial Bank Statement Analysis | December 2024

## Table of Contents
1. [Overview](#overview)
2. [Objectives](#objectives)
3. [Methodology](#methodology)
4. [Measures Used](#measures-used)
5. [Key Insights](#key-insights)
6. [Recommendations](#recommendations)
7. [Challenges](#challenges)
8. [Screenshots](#screenshots)

## Overview
This analysis provides insights into my December 2024 personal bank statement, evaluating income, expenses, transaction patterns, and spending habits. The goal is to track financial health, identify trends, and make data-driven financial decisions.

## Objectives
- Understand daily financial performance.
- Identify spending patterns and major expense categories.
- Compare income vs. expenses.
- Track net cash flow.
- Provide actionable financial recommendations.

## Methodology
1. **Data Extraction**: Opened the bank statement PDF directly in Excel, which converted it into a tabular format.
2. **Data Cleaning**:
   - Removed duplicates (none found).
   - Standardized currency and text formats.
   - Deleted the `Value Date` column as it was not required.
   - Added a new **Serial Number (S/N)** column.
   - Manually classified transaction types and beneficiaries using:
     - **Text-to-Column**
     - **Power Query Extraction**
     - `IF(ISNUMBER(SEARCH()))` formula.
3. **Data Loading**: Imported cleaned data into **Power BI** for visualization and analysis.

## Measures Used
Below are the **DAX measures** created in Power BI for analysis:

---

### **1. Total Debit**
```DAX
Total Debit = SUM('Clean Data'[DEBIT])
```
🔹 This calculates the total amount spent.

---

### **2. Total Credit**
```DAX
Total Credit = SUM('Clean Data'[CREDIT])
```
🔹 This calculates the total amount received.

---

### **3. Net Cash Flow**
```DAX
Net Cash Flow = 
VAR TotalCredit = SUMX('Clean Data', 'Clean Data'[CREDIT])
VAR TotalDebit = SUMX('Clean Data', 'Clean Data'[DEBIT])
RETURN
[Total Credit] - [Total Debit]

```
🔹 This shows whether more money is coming in or going out.

---

### **4. Debit-to-Credit Ratio**
```DAX
Debit to Credit Ratio = DIVIDE([Total Debit], [Total Credit], 0)
```
🔹 Helps analyze spending versus earnings.

---

### **5. Average Transaction Value**
```DAX
Average Transaction Value = AVERAGE('Clean Data'[DEBIT]) + AVERAGE('Clean Data'[CREDIT])
```
🔹 Calculates the average amount per transaction.

---

### **6. Total Stamp Duty**
```DAX
Total Stamp Duty = 
CALCULATE(
    SUM('Clean Data'[DEBIT]), 
    'Clean Data'[Transaction Type] = "Stamp Duty"
)
```
🔹 Summarizes the total stamp duty paid.

---

### **7. Total Charges**
```DAX
Total Charges = 
CALCULATE(
    SUM('Clean Data'[DEBIT]), 
    'Clean Data'[Transaction Type] = "Charges"
)
```
🔹 Summarizes all bank charges.

---

### **8. Transaction Count**
```DAX
Transaction Count = COUNTROWS('Clean Data')
```
🔹 Counts the total number of transactions.

📌 **Notes:**
- Ensure that `'Clean Data'` is the correct table name in your Power BI dataset.
- Use these measures in your dashboard for deeper financial insights.


---

## Key Insights
- **Total Credit**: ₦869,200
- **Total Debit**: ₦878,800
- **Net Cash Flow**: **₦-9,600** (Spent more than income, relying on November balance)
- **Credit-to-Debit Ratio**: **1.01** (Almost equal income and expenses)
- **Average Transaction Value**: **₦5,231**
- **Highest Credit & Debit Transaction Day**: **December 27th**
- **Major Expense Categories**:
  - Transfers: **₦546,150**
  - POS Transactions: **₦328,099**
  - Stamp Duty & Charges: **₦1,740**

## Recommendations
- **Budget Optimization**: Reduce expenses to ensure spending does not exceed income.
- **Expense Tracking**: Categorize expenses further to identify unnecessary costs.
- **Savings Plan**: Set aside a fixed percentage of income monthly to avoid negative cash flow.
- **Alternative Payment Methods**: Consider minimizing POS transactions to avoid excess fees.
- **Monitoring High Transaction Days**: December 27th had the highest activity—analyze if it’s recurring to plan better.

## Challenges
- **Manual Classification**: Required extensive effort in categorizing transactions from the narration column.
- **Limited Data Scope**: Only one month analyzed—trends over multiple months could provide deeper insights.

## Screenshots
### Dashboard Overview
![](https://github.com/Olowookere-Abidemi/Bank-Statement-Analysis/blob/main/FINANCIAL%20DASHBOARD.jpg))

---
## Before and After Cleaning

<p align="LEFT">
  <img src="UNCLEAN DATA.png" alt="Unclean Data" width="100%">
  
  <img src="CLEAN DATA.png" alt="Clean Data" width="100%">


---
This analysis provided a clear view of my financial health in December 2024, helping me make better financial decisions. 



