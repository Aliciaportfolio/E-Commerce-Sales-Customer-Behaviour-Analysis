# E-commerce Sales & Customer Behaviour Analysis(EDA)- Power BI

## Executive Overview
Analyzed 1,200 e-commerce orders totaling $1.26M revenue to identify sales drivers, customer behavior, and growth opportunities. Dashboard reveals strong digital adoption but exposure to high-value outliers.

## Key KPIs
- **Total Revenue**: $1.26M
- **Average Order Value**: $1.05K vs **Median**: $824 - indicates high-value outliers up to $3.46K
- **Total Orders**: 1,200
- **Order Range**: $11.39 - $3.46K

## Dashboard Features
1. **Total Revenue By Product** - Bar chart showing top sellers: Product performance
   
   <img width="392" height="244" alt="Image" src="https://github.com/user-attachments/assets/d18a2a48-bcd0-49c3-98dc-121bc17279df" />
- Chair and Printer generate highest revenue at $200K each
- 25% revenue gap between Chair $200K and Phone $150K 
- Action: Bundle low-performing Phone with top Chair/Printer as "Office Setup" to lift Phone sales. Investigate if Phone inventory was limited.
   
2. **Total Orders By PaymentMethod** - Pie chart: Payment Method Behavior

   <img width="358" height="237" alt="Image" src="https://github.com/user-attachments/assets/0f82edd6-c0c4-424b-bcff-b17984cac3da" />
- **Digital Adoption**: 79.5% use non-cash methods. Online leads at 21.5%
- **Cash Risk**: 246 Cash orders = 20.5%. Higher fraud/return risk vs digital
- **Gift Card Note**: 230 Gift Card orders at 19.17% shows strong promo/gifting program
- **Action**: Run 3% cashback promo for Online + Credit Card to convert 50% of Cash users.
  
3. **Sum Of TotalPrice By ReferralSource** - Funnel Chart: Marketing ROI

   <img width="344" height="206" alt="Image" src="https://github.com/user-attachments/assets/85c6f10a-5ad3-4938-bfc3-75142cd42b84" />
- Visual confirms Instagram leads by 21.4% over lowest channel Referral
- Action: Relocate $10K ad spend from Referral program to Instagram influencers to close $48K gap
  
4. **Total Revenue By Year** - Line chart: Year-over-Year Trend 

   <img width="344" height="221" alt="Image" src="https://github.com/user-attachments/assets/d1e9b82d-78a4-472b-b3bb-c6a13448ed4b" />
- **2023**: $0.55M | **2024**: $0.48M | **2025**: $0.23M
- **Insight**: Revenue dropped 58% from 2023 peak. 2025 decline of 52% vs 2024 is severe.
- **Action**: If 2025 is partial year, annotate dashboard "YTD 2025". If full year, audit for: site outages, inventory issues, competitor entry, or ad budget cuts. Immediate recovery plan needed.
  
5. **Interactive Slicers** - Filter by Year/Quarter and PaymentMethod

   <img width="437" height="164" alt="Image" src="https://github.com/user-attachments/assets/480f4b8b-784c-4c25-8f9e-aff05eceeae0" />
   **Slicer 1: Year, Quarter**
- **Type**: Dropdown slicer with hierarchy
- **Field**: `Sheet1[Date]` → Date hierarchy enabled
- **Purpose**: Filter all visuals by specific year or quarter
- **Key Requirement**: Enables YTD vs full-year comparison. Selecting `2025` shows partial-year data with YTD disclaimer.
- **Default State**: No filter applied - shows all years 2023-2025

**Slicer 2: PaymentMethod**
- **Type**: List slicer, multi-select enabled
- **Field**: `Sheet1[PaymentMethod]`
- **Values**: Cash, Credit Card, Debit Card, Gift Card, Online
- **Purpose**: Analyze revenue trends and product performance by payment type
- **Insight**: Reveals Credit Card drives 58% of revenue; Online at 22%

**DASHBOARD 
<img width="570" height="322" alt="Image" src="https://github.com/user-attachments/assets/a2bb1e49-e9bd-4b75-a18b-355bfa4419ae" />

### **Outlier & Price Distribution Analysis**
Statistical review of `Avg TotalPrice` vs `Median TotalPrice` by Product revealed 
significant right-skew in two categories:

1. **Phone**: Mean $972.58 exceeds median $692.00 by **40.5%**. Indicates a small 
   number of high-value transactions inflate the average. Low `MIN PRICE` of $11.39 
   also suggests data entry anomalies or clearance SKUs.

2. **Tablet**: Mean $1,042.28 exceeds median $787.00 by **32.4%**. `MAX PRICE` of 
   $3,457 is the dataset high, confirming presence of premium-tier outliers.

3. **Remaining Categories**: Chair, Desk, Laptop, Monitor, Printer show skew < 26%, 
indicating stable, balanced pricing with fewer extreme transactions.

**Business Impact**: Avg Price KPI is misleading for Phone/Tablet. Use Median for 
pricing strategy. Audit $11.39 Phone and $3,457 Tablet transactions for data quality.

<img width="608" height="346" alt="Image" src="https://github.com/user-attachments/assets/8035c41a-7656-425b-b110-9e7191c5f7ba" />

## Key Insights
1. **Outlier Impact**: Mean-median skew analysis flags Phone (40.6%) and Tablet (32.4%) as high-skew categories, indicating premium transactions distort average pricing.
2. **Marketing ROI**: Instagram drives highest revenue $275.29K vs Referral $226.82K. Shift budget accordingly.
3. **Payment Trend**: Online + Credit Card = 47% of orders. Cash still 20.5% - consider incentives for digital.
4. **2025 Dip**: Revenue dropped $0.55M → $0.40M. Investigate Q1-Q2 2025 seasonality or inventory issues.

## Tools Used
Power BI Desktop, DAX, Power Query

## Data Source
Cleaned e-commerce dataset - see Project 1: `E-Commerce-Data-Cleaning-Project` for cleaning steps.# E-Commerce-Sales-Customer-Behaviour-Analysis
