# 🌍 Global Government Budget Dashboard

An interactive Excel dashboard for exploring **90 years of government spending** (1936–2026) across **45 countries**, broken down into 9 spending categories (Defense, Education, Health, Infrastructure, Social Welfare, and more).

![Excel](https://img.shields.io/badge/Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

---

## 📊 What's inside

| File | Description |
|---|---|
| `Global_Budget_Dashboard.xlsx` | The interactive dashboard workbook (see below) |

### Workbook structure

| Sheet | Purpose |
|---|---|
| **Dashboard** | The interactive dashboard — start here |
| **Master_Global_Budgets_Historica** | Raw source data (3,654 rows: country × year × category) |
| **Analysis** | Summary statistics for every numeric column |
| `Lists` *(hidden)* | Dropdown source lists (countries, years) |
| `Data_Calc` *(hidden)* | Formula engine that powers the dashboard's KPIs and charts |

## ✨ Dashboard features

- **Country & Year selectors** — two dropdowns drive every chart and metric on the page.
- **KPI cards** — total budget, year-over-year change, top spending category, and global rank for the current selection.
- **Category breakdown** — pie chart of the 9 spending categories for the selected country/year.
- **Budget trend** — line chart of total budget over time (1936–2026) for the selected country.
- **Top 10 countries** — bar chart ranking all 45 countries by total budget for the selected year.
- **Global overview** — world total budget trend and the global average category mix, independent of the country selector.

Everything is formula-driven (`SUMIFS`, `AVERAGEIFS`, `RANK`, `INDEX`/`MATCH`) — change the dropdowns and the whole dashboard recalculates instantly. No macros, no VBA.

## 🗂 Data dictionary

Each row in `Master_Global_Budgets_Historica` represents one country in one year, with:

- **Percentage columns** (`*_Percentage`) — share of that year's total budget spent on each category.
- **Amount columns** (`*_Amount_Billions_USD`) — absolute spend in billions of USD.
- **`Total_Budget_Billions_USD`** — total government budget for that country/year.

Categories covered: Defense, Education, Health, Interest Payments, Infrastructure, Agriculture, State Transfers, Social Welfare, Administration & Others.

## 🚀 Getting started

1. Download `Global_Budget_Dashboard.xlsx` and open it in Excel (or LibreOffice Calc).
2. Go to the **Dashboard** tab.
3. Use the **Select Country** and **Select Year** dropdowns in the control panel to explore.

> Excel Online and Google Sheets have partial chart-rendering support — for full fidelity, open the file in desktop Excel or LibreOffice Calc.

## 🛠 Built with

- Python (`openpyxl`) for workbook generation
- LibreOffice for formula recalculation/validation

## 📄 License

MIT — feel free to fork, adapt, and reuse for your own datasets.
