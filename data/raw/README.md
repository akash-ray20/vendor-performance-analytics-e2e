# 📁 Raw Data – Vendor Performance Analytics Project

This folder contains the original raw datasets used in the Vendor Performance Analytics project.

---

## 📄 Files Included

- `begin_inventory.csv` – Opening inventory quantities per product  
- `end_inventory.csv` – Closing inventory quantities per product  
- `purchase_prices.csv` – Vendor-wise purchase price reference data  
- `sample_purchases.csv` – Sample of purchase transaction data  
- `sample_sales.csv` – Sample of sales transaction data  

---

## ⚠️ Important Note on Data Size

The original **Purchases** and **Sales** datasets are significantly large and exceed GitHub’s file size limits.

Therefore:

- Only **sample datasets** (`sample_purchases.csv`, `sample_sales.csv`) are uploaded in this repository.
- These samples maintain the original schema and structure to allow full reproducibility of the analysis pipeline.
- The complete datasets were used for the full-scale analysis and dashboard creation but are not included due to size constraints.

Full datasets can be shared upon request.

---

## 🔎 Purpose of These Files

These raw datasets serve as the foundational inputs for:

- Data cleaning and transformation (Python – Pandas)
- Vendor-level aggregations
- Profitability and margin analysis
- Inventory turnover analysis
- Unsold capital computation
- Power BI dashboard development

---

## 📌 Usage

All transformation logic is implemented in the `/notebooks` and `/src` directories.  
The final analytical dataset (`vendor_sales_summary`) used in Power BI is generated from these raw files.
