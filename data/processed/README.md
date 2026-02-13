# 📁 Processed Data – Vendor Performance Analytics Project

This folder contains datasets generated after data cleaning, transformation, aggregation, and KPI engineering in Python.

These files serve as structured analytical outputs and were used directly for Power BI dashboard development.

---

## 📄 Files Included

- `vendor_sales_summary.xlsx`  
  Final consolidated vendor-level analytical table combining:
  - Total Purchase Dollars
  - Total Sales Dollars
  - Gross Profit
  - Profit Margin
  - Stock Turnover
  - Sales-to-Purchase Ratio
  - Freight Allocation
  - Derived KPIs

- `BrandPerformance.xlsx`  
  Brand-level aggregated performance including:
  - Total Sales
  - Profit Margin
  - Target brand identification logic

- `PurchaseContribution.xlsx`  
  Vendor-level purchase contribution percentages used for:
  - Pareto analysis
  - Donut and contribution charts in Power BI

- `LowTurnoverVendor.xlsx`  
  Vendors filtered for low inventory turnover (StockTurnover < 1), used to identify slow-moving inventory risk.


---

## 🔎 Purpose of Processed Data

These datasets represent the **analytics-ready layer** of the project.

They were created to:

- Reduce transformation load inside Power BI
- Maintain consistency between Python analysis and BI layer
- Improve dashboard performance
- Enable reproducibility of business insights

---

## 📌 Data Pipeline Flow

Raw Data → Python Cleaning & Feature Engineering → Aggregated Analytical Tables → Power BI Dashboard

All transformation logic used to generate these files is documented in:

- `/notebooks`
- `/src`

---

## ⚠️ Important Note

These files are outputs derived from the full raw datasets.  
If using sample raw data (due to GitHub size limits), results may slightly differ from the original dashboard metrics.
