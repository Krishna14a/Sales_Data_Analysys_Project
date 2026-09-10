# Sales_Data_Analysys_Project
# 📊 USA Regional Sales Analysis | Exploratory Data Analysis

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** of Acme Co.'s USA sales data covering **2014–2018**.

The analysis focuses on understanding sales and profitability across **products, customers, sales channels, states, and regions**. It also investigates sales trends, order-value distributions, pricing patterns, outliers, and relationships between key business metrics.

The project was developed using **Python, Pandas, NumPy, Matplotlib, and Seaborn**, with the analysis designed to support the development of a **Power BI dashboard** for business decision-making.

---

## 🎯 Business Problem

The objective of this project is to analyze historical sales performance and identify the major factors influencing **revenue and profitability**.

The analysis aims to answer questions such as:

* Which products generate the highest revenue?
* Which sales channels contribute the most to overall sales?
* Which regions and states are performing strongly?
* How does sales performance change over time?
* Are there seasonal patterns in sales?
* Where do unusual or extreme transactions occur?
* How are unit price, cost, revenue, and profit related?
* Which areas present opportunities for growth and improvement?

---

## 🎯 Project Objectives

* Identify top-performing **products, customers, channels, and regions**
* Analyze **revenue and profit-margin performance**
* Understand monthly and yearly **sales trends**
* Detect **outliers and unusual transactions**
* Analyze **unit-price and order-value distributions**
* Study relationships between **revenue, cost, quantity, price, and profit**
* Identify regional and state-level sales opportunities
* Generate actionable business recommendations
* Prepare insights for a future **Power BI dashboard**

---

## 🗂️ Dataset Overview

The Excel workbook contains multiple related datasets:

| Dataset       | Records | Description                         |
| ------------- | ------: | ----------------------------------- |
| Sales Orders  |  64,104 | Transaction-level sales information |
| Customers     |     175 | Customer information                |
| Products      |      30 | Product information                 |
| Regions       |     994 | Delivery-region information         |
| State Regions |      49 | State and regional mapping          |
| 2017 Budgets  |      30 | Product-level budget information    |

The main sales dataset contains information such as:

* Order Number
* Order Date
* Customer
* Sales Channel
* Currency
* Warehouse
* Delivery Region
* Product
* Order Quantity
* Unit Price
* Line Total
* Total Unit Cost

---

## 🛠️ Technologies & Libraries

### Programming Language

* Python

### Data Analysis

* Pandas
* NumPy

### Data Visualization

* Matplotlib
* Seaborn

### Analytics Techniques

* Data Profiling
* Data Cleaning
* Univariate Analysis
* Bivariate Analysis
* Trend Analysis
* Distribution Analysis
* Outlier Detection
* Correlation Analysis
* Customer Segmentation

### Business Intelligence

* Power BI

---

## 🔍 Analysis Workflow

### 1. Data Loading

The project loads the Excel workbook and separates the different sheets into individual Pandas DataFrames.

```python
sheets = pd.read_excel(file_path, sheet_name=None)

df_sales = sheets['Sales Orders']
df_customers = sheets['Customers']
df_products = sheets['Products']
df_regions = sheets['Regions']
df_state_reg = sheets['State Regions']
df_budgets = sheets['2017 Budgets']
```

---

### 2. Data Profiling & Exploration

Initial analysis was performed to understand:

* Dataset size
* Column structure
* Data types
* Unique values
* Numerical ranges
* Date ranges
* Potential data-quality issues

The sales dataset contains **64,104 transaction records**, covering orders from **January 2014 through February 2018**.

---

### 3. Data Cleaning & Preparation

The analysis includes data-quality checks and preparation such as:

* Reviewing missing values
* Validating data types
* Converting date fields
* Checking numerical columns
* Preparing datasets for analysis
* Creating derived metrics where required

---

## 📈 Exploratory Data Analysis

The project investigates several important business dimensions.

### 📅 Sales Trend Analysis

Monthly and yearly sales trends were analyzed to identify changes in revenue over time.

The analysis shows relatively stable sales performance, with monthly revenue generally falling within approximately **$23M–$26.5M**, while an unusual decline of approximately **$21.2M occurred in early 2017**.

---

### 🛍️ Sales Channel Analysis

Sales were analyzed across three major channels:

| Channel     | Share of Sales |
| ----------- | -------------: |
| Wholesale   |            54% |
| Distributor |            31% |
| Export      |            15% |

Wholesale is the largest contributor, while the lower export contribution indicates potential opportunities for international growth.

---

### 📦 Product Performance Analysis

Product-level revenue was compared to identify the strongest and weakest performers.

The analysis identified:

* **Product 26:** approximately $118M
* **Product 25:** approximately $110M
* **Product 13:** approximately $78M
* Mid-performing products: approximately $68M–$75M
* Lower-performing products: approximately $52M–$57M

