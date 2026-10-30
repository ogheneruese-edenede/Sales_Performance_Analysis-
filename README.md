# 📊 Sales Performance Analysis Report (2024–2025)

## SECTION 1: INTRODUCTION

### BUSINESS OBJECTIVE
The goal of this analysis is to understand the company’s 2024-2025 sales performance across products, regions, channels, and time, in order to guide inventory, marketing, and distribution decisions[cite: 2].

* **Problem Statement:** The business sells across six categories, five regions, and four channels, but its 2024-2025 sales data has not been turned into clear insight[cite: 2]. Leadership cannot easily see which areas drive revenue or underperform, making it hard to allocate inventory, marketing, and distribution resources effectively[cite: 2].
* **Business Questions:**
  * Which product categories and individual products generate the most revenue?[cite: 2]
  * Which regions are the strongest and weakest markets by revenue?[cite: 2]
  * How has monthly revenue changed over time, and how did 2025 compare with 2024?[cite: 2]
  * What are the key KPIs (total revenue, average order value, units sold, orders, and customers), and how have they changed year on year?[cite: 2]

---

## SECTION 2: DATA OVERVIEW

This is a synthetic dataset containing 512 order records from January 3, 2024 to December 27, 2025[cite: 2]. After cleaning, 500 records remain[cite: 2].

* **Tools:** Excel 2019, PivotTables, Pivot Charts, slicers, timeline[cite: 2]

### Key Fields:
* **Order ID:** Unique identification number assigned to each individual sales transaction[cite: 1, 2].
* **Order Date:** Calendar date when the customer placed the order[cite: 1, 2].
* **Month:** Extracted month name of the transaction, used for analyzing monthly sales trends[cite: 1, 2].
* **Year:** Extracted calendar year of the order, used for year-over-year performance comparisons[cite: 1, 2].
* **Customer ID:** Unique identifier for each individual buyer, used to track customer purchasing patterns[cite: 1, 2].
* **Customer:** Categorical field or flag classifying customer profile types[cite: 1, 2].
* **Full Name:** Combined first and last name of the customer who made the purchase[cite: 1, 2].
* **Age:** Customer's age in years, used for demographic analysis[cite: 1, 2].
* **City:** Specific municipality or location where the order was delivered[cite: 1, 2].
* **Region:** Broader geographical territory (e.g., South West, North Central) grouping related cities[cite: 1, 2].
* **ProductID:** Unique numeric code assigned to each distinct inventory item[cite: 1, 2].
* **Product Name:** Descriptive name of the item sold[cite: 1, 2].
* **Category:** Product classification grouping related items together (e.g., Home Appliances, Electronics)[cite: 1, 2].
* **Price:** Selling cost per single unit of the product in Naira[cite: 1, 2].
* **Quantity:** Total number of product units purchased in a single order[cite: 1, 2].
* **Revenue:** Total monetary value generated from the order ($\text{Price} \times \text{Quantity}$)[cite: 1, 2].
* **Sales Channel:** Point of purchase or avenue where the transaction occurred (e.g., Online, Retail Store)[cite: 1, 2].

### Data Cleaning and Transformation Steps:
* **Duplicate Removal:** Removed 12 exact duplicate records, reducing the dataset from 512 to 500 rows[cite: 2].
* **Text Standardization:** Fixed category text inconsistencies, case formatting, and extra spacing using `TRIM`, `CLEAN`, and `PROPER` functions[cite: 2].
* **Name Cleaning:** Trimmed leading and trailing whitespace from customer first names[cite: 2].
* **Data Type Conversion:** Converted `Quantity` and `Age` fields from text/mixed types into proper numeric values[cite: 2].
* **Currency Formatting:** Formatted `Price` and `Revenue` fields explicitly as currency[cite: 2].
* **Anomaly Correction (Prices):** Investigated and corrected 8 records containing invalid negative prices[cite: 2].
* **Revenue Calculation:** Generated the `Revenue` field using the formula: `(Unit Price * Quantity)`[cite: 2].
* **Temporal Feature Engineering:** Created dedicated `Year` and `Month` columns for time-series and trend analysis[cite: 2].
* **Data Imputation (Age):** Handled impossible, missing, and inconsistent age values (0, 150, unknown, blanks) by cross-referencing customer names and IDs to locate and impute valid records[cite: 2].
* **Geographic Standardization:** Standardized inconsistent region spellings and mapped all cities to their correct corresponding regions using a master mapping reference[cite: 2].
* **Full Name Concatenation:** Created a unified `Full Name` column by combining customer first and last names using the `CONCAT` function[cite: 2].
* **Channel Simulation:** Added a simulated `Sales Channel` column via Excel formulas[cite: 2].
* **Category Mapping Correction:** Investigated and corrected 11 products assigned to incorrect product categories by reassigning them via a standardized mapping table[cite: 2].
* **Outlier Detection:** Checked for statistical outliers across numerical metrics using the Interquartile Range (IQR) method (none found)[cite: 2].
* **Final Validation:** Performed comprehensive validation checks to guarantee completeness, uniqueness, label consistency, and valid ranges[cite: 2].

