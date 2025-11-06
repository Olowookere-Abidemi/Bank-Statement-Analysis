
# Financial Bank Statement Analysis | December 2024  

## Table of Contents  
1. [Overview](#overview)  
2. [Objectives](#objectives)  
3. [Workflow](#workflow)  
   - [1. Data Source & Extraction](#1-data-source--extraction)  
   - [2. Data Cleaning & Preparation (Excel)](#2-data-cleaning--preparation-excel)  
   - [3. Dashboard Development (Excel)](#3-dashboard-development-excel)  
   - [4. Dashboard Development (Power-BI)](#4-dashboard-development-power-bi)  
4. [Key Insights](#key-insights)  
5. [Recommendations](#recommendations)  
6. [Challenges](#challenges)  
7. [Tools Used](#tools-used)  
8. [Project Highlights](#project-highlights)  
9. [Lessons Learned](#lessons-learned)  
10. [Author](#author)  

---

## Overview  
This project explores my **December 2024 personal bank statement** to uncover **spending patterns, income sources, and cash flow behavior**.  
The analysis was conducted using **Microsoft Excel** and **Power BI** — both used to design **fully interactive dashboards**.  

The goal is to transform raw financial data into meaningful, visual insights that guide better personal financial decisions.

---

## Objectives  
- Track **daily cash inflow and outflow** to monitor personal financial health.  
- Identify **top income sources** and **major expense areas**.  
- Measure and visualize **Net Cash Flow trends** over time.  
- Build **interactive dashboards** in both Excel and Power BI.  
- Provide **data-driven financial recommendations** for improvement.  

---

## Workflow  

### 1. **Data Source & Extraction**  
- Source: Personal **Jaiz Bank Statement (PDF)** for **December 2024**.  
- Extracted directly into **Excel**, which automatically converted the data into tabular format.  

---

### 2. **Data Cleaning & Preparation (Excel)**  
Data cleaning and transformation steps were performed using **Excel formulas** and **Power Query**:  

- Removed duplicates and dropped irrelevant columns (e.g., *Value Date*).  
- Standardized all **₦ currency values** for consistency.  
- Added a **Serial Number (S/N)** column for record indexing.  
- Split the **Narration** column using **Text-to-Columns** to isolate transaction type and beneficiary.  
- Classified transactions into **Credit** and **Debit** using:  
  ```Excel
  =IF(ISNUMBER(SEARCH("CR", [Narration])), "Credit", "Debit")
   ```
* Categorized transactions by payment channels such as **Transfer**, **POS**, and **Charges**.

---

### 3. **Dashboard Development (Excel)**

Designed a **dynamic and interactive Excel dashboard** using slicers, charts, and pivot tables.
The dashboard enables users to filter by transaction type, date, and category, while visualizing income and expense patterns.

#### 📊 Excel Dashboard Preview

> ![Excel Financial Dashboard](EXCEL%20FINANCIAL%20DASHBOARD.png)

**Dashboard Features:**

* Interactive weekday filters (Mon–Sun).
* Dynamic KPIs (Total Income, Total Expense, Net Cash Flow, Available Balance).
* Top contributors for income and spending.
* Day-by-day cash flow trend visualization.
* Credit vs. Debit donut chart.
* Weekly transaction behavior breakdown.

---

### 4. **Dashboard Development (Power BI)**

Rebuilt the same dataset in **Power BI** to create an advanced version with deeper insights and interactivity.

#### 🖥️ Power BI Dashboard Preview

> ![Power BI Dashboard](https://github.com/Olowookere-Abidemi/Bank-Statement-Analysis/blob/main/FINANCIAL%20DASHBOARD.jpg)

**Power BI Enhancements:**

* Dynamic cards and KPIs with arrows indicating positive/negative change.
* Cash flow trend chart with line markers for Income vs. Expense.


---

## Key Insights

| Metric                        | Value                | Insight                                                       |
| ----------------------------- | -------------------- | ------------------------------------------------------------- |
| **Total Credit (Income)**     | ₦869,200             | Total money received during December 2024.                    |
| **Total Debit (Expenses)**    | ₦878,800             | Total amount spent across all categories.                     |
| **Net Cash Flow**             | ₦-9,600              | Slight deficit, indicating reliance on prior month’s balance. |
| **Credit-to-Debit Ratio**     | 1.01                 | Almost equal income and expenses.                             |
| **Average Transaction Value** | ₦5,231               | Suggests small, frequent transactions.                        |
| **Peak Financial Day**        | December 27th        | Highest transaction volume (income & expenses).               |
| **Top Expense Channel**       | Transfers (₦546,150) | Main source of cash outflow.                                  |
| **Top Income Source**         | Eyitayo (₦339K)      | Largest inflow contributor.                                   |

---

## Recommendations

* **Budget Optimization:** Track spending categories and reduce POS or frequent transfer charges.
* **Savings Discipline:** Automate monthly transfers to savings or investment accounts.
* **Analyze Recurring Peaks:** Investigate high-activity dates (like Dec 27) to understand spending triggers.
* **Use Data Continuously:** Update and monitor monthly statements to identify behavioral trends.
* **Fee Minimization:** Consolidate payments to reduce stamp duty and POS transaction fees.

---

## Challenges

| Challenge                 | Description                                                    |
| ------------------------- | -------------------------------------------------------------- |
| **Manual Classification** | Required careful tagging of transaction descriptions.          |
| **Single-Month Dataset**  | Limited long-term trend analysis.                              |
| **Data Consistency**      | Maintaining uniform categorization between Excel and Power BI. |

---

## Tools Used

| Tool                | Purpose                                                            |
| ------------------- | ------------------------------------------------------------------ |
| **Microsoft Excel** | Data cleaning, transformation, and interactive dashboard creation. |
| **Power BI**        | Advanced analytics, data modeling, and visual storytelling.        |
| **Power Query**     | Automated data preparation and formatting.                         |

---

## Project Highlights

* Dual-tool analysis combining **Excel interactivity** and **Power BI storytelling**.
* Built a **scalable financial monitoring workflow** for future months.
* Created **visual and analytical parity** between Excel and Power BI.
* Transformed raw statement data into actionable personal finance insights.

---

## Lessons Learned

* Data visualization becomes meaningful when connected to a story.
* Both Excel and Power BI can complement each other when used strategically.
* Even personal finance data reveals trends that can influence better money habits.

---

## Visual Gallery

### 🔹 Data Cleaning Comparison

| Before                              | After                           |
| ----------------------------------- | ------------------------------- |
| ![Unclean Data](UNCLEAN%20DATA.png) | ![Clean Data](CLEAN%20DATA.png) |

---

## Author

**Abidemi O.**
📊 *Data Analyst | Financial Analytics | Power BI | Excel | SQL*

---