This comparison helps identify products that may require additional promotion, pricing optimization, or cost improvements.

---

### 💰 Profit Margin Analysis

Profit margins were analyzed across products, channels, and customers.

Overall margins were concentrated approximately between **18% and 60%**. The analysis did not identify a strong direct relationship between unit price and profit margin.

Channel-level average margins were also highly consistent:

* Export: **37.93%**
* Distributor: **37.56%**
* Wholesale: **37.09%**

---

### 📊 Order Value Distribution

The Average Order Value (AOV) distribution was analyzed using a histogram.

Most orders fall approximately within the **$20K–$120K** range, with a concentration around **$50K–$60K**.

There is also a long tail of high-value transactions extending toward approximately **$400K–$500K**, representing a relatively small portion of transactions.

---

### 🌎 Regional Analysis

Regional performance was analyzed to understand geographic sales concentration.

Key observations:

* **West:** approximately $360M in sales
* **South:** more than $320M
* **Midwest:** more than $320M
* **Northeast:** approximately $210M

The West is the strongest region, while the Northeast represents a potential area for targeted growth initiatives.

---

### 🇺🇸 State-Level Analysis

State-level analysis highlighted significant differences in revenue and order volume.

**California** was the strongest-performing state with approximately:

* **$230M revenue**
* **7,500+ orders**

Illinois, Florida, and Texas formed the next major group, with approximately **$85M–$110M** in revenue.

---

### 🚨 Outlier Analysis

Outlier analysis was performed to identify unusually high or low transactions.

Some products showed unusually high revenue values, while Products 20 and 27 also contained very low-end observations.

These outliers may represent:

* Bulk orders
* Promotional transactions
* Special products
* Test SKUs
* Unusual pricing situations

Outliers should therefore be considered carefully when calculating average pricing, revenue, and margin metrics.

---

### 🔗 Correlation Analysis

Correlation analysis was used to understand relationships between important numerical variables.

Key findings include:

| Relationship         | Correlation |
| -------------------- | ----------: |
| Profit ↔ Revenue     |        0.87 |
| Unit Price ↔ Revenue |        0.91 |
| Unit Price ↔ Profit  |        0.79 |
| Unit Price ↔ Cost    |        0.94 |
| Cost ↔ Revenue       |        0.85 |
| Cost ↔ Profit        |        0.58 |

Order quantity showed comparatively weaker relationships with revenue and profit, suggesting that **pricing and transaction value are more influential factors than order quantity alone**.

---

## 💡 Key Business Insights

### 1. Strong Wholesale Dependence

Wholesale contributes approximately **54% of total sales**, making it the dominant sales channel.

### 2. Export Growth Opportunity

Exports contribute approximately **15%**, creating an opportunity to diversify revenue through international expansion.

### 3. Product Performance is Uneven

A small group of products generates significantly higher revenue than lower-performing products.

### 4. California is the Leading Market

California significantly outperforms other states in both revenue and order volume.

### 5. 2017 Revenue Drop Requires Investigation

The early-2017 decline stands out as an unusual event and may require additional business investigation.

### 6. Pricing is an Important Revenue Driver

Unit price shows a strong correlation with revenue, profit, and cost.

### 7. Outliers Can Affect Business Metrics

Bulk orders and promotional transactions can significantly influence average revenue and pricing calculations.

---

## 💡 Business Recommendations

Based on the analysis:

1. **Outlier Management**
   Separate or appropriately classify bulk-order and promotional transactions when calculating average business metrics.

2. **Improve Lower-Performing Products**
   Review pricing, cost structure, promotions, and product strategy for mid- and lower-performing products.

3. **Expand Export Sales**
   Explore targeted international marketing and distributor partnerships to diversify revenue.

4. **Improve Seasonal Planning**
   Use historical sales patterns to optimize inventory, promotions, and marketing activities.

5. **Investigate the 2017 Revenue Drop**
   Perform additional business analysis to understand the reason behind the unusual decline.

6. **Build a Power BI Dashboard**
   Convert the analytical findings into an interactive dashboard for management reporting and decision-making.

---

## 📊 Planned Power BI Dashboard

The analysis was designed to provide a foundation for a Power BI dashboard containing areas such as:

* KPI Summary
* Revenue Analysis
* Profit Analysis
* Product Performance
* Channel Performance
* Regional Performance
* State-Level Analysis
* Monthly/Yearly Trends
* Customer Analysis
* Outlier Analysis

---

## 📁 Project Structure

```text
USA-Regional-Sales-Analysis/
│
├── EDA_Regional_Sales_Analysis.ipynb
├── Sales_data(EDA Exported).csv
├── README.md
└── data/
    └── Regional Sales Summary.xlsx
```