---

## SECTION 3: KEY METRICS

| KPI | Total | 2024 | 2025 | YoY Growth Rate |
| :--- | :--- | :--- | :--- | :--- |
| **Total Revenue** | ₦1,518,872[cite: 2] | ₦695,223[cite: 2] | ₦823,649[cite: 2] | 18%[cite: 2] |
| **Average Order Value** | ₦3,038[cite: 2] | ₦2,958[cite: 2] | ₦3,108[cite: 2] | 5%[cite: 2] |
| **Total Orders** | 500[cite: 2] | 235[cite: 2] | 265[cite: 2] | 13%[cite: 2] |
| **Total Quantity** | 1,763[cite: 2] | 815[cite: 2] | 948[cite: 2] | 16%[cite: 2] |
| **Total Customers** | 117[cite: 2] | 103[cite: 2] | 111[cite: 2] | 8%[cite: 2] |

The dataset shows that the company generated approximately **₦1,518,872** in revenue from **500 orders** and **1,763 units sold**, representing an **18% growth** vs last year[cite: 2]. The average order generated approximately **₦3,038** in value (+5% YoY), while total customers grew to **117** (+8%), indicating healthy repeat purchases[cite: 2]. South West dominates revenue with over ₦556k, nearly double any other region[cite: 2]. The company has strong sales activity, with revenue, units (+16%) and orders (+13%) all growing faster than its customer base, but is highly dependent on the South West region[cite: 2].

---

## SECTION 4: REVENUE PERFORMANCE BREAKDOWN

### Performance by Region
* **South West:** The primary revenue driver, generating **₦556,562.46** (36.64% market share across 175 orders)[cite: 2].
* **North Central:** The second largest territory, generating **₦283,062.85** (18.64% share across 92 orders), expanding YoY from ₦119,065.10 in 2024 to ₦163,997.75 in 2025[cite: 2].
* **North West:** The weakest performing region, recording **₦193,006.29** (12.71% share across 69 orders)[cite: 2]. 

> **Strategic Note:** While the South West provides a strong baseline, the business is overly dependent on a single territory[cite: 2]. Conversely, the **South South** region represents the highest-growth expansion opportunity, surging **+62.4% YoY** from ₦88,789.24 to ₦144,192.86[cite: 2].

### Performance by Category
* **Home Appliances:** The top-performing category, bringing in **₦307,428.90** (20.24% share across 85 orders)[cite: 2].
* **Office:** Generated **₦289,383.36** (19.05% share across 81 orders), though it experienced a YoY contraction from ₦163,409.39 in 2024 to ₦125,973.97 in 2025[cite: 2].
* **Gaming:** The lowest-performing category, recording **₦185,257.89** (12.20% share across 82 orders)[cite: 2].

> **Strategic Note:** Home Appliances is the core growth engine (+70% YoY growth)[cite: 2]. In contrast, Gaming lags behind overall despite housing a top-3 selling individual product, pointing to catalog weakness outside its flagship item[cite: 2].

### Performance by Product
* **Top Product:** The **Electric Kettle (Home Appliances)** led all individual SKUs, generating **₦113,951.00** across 21 orders[cite: 2].
* **Top 5 Portfolio Contribution:** The top 5 SKUs (Electric Kettle, Smartphone [₦98,901.38], Gaming Headset [₦88,156.16], Printer [₦86,650.30], and Webcam [₦85,846.10]) generated a combined **₦473,504.94**, accounting for **31.17%** of total enterprise revenue[cite: 2]. Portfolio risk is high, with nearly one-third of total revenue dependent on just 5 SKUs across 96 orders[cite: 2].
* **Highest Average Price Items:** Smartphone (₦1,476), Gaming Headset (₦1,377), Electric Kettle (₦1,341), Mouse (₦1,331), Air Conditioner (₦1,330)[cite: 2].

