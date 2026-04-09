# 📊 Retail Sales Analytics Dashboard — Power BI

A 3-page interactive Power BI dashboard built for NovaMart — a fictional retail company — analysing one full year of sales transactions across customers, products, and salespersons.

---

## ✨ Key Features

- **Executive Summary** — Total Revenue: $413K, Total Orders: 300, Average Order Value: $1K, Gross Profit Margin: 32%. Revenue by Month line chart and Revenue by Category donut chart with an interactive Region Slicer
- **Sales Performance** — Salesperson leaderboard (Emma Brown leads at $103K), Revenue by Customer Segment pie chart (Wholesale at 33.84%), and Top 10 Customers bar chart
- **Product Insights** — Full product revenue table with Gross Profit per SKU and a Margin Scatter Chart (Revenue vs Gross Profit by category). Monitor leads Electronics at ₹60,992 revenue

---

## 🔍 Key Insights

- **Electronics dominates** at $214.47K — over 50% of total revenue
- **June was the peak month** with ~$58K in revenue
- **Emma Brown** topped the salesperson table with $103K across 61 orders
- **Wholesale segment** leads all customer segments at 33.84%
- **Monitor** is the highest-grossing product with ₹60,992 revenue and ₹28,646 gross profit
- **Customer 47** is the top buyer at $30K

---

## 🧰 Skills Used

`Power Query` · `Star Schema Modelling` · `DAX Measures` · `KPI Cards` · `Slicers` · `Scatter Chart` · `Top N Filters` · `Pie Chart` · `Line Chart` · `Multi-page Report Design`

---

## 📁 Data Model

| Table | Type | Rows |
|---|---|---|
| `FactSales` | Fact | 300 |
| `DimCustomers` | Dimension | 50 |
| `DimProducts` | Dimension | 16 |
| `DimSalespersons` | Dimension | 5 |
| `_Measures` | Measures Table | — |

---

## 🛠 Requirements

- Power BI Desktop (latest version)
- Dataset: `RetailSalesData.xlsx` — Sales, Customers, Products, Salespersons
