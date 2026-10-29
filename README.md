# Retail Product Performance Analytics

### Retail Sales Intelligence | Product Performance | ABC Analysis | Transaction Monitoring

An interactive retail analytics project built using **Google Sheets** and **Google Looker Studio** to transform raw transaction records into actionable business insights.

<img width="1244" height="853" alt="image" src="https://github.com/user-attachments/assets/a15b9e7a-80b6-4160-a588-8dbef624c5b7" />

<img width="1241" height="866" alt="image" src="https://github.com/user-attachments/assets/69b7d08f-bcfe-4ec4-b26e-73a225928a12" />

<img width="888" height="387" alt="image" src="https://github.com/user-attachments/assets/81fc62f2-342b-4dad-9f3d-970bfe3d58d6" />




The project covers sales performance, product contribution, ABC classification, geographic trends, cancellations, and transaction-level analysis.

### [View Live Interactive Dashboard](https://datastudio.google.com/reporting/8020203f-e331-43e1-92cb-f2f87bab1bfc)

---

## 1. Project Overview

This project demonstrates an end-to-end retail analytics workflow, from raw data preparation to interactive business intelligence reporting.

**Objectives:**
- Analyze retail sales and product performance.
- Identify high-revenue products using ABC classification.
- Monitor sales trends and geographic performance.
- Investigate cancellations and invalid transactions.
- Improve data quality through cleaning and reconciliation.
- Present management-level insights using interactive dashboards.

## 2. Technology Stack

| Technology | Application |
|---|---|
| Google Sheets | Data preparation, cleaning, validation, aggregation |
| Google Looker Studio | Interactive dashboards and visualization |
| Google Sheets QUERY | Product-level aggregation and analysis |
| Calculated Fields | Cancellation metrics and KPI calculations |
| ABC Analysis | Revenue-based product classification |

## 3. Dataset Overview

**Source:** UCI Online Retail Dataset

The project analyzes a subset of the dataset containing 49,999 transaction records.

| Dataset Metric | Value |
|---|---:|
| Source Records | 49,999 |
| Valid Sales Line Items | 48,779 |
| Cancellation Records | 923 |
| Invalid Records | 297 |
| Distinct Products in Valid Sales | 2,840 |
| Reporting Period | December 2010 – January 2011 |

The dataset includes invoice numbers, product codes, product descriptions, quantities, transaction dates, unit prices, customer IDs, and countries.

## 4. Key Performance Indicators

| KPI | Result |
|---|---:|
| Total Sales Revenue | 955,338.93 |
| Units Sold | 435,085 |
| Active Products | 2,840 |
| Sales Line Items | 48,779 |
| Cancellation Value | 114,726.38 |
| Line-Item Cancellation Rate | 1.86% |

**Currency disclosure:** The original dataset records prices in GBP. The current dashboard uses a USD ($) display symbol without exchange-rate conversion. Therefore, the monetary figures above retain their original numerical values and should not be interpreted as converted USD amounts.

## 5. Dashboard Overview

### Page 1 — Sales Performance

Provides an executive overview of product and sales performance.

**Features:**
- Total revenue, units sold, active products, and sales line items
- Top 10 products by sales line-item count
- ABC product distribution
- Revenue contribution by ABC category

#### ABC Product Classification

Products are classified according to their cumulative contribution to sales revenue.

| Classification | Products | Revenue Contribution |
|---|---:|---:|
| A | 577 | 763,935.41 |
| B | 761 | 143,565.98 |
| C | 1,502 | 47,837.54 |
| **Total** | **2,840** | **955,338.93** |

ABC classification helps identify which products contribute most significantly to revenue and supports inventory prioritization.

### Page 2 — Sales Trends & Geographic Performance

Analyzes revenue patterns across time and geographic markets.

**Features:**
- Daily revenue trend
- Date-range filtering
- Transaction-type selection
- Top 10 countries by line revenue

The dashboard uses daily trends because the selected dataset spans approximately two months.

### Page 3 — Transaction Explorer

Supports detailed investigation of retail transactions.

**Features:**
- Date, transaction-type, country, and product filters
- Transaction summary by classification
- Transaction details table
- Cancellation rate KPI
- Total cancellation value KPI
- Top 10 StockCodes by cancellation value

The report distinguishes three transaction classifications: `SALE`, `CANCELLATION`, and `INVALID`.

## 6. Data Preparation & Analytical Methodology

The data preparation process includes:

1. **Data profiling:** Identifying missing values, negative quantities, cancellation invoices, and invalid prices.
2. **Transaction classification:** Separating valid sales, cancellations, and invalid records.
3. **Revenue calculation:** Calculating line-level revenue using quantity and unit price.
4. **Product aggregation:** Grouping valid sales by StockCode.
5. **ABC analysis:** Ranking products by revenue and assigning cumulative revenue classifications.
6. **Data reconciliation:** Validating revenue, quantity, product counts, and sales line items against the prepared datasets.
7. **Dashboard development:** Connecting validated Google Sheets data sources to Looker Studio.

The workbook maintains separate raw data, cleaned sales, product master, analysis, pivot, and reporting layers.

## 7. Business Insights

The analysis highlights several important retail performance considerations:

- Revenue is concentrated among higher-performing products.
- ABC classification helps prioritize products for monitoring and inventory decisions.
- Geographic revenue is heavily concentrated in the United Kingdom.
- Cancellations and adjustments represent a measurable component of transaction activity.
- Some high-value cancellation records relate to fees or adjustments rather than ordinary merchandise.

These observations demonstrate the importance of distinguishing transaction types and interpreting product performance within the appropriate business context.

## 8. Data Quality & Validation

The project incorporates reconciliation checks to verify that aggregated metrics match the cleaned transaction data.

**Validated benchmarks:**
- Sales revenue: 955,338.93
- Sales quantity: 435,085
- Active products: 2,840
- Valid sales line items: 48,779
- Total classified transaction records: 49,999

Invalid records are retained for investigation rather than silently removed from the analytical process.

## 9. Project Limitations

- The project uses a 49,999-record subset rather than the complete UCI dataset.
- The reporting period covers only December 2010 and January 2011.
- Product-level aggregated charts do not dynamically respond to transaction-level date filters.
- Cancellation value represents recorded cancellation activity, not necessarily completed customer refunds.
- Fee and adjustment codes can influence product-level cancellation rankings.
- Monetary values retain the source dataset's GBP amounts, despite the current dashboard's USD display symbol.
- Some dashboard filtering, labeling, and data-quality enhancements remain in progress.

## 10. Future Enhancements

- Dynamic product KPIs based on selected reporting periods
- Improved product description display
- Merchandise-only cancellation analysis
- Advanced data-quality monitoring
- Customer and purchasing-behavior analysis
- Additional inventory and sales performance indicators
- Expanded reporting periods and dataset coverage

## 11. Live Dashboard

Explore the interactive Looker Studio report:

**[Open Retail Product Performance Analytics](https://datastudio.google.com/reporting/8020203f-e331-43e1-92cb-f2f87bab1bfc)**

Dashboard availability depends on the report's sharing permissions.

## 12. Author

**Ankon Banik**

MIS | Business Analytics | ERP | Data Analytics

[GitHub Profile](https://github.com/AnkonBanik)

---

*This project is intended for portfolio demonstration and analytical learning using historical retail transaction data.*
