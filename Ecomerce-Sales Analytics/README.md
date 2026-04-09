# 📊 E-Commerce Sales Performance & Customer Intelligence Dashboard
### Powered by Microsoft Power BI Desktop

---

## 🏢 Project Overview

| Field | Details |
|---|---|
| **Organization** | GlobalMart Online Retail Pvt. Ltd. *(Simulated)* |
| **Domain** | E-Commerce & Retail Analytics |
| **Dataset** | Brazilian E-Commerce Public Dataset by Olist (Kaggle) |
| **Tool** | Microsoft Power BI Desktop |
| **Difficulty** | Advanced / Industry Grade |

This is an end-to-end Business Intelligence project that transforms raw multi-table e-commerce data into an interactive, executive-ready Power BI dashboard. It covers the full analytics pipeline — from data ingestion and cleaning to data modeling, DAX measures, and multi-page visualizations.

---

## 📁 Dashboard Pages

| Page | Description |
|---|---|
| 🏠 Executive Summary | KPI Cards, Monthly Revenue Trend, Category Performance, Map Visual |
| 📈 Sales Analysis | YOY Revenue Chart, Waterfall Chart, Product Category Matrix, Top 10 Products |
| 🚚 Delivery & Operations | Delivery Status Donut, State-wise Map, Late Delivery Trend, Actual vs Estimated Days |
| 👥 Customer & Seller Intelligence | Customer Map, Top 10 Sellers, Review Score Distribution, Seller Performance Matrix |
| 🔍 Drill Through | Order-level detail, Customer info, Seller info, Payment breakdown |
| ℹ️ Tool Tip (Hidden) | Compact KPI summary shown as tooltip on hover |

---

## 📌 Key KPIs

- **Total Revenue:** ₹14.03M
- **Total Orders:** 96K
- **Average Order Value:** ₹145.44
- **Average Review Score:** 4.09 / 5
- **On-Time / Early Delivery Rate:** 91.89%
- **Late Delivery Rate:** 8.11%

---

## 🗂️ Dataset

- **Source:** [Brazilian E-Commerce Public Dataset by Olist — Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- **License:** CC BY-NC-SA 4.0 (Open for Educational Use)
- **Volume:** ~100,000 Orders | 9 Interrelated CSV Files

### Dataset Tables

| File | Type | Description |
|---|---|---|
| `olist_orders_dataset.csv` | Fact | Order ID, Status, Purchase Timestamp, Delivery Dates |
| `olist_order_items_dataset.csv` | Fact | Product ID, Seller ID, Price, Freight Value |
| `olist_order_payments_dataset.csv` | Fact | Payment Type, Installments, Payment Value |
| `olist_order_reviews_dataset.csv` | Fact | Review Score, Review Text, Comment Date |
| `olist_customers_dataset.csv` | Dimension | Customer ID, City, State, Zip Code |
| `olist_sellers_dataset.csv` | Dimension | Seller ID, City, State, Zip Code |
| `olist_products_dataset.csv` | Dimension | Product ID, Category Name, Weight, Dimensions |
| `olist_geolocation_dataset.csv` | Lookup | Zip Code, Latitude, Longitude |
| `product_category_name_translation.csv` | Lookup | Portuguese → English Category Names |

---

## 🛠️ Technical Implementation

### Data Cleaning & Power Query
- Removed duplicate rows on primary key columns
- Handled null values in delivery date columns with conditional flags
- Corrected data types for all date/time columns
- Created custom columns: `Delivery_Status`, `Delivery_Days`
- Merged `CategoryTranslation` into Products for English category names
- Built a dedicated **Date Dimension Table** in Power Query

### Data Modeling
- Implemented a **Star Schema** with 2 Fact tables and 5 Dimension tables
- Properly defined relationships with correct cardinality (Many-to-One)
- No circular dependencies; foreign key columns hidden from Report View

### DAX Measures
- **Core:** Total Revenue, Total Orders, AOV, Avg Review Score, Late Delivery %
- **Time Intelligence:** YTD, MTD, SPLY, YOY Growth %, MOM Growth %, Running Total
- **Advanced:** RANKX for Top N, Category % Contribution, Dynamic Titles, What-If Scenario

### Advanced Power BI Features
- ✅ Bookmarks (Default View, Year 2018 Filter, Late Deliveries Only)
- ✅ Page Navigation Buttons
- ✅ Drill-Through Page
- ✅ Custom Tooltip Page
- ✅ Synchronized Slicers across pages
- ✅ What-If Parameter (Revenue Growth Scenario 0–50%)
- ✅ Field Parameters for dynamic Y-axis switching
- ✅ Custom JSON Theme

---

## 🎨 Color Theme

| Role | Color |
|---|---|
| Primary (Headers, Nav) | `#1F3864` Dark Navy |
| Secondary (Charts) | `#2E75B6` Corporate Blue |
| Accent (KPI Values) | `#C9A800` Gold |
| Background | `#F8F9FA` Off-White |
| Alert / Late Delivery | `#C0392B` Red |
| Success / On-Time | `#27AE60` Green |

---

## 📊 Key Business Insights

1. **Health & Beauty** is the top revenue-generating category at ₹1.3M.
2. **São Paulo (SP)** dominates both seller activity and customer orders across all years.
3. Late delivery rate has been **steadily increasing** from 2016 to 2018 — an operational red flag.
4. **Credit card** is the dominant payment method, accounting for **79%** of total revenue.
5. **watches_gifts** has the highest Average Order Value (AOV) at ₹223, indicating a premium buyer segment.
6. Revenue shows a strong peak in **March and November**, suggesting seasonal demand patterns.
7. Top seller from Lauro De Freitas (BA) generated ₹2.14L with only 348 orders — high per-order value.
8. **bed_bath_table** leads in total order volume (9,167 orders) but has a lower AOV of ₹115.
9. Review scores are highly skewed — **57K customers rated 5/5**, but 11K gave a 1/5 rating.
10. 2018 contributed the highest annual revenue at ₹76.87L, nearly doubling 2017's figure.

---

## ⚙️ How to Run

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
2. Extract all 9 CSV files into a local folder (e.g., `C:\PowerBI_Project\Olist_Data\`)
3. Open the `.pbix` file in **Microsoft Power BI Desktop** (latest version)
4. Go to **Transform Data > Data Source Settings** and update the folder path to your local directory
5. Click **Refresh** to reload all data
6. Explore the dashboard using the navigation buttons on each page

---

## 📚 Resources

- [DAX Guide](https://dax.guide)
- [SQLBI DAX Patterns](https://www.daxpatterns.com)
- [Microsoft Learn — Power BI](https://learn.microsoft.com/en-us/power-bi/)
- [Olist Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
- [Power BI Community Forum](https://community.powerbi.com)


---

> *"Data is not just numbers — it is the voice of your business. Build dashboards that tell stories."*
