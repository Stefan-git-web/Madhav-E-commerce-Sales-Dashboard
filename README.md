# 📊 Madhav Ecommerce Sales Dashboard – Power BI

An interactive Ecommerce Sales Dashboard built in Power BI to analyze sales performance, profits, and customer purchasing behavior.
It delivers actionable insights through KPIs, charts, and filters, empowering businesses to make data-driven decisions.

# 🚀 Features

KPIs: Total Sales Amount, Profit, Quantity Sold, Average Order Value (AOV)

State-wise Sales analysis

Category-wise Quantity distribution

Monthly Profit Trend

Customer-wise Sales

Payment Mode Usage

Sub-category Profit Analysis

Interactive Quarter Filter & Global Filter

# 📂 Dataset

The dataset includes:

Order details (Amount, Quantity, Profit)

Customer Information

Product Category & Sub-category

Order Date

Payment Mode

Location (State)

# 🛠 Steps Followed
# 1️⃣ Data Loading & Cleaning

Imported dataset into Power BI

Checked for missing/null values

Verified correct data types (Date, Text, Number)

# 2️⃣ Data Modelling

Created relationships between fact and dimension tables

Implemented Star Schema for optimized reporting

# 3️⃣ DAX Measures
-- Total Amount
Amount = SUM(Sales[Amount])

-- Total Profit
Profit = SUM(Sales[Profit])

-- Total Quantity
Quantity = SUM(Sales[Quantity])

-- Average Order Value
AOV = DIVIDE([Amount], DISTINCTCOUNT(Sales[Order_ID]), 0)

-- Profit by Month
Profit by Month = SUM(Sales[Profit])

-- % Quantity by Category
Quantity % = DIVIDE(SUM(Sales[Quantity]), CALCULATE(SUM(Sales[Quantity]), ALL(Sales[Category])), 0)

-- % Quantity by Payment Mode
Payment Mode % = DIVIDE(SUM(Sales[Quantity]), CALCULATE(SUM(Sales[Quantity]), ALL(Sales[PaymentMode])), 0)

# 4️⃣ Visualization

Card visuals for KPIs

Bar charts for Amount by State, Amount by Customer, and Profit by Sub-Category

Donut charts for Quantity by Category & Quantity by Payment Mode

Clustered column chart for Monthly Profit

Slicers for Quarter & All-field selection

# 5️⃣ Formatting

Applied dark theme with high-contrast colors

Added data labels and legends for clarity

Used consistent color mapping for categories


## 📊 Dashboard Preview  
[Dashboard PDF](https://github.com/Stefan-git-web/Madhav-E-commerce-Sales-Dashboard/blob/main/Madhav_Ecommerce_Dashboard_Insights.pdf)  
[Dashboard Image](https://github.com/Stefan-git-web/Madhav-E-commerce-Sales-Dashboard/blob/main/Screenshot%202025-08-14%20164452.png)



# 🛠 Tools Used

Power BI – Data modeling & visualization

Excel/CSV – Data source
