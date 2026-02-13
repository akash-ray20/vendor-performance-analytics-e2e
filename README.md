# Vendor Performance & Inventory Optimization  
### End-to-End Data Analytics & Business Intelligence Project  

An end-to-end analytics project focused on optimizing profitability in a retail/wholesale distribution environment by addressing vendor dependency, pricing inefficiencies, and inventory turnover risk.

This project integrates data engineering, statistical validation, and business intelligence to deliver executive-level insights.

---

## 📌 Business Objective  

To improve sustainable profitability by:

- Identifying vendor concentration risk  
- Quantifying bulk purchasing cost advantages  
- Detecting high-margin, low-sales brands  
- Measuring capital locked in unsold inventory  
- Statistically validating margin differences across vendor tiers  

---

## 🏗 Project Architecture  

### 1. Data Infrastructure  

- ~2GB of raw transactional data  
- Python-based ingestion into SQLite  
- Logging-enabled ETL scripts  
- SQL Common Table Expressions (CTEs) for optimized joins  
- Creation of consolidated analytical table: `vendor_sales_summary`  

### 2. Data Preparation  

- Data type validation  
- Missing value handling  
- Vendor name standardization  
- Removal of non-profitable and zero-sales records  
- Feature engineering for core KPIs  

### 3. Feature Engineering  

Derived performance metrics include:

- Gross Profit  
- Profit Margin (%)  
- Stock Turnover  
- Unsold Inventory Value  
- Purchase Contribution (%)  
- Sales-to-Purchase Ratio  

---

## 📊 Exploratory Data Analysis  

Key observations:

- Significant outliers in purchase price and freight costs  
- Long-tailed pricing distribution (premium products present)  
- Negative margin and zero-sales records detected and filtered  
- Revenue performance found to be primarily volume-driven  
- Weak correlation between pricing variation and total sales revenue  

---

## 🔎 Key Research Findings  

### Vendor Dependency  
Top 10 vendors contribute ~66% of total purchase volume, indicating procurement concentration risk.

### Bulk Purchasing Impact  
Unit cost decreases by approximately 72% when moving from small to large order sizes.

### Brand Optimization  
198 brands identified in the bottom 15% of sales but top 85% of profit margins — representing pricing and visibility inefficiencies.

### Unsold Capital  
$2.7M in working capital is currently locked in unsold inventory.

---

## 📈 Statistical Validation  

### 95% Confidence Interval  

- Top Vendors Margin: 31.17% (CI: 30.74% – 31.61%)  
- Low Vendors Margin: 41.55% (CI: 40.48% – 42.62%)  

Confidence intervals do not overlap.

### Welch’s Two-Sample T-Test  

- t-statistic: -17.6695  
- p-value: < 0.001  

Result: Statistically significant difference in mean profit margins.  
Low-performing vendors operate at higher margins but lower volumes, indicating structurally distinct profitability models.

---

## 📊 Power BI Dashboard  

The dashboard consolidates:

- Total Sales, Purchases, Gross Profit, Margin  
- Unsold Capital  
- Vendor Purchase Contrib
