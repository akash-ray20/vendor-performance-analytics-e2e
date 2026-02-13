# 📊 Power BI Dashboard – Vendor Performance Analytics

This folder contains the Power BI dashboard file built using the processed outputs from the Python analytics pipeline.

The dashboard presents procurement efficiency, vendor contribution, profitability distribution, and brand-level optimization insights in a clean executive view.

---

# 🧭 Dashboard Walkthrough

## 1️⃣ Executive KPI Overview (Top Row)

Five KPI cards provide an instant summary of overall business health:

- **Total Sales ($)** → Total revenue generated
- **Total Purchase ($)** → Total procurement spend
- **Gross Profit ($)** → Sales – Purchase
- **Profit Margin (%)** → Average profit margin across vendors
- **Unsold Capital ($)** → Value of purchased inventory not yet sold

These KPIs dynamically update with any filter interaction.

---

## 2️⃣ Purchase Contribution % (Donut Chart)

This visualization shows the **Top 10 vendors' share of total purchase dollars**.

- The center value (65.7%) represents cumulative contribution of top vendors.
- Highlights procurement concentration risk.
- Demonstrates Pareto behavior (few vendors drive majority of spend).

Business Insight:
> Top vendors account for ~66% of total purchases → High supplier dependency.

---

## 3️⃣ Top Vendors by Sales (Bar Chart)

Ranks vendors by total sales.

- Identifies revenue-driving suppliers.
- Useful for negotiating contracts and volume-based discounts.
- Shows clear sales hierarchy among suppliers.

---

## 4️⃣ Top Brands by Sales (Bar Chart)

Displays highest performing brands by revenue.

- Highlights customer demand concentration.
- Useful for inventory prioritization.
- Supports brand portfolio optimization.

---

## 5️⃣ Low Performing Vendors (Stock Turnover)

Displays vendors with **Stock Turnover < 1**.

- Indicates slow-moving inventory.
- Signals excess stock or over-procurement.
- Directly linked to working capital inefficiency.

Business Insight:
> Low turnover vendors contribute to higher unsold capital and capital lock-in.

---

## 6️⃣ Low Performing Brands (Scatter Plot)

Plots:
- X-Axis → Total Sales
- Y-Axis → Profit Margin

Brands with:
- Low sales (bottom segment)
- High profit margins (top segment)

are identified as **Target Brands** for potential pricing or promotional strategy adjustments.

This helps answer:
- Should high-margin low-volume brands be promoted?
- Are premium brands under-marketed?

---

# 🔢 DAX Calculations Used

Key computed elements in the dashboard:

- **Unsold Capital**
  ```
  (Total Purchase Quantity - Total Sales Quantity) * Purchase Price
  ```

- **Purchase Contribution %**
  ```
  (Vendor Purchase / Total Purchase) * 100
  ```

- **Low Turnover Filter**
  ```
  Stock Turnover < 1
  ```

- **Target Brand Logic**
  Bottom 15% Sales + Top 85% Profit Margin

---

# 🎨 Design & Interaction

- Blue-Green professional theme
- Dynamic filtering enabled ("Keep All Filters")
- Tooltip-enabled scatter plot for brand-level drill-down
- Consistent metric alignment with Python analysis layer

---

# 🔁 Data Flow

Raw Data → Python Cleaning & KPI Engineering → Processed Tables → Power BI Visualization Layer

This ensures:
- Analytical consistency
- Performance optimization
- Reproducible insights

---

# 🎯 Business Value

This dashboard enables:

- Procurement dependency analysis
- Profitability comparison across vendor tiers
- Inventory risk identification
- Brand pricing strategy evaluation
- Working capital optimization decisions

---

If using sample datasets (due to GitHub size limits), KPI totals may slightly differ from the original full-data dashboard.
