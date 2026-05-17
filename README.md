# Supermarket Sales Analysis

## 1. Data Overview

This project analyzes the **“Supermarket Sale”** dataset to explore customer purchasing behaviour, product category performance, and sales patterns across supermarket branches. The dataset contains retail transaction records including customer type, product category, purchase quantity, and transaction value.

The objective of this analysis is to identify meaningful business insights that can support decision-making related to customer retention, inventory planning, and sales strategy. The project was completed using Excel tools such as **PivotTables, descriptive statistics, sorting, filtering, and data visualization**.

- **Original Dataset Size:** 253 rows × 8 columns  
- **Final Cleaned Dataset:** 250 rows × 8 columns

### Columns
- `Sale_ID` — Unique transaction identifier  
- `Branch` — Supermarket branch location  
- `City` — City where the transaction occurred  
- `Customer_Type` — Member, Normal, or Unknown customer  
- `Product_Name` — Purchased product name  
- `Product_Category` — Product classification  
- `Quantity` — Number of units purchased  
- `Total_price` — Total transaction value in USD  

<img width="924" height="678" alt="image" src="https://github.com/user-attachments/assets/0099c769-4155-4388-b094-37bd50bb9ee7" />



## 2. Data Cleaning

Before conducting the analysis, the dataset was carefully reviewed to improve accuracy and reliability. Cleaning the data was essential because duplicate records and missing values could distort statistical results and business insights.

### Duplicate Records

After checking the dataset using Excel’s **Remove Duplicates** function, 3 duplicate transactions were identified and removed. Removing duplicate transactions helps ensure that sales revenue and customer behaviour are represented accurately.


<img width="975" height="233" alt="image" src="https://github.com/user-attachments/assets/47ea5e16-c83a-444b-9dce-9334d1335c82" />



### Missing Values

Several missing values were identified in the following variables:

| Column | Missing Values | Handling Method |
|---|---|---|
| Customer_Type | 3 | Replaced with “Unknown” |
| Product_Category | 6 | Replaced with “Unknown” |
| Quantity | 3 | Replaced using median value |

#### Customer_Type  

<img width="940" height="193" alt="image" src="https://github.com/user-attachments/assets/cbdba2ab-070b-4e32-849f-55ff1fb33694" />

<img width="940" height="150" alt="image" src="https://github.com/user-attachments/assets/c35984bd-3342-40f4-93c6-fcf4c7e66230" />

#### Product_Category
<img width="941" height="209" alt="image" src="https://github.com/user-attachments/assets/7fffaed8-61ea-4252-84ba-ad4984ecf376" />

<img width="941" height="224" alt="image" src="https://github.com/user-attachments/assets/69639fa0-8932-4efd-b219-75c2bd9e5a8b" />

Instead of deleting incomplete records, missing categorical values were replaced with **“Unknown”**. This approach preserves important transaction information while avoiding inaccurate assumptions about customer classification or product grouping.

#### Quantity

Because `Quantity` is a numerical variable, missing values were replaced using the **median** quantity value calculated in Excel =MEDIAN(G:G)

The median quantity was **11**.

<img width="941" height="204" alt="image" src="https://github.com/user-attachments/assets/c9fbe6ff-a0c8-472b-b657-267b29fd0cec" />

The median was selected instead of the mean because it is less sensitive to unusually high or low values, making it more appropriate for maintaining stability within the dataset.


## 3. Descriptive Statistics

Descriptive statistics were used to summarize customer purchasing behaviour and transaction patterns, focusing mainly on `Quantity` and `Total_price`.

<img width="839" height="385" alt="image" src="https://github.com/user-attachments/assets/92b21c50-e600-47a8-aa44-b41079634896" />

### Quantity

- Average purchase quantity: **10.62 units**
- Median quantity: **11 units**
- Standard deviation: **5.98**

The mean and median are relatively close, suggesting a fairly balanced purchasing distribution. However, the standard deviation indicates noticeable variation in shopping quantity between customers.

This suggests that customer purchasing behaviour differs significantly depending on shopping needs and consumption habits.


### Total Price

- Average transaction value: **123.77**
- Median transaction value: **94.17**

The gap between the mean and median suggests that several high-value transactions increased the overall average spending level.

This indicates that although many customers spend around the median amount, a smaller group of customers contributes disproportionately higher revenue. The relatively high variation in transaction value also reflects differences in customer spending capacity and purchasing behaviour.


## 4. Key Insights

### Insight 1: Member Customers Generate Higher Revenue

A PivotTable and bar chart were used to compare revenue performance between customer groups.

<img width="681" height="364" alt="image" src="https://github.com/user-attachments/assets/b215ce1c-c6c1-4c8d-b53d-b1be85f7a451" />

The analysis shows that **Member customers generated approximately 57% of total revenue**, outperforming Normal customers in both total sales and average transaction value.

- Average spending per Member transaction: **136.30**
- Average spending per Normal transaction: **112.99**

This suggests that loyalty programs positively influence purchasing behaviour. Customers who receive membership benefits such as discounts, reward points, or exclusive promotions are more likely to shop frequently and spend more during each visit. From a business perspective, improving membership programs could help increase long-term customer value and strengthen customer retention.


### Insight 2: Fruits Category Achieved the Strongest Sales Performance

Using a PivotTable and clustered column chart, product category analysis revealed that the **Fruits** category generated the highest revenue contribution, accounting for approximately **25% of total category sales**.

<img width="702" height="368" alt="image" src="https://github.com/user-attachments/assets/fb2358c0-2cbf-4d90-8478-c7487aecccd5" />

This result suggests that food-related products experience stable and frequent customer demand because they are purchased regularly during routine shopping trips. The analysis also shows relatively strong sales performance from categories such as **Beverages** and **Stationery**, indicating that customers often purchase products across multiple categories within the same visit. High-performing categories should receive greater inventory attention to avoid stock shortages and maintain sales performance.

These findings can support:
- Inventory planning
- Product placement decisions
- Cross-selling strategies
- Promotional campaign planning


