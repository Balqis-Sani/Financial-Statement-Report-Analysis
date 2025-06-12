# Financial Statements Analysis of a SaaS Company

### Project Overview
---
This report effectively analyses the financial growth of a SaaS company from 2023-2024, deriving insights and unclocking growth patterns over the period. It breaks down the company's income, budget and expenses.
![onyx 4-1](https://github.com/user-attachments/assets/2ab0854b-c3f2-4024-a66e-1812da463deb)



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
### Results/Findings
---
1. **Year 2022**: Foundation Year, Low Revenue, and Missed Investments.

Revenue in 2022 was the lowest across the three years, resulting in the greatest loss and a negative profit margin of -12.12%.
Although revenue exceeded expenses from January to April, there were no recorded expenses for Customer Support or R&D, indicating a lack of investment in key growth areas.
From June to December, expenses began to exceed revenue, likely due to increased spending in areas such as General & Administrative (G&A) and Sales & Marketing; possibly in an attempt to stimulate growth.
Despite some effort to invest later in the year, the absence of early strategic spending may have contributed to the year’s poor financial performance.

2. **Year 2023**: Investment Phase with Higher Revenue and Expenses.

Revenue nearly doubled (+92.12%) compared to 2022, signaling improved business traction.
However, expenses also increased significantly (+109.61%), resulting in a higher loss and a profit margin of -22.33%, which is -84.21% lower than in 2022.
Throughout all 12 months, expenses consistently exceeded revenue, suggesting the business was in a heavy investment phase.
Major increases were observed across all spending classes i.e. G&A, R&D, Sales & Marketing, and Customer Support—indicating a more robust and holistic approach to scaling.
A notable revenue spike occurred in June 2023, with MoM growth jumping from 2.03% (May) to 10.95% (June). This was due to a revenue increase from $469.5K to $520.9K.

3. **Year 2024**: Growth and Return on Investment.

The business experienced a significant uplift in performance, generating $8.675M in revenue, which is +42.1% higher than in 2023.
Revenue surpassed expenses, resulting in a net profit of $299.9K, representing a +122% increase from the previous year.
The profit margin turned positive at 3.46%, a +115.48% improvement over 2023.
May 2024 marked another key turning point, with MoM revenue growth jumping from 2.37% (April) to 7.13% (May). This reflected a revenue increase from $646K to $692.7K.
Top revenue-generating clients in 2023 and 2024 were mostly SMBs, with monthly SaaS subscriptions being the leading revenue service line.
In contrast, in 2022, the top client was Global Tech, and the most profitable service was Product License – Enterprise, indicating a shift in target market and strategy over time.

### Recommendations
- Maintain and optimize investments in the R&D and Customer Support departments, to sustain momentum and drive innovation.
- Implement stronger budgeting and financial controls to reduce unnecessary overheads, particularly in G&A and Marketing, without affecting growth.
- Double down on the SMB segment by tailoring offerings, pricing models, and customer success strategies specifically to this market.
- Prioritize early-year investments and align quarterly plans with strategic goals, using data from prior years to guide decisions.
- Continue expanding recurring revenue lines, but test new service offerings carefully to reduce dependence on a single stream.

