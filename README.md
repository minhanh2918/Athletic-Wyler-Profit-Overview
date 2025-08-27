# Athletic Wyler Profit Overview
<img width="2385" height="1366" alt="image" src="https://github.com/user-attachments/assets/6a0ff504-855c-478f-9150-3f2276b55278" />

# Project Overview
Athletic Wyler, a sports company specialising in selling cardio exercise machines, is tracking the profit performance of its products from January 2018 to May 2024. The company needs
to determine which product(s) will be the best seller and decide whether to discontinue the others.

# Dataset
- The dataset covers historical transactions from the company’s sales/profit system covering Jan-2018 → May-2024.
- It contains aggregated monthly profit values by Category, Supplier, and Brand.
  
# Key Features:
- date (transaction month/year).
- category (Treadmill, Rowing Machine, Airbike, Elliptical Trainer).
- supplier (Iron Strength Equipment, Peak Performance Gear, Titan Fitness Supply).
- brand (Titan Training, Summit Strength, Steel Power, Spartan Sports, etc.).
- profit (monthly profit amount).

# Steps to reproduce
**1. Import Datas:** 
- The project begins by importing essential data into Excel for data manipulation and visualisation.

**2. Data Collection:**
- Collect Data: The dataset records monthly profits between January 2018 and May 2024.
  
**3. Data Cleaning**
  
**Handling Duplicates:**

- Check for duplicate rows (same date, category, supplier, brand, and profit). Remove duplicates to avoid double-counting.

**Handling Invalid Records:**

- Remove the Vending Machine record on 2018-01-01, which was identified as a likely test or entry error.
- Ensure all profit values are numeric. Replace non-numeric entries (e.g., text errors) with nulls and handle accordingly.

**Missing Values:**

Verify if any months are missing for a given category. If gaps exist:

- If profit = 0, fill explicitly as 0.

- If data is missing, flag as null for further investigation instead of imputing.

**Standardising Categories/Suppliers/Brands:**

Normalise text fields by:

- Removing extra spaces, converting to consistent case (e.g., “eliptical trainer” → “Elliptical Trainer”).

- Fixing inconsistent spelling across records.

Ensure supplier and brand names are standardised (e.g., “Peak Perf. Gear” → “Peak Performance Gear”).

**Date Formatting:**

- Convert all dates into consistent YYYY-MM format.

- Extract year and month fields for time-series analysis.

**Profit Validation:**

- Remove or flag rows where profit < 0 unless verified as legitimate (e.g., returns).

- Cross-check that total profit = sum of all monthly profits by category/brand/supplier.
  
**4. KPI Calculation & Derived Metrics**

Average Monthly Profit: total profit ÷ number of months.

YoY Change: year-over-year profit percentage.

MoM Change: month-over-month profit percentage.

QoQ Change: quarter-over-quarter profit change.

High/Low Flags: mark the highest and lowest profit months for reporting.

**5. Exploratory Data Analysis (EDA)**

**From the dashboard:**

Total Profit: $18,906,855

Highest Profit Month: Jan 2018 ($24,299)

Lowest Profit Month: Jun 2020 ($1,020)

Average Monthly Profit: $14,499

**Category Performance:**

Airbike = $7.0M (top category, ~37%)

Rowing Machine = $5.8M (~31%)

Treadmill = $5.7M (~30%)

Elliptical Trainer = $0.36M (~2%) → lowest performer

**Supplier Performance:**

Peak Performance Gear = $7.99M (39%)

Iron Strength = $5.76M (30%)

Titan Fitness Supply = $5.75M (30%)

**Brand Performance:**

Steel Power = $3.4M (18%)

Apex Athletics = $2.7M (14%)

Elevate Fitness = $2.3M (12%)

Remaining brands range from $1.1M–$2.3M

**Profit Change Trends:**

YoY: Strong growth until 2022, then noticeable decline after 2023.

MoM: Significant monthly fluctuations, multiple swings outside ±10%.

QoQ: Drop in Q2/Q3 followed by Q4 recovery.

**6. Insights & Recommendations**

Focus: Airbike, Rowing Machine, and Treadmill are the profit backbone.

Risk: Elliptical Trainer is consistently underperforming → candidate for discontinuation or repositioning.

Suppliers: Peak Performance Gear dominates (39%), but over-reliance risk exists. Diversification recommended.

Brands: Steel Power and Apex Athletics stand out. Smaller brands should be reassessed.

Trends: Decline post-2023 suggests structural issues (market, pricing, supply). Deep dive required.

## Summary:
The analysis confirms a strong concentration of profits in three categories and a handful of suppliers/brands. Cleaning and structuring the dataset enables clear visibility of trends, risks, and opportunities — helping the company decide where to invest and where to cut back.
