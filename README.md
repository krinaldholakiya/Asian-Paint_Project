<div align="center">

# -- ! Asian Paints Executive Sales Analytics Dashboard ! --
### *Interactive Power BI Report for Revenue, Regions, Products, Dealers & Trends*

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-Measures%20%26%20Time%20Intelligence-E4002B?style=for-the-badge&logo=microsoft&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Power Query](https://img.shields.io/badge/Power%20Query-ETL%20from%20CSV-0078D4?style=for-the-badge&logo=microsoftexcel&logoColor=white)](https://learn.microsoft.com/en-us/power-query/)
[![Data Model](https://img.shields.io/badge/Data%20Model-Star%20Schema-9C27B0?style=for-the-badge&logo=databricks&logoColor=white)](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)


 Video Link-https://drive.google.com/file/d/1fcbFQ2cQ9wT6bU2YL5O3iklOb1y90opG/view?usp=sharing
<br/>

> *"Great businesses are painted one region, one product and one dealer at a time."*

</div>

---

## 📋 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Problem Statement](#-problem-statement)
- [✨ Key Features](#-key-features)
- [🏗️ Project Structure](#️-project-structure)
- [🔄 Project Workflow](#-project-workflow)
- [🧱 Part A — Data Model & DAX](#-part-a--data-model--dax)
- [📊 Part B — Dashboard Pages](#-part-b--dashboard-pages)
- [🛠️ Tech Stack](#️-tech-stack)
- [📈 Results & Insights](#-results--insights)
- [🏆 Advantages](#-advantages)
- [📄 License](#-license)
- [👤 Author](#-author)
- [🙏 Acknowledgements](#-acknowledgements)

---

## 📌 Overview

The **Asian Paints Executive Sales Analytics Dashboard** is a multi-page, interactive **Power BI** report that analyses a paint-industry dataset of **300,000 sales invoices**, **5,000 dealers**, **500 products**, **100,000 customers** and **150 regions** across **5 regions, 28 states** (2022–2025). It demonstrates core business-intelligence concepts such as **star-schema modeling**, **DAX measures**, **target-vs-actual tracking**, **YTD and previous-year comparisons**, and **executive-style visual storytelling**.

This project is designed to:
- Build a clean **star-schema data model** from raw CSV files using Power Query
- Practice writing **DAX measures** for revenue, profit, margin, inventory turnover and dealer KPIs
- Apply **time intelligence** (`SAMEPERIODLASTYEAR`, `DATEADD`, `TOTALYTD`) for YoY and YTD analysis
- Design a consistent, branded **1920 × 1080 dashboard** with navigation, slicers and KPI cards

---

## 🎯 Problem Statement

> **Objective:** Build an interactive executive dashboard that helps sales leadership track revenue and profit, compare regions, products and dealers, and monitor trends against targets.

You are building a reporting solution for a paint manufacturer's sales and strategy teams. The report must let users slice data by **Date, Region, Zone, State, City, Product Category, Sub-Category and Dealer Type**, and answer questions such as *"Which regions and products drive profit?"*, *"Are we meeting targets?"* and *"Which dealers matter most?"*

| 📂 Dashboard Page | 📄 Type | 🔍 Description |
|-------------------|---------|----------------|
| Overview | Executive | Revenue, profit, margin, orders and target achievement at a glance |
| Regional Performance | Geographic | Region → Zone → State → City revenue, contribution and margin |
| Product Analytics | Product | Category and product revenue, profit, margin and inventory turnover |
| Dealer Performance | Channel | Dealer revenue, visits, tiers and dealer-type profitability |
| Trends & Forecasting | Time-based | Current vs previous year, YTD growth and a metric scorecard |

The goal is to demonstrate **end-to-end Power BI skills** — from raw data to a polished, interactive executive report.

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 📑 **5 Report Pages** | Overview, Regional Performance, Product Analytics, Dealer Performance, Trends & Forecasting |
| 🧭 **Page Navigator** | Built-in navigation between all pages |
| 🎛️ **Rich Slicers** | Date, Region, Zone, State, City, Category, Sub-Category and Dealer Type |
| 📐 **Star Schema Model** | 5 dimension tables and 4 fact tables linked by Date, Product, Dealer, Region and Customer keys |
| 🧮 **100+ DAX Measures** | KPIs, PY / PM / PQ comparisons, YTD, growth %, margin and scorecard measures |
| ▲▼ **Dynamic PY Labels** | Text measures like `▲ 5.2%` and `vs PY ₹ 175 Cr` appear under each KPI card |
| 🎨 **Conditional Colors** | `Products Color`, `Turnover Color` and `YTD Profit Color` measures drive green/red indicators |
| 🎯 **Target Tracking** | `FactTargets` enables revenue and profit achievement % |
| 🗺️ **Filled Map** | State-level revenue map with region contribution |
| 📋 **Scorecard Matrix** | Disconnected `Scorecard Rows` table with `SWITCH` measures for actual, target, YoY and achievement |
| 🖥️ **Fit-to-Page Layout** | All pages designed at 1920 × 1080 for presentation-ready viewing |

---

## 🏗️ Project Structure

```
📦 asian-paints-analytics/
│
├── 📄 Asian_Paints.pbix         ← Power BI report (model + 5 report pages)
│
├── 📁 DATASET/                  ← Source CSV files loaded through Power Query
│   ├── DimCustomer.csv
│   ├── DimDate.csv
│   ├── DimDealer.csv
│   ├── DimProduct.csv
│   ├── DimRegion.csv
│   ├── FactDealerVisits.csv
│   ├── FactInventory.csv
│   ├── FactSales.csv
│   ├── FactTargets.csv
│   ├── MarketingCampaigns.csv
│   └── ProductCostMaster.csv
│
└── 📄 README.md                 ← Project documentation
```

> ℹ️ The `.pbix` file points to a local `DATASET` folder. After downloading, update the file path in **Transform data → Data source settings**.

---

## 🔄 Project Workflow

```
Raw CSV Files (11 tables)
          │
          ▼
┌─────────────────────────────┐
│   Power Query (ETL)         │  ← Promote headers, set data types
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   Data Model (Star Schema)  │  ← Relationships on Date, Product,
│                             │    Dealer, Region & Customer keys
└────────────┬────────────────┘
             │
             ▼
┌─────────────────────────────┐
│   DAX Measures              │  ← KPIs, targets, PY / YTD, labels
└────────────┬────────────────┘
             │
     ┌───────┴────────┐
     ▼                ▼
┌─────────────┐   ┌──────────────────┐
│  Visuals    │   │ Slicers + Page   │
│  & KPI Cards│   │ Navigation       │
└──────┬──────┘   └────────┬─────────┘
       │                   │
       ▼                   ▼
┌─────────────────────────────┐
│   5-Page Interactive Report │
└────────────┬────────────────┘
             │
             ▼
   Share / Publish to Power BI Service ✅
```

---

## 🧱 Part A — Data Model & DAX

### 📝 1. What is the Data Model?

The model follows a **star schema**: descriptive **dimension** tables (date, product, dealer, region, customer) surround the transactional **fact** tables (sales, dealer visits, inventory, targets). Slicers on a dimension filter every connected fact table.

---

### 🗺️ 2. Tables — Overview

| Table | Type | Key Columns | Rows (approx.) |
|-------|------|-------------|----------------|
| 🗓️ **DimDate** | Dimension | DateKey, Date, Year, Quarter, Month, MonthName | 1,461 (2022–2025) |
| 📦 **DimProduct** | Dimension | ProductID, ProductName, Category, SubCategory | 500 |
| 🏪 **DimDealer** | Dimension | DealerID, DealerName, DealerType, City, State, Dealer Tier | 5,000 |
| 🌍 **DimRegion** | Dimension | RegionID, Region, Zone, State, City | 150 |
| 👤 **DimCustomer** | Dimension | CustomerID, CustomerName, CustomerType | 100,000 |
| 🧾 **FactSales** | Fact | InvoiceID, DateKey, ProductID, DealerID, CustomerID, RegionID, Quantity, SalesAmount, DiscountAmount, NetSales, CostAmount, ProfitAmount | 300,000 |
| 🚚 **FactDealerVisits** | Fact | VisitID, DateKey, DealerID, SalesRepID, VisitType, RevenueGenerated | 100,000 |
| 🏬 **FactInventory** | Fact | InventoryID, DateKey, ProductID, RegionID, OpeningStock, ClosingStock | 100,000 |
| 🎯 **FactTargets** | Fact | DateKey, RegionID, ProductID, RevenueTarget, ProfitTarget | 30,000 |
| 💵 **ProductCostMaster** | Reference | ProductID, ManufacturingCost, PackagingCost, TransportationCost | 500 |
| 📣 **MarketingCampaigns** | Reference | CampaignID, CampaignName, Budget, Spend | 1,000 |
| 🛠️ **Calendar / Scorecard Rows** | Helper | Date (measure table), Metric (scorecard rows) | — |

**Product categories:** Interior Emulsion · Exterior Emulsion · Putty · Primer · Wood Finish · Waterproofing · Industrial Coating

**Dealer types:** Gold · Silver · Premium · Retail · Distributor | **Visit types:** Sales Visit · Demo · Training · Collection

---

### 🔗 3. Relationships

```
                         DimDate
                            ▲
                            │ DateKey
      ┌──────────────┬──────┴───────┬────────────────┐
      │              │              │                │
  FactSales   FactDealerVisits  FactInventory    FactTargets
   │ │ │ │          │              │ │              │ │
   │ │ │ └─ DimDealer ◄── DealerID ─┘ │              │ │
   │ │ └──── DimCustomer (CustomerID) │              │ │
   │ └────── DimProduct ◄─────── ProductID ──────────┘ │
   └──────── DimRegion  ◄─────── RegionID ─────────────┘

ProductCostMaster ──► DimProduct   (1:1 on ProductID)
```

---

### 🧮 4. Core DAX Measures

**Revenue, Profit & Margin**
```dax
Total Revenue    = SUM(FactSales[NetSales])
Total Revenue Cr = DIVIDE([Total Revenue], 10000000)
Total Profit     = SUM(FactSales[ProfitAmount])
Profit Margin %  = DIVIDE([Total Profit], [Total Revenue])
Total Orders     = DISTINCTCOUNT(FactSales[InvoiceID])
```

**Targets & Achievement**
```dax
Revenue Target     = SUM(FactTargets[RevenueTarget])
Target Achievement % = DIVIDE([Total Revenue], [Revenue Target])
Revenue Contribution % =
DIVIDE([Total Revenue], CALCULATE([Total Revenue], ALLSELECTED(DimRegion[Region])), 0) * 100
```

**Dealer & Inventory KPIs**
```dax
Avg Revenue per Dealer Lakh = DIVIDE(DIVIDE([Total Revenue], [Total Dealers]), 100000)

Avg Visits per Dealer = DIVIDE(DISTINCTCOUNT(FactDealerVisits[VisitID]), [Total Dealers])

Avg Inventory Turnover =
DIVIDE([Units Sold],
       DIVIDE(SUM(FactInventory[OpeningStock]) + SUM(FactInventory[ClosingStock]), 2))
```

**Time Intelligence — PY, YTD & Growth**
```dax
Revenue PY = CALCULATE([Total Revenue], SAMEPERIODLASTYEAR(DimDate[Date]))

Revenue Growth % = DIVIDE([Total Revenue] - [Revenue PY], [Revenue PY])

YTD Revenue Cr = DIVIDE(TOTALYTD([Total Revenue], DimDate[Date]), 10000000)

Revenue Growth Text =
IF([Revenue Growth %] >= 0, "▲ ", "▼ ") & FORMAT(ABS([Revenue Growth %]), "0.0%")
```

**Scorecard (disconnected table + SWITCH)**
```dax
Scorecard Actual =
SWITCH(SELECTEDVALUE('Scorecard Rows'[Metric]),
    "Revenue", [Total Revenue Cr],
    "Profit",  [Total Profit Cr],
    "Orders",  [Total Orders],
    BLANK())
```

**Key Concepts Used:**

| Concept | Detail |
|---------|--------|
| 🔁 `CALCULATE()` | Changes filter context for PY, YTD and contribution measures |
| 🗓️ `SAMEPERIODLASTYEAR()` / `DATEADD()` / `TOTALYTD()` | YoY, previous month/quarter and year-to-date comparisons |
| 🎯 `ALLSELECTED()` | Share-of-total calculations for region and state contribution |
| 🔀 `SWITCH()` + `SELECTEDVALUE()` | One measure that adapts to every row of the scorecard |
| ➗ `DIVIDE()` | Safe division that avoids divide-by-zero errors |
| 🔤 `FORMAT()` | Dynamic "▲▼" labels and conditional hex colors for KPI cards |

---

## 📊 Part B — Dashboard Pages

### 🗺️ 5. Pages — Overview

| # | Page | Main Visuals | Key Measures |
|---|------|--------------|--------------|
| 1️⃣ | **Overview** | KPI cards, revenue-vs-target combo chart, monthly revenue line, category treemap, state map, category table | Total Revenue Cr, Total Profit Cr, Profit Margin %, Total Orders, Target Achievement % |
| 2️⃣ | **Regional Performance** | KPI cards, region & state bar charts, achievement combo chart, filled map, margin matrix | Revenue Contribution %, Achievement %, Profit Margin % |
| 3️⃣ | **Product Analytics** | KPI cards, category donut, revenue/profit bars by product, revenue-profit-quantity scatter, turnover column chart, product table | Total Products, Avg Inventory Turnover, Profit Margin % |
| 4️⃣ | **Dealer Performance** | KPI cards, dealer-city map, top-dealer bar/column charts, tier donut, dealer-type combo chart, visits trend | Total Dealers, Avg Revenue per Dealer, Avg Visits per Dealer |
| 5️⃣ | **Trends & Forecasting** | CY vs PY revenue and profit lines, YTD line, growth line, KPI cards, scorecard matrix | YTD Revenue/Profit Cr, YoY Change, Scorecard Actual / Target / YoY % |

---

### 📈 6. Overview

> Answers: *How is the business performing right now?*

- Revenue, profit, margin, orders and target-achievement cards, each with growth and **vs-PY** labels
- Monthly **Revenue vs Target** combo chart with achievement line
- Revenue by **product category** (treemap) and by **state** (filled map)

---
### 🖼️ 1.Overview

<img src="Assets/Screenshot 2026-11-06 091858.png">


### 🌍 7. Regional Performance

> Answers: *Which regions and states drive revenue and margin?*

- Revenue and **contribution %** by region and by state
- Target achievement by region
- Region → State margin matrix and a state-level filled map

---
### 🖼️ 2.Regional Performance

<img src="Assets/Screenshot 2026-11-06 091912.png">

### 🎨 8. Product Analytics

> Answers: *Which products and categories are winners?*

- Category revenue share (donut) and top products by **revenue** and **profit**
- Revenue vs profit vs quantity **scatter plot**
- Inventory turnover by category and a product-level margin table

---
### 🖼️ 3.Product Analytics


<img src="Assets/Screenshot 2026-11-06 091932.png">

### 🏪 9. Dealer Performance

> Answers: *Which dealers and dealer types matter most?*

- Total dealers, average revenue per dealer and average visits per dealer
- Top dealers by revenue (bar / column) and revenue by city
- Dealer **tier** donut, dealer-type revenue-profit-margin combo chart and monthly **visits** trend

---
### 🖼️ 4. Dealer Performance

<img src="Assets/Screenshot 2026-11-06 091949.png">

### 🔮 10. Trends & Forecasting

> Answers: *How are we trending against last year?*

- **Current Year vs Previous Year** revenue and profit lines by month
- **YTD revenue** with growth % and YoY change cards
- A metric **scorecard** (Revenue, Profit, Margin, Orders, Revenue/Dealer, Inventory Turnover) with actual, target, YoY and achievement

---
### 🖼️ 5.Trends & Forecasting

<img src="Assets/Screenshot 2026-11-06 092006.png">

## 🛠️ Tech Stack

| Tool | Version | Purpose |
|------|---------|---------|
| 📊 **Power BI Desktop** | Latest | Report authoring and visualisation |
| 🧮 **DAX** | Built-in | Measures, KPIs, targets and time intelligence |
| 🔧 **Power Query (M)** | Built-in | Loading CSV files and setting data types |
| 🗃️ **CSV Files** | — | Source data for dimensions and facts |
| 🗺️ **Filled Map / Map** | Built-in | State- and city-level geographic analysis |
| 🖼️ **PNG Icons** | — | Custom KPI and navigation icons inside the report |

---

## 📈 Results & Insights

After exploring the dashboard, the following insights are produced:

- 🧾 **Large Transaction Base** — **300,000 invoices** and about **7.5 million units** sold across **5,000 dealers** and **500 products**
- 💰 **Revenue & Profit** — Net revenue is about **₹702 Cr** with a profit of about **₹228 Cr**, a **profit margin of ~32.5%**
- 📅 **Steady Yearly Revenue** — Net revenue stays close to **₹175 Cr per year** from 2022 to 2025
- 🌍 **Regional Leader** — **West** is the top region (~₹172 Cr), ahead of **Central** and **East** (~₹136 Cr each); **South** is the lowest (~₹126 Cr)
- 🎨 **Top Categories** — **Putty** (~₹116 Cr) and **Interior Emulsion** (~₹114 Cr) lead; **Waterproofing** is the smallest (~₹80 Cr)
- 🏪 **Dealer Network** — Dealers are grouped into five types and five tiers, with visit types covering Sales Visits, Demos, Training and Collection
- 📊 **Scorecard View** — Revenue, profit, margin, orders, revenue per dealer and inventory turnover are tracked against the previous year in one table
- 📈 **YTD Tracking** — YTD revenue and profit are compared to the same period last year with growth labels

---

## 🏆 Advantages

| Advantage | Detail |
|-----------|--------|
| 🎓 **Portfolio Ready** | Covers modeling, DAX, time intelligence, visual design and storytelling in one project |
| 🔄 **Reusability** | Measures follow a repeatable *Value → PY → Growth → Text → Color* pattern |
| 📚 **Educational** | Shows star schema, filter context, `SWITCH` scorecards and conditional formatting |
| 🧭 **Easy Navigation** | Page navigator guides users across five pages |
| 🎛️ **Fully Interactive** | Slicers cross-filter visuals; maps and charts drill into detail |
| 📏 **Scalable** | Handles 300K invoices and 100K visit/inventory rows smoothly |
| 🧪 **Extensible** | Easy to add pages (Marketing ROI, Cost Analysis) using the cost and campaign tables |
| 🛡️ **Safe Calculations** | `DIVIDE()` prevents errors in KPI labels and ratios |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for full details.

```
MIT License — Free to use, modify, and distribute with attribution.
```

---

## 👤 Author

<div align="center">

### Krinal Dholakiya

[![GitHub](https://img.shields.io/badge/GitHub-krinaldholakiya-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/krinaldholakiya)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/krinaldholakiya/)

> *"Every dashboard starts with a question — and the best ones answer it at a glance."*

**🎓 Role:** Data Analyst | Power BI Enthusiast \
**📍 Location:** India\
**🛠️ Skills:** Power BI · DAX · Power Query · Data Modeling · Dashboard Design

</div>

---

## 🙏 Acknowledgements

Special thanks to the following resources and communities that made this project possible:

- 📚 [Microsoft Power BI Docs](https://learn.microsoft.com/en-us/power-bi/) — Official Power BI reference
- 🧮 [DAX Guide](https://dax.guide/) — Complete DAX function reference
- 🔧 [Power Query M Docs](https://learn.microsoft.com/en-us/powerquery-m/) — M language reference
- ⭐ [Star Schema Guidance](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema) — Data modeling best practices
- 📖 [SQLBI](https://www.sqlbi.com/) — In-depth DAX and modeling articles
- 💬 [Power BI Community](https://community.fabric.microsoft.com/) — Problem-solving support
- 🎨 [Flaticon](https://www.flaticon.com/) — Icon inspiration

---

<div align="center">

---

*Made with ❤️ — Last updated: 6 November, 2026*

</div>
