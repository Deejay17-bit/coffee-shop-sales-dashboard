# ☕ Coffee Shop Sales Dashboard

## Project Overview
End-to-end data analytics project analyzing coffee shop sales 
performance across 3 stores from January to June 2023.

## Tools Used
- **Python (Pandas, NumPy)** — Data cleaning and preparation
- **Jupyter Notebook** — Analysis environment
- **Power BI** — Interactive dashboard and data modeling
- **DAX** — Business measures and KPIs
- **Star Schema** — Data modeling best practice

## Dataset
- **Source:** [Kaggle — Coffee Shop Sales](https://www.kaggle.com/)
- **Records:** 149,116 transactions
- **Period:** January 2023 – June 2023
- **Stores:** BigBrew, Dunkin, Starbucks

## Project Structure

coffee-shop-sales-dashboard/
│
├── Coffee_Project101.ipynb    ← Data cleaning & EDA notebook
├── Coffee Shop Sales.xlsx     ← Raw dataset from Kaggle
├── coffee_sales_cleaned.csv   ← Cleaned dataset for Power BI
└── README.md

## What I Did

### 1. Data Cleaning (Jupyter/Python)
- Built a reusable cleaning pipeline using Python functions
- Stripped whitespace from all text columns
- Mapped store IDs to store names
- Mapped store locations to Philippine regions
- Created new columns: Month, Year, Hour, Day, Day_parts, Total_Amount
- Applied categorical ordering for correct sorting in Power BI
- Validated data quality — no nulls, no duplicates

### 2. Data Modeling (Power BI)
- Built a proper **Star Schema** with 4 tables
- **Fact table:** Coffee1 (transactions)
- **Dimension tables:** Product, Store, Date
- Created relationships between all tables

### 3. DAX Measures
- Total Revenue
- Orders
- AOV (Average Order Value)
- Total Quantity
- Best Performing Store
- Worst Performing Store
- Average Revenue Per Store
- Revenue MoM %

### 4. Dashboard (3 Pages)

**Page 1 — Sales Overview**
- Monthly sales performance by store
- KPI cards for key metrics
- Store slicer for interactive filtering

**Page 2 — Product & Time Analysis**
- Top products by revenue and quantity
- Revenue by hour (area chart)
- Waterfall chart for monthly revenue
- Day-parts heat map matrix

**Page 3 — Store Performance**
- Store comparison by revenue
- Small multiples by month
- Revenue share donut chart
- Day-parts by product category matrix

## Key Insights
- **BigBrew** consistently leads all stores in revenue
- **Mid-Morning (9–10 AM)** is the peak sales period
- **Coffee category** dominates revenue across all stores
- Consistent **upward sales trend** from February to June
- All three stores perform similarly — revenue gap is less than 3%

## Dashboard Screenshots
*(Add screenshots here after uploading)*

## How to Run
1. Clone this repository
2. Open `Coffee_Project101.ipynb` in Jupyter Notebook
3. Run all cells to reproduce the cleaning pipeline
4. Open `coffee_sales_cleaned.csv` in Power BI
