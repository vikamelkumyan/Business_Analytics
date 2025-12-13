# Customer Personality Analysis — Project Report
### Author : Viktoria Melkumyan 
### Course : Business Analytics for Data Science
### Instructor : Yevgenya Bazinyan
## 1. Purpose of the Project

The dataset is from a **retail company’s customer database**, containing transaction and demographic information for individual customers. It captures purchasing behavior across product categories, engagement with marketing campaigns, and personal characteristics like income, education, and family structure.

**Main Business Question:**  
*How can the company better understand the purchasing patterns and preferences of its customers to improve targeted marketing efforts?*

This question matters because personalized strategies—such as segmenting customers based on spending habits and responsiveness to promotions—can increase *marketing effectiveness* and *return on investment*. Marketing teams can allocate resources more efficiently, reduce wasted spend on uninterested segments, and improve overall campaign performance.

## 2. Business Strategy

This project supports a **customer segmentation and targeted marketing strategy**.

**Justification:**

- By identifying distinct groups of customers based on demographics, spending patterns, and responsiveness to campaigns, the business can **tailor promotions** to those most likely to convert.  
- The strategy aims for **customer retention** and **marketing efficiency**—reducing the cost of broad, untargeted campaigns and increasing revenue through focused engagements.  
- Such segmentation also helps with **market expansion** by revealing under‑served segments with high growth potential.

## 3. Data, KPIs, and Descriptive Analysis

### Dataset Description

- **Source:** Kaggle – *Customer Personality Analysis* dataset.  
- **Size:** 2,240 customer records with roughly 29 variables.  
- **Time Period:** Customer acquisition and purchases over the last two years.  
- **Key Variables:**
  - **Demographics:** `Year_Birth`, `Education`, `Marital_Status`, `Income`, `Kidhome`, `Teenhome`
  - **Purchasing Behavior:** `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`
  - **Marketing Engagement:** `AcceptedCmp1–AcceptedCmp5`, `Response`, `NumDealsPurchases`
  - **Purchase Channels:** `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`
  - **Recency:** Days since last purchase (`Recency`)

### KPIs (Key Performance Indicators)

| KPI | Description |
|-----|-------------|
| **Total Spend per Customer** | Sum of all product spending (e.g., wines + fruits + meat, etc.) |
| **Average Spend by Product Category** | Determines product categories that drive revenue |
| **Campaign Acceptance Rate** | Proportion of customers who accepted marketing offers (`Response`) |
| **Recency** | Days since last purchase — lower values indicate higher engagement |
| **Channel Purchase Counts** | Number of purchases via web, catalog, and store |

### Data Cleaning Steps

1. **Remove or Impute Missing Values:** Handle missing values (e.g., drop or fill using median/mean).  
2. **Date Processing:** Convert `Dt_Customer` to a date format and derive features like *Customer Tenure*.  
3. **Feature Engineering:**  
   - `Age` from `Year_Birth` (e.g., `2025 − Year_Birth`).  
   - `Total_Spend` as the sum of all `Mnt*` columns.  
   - `Total_Children` as `Kidhome + Teenhome`.  
4. **Standardize Categorical Levels:** Clean up and group similar categories in `Education` and `Marital_Status`.  
5. **Outlier Handling:** Trim extreme values in income or spending before modeling.

### Descriptive Statistics and Patterns

Suggested visualizations and observations:

1. **Income Distribution**
   - Histogram of `Income` to see skewness and average earnings per customer.
   - Insight on which income groups spend more.

2. **Spending by Product Category**
   - Bar chart of average spend (`Mnt*`) for different product categories.
   - Identify top revenue-driving products.

3. **Campaign Responses**
   - Distribution of `Response` and campaign acceptances (`AcceptedCmp1` to `AcceptedCmp5`).
   - Identify which campaigns performed better.

4. **Recency vs. Total Spend**
   - Scatter or boxplot: Customers with recent purchases tend to spend more.

5. **Purchase Channels**
   - Stacked or grouped bars: Compare `NumWebPurchases`, `NumStorePurchases`, `NumCatalogPurchases`.

---

*This document provides a structured foundation for a complete project report on Customer Personality Analysis.*

