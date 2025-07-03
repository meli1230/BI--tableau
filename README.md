# Comparative Analysis with the use of Tableau

This project analyzes the economic performance of companies in the **IT** and **Insurance** sectors located in **Cluj-Napoca, Turda, and Dej** (Romania) during the period **2018–2021**, using **Tableau Prep** for data preprocessing and **Tableau Desktop** for interactive dashboards and visual analytics.

## Repository Contents

- `Tableau Prep.tfl` – Tableau Prep flow file used for importing, cleaning, filtering, and merging raw data.
- `Tableau Desktop.twb` – Tableau workbook containing all charts, dashboards, and visual analyses built on the processed dataset.

## Project Overview

Amid rapid digitalization and the economic fluctuations caused by the COVID-19 pandemic, this project explores:

- Average profit and revenue comparison between IT and Insurance companies
- Financial efficiency and operational cost analysis
- Clustering firms based on revenue and employee count
- Geographic distribution of businesses
- Stability of sectors over time

## Data Preparation with Tableau Prep

- Raw data was sourced from Romania’s [data.gov.ro](https://data.gov.ro), particularly from the Ministry of Public Finance datasets (long, short, IFRS reports).
- Data from 4 years (2018–2021) was loaded and unified using `Union`.
- A firm identification dataset (`3firme_neradiate_cu_sediu_2023-01-07.csv`) was joined using the common `CUI` field.
- Null values and irrelevant entries (wrong location/sector) were filtered.
- Firms were filtered by:
  - CAEN codes: 620x, 631x (IT); 65xx, 66xx (Insurance)
  - Location: Cluj-Napoca, Turda, and Dej
- Unnecessary columns were removed, and indicator names (e.g., I13 → Net Turnover) were renamed.

Final indicators included:

- Total Revenue
- Total Expenses
- Gross and Net Profit/Loss
- Number of Employees

## Visualizations with Tableau Desktop

The contents in Tableau Desktop answer the following questions:

- Which sector is more profitable on average?
- How do revenue trends evolve per domain?
- What types of companies exist in each domain (via clusters)?
- Where are companies geographically concentrated?
- Which sector has higher average operational costs?
- How efficiently does each sector turn revenue into profit?

## Technologies Used

- Tableau Prep
- Tableau Desktop
- Public data from [data.gov.ro](https://data.gov.ro)

