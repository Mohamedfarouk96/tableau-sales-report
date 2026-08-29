# 📦 Sales Report Dashboard (Tableau)

A Tableau dashboard analyzing order and cost data by category, country, order type, and time — built from an Excel sales dataset.

<!-- Add a screenshot of the dashboard here, e.g.: ![Dashboard Preview](./screenshot-dashboard.png) -->

## 📊 Overview

This dashboard gives a quick view of sales activity to answer questions like:

- What's the total order count and final cost?
- How do orders and final cost break down by product category?
- How are orders distributed by order type?
- Where are customers/orders located geographically (by country)?
- How does total cost trend by order month?

## 🗂️ Data Source

- **Source file:** `Sales_Data.xlsx` (single sheet: `Sheet1`)
- **Connection type:** Excel, extracted into a Tableau **Hyper extract** for fast performance
- **Key fields:** Order Num, Order Date, Order Type, Prod Category, Prod Name, Prod Number, Cust Name, Cust City, Cust Country, Customer Type, sales

No custom calculated fields were needed — the visuals use the raw fields directly (counts, sums, and date parts).

## 📄 Worksheets → Dashboard

`Dashboard 1` combines the following worksheets into a single view:

| Worksheet | Mark Type | Purpose |
|---|---|---|
| Total Order | Text/KPI | Total order count |
| Final Cost | Text/KPI | Total final cost |
| Qnt | Text/KPI | Quantity summary |
| Order By Category | Bar | Orders broken down by product category |
| Fainal Cost By Category | Bar | Final cost broken down by product category |
| Order By Type | Pie | Orders split by order type |
| Order By Country | Map (Latitude/Longitude) | Geographic distribution of orders by country |
| Month Of Order Date | Line | Total cost trend by order month |

*(`Sheet 1`, `Sheet 10`, and `Sheet 11` are exploratory/staging worksheets not used on the final dashboard.)*

## 🛠️ Steps I Used to Build This Project

1. **Connected Tableau to the `Sales_Data.xlsx` Excel file** and loaded `Sheet1` as the data source.
2. **Extracted the data into a Hyper extract** rather than a live connection, for faster performance on the dashboard.
3. **Built individual worksheets** for each metric/breakdown needed: order counts, final cost, quantity, category breakdowns (orders and cost), order type split, geographic distribution, and a monthly cost trend.
4. **Chose the mark type for each worksheet** — bar charts for category comparisons, a pie chart for order type, a map for country-level geography (using Tableau's generated Latitude/Longitude), and a line chart for the monthly trend.
5. **Assembled the worksheets into a single dashboard** (`Dashboard 1`), arranging the KPI worksheets, category charts, the country map, the order-type pie chart, and the monthly trend line into one layout.
6. **Tested filtering and cross-highlighting** across the dashboard's worksheets before finalizing.

## 🧰 Tools & Skills Used

- **Tableau Desktop** — data connection, worksheet design, dashboard assembly
- **Hyper extract** — for performance
- **Tableau's geographic role mapping** — country-level map visualization

## 🚀 How to Use

1. Download `sales_report__2_.twbx` (a packaged Tableau workbook — the data extract is bundled inside, no separate file needed).
2. Open it in **Tableau Desktop** or **Tableau Reader** (free).
3. Explore `Dashboard 1` for the combined view, or open individual worksheets for a closer look at each chart.

## 📁 Files in This Repo

```
├── sales_report__2_.twbx   # Packaged Tableau workbook (includes the data extract)
└── README.md               # This file
```

## 👤 Author

**Mohamed Farouk**
Data Quality Reviewer & Analyst | Building a portfolio in Power BI, Excel, Tableau, and data analytics
[GitHub: Mohamedfarouk96](https://github.com/Mohamedfarouk96)

---

> ⚠️ Note: The build steps above summarize the general workflow based on the workbook's structure (data source, worksheets, and dashboard layout). If any detail doesn't match exactly how you built it, feel free to tweak the wording before publishing.
