# 🏏 Virat Kohli | Batting Performance Analysis Dashboard

> A professional 2-page Power BI dashboard analyzing Virat Kohli's complete cricket career across all formats — ODI, TEST, T20I, and IPL — from 2008 to 2026.

---

## 📌 Project Overview

This dashboard tells the complete career story of Virat Kohli through data. It is designed to provide both a high-level career overview and a deep-dive analysis of his batting performance across formats, oppositions, venues, and ICC tournaments.

Built as a portfolio project to demonstrate real-world **Data Analytics** and **Power BI** skills including data modeling, DAX measures, and data storytelling.

---

## 📊 Dashboard Pages

### Page 1 — Who is Virat Kohli as a Batsman?
A career overview page with key KPIs and format-level comparisons.

| Visual | Description |
|--------|-------------|
| 5 KPI Cards | Total Runs, Total Centuries, Total Matches, Overall Strike Rate, Overall Average |
| Runs by Format | Horizontal bar chart showing ODI dominance |
| Centuries vs Half-Centuries by Format | Stacked bar showing conversion rate |
| Home vs Away vs Neutral | Donut chart showing venue-wise performance split |
| Format Slicer | Dynamic filter — ODI / TEST / T20I / IPL |

---

### Page 2 — How, When & Against Whom Does Kohli Perform?
A deep-dive analysis page focused on patterns and insights.

| Visual | Description |
|--------|-------------|
| 4 KPI Cards | Home Average, Count of Sixes, Chase Average, Best Avg vs Opposition |
| Runs by Year (2008–2026) | Line chart showing career journey, peak years and dips |
| Kohli vs Opposition | Horizontal bar chart sorted by average against each team |
| Format Slicer | Same dynamic filter synced across both pages |

---

## 🗂️ Dataset Structure

The dataset was custom-built with **7 tables**, each designed for a specific analysis angle:

| Sheet | Purpose |
|-------|---------|
| `Career_Summary` | Overall stats by format — used for KPI cards |
| `Yearly_Performance` | Year-wise runs, average, centuries by format |
| `Landmark_Innings` | 14 iconic innings with match details and milestones |
| `vs_Opposition` | Performance breakdown against each opponent |
| `ICC_Tournaments` | Stats across all ICC events from 2011–2025 |
| `Home_Away_Neutral` | Venue-type performance split |
| `Chase_vs_Setting` | Chasing vs Setting analysis across formats |

---

## 🧮 DAX Measures Used

```DAX
Total Runs = SUM(Career_Summary[Total_Runs])

Total Centuries = SUM(Career_Summary[Centuries])

Overall Average = AVERAGE(Career_Summary[Average])

Overall Strike Rate = AVERAGE(Career_Summary[Strike_Rate])

Chase Average =
CALCULATE(
    AVERAGE(Chase_vs_Setting[Average]),
    Chase_vs_Setting[Innings_Type] = "Chasing (2nd Innings)"
)

Home Average =
CALCULATE(
    AVERAGE(Home_Away_Neutral[Average]),
    Home_Away_Neutral[Venue_Type] = "Home"
)

Best Avg vs Opposition =
MAXX(vs_Opposition, vs_Opposition[Average])
```

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|------|-------|
| **Power BI Desktop** | Dashboard design, DAX, data modeling |
| **Microsoft Excel (.xlsx)** | Dataset preparation with 7 structured tables |
| **Python (openpyxl)** | Dataset creation and formatting |
| **DAX** | Custom measures and KPI calculations |

---

## 📁 Files in This Repository

```
📦 Virat-Kohli-PowerBI-Dashboard
 ┣ 📊 Virat_Kohli_PowerBI_Dashboard.pbix     ← Power BI file
 ┣ 📂 Dataset
 ┃ 📗 Virat_Kohli_PowerBI_Dataset.xlsx     ← Excel dataset (7 sheets)
 ┗ 📄 README.md
```

---

## 🔍 Key Insights from the Dashboard

- **ODI is Kohli's strongest format** — 14,797 runs with an average of 63.5, the highest among all formats
- **Chase Master** — His chasing average (80.2) is significantly higher than his setting average (50.6) in ODIs
- **Peak years were 2016–2018** — Consistently scoring 1,200+ runs per year across formats
- **Home dominance** — Average of 55.8 in home Tests vs 43.8 away, but still world-class abroad
- **ICC Tournament performer** — Won Player of Tournament at 2014 & 2016 T20 World Cups; scored 765 runs in 2023 ODI WC

---

## 🚀 How to Use This Dashboard

1. Download the `.pbix` file from this repository
2. Open it in **Power BI Desktop** (free download from Microsoft)
3. Use the **Format slicer** (ODI / TEST / T20I / IPL) to filter all visuals dynamically
4. Navigate between **Page 1** (Overview) and **Page 2** (Deep Dive) using the page tabs at the bottom

---


## 🎯 Skills Demonstrated

- ✅ Data Collection & Structuring
- ✅ Data Modeling in Power BI (relationships across 7 tables)
- ✅ DAX Measure Writing
- ✅ Dashboard Design & Layout
- ✅ Data Storytelling & Business Insight Communication
- ✅ KPI Selection based on business questions

---

## 👤 Author

**Tejas Sonawane**
📍 Pune, India
🔗 [LinkedIn — linkedin.com/in/tejas-sonawane09](https://www.linkedin.com/in/tejas-sonawane09/)

---

*If you found this project useful, feel free to ⭐ star the repository!*
