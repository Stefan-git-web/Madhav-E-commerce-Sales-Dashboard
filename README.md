# Madhav-E-commerce-Sales-Dashboard
# 📊 Madhav Ecommerce Sales Dashboard – Power BI

This project showcases an interactive **Ecommerce Sales Dashboard** built in **Power BI** to analyze sales performance, profits, and customer purchasing behavior.  
It provides clear insights through KPIs, charts, and filters, enabling better decision-making for business growth.

---

## 🚀 Features
- **KPIs**: Total Sales Amount, Profit, Quantity Sold, Average Order Value (AOV)
- **State-wise Sales** analysis
- **Category-wise Quantity** distribution
- **Monthly Profit Trend**
- **Customer-wise Sales**
- **Payment Mode Usage**
- **Sub-category Profit Analysis**
- Interactive **Quarter Filter** & **Global Filter**

---

## 📂 Dataset
The dataset contains:
- Order details (Amount, Quantity, Profit)
- Customer Information
- Product Category & Sub-category
- Order Date
- Payment Mode
- Location (State)

---

## 🛠 Steps Followed

### 1️⃣ Data Loading & Cleaning
- Imported the dataset into Power BI
- Checked for null or missing values
- Ensured data types were correct (Date, Text, Number)

### 2️⃣ Data Modelling
- Created relationships between tables (Fact table for orders, Dimension tables for customers, products, etc.)
- Ensured a **Star Schema** for efficient reporting


### 4️⃣ Visualization

Card visuals for KPIs

Bar charts for:

Amount by State

Amount by Customer

Profit by Sub-Category

Donut charts for:

Quantity by Category

Quantity by Payment Mode

Clustered column chart for Monthly Profit

Slicers for Quarter & All-field selection

### 5️⃣ Formatting

Applied a dark theme with high-contrast colors for better readability

Added data labels and legends for clarity

Used consistent color mapping for categories

### 🛠 Tools Used

Power BI for data modeling & visualization

Excel/CSV as the data source 

### 3️⃣ DAX Measures
**KPIs**
```DAX
Amount = SUM(Sales[Amount])

Profit = SUM(Sales[Profit])

Quantity = SUM(Sales[Quantity])

AOV = DIVIDE([Amount], DISTINCTCOUNT(Sales[Order_ID]), 0)
Monthly Profit

Profit by Month = SUM(Sales[Profit])


% Quantity by Category
Quantity % = DIVIDE(SUM(Sales[Quantity]), CALCULATE(SUM(Sales[Quantity]), ALL(Sales[Category])), 0)


% Quantity by Payment Mode
Payment Mode % = DIVIDE(SUM(Sales[Quantity]), CALCULATE(SUM(Sales[Quantity]), ALL(Sales[PaymentMode])), 0)