### Trend over Time
* **Peak Month:** **April 2025** achieved the highest single-month revenue across the two-year period at **₦102,962.53** (31 orders), representing **+70% growth** compared to April 2024[cite: 2].
* **Trough Month:** **February 2024** was the lowest-performing month, generating **₦34,598.78** (15 orders)[cite: 2].
* **Q4 Seasonality Shift:** While Q4 remains the annual peak demand period (October–November), Q4 2025 revenue (₦228,412) declined by ~3.4% compared to Q4 2024 (₦226,311.35)[cite: 2]. The annual 18% YoY growth was driven entirely by strong performance during the first nine months (Jan–Sept)[cite: 2]. The Q4 slowdown indicates late-year performance fatigue that requires promotional or inventory adjustments[cite: 2].

---

## SECTION 5: FINDINGS AND RECOMMENDATIONS

### Key Findings
1. **Strong overall growth:** Revenue grew 18%, from ₦695.2K in 2024 to ₦823.6K in 2025 (₦1.52M combined)[cite: 2]. Orders rose 13%, units 16%, customers 8%, and average order value 5%[cite: 2]. About 70% of the growth came from more orders (+13%) and 30% from higher order value (+5%), and orders grew faster than customers, which suggests repeat buying[cite: 2].
2. **Revenue concentration in one region:** South West generates ₦557K (37% of revenue), nearly double North Central (₦283K, the second-largest)[cite: 2]. North West is weakest at ₦193K (13%)[cite: 2].
3. **Home Appliances and Office lead:** Together they bring in 39% of revenue[cite: 2]. Home Appliances (₦307K) is only slightly ahead of Office (₦289K), so treat them as joint leaders[cite: 2].
4. **Gaming and Accessories lag:** They are the bottom two categories, at 12% and 13% of revenue[cite: 2]. Gaming Headset is the #3 product overall, so the weakness is in the rest of the Gaming range, not its best seller[cite: 2].
5. **Revenue depends on a few products:** The top five products (Electric Kettle, Smartphone, Gaming Headset, Printer, Webcam) generate ₦474K, or 31% of revenue[cite: 2].
6. **Growth slowed in Q4:** Q4 2025 was about 3% below Q4 2024, though it was still 2025’s strongest quarter[cite: 2]. The 18% growth came from the first nine months[cite: 2].

### Recommendations
1. **Defend South West and reduce dependence on it:** Protect stock availability and retention there, and track its revenue share quarterly[cite: 2]. A fall in South West would hit the whole business[cite: 2].
2. **Diagnose North West before investing:** Compare its order count and average order value with other regions first[cite: 2]. Then run a small targeted promotion and measure the result[cite: 2].
3. **Prioritize Home Appliances and investigate Office:** Office revenue fell 22.9% in 2025 (₦163K to ₦126K); find out why before adding stock[cite: 2].
4. **Review the Gaming and Accessories range:** Check pricing and demand for weak products[cite: 2]. Bundle Accessories with Electronics and Gaming purchases to lift sales of both[cite: 2].
5. **Plan for Q4:** Investigate the October and December declines by comparing orders, order value, and product mix with 2024[cite: 2]. Confirm the cause before committing promotion budget[cite: 2].
6. **Grow order value:** Average order value rose only 5%, so use bundles and upsells to increase it alongside order volume[cite: 2].

---

## Limitations
* **Simulated Channel Field:** Channel results are excluded because the sales channel is simulated[cite: 2].
* **Sample Size Sensitivity:** The dataset reflects an average of ~21 orders per month; short-term monthly fluctuations should be interpreted as directional indicators rather than macro trends[cite: 2].
* **Cost & Margin Visibility:** Without Cost of Goods Sold (COGS) and operational expense data, net profitability and true SKU contribution margins cannot be calculated[cite: 2].

---

## Conclusion
This 2024-2025 sales analysis demonstrates solid top-line momentum, driven by an 18% YoY revenue expansion and strong repeat purchasing[cite: 2]. However, heavy reliance on the South West region and late-year deceleration highlight structural vulnerabilities[cite: 2]. By actively diversifying regional operations, optimizing lagging product categories, and refining pre-season inventory planning, the business is well-positioned for sustainable, long-term growth[cite: 2].

---

## Author
**Edenede Ogheneruese**[cite: 2]
