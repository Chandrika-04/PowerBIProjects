# 🚤 WaveX Watercraft — Sales & HR Analytics | Power BI

An end-to-end Power BI project built for WaveX — a Jet Ski and Watercraft manufacturing company — covering the complete BI workflow across two professional reports: a Sales Report and an HR Report. Built from raw multi-source data (Text, Excel, PDF) all the way through to a published online dashboard on Power BI Service.

---

## ✨ Key Features

### 📊 Sales Report
- **4 KPI Cards** — Total Sales: $15M, Total Quantity: $2K, Total Profit: $892K, Avg Profit Per Unit: $524.62
- **Sales by Category** — Bar chart with conditional formatting (Performance leads at $4.6M)
- **Top Distributors** — Clustered column chart comparing Sales vs Cost Price for top 4 distributors (Jane Lewis tops the list)
- **Sales Growth** — Quarter-on-Quarter YoY% column chart (Q4 peaks at 67.88%)
- **Sales & Forecast** — Line chart with 2-year forecast at 99% confidence interval
- **Sales by Country** — Bubble map visual showing global distribution
- **Sales by Payment Method** — Donut chart (PayPal, Bank Transfer, Credit Card, Debit Card each at ~20%)
- **Filter by Year** — Dropdown slicer for interactive year filtering

### 👥 HR Report
- **Total Employees: 130** | **Employee Stay Rate: 53% Near / 47% Far**
- **Average Age by Department** — Area chart across Finance, Sales, Marketing, Manufacturing & R&D
- **Total Employees by Gender** — Pie chart (Male: 53.81%, Female: 46.19%)
- **Employees by Education** — Waterfall chart (Bachelor's: 78, Master's: 52, Total: 130)
- **Job Satisfaction by Experience** — Matrix showing satisfaction scores by years in service
- **Promotion Status** — Funnel chart (Not Done: 117, Due For Promotion: 13)
- **Average Job Satisfaction** — Gauge visual scoring 4 out of 5
- **Q&A Visual** — Interactive natural language query panel

### ☁️ Published on Power BI Service
- Online dashboard created at **app.powerbi.com**
- Exported to **PDF** and **PowerPoint (with live embedded data)**
- Mobile layout customized for responsive viewing
- Dashboard shared with stakeholders via email link



## 🔍 Key Insights

- **Performance category** leads all product lines at $4.6M in sales
- **Q4 recorded the highest YoY growth** at 67.88% — strong seasonal demand
- **Jane Lewis** is the top distributor by sales volume
- **Australia** shows the strongest geographic revenue concentration on the map
- **53% of employees stay close** to the office (within 10 miles)
- **Only 13 employees are due for promotion** out of 130 — a potential retention risk
- **Average Job Satisfaction is 4/5** — a healthy but improvable score
- All 4 payment methods share roughly equal usage at ~20% each

---

## 🧰 Power BI Skills Used

`Power Query` · `Append Queries` · `Merge Queries` · `Unpivot Columns` · `Conditional Columns` · `Custom Columns` · `Split Columns` · `Column from Examples` · `Star Schema Modelling` · `DAX Measures` · `Quick Measures` · `YoY% Change` · `CALCULATE` · `DIVIDE` · `COUNTROWS` · `Forecast (Line Chart)` · `Conditional Formatting` · `Slicer` · `Map Visual` · `Donut Chart` · `Gauge Visual` · `Waterfall Chart` · `Funnel Chart` · `Q&A Visual` · `Matrix` · `Navigation Buttons` · `Power BI Service Publishing` · `Mobile Layout` · `PDF & PPT Export`

---

## 📁 Data Sources

| File | Type | Description |
|---|---|---|
| WaveX Company 2022 Sales Data | Text (.txt) | 2022 sales transactions |
| WaveX Company Data | Excel (.xlsx) | HR, Products, Categories, Payment Methods |
| WaveX Distributor List | PDF | Distributor names, country, city, email |

---

## 📐 DAX Measures Built

| Measure | Formula / Purpose |
|---|---|
| `TotalProfitMeasure` | `SUM(Sales[Profit])` |
| `TotalQuantitySoldMeasure` | `SUM(Sales[QuantitySold])` |
| `Sales($) YoY%` | Quick Measure — Year-over-year % change in sales |
| `TotalEmployees` | `COUNTROWS(HR)` |
| `AverageAgeEmployees` | `AVERAGE(HR[Age])` |
| `AverageJobSatisfaction` | `AVERAGE(HR[JobSatisfaction])` |
| `DistanceNear` | `CALCULATE([TotalEmployees], HR[DistanceStatus]="Stay Close")` |
| `DistanceFar` | `CALCULATE([TotalEmployees], HR[DistanceStatus]="Stay Far")` |
| `%DistanceNear` | `DIVIDE([DistanceNear],[TotalEmployees],0)` |
| `%DistanceFar` | `DIVIDE([DistanceFar],[TotalEmployees],0)` |

---

## 🛠 Requirements

- Microsoft Power BI Desktop (latest version)
- Power BI Service account (Work/School email) for publishing
- Data files: WaveX 2022 Sales Data (.txt) · WaveX Company Data (.xlsx) · Distributor List (.pdf)
