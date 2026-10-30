# 📊 Sales Performance Analysis (2024-2025)

## SECTION 1: INTRODUCTION

### Business Objective
The goal of this analysis is to understand the company's 2024-2025 sales performance across products, regions, channels to guide inventory, marketing, and distribution decisions.

**Problem Statement:** The business sells across six categories, five regions, and four channels, but its 2024-2025 sales data has not been turned into clear insights. Leadership cannot easily see which areas drive revenue or underperform, making it hard to allocate resources effectively.

**Business Questions:**
1. Which product categories and individual products generate the most revenue?
2. Which regions are the strongest and weakest markets by revenue?
3. How has monthly revenue changed over time, and how did 2025 compare with 2024?
4. What are the key KPIs (total revenue, average order value, units sold, orders, and customers), and how have they changed year on year?

## SECTION 2: DATA OVERVIEW

Synthetic dataset containing 512 order records from Jan 3, 2024 to Dec 27, 2025. After cleaning, **500 records remains**.

**Tools:** Excel 2019, PivotTables, Pivot Charts, Slicers, Timeline

**Key Fields:**
- **Order ID:** Unique ID for each sales transaction
- **Order Date:** Date when customer placed order
- **Month / Year:** Extracted for trend analysis
- **Customer ID / Full Name / Age / City / Region:** Customer and location details
- **ProductID / Product Name / Category:** Product details
- **Price / Quantity / Revenue:** Price x Quantity = Revenue
- **Sales Channel:** Point of purchase (e.g., Online, Retail Store)

## SECTION 3: KEY METRICS

| KPI | Total | 2024 | 2025 | YoY Growth |
|---|---|---|---|---|
| **Total Revenue** | ₦1,518,872 | ₦695,223 | ₦823,649 | 18% |
| **Average Order Value** | ₦3,038 | ₦2,958 | ₦3,108 | 5% |
| **Total Orders** | 500 | 235 | 265 | 13% |
| **Total Quantity** | 1,763 | 815 | 948 | 16% |
| **Total Customers** | 117 | 103 | 111 | 8% |

The dataset shows the company generated approximately ₦1,518,872 from 500 orders and 1,763 units sold, representing an **18% growth vs last year**. Average order was ₦3,038 (+5% YoY), customers grew to 117 (+8%), indicating healthy repeat purchases. South West dominates revenue with over ₦556k, nearly double any other region.

## 📸 Dashboard

![Sales Performance Dashboard](sales_dashboard.png)

## 🛠️ Files
- `sales_dashboard.png` - Interactive Dashboard Screenshot
- `Sales_Performance_Analysis.xlsx` - Excel File
- `Sales_Performance_Analysis_Report.docx` - Full Report in Word (upload your original)

## 👤 Author
Oghene Ruese Edenede - Data Analyst
