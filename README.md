# Comparative Analysis with the use of Tableau

This project analyzes the economic performance of companies in the **IT** and **Insurance** sectors located in **Cluj-Napoca, Turda, and Dej** (Romania) during the period **2018–2021**, using **Tableau Prep** for data preprocessing and **Tableau Desktop** for interactive dashboards and visual analytics.

## 📁 Repository Contents

- `Tableau Prep.tfl` – Tableau Prep flow file used for importing, cleaning, filtering, and merging raw data.
- `Tableau Desktop.twb` – Tableau workbook containing all charts, dashboards, and visual analyses built on the processed dataset.

## 🔍 Project Overview

Amid rapid digitalization and the economic fluctuations caused by the COVID-19 pandemic, this project explores:

- **Average profit and revenue** comparison between IT and Insurance companies
- **Financial efficiency and operational cost analysis**
- **Clustering firms** based on revenue and employee count
- **Geographic distribution** of businesses
- **Stability of sectors over time**

We chose IT due to its relevance in Cluj-Napoca and compared it with the Insurance sector, which—while smaller—is expected to show financial stability and profitability.

To ensure fair comparison, **averages** were used instead of totals, accounting for the difference in the number of firms across sectors.

## 🧹 Data Preparation with Tableau Prep

- Raw data was sourced from Romania’s [data.gov.ro](https://data.gov.ro), particularly from the Ministry of Public Finance datasets (long, short, IFRS reports).
- Data from 4 years (2018–2021) was loaded and unified using `Union`.
- A firm identification dataset (`3firme_neradiate_cu_sediu_2023-01-07.csv`) was joined using the common `CUI` field.
- Null values and irrelevant entries (wrong location/sector) were filtered.
- Firms were filtered by:
  - **CAEN codes**: 620x, 631x (IT); 65xx, 66xx (Insurance)
  - **Location**: Cluj-Napoca, Turda, and Dej
- Unnecessary columns were removed, and indicator names (e.g., I13 → Net Turnover) were renamed.

Final indicators included:

- Total Revenue
- Total Expenses
- Gross and Net Profit/Loss
- Number of Employees

## 📈 Visualizations with Tableau Desktop

### Key Techniques

- **Calculated fields** to standardize city names for geographic maps
- **Filters** for year, domain, and city
- **Customized markers** for better readability
- **Interactive dashboards** with action filters for dynamic exploration

### Sheets & Dashboards

| Sheet | Description |
|-------|-------------|
| **Sheet 1** | Vertical bar chart: compares average net profit by year and sector |
| **Sheet 2** | Line chart: trends of average revenues with trend lines and moving averages |
| **Sheet 3** | Scatter plot + clustering: firms grouped by revenue & number of employees |
| **Sheet 4** | Map view: aggregated geographic distribution based on total revenue and employees |
| **Sheet 5** | Horizontal bar chart: compares total average expenses by sector |
| **Sheet 6** | Interactive dashboard with action filters (year/domain) |
| **Sheet 7** | Dual-axis chart: average revenue vs gross profit over time |

## 💡 Business Insights

The dashboard answers key questions such as:

- **Which sector is more profitable on average?**
- **How do revenue trends evolve per domain?**
- **What types of companies exist in each domain (via clusters)?**
- **Where are companies geographically concentrated?**
- **Which sector has higher average operational costs?**
- **How efficiently does each sector turn revenue into profit?**

## 🧠 Technologies Used

- Tableau Prep
- Tableau Desktop
- Public data from [data.gov.ro](https://data.gov.ro)

## 👥 Team Roles

| Member               | Role                                    |
|----------------------|------------------------------------------|
| Melisa Marian        | Scrum Master, story writing, structure   |
| Iulia Ana Anca       | Developer – Tableau Prep                 |
| Paula Andreea Moldovan | Developer – Tableau Desktop            |
| Alexandra Nanu       | Presentation design                      |

## 📌 Summary

This project delivers a visual, data-driven comparison of two important sectors—IT and Insurance—highlighting their financial evolution, risk profiles, and strategic differences across three Romanian cities over four years.

The dashboard serves as a decision-support tool for economic analysts, investors, and policymakers.

