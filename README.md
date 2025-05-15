# 📊 Excel Sales Dashboard – Advanced DAX-Powered Analysis

## 📘 Project Overview
This project presents an interactive, Excel-based sales dashboard built using Power Pivot and DAX measures. It focuses on analyzing sales performance, product effectiveness, customer value, and temporal trends from a retail dataset. By combining robust data modeling with insightful KPIs, the dashboard helps stakeholders make data-driven business decisions.

---

## 🎯 Business Objectives & DAX-Driven Metrics

This dashboard addresses several key business questions:

- 🔢 **How many transactions have been completed?**
- 📦 **What percentage of products are actively driving revenue?**
- 💰 **What is the overall profit margin?**
- 👥 **What is the average age of our customers?**
- 🚫 **How can unsold inventory be minimized?**

### 🧮 Core DAX Measures

| Measure              | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `#Transaction`       | Total number of transactions: `COUNTROWS(FactInternetSales)`                |
| `All Products`       | Total unique products: `COUNTROWS(DimProduct)`                              |
| `Sold Products`      | Distinct sold products: `DISTINCTCOUNT(FactInternetSales[ProductKey])`      |
| `Unsold Products`    | Products with no sales: `[All Products] - [Sold Products]`                  |
| `% Profit Margin`    | Revenue retained as profit: `DIVIDE([Total Profit], [Total Revenue], 0)`    |
| `Average Customer Age` | Mean customer age: `AVERAGE(DimCustomer[Customer Age])`                   |

---

## 📌 Key Business Insights

### 🧾 Transactional Overview
- **Total Transactions:** ~60,398

### 📦 Product Performance
- **All Products:** 606
- **Sold Products:** 158
- **Unsold Products:** 448 (~73.9% unsold rate)

### 💰 Profitability Metrics
- **Total Revenue:** ~$307M
- **Total Profit:** ~$126M
- **Profit Margin:** ~41.12%

### 👥 Customer Demographics
- **Average Customer Age:** (derived using DAX)

### 📈 Sales Trends and Seasonality
- **Peak Months:** January and May
- **Profit Distribution:** 72% of profits occur on weekdays
- **Best Quarters:** Q1 and Q2

### 🎯 Customer Value and Geography
- **Top Customer:** Willie Xu
- **Top Regions by Profit:** Australia, Canada, France

---

## ⚙️ Tools & Techniques

| Tool             | Application                                                                 |
|------------------|-----------------------------------------------------------------------------|
| Microsoft Excel  | Data modeling, slicers, dashboard creation                                   |
| Power Pivot      | Table relationships and efficient querying                                  |
| DAX              | KPI calculation and advanced business logic                                 |
| Pivot Tables     | Dynamic aggregation and visualization                                       |
| Conditional Formatting | Color-coded cues for easy data interpretation                      |

---

## 💡 Business Impact

- 📈 **Product Profitability:** Identify high-margin offerings.
- 🎯 **Customer Targeting:** Spotlight top-value customers.
- 📅 **Seasonal Strategy:** Plan campaigns and inventory wisely.
- 📦 **Inventory Optimization:** Address unsold SKUs proactively.
- 🧬 **Customer Insights:** Inform demographic segmentation and strategy.

---

## 📂 Repository Structure

```
excel-sales-dashboard/
├── README.md
├── 
│   └── measures.dax
├── 
│   └── Sales_Dashboard_Final.xlsx 
├── 
│   └── dashboard_screenshot.png
```

---

## 📜 License

This project is open-source under the MIT License.
