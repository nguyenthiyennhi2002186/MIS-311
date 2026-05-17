# Supermarket Sales Analysis 

This project analyses a supermarket sales dataset using Microsoft Excel to explore customer purchasing behaviour, sales performance, and business insights. The analysis focuses on data cleaning, descriptive statistics, PivotTable analysis, and data interpretation to support business decision-making.

The dataset contains retail transaction records from supermarket branches located in different cities and includes customer information, product categories, purchasing quantity, and transaction values.

# 1. Data Overview

### Dataset Information
- Dataset Name: Supermarket Sale Dataset
- Size After Cleaning: 250 rows × 8 columns
- Analysis Tool: Microsoft Excel
- Analysis Type: Exploratory Data Analysis (EDA)

### Variables Included
| Variable | Description |
|---|---|
| Sale_ID | Unique transaction identifier |
| Branch | Supermarket branch |
| City | Purchase location |
| Customer_Type | Customer classification |
| Product_Name | Purchased product |
| Product_Category | Product category |
| Quantity | Number of units purchased |
| Total_price | Total transaction value (USD) |

### Project Objective
The main objective of this analysis is to:
- Understand customer spending behaviour
- Identify high-performing customer groups
- Evaluate product category performance
- Support business decisions related to inventory and marketing strategies

# 2. Data Cleaning

Before conducting the analysis, the dataset was cleaned to improve accuracy and reliability.

## Duplicate Removal
Excel’s **Remove Duplicates** function was used to identify duplicate transactions.

| Cleaning Result | Value |
|---|---|
| Original Rows | 253 |
| Duplicate Rows Removed | 3 |
| Final Cleaned Rows | 250 |

Removing duplicates was important because duplicated transactions could artificially increase revenue and distort statistical results.

## Handling Missing Values

### Customer_Type
- 3 blank cells were identified
- Replaced with `"Unknown"`

Reason:
Keeping the records preserves important sales information while reflecting realistic business situations where customer information may be incomplete.

### Product_Category
- 6 blank cells were identified
- Replaced with `"Unknown"`

Reason:
There was insufficient information to accurately assign categories, so replacing them randomly could reduce analysis reliability.

### Quantity
- 3 blank cells were identified
- Missing values replaced using the median value

Formula used in Excel: 
=MEDIAN(G:G)

Median value:
```text
11
```

Reason:
The median is less affected by extreme values and better represents typical customer purchasing behaviour.

# 3. Descriptive Analysis

The analysis focused mainly on two numerical variables:
- Quantity
- Total_price

## Quantity Analysis

| Statistic | Value |
|---|---|
| Mean | 10.62 |
| Median | 11 |
| Standard Deviation | 5.98 |

### Interpretation
- The mean and median are very close, indicating a relatively balanced distribution.
- The standard deviation shows noticeable variation in purchasing quantity between customers.
- Some customers purchase only a few products, while others buy significantly larger quantities.

This suggests that customer purchasing behaviour varies depending on shopping habits and consumption needs.

## Total Price Analysis

| Statistic | Observation |
|---|---|
| Mean | Higher than median |
| Median | Lower than mean |
| Standard Deviation | Relatively high |

### Interpretation
- The noticeable gap between mean and median indicates the presence of several high-value transactions.
- Revenue contribution is not evenly distributed across customers.
- Some customers contribute significantly higher transaction values compared to others.

This demonstrates different customer spending patterns and highlights the importance of identifying valuable customer segments.

# 4. Key Business Insights

## Insight 1: Member Customers Generate Higher Revenue

### Findings
- Member customers contributed approximately **57%** of total revenue.
- Average spending per transaction:
  - Member: **136.30**
  - Normal: **112.99**

### Business Interpretation
Member customers not only purchase more frequently but also spend more during each transaction. This suggests that loyalty programs positively influence customer behaviour.

### Recommendation
The supermarket should:
- Improve membership reward systems
- Offer personalised promotions
- Increase exclusive member benefits
- Strengthen customer retention strategies

## Insight 2: Fruits Category Has the Highest Sales Performance

### Findings
- Fruits generated approximately **25%** of total category revenue.
- Beverages and Stationery also showed strong performance.

### Business Interpretation
Fruits are daily necessity products with stable and frequent demand. Customers also tend to purchase products from multiple categories during the same visit.

### Recommendation
The supermarket should:
- Prioritise inventory management for high-demand categories
- Apply stronger promotional support for top-performing products
- Use cross-selling strategies to increase spending per visit


- Customer Behaviour Analysis
- Business Insight Generation
- Data Visualisation
