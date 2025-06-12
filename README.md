# Financial Statements Analysis of a SaaS Company

### Project Overview
---
This report effectively analyses the financial growth of a SaaS company from 2023-2024, deriving insights and unclocking growth patterns over the period. It breaks down the company's income, budget and expenses

### Data Sources
---
The primary dataset used for this analysis is the "Finance_Dataset.xlsx" file, which contains actual records of income, expenses and a budget that shows what was planned for that period.

### Tools
---
- Microsoft Excel - Data Cleaning
- Power BI - Data Analysis & Data Visualisation

### Data Cleaning / Preparation 
---
In the data preparation phase, the following tasks were performed:
- Loading the dataset
- Inspecting the datset for data quality issues
- Handling missing values
- Removing Duplicates
- Loadng data into Power BI
- Created a table for measures table in Power BI

### Exploratory Data Analysis
---
EDA involved exploring the dataset to answer the following questions:
- How did the Total Revenue, Expenses, Budget and Profit change over the years?
- What was the monthly Revenue growth across those years?
- How did the Total Pprofit and Profit margin change across those years and what factors influenced these changes?
- What were the top revenue-generating services?
- How much did the actual income, expenses and budget differ from what was planned and what contributed to these differences?
- What services took up the most expenses?

### Data Analysis
---
Some interesting DAX worked with in power BI include :

``` DAX
Revenue MoM% = DIVIDE([Actual Revenue]-[REVENUE LM],[REVENUE LM])
```
```DAX
Revenue Variance LY = CALCULATE('finances and profit'[Revenue Variance],DATEADD('DateTable'[Date],-1,YEAR))
```
```DAX
PROFIT MoM% CHANGE = CALCULATE('finances and profit'[Profit],DATEADD(DateTable[Date],-1,MONTH))
```
```DAX
Total Budget = SUM(BUDGET[BUDGET])
```
```DAX
Profit Margin = DIVIDE([Profit],[Actual Revenue])
```
