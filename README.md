# 📊 Dashboard Preview:

![Dashboard Preview](https://raw.githubusercontent.com/GADEKAR328/Life-Sciences-India-Business-Dashboard-by-YSG/38e7a0e32b3d74beceb63ffc4585ac2c803492d9/Business%20Dashboard%20-%20Life%20Sciences.jpg)

---

## 🏥 Project Overview

A **single-page interactive Power BI dashboard** built for the Life Sciences / Pharmaceutical sector in India. This project covers key business KPIs, revenue trends, regional performance, therapeutic area breakdown, and product-level insights — all on one clean dashboard page.

> **Made by:** Yogesh Gadekar (YSG) | Maharashtra, India
> **Tool:** Microsoft Power BI Desktop
> **Dataset:** 1,000 rows · 29 columns · INR currency · 2022–2024

---

## 🔢 Key KPIs

| KPI | Value |
|-----|-------|
| 💰 Total Revenue | ₹ 1.36 Bn |
| 📈 Total Profit | ₹ 950.46 M |
| 📊 Gross Margin % | 70.11% |
| 💊 Total Units Sold | 251K |
| 📅 YoY Growth % | 49.85% |

---

## 📁 Files in this Repository

| File | Description |
|------|-------------|
| `lifescience_india_dataset.csv` | Dataset with 1,000 rows and 29 columns |
| `Business Dashboard - Life Sciences.pbix` | Power BI dashboard file |
| `Business Dashboard - Life Sciences.jpg` | Dashboard screenshot |
| `LifeScience_DAX_Formulas_YSG.pdf` | All 10 DAX measures with explanation |
| `README.md` | This file |

---

## 📊 Dashboard Visuals

| Visual | Description |
|--------|-------------|
| 5 KPI Cards | Total Revenue, Profit, Margin %, Units, YoY Growth |
| 📉 Line Chart | Monthly Revenue Trend (Jan–Dec) |
| 🍩 Donut Chart | Revenue by Therapeutic Area |
| 📊 Bar Chart | Total Revenue by Region |
| 📋 Table | Product-wise Revenue and Gross Margin % |
| 🔽 Year Slicer | Filter all visuals by Year |

---

## 🧮 DAX Measures (10 Total)

All 10 are **Measures** — added via Home → New Measure in Power BI.

```dax
Total Revenue = SUM(LifeScience_Sales[Net_Revenue_INR])
```
```dax
Total Profit = SUM(LifeScience_Sales[Gross_Profit_INR])
```
```dax
Gross Margin % = DIVIDE([Total Profit], [Total Revenue], 0) * 100
```
```dax
Total Units Sold = SUM(LifeScience_Sales[Units_Sold])
```
```dax
Avg Discount % = AVERAGE(LifeScience_Sales[Discount_Pct]) * 100
```
```dax
Total Patients = SUM(LifeScience_Sales[Patient_Count])
```
```dax
Compliance Rate % = AVERAGE(LifeScience_Sales[Compliance_Rate_Pct])
```
```dax
Total RnD Spend = SUM(LifeScience_Sales[RnD_Spend_INR])
```
```dax
YoY Growth % =
DIVIDE(
  [Total Revenue] - CALCULATE([Total Revenue], DATEADD(LifeScience_Sales[Sale_Date], -1, YEAR)),
  CALCULATE([Total Revenue], DATEADD(LifeScience_Sales[Sale_Date], -1, YEAR)),
  BLANK()
) * 100
```
```dax
Revenue by Region % =
DIVIDE(
  [Total Revenue],
  CALCULATE([Total Revenue], ALL(LifeScience_Sales[Region])),
  0
) * 100
```

---

## 🚀 How to Run

**Step 1** — Clone this repo
```bash
git clone https://github.com/GADEKAR328/Life-Sciences-India-Business-Dashboard-by-YSG.git
```
**Step 2** — Open Power BI Desktop

**Step 3** — Load dataset: Home → Get Data → Text/CSV → `lifescience_india_dataset.csv`

**Step 4** — Add all 10 DAX measures via Home → New Measure

**Step 5** — Build visuals as shown in the screenshot

---

## 🗺️ Layout
