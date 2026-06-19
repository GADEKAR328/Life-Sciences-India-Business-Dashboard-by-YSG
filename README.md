<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=7B1D1D&height=200&section=header&text=Business%20Dashboard&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Life%20Sciences%20%7C%20Power%20BI%20%7C%20by%20YSG&descAlignY=58&descSize=20" width="100%"/>

<br/>

# 🧬 Business Dashboard — Life Sciences

### *Transforming Pharma Data into Actionable Insights*

<br/>

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com)
[![DAX](https://img.shields.io/badge/DAX-10%20Measures-7B1D1D?style=for-the-badge&logoColor=white)](https://learn.microsoft.com/en-us/dax/)
[![Dataset](https://img.shields.io/badge/Dataset-1000%20Rows-2ECC71?style=for-the-badge&logoColor=white)](#)
[![Currency](https://img.shields.io/badge/Currency-INR%20₹-orange?style=for-the-badge&logoColor=white)](#)
[![India](https://img.shields.io/badge/Made%20in-India%20🇮🇳-FF9933?style=for-the-badge&logoColor=white)](#)

<br/>

> 💡 *A portfolio-ready, single-page Power BI dashboard covering KPIs, growth trends, regional performance, and product-level insights for the Indian pharmaceutical sector.*

</div>

---

## 📸 Dashboard Preview

<div align="center">

![Dashboard](https://raw.githubusercontent.com/GADEKAR328/Life-Sciences-India-Business-Dashboard-by-YSG/38e7a0e32b3d74beceb63ffc4585ac2c803492d9/Business%20Dashboard%20-%20Life%20Sciences.jpg)

</div>

---

## ⚡ KPI Highlights

<div align="center">

| 💰 Total Revenue | 📈 Total Profit | 📊 Gross Margin | 💊 Units Sold | 🚀 YoY Growth |
|:---:|:---:|:---:|:---:|:---:|
| **₹ 1.36 Bn** | **₹ 950.46 M** | **70.11%** | **251K** | **49.85%** |

</div>

---

## 🗂️ Repository Structure

```
📦 Life-Sciences-India-Business-Dashboard-by-YSG
 ┣ 📊 Business Dashboard - Life Sciences.pbix     ← Power BI file
 ┣ 🖼️  Business Dashboard - Life Sciences.jpg     ← Dashboard screenshot
 ┣ 📄 lifescience_india_dataset.csv               ← 1000 rows · 29 columns
 ┣ 📋 LifeScience_DAX_Formulas_YSG.pdf           ← All 10 DAX measures
 ┗ 📝 README.md                                   ← You are here
```

---

## 📊 Dashboard Visuals at a Glance

```
┌─────────────────────────────────────────────────────────────────┐
│  🏠  Business Dashboard - Life Sciences by YSG      [Year ▼]   │
├──────────┬──────────┬──────────┬──────────┬────────────────────┤
│ 💰 1.36B │ 📈 950M  │ 📊 70%   │ 💊 251K  │    🚀 49.85%       │
│  Revenue │  Profit  │  Margin  │  Units   │    YoY Growth      │
├──────────────────────┬──────────────────────────────────────────┤
│                      │                                          │
│  📉 Monthly Revenue  │  🍩 Revenue by Therapeutic Area          │
│     Line Chart       │     Oncology 42% · Neurology 22%        │
│                      │                                          │
├──────────────────────┼──────────────────────────────────────────┤
│                      │                                          │
│  📊 Revenue by       │  📋 Top Products Table                   │
│     Region Bar Chart │     Product · Revenue · Margin %        │
│                      │                                          │
└──────────────────────┴──────────────────────────────────────────┘
```

| # | Visual | Fields Used |
|---|--------|------------|
| 1 | 🃏 KPI Cards (×5) | Total Revenue · Total Profit · Gross Margin % · Units Sold · YoY Growth % |
| 2 | 📉 Line Chart | Axis: `Month_Name` · Values: `[Total Revenue]` · Legend: `Year` |
| 3 | 🍩 Donut Chart | Legend: `Therapeutic_Area` · Values: `[Total Revenue]` |
| 4 | 📊 Horizontal Bar | Y-Axis: `Region` · X-Axis: `[Total Revenue]` |
| 5 | 📋 Table | `Product_Name` · `[Total Revenue]` · `[Gross Margin %]` |
| 6 | 🔽 Year Slicer | `Year` — filters all visuals |

---

## 🧪 Dataset Overview

> 📁 File: `lifescience_india_dataset.csv` &nbsp;|&nbsp; 🗓️ Period: 2022–2024 &nbsp;|&nbsp; 💹 Currency: INR (₹)

| Column | Type | Description |
|--------|------|-------------|
| `Record_ID` | Text | Unique transaction ID |
| `Sale_Date` | Date | Date of sale |
| `Year / Quarter / Month_Name` | Text | Time dimensions |
| `Therapeutic_Area` | Text | Oncology, Neurology, Diabetes, Cardiology, Respiratory, Infectious Disease |
| `Product_Name` | Text | 12 pharmaceutical products |
| `Region` | Text | Maharashtra, Gujarat, Delhi NCR, Karnataka, Tamil Nadu, etc. |
| `Sales_Channel` | Text | Government Hospital, Retail Pharmacy, Online, Specialty Clinic, Corporate Hospital |
| `Units_Sold` | Number | Quantity sold per transaction |
| `Net_Revenue_INR` | Decimal | Revenue after discount in ₹ |
| `Gross_Profit_INR` | Decimal | Profit after COGS in ₹ |
| `Gross_Margin_Pct` | Decimal | Gross margin percentage |
| `RnD_Spend_INR` | Decimal | Research & development spend in ₹ |
| `Patient_Count` | Number | Number of patients per record |
| `Compliance_Rate_Pct` | Decimal | Medication compliance rate % |

---

## 🧮 DAX Measures — All 10

> ℹ️ All are **Measures** (calculator icon ⚡), not calculated columns. Add via **Home → New Measure**.

### 💰 Revenue & Profit

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

### 🏥 Clinical

```dax
Total Patients = SUM(LifeScience_Sales[Patient_Count])
```

```dax
Compliance Rate % = AVERAGE(LifeScience_Sales[Compliance_Rate_Pct])
```

### 📈 Growth & Spend

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

## 🚀 How to Run This Project

```bash
# Step 1 — Clone the repository
git clone https://github.com/GADEKAR328/Life-Sciences-India-Business-Dashboard-by-YSG.git
```

```
Step 2 — Open Power BI Desktop
         Download free → https://powerbi.microsoft.com/desktop
```

```
Step 3 — Load the dataset
         Home → Get Data → Text/CSV → lifescience_india_dataset.csv
         Table name: LifeScience_Sales
```

```
Step 4 — Add all 10 DAX Measures
         Click LifeScience_Sales in Fields pane
         Home → New Measure → paste formula → Enter
         Repeat for all 10 (they show with ⚡ icon)
```

```
Step 5 — Build visuals as shown in the layout above
         OR open the .pbix file directly
```

---

## 🎨 Color Theme

<div align="center">

| Role | Color | Hex |
|------|-------|-----|
| 🔴 Primary | ![#7B1D1D](https://placehold.co/15x15/7B1D1D/7B1D1D.png) Dark Red | `#7B1D1D` |
| 🟥 Accent | ![#A93226](https://placehold.co/15x15/A93226/A93226.png) Medium Red | `#A93226` |
| 🩷 Card BG | ![#F9EBEA](https://placehold.co/15x15/F9EBEA/F9EBEA.png) Light Pink | `#F9EBEA` |
| ⬜ Background | ![#FFFFFF](https://placehold.co/15x15/FFFFFF/FFFFFF.png) White | `#FFFFFF` |
| ⬛ Text | ![#1A1A1A](https://placehold.co/15x15/1A1A1A/1A1A1A.png) Dark | `#1A1A1A` |

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Formula-7B1D1D?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-Dataset%20Generated-3776AB?style=for-the-badge&logo=python&logoColor=white)
![CSV](https://img.shields.io/badge/CSV-1000%20Rows-2ECC71?style=for-the-badge)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=for-the-badge&logo=github)

</div>

---

## 👤 About the Author

<div align="center">

### YOGESH GADEKAR (YSG)

📍 Maharashtra, India &nbsp;|&nbsp; 📊 Data Analytics Enthusiast &nbsp;|&nbsp; 💡 Power BI Developer

[![GitHub](https://img.shields.io/badge/GitHub-GADEKAR328-181717?style=for-the-badge&logo=github)](https://github.com/GADEKAR328)

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=7B1D1D&height=100&section=footer" width="100%"/>

### ⭐ If this project helped you, please give it a Star!

*Built with ❤️ from Maharashtra, India*

</div>
