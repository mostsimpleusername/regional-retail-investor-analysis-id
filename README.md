# Indonesia Retail Investor Dashboard (2020–2025)

This project analyzes the growth and regional distribution of retail investors in Indonesia from 2020 to 2025, using publicly available data from KSEI, OJK, and BPS.  
The goal is to understand how regional socioeconomic and digital factors relate to retail investor participation in the Indonesian capital market.

The final output of this project is an interactive dashboard built with Looker Studio.

---

## 📊 Research Focus

**Main Question:**
How does retail investor participation vary across regions in Indonesia, and how is it associated with population size, internet penetration, and economic conditions?

**Unit of Analysis:**
- Region (6 major regions in Indonesia)
- Year (2020–2025, year-end snapshots)

---

## 🗂 Data Sources

All data used in this project are **aggregated, public, and non-personal**.

### 1. Retail Investor Data
- Source: KSEI (Kustodian Sentral Efek Indonesia)
- Data: Number of Single Investor Identification (SID)
- Frequency: Monthly publications
- Processing choice: **Year-end (December) snapshots** to avoid redundancy and ensure consistency

### 2. Population Data
- Source: BPS (Statistics Indonesia)
- Data: Population by region and year

### 3. Internet Penetration
- Source: BPS / ICT Statistics
- Data: Percentage of population with internet access by region

### 4. Economic Indicators
- Source: BPS
- Data: GRDP / GDP per capita by region

---

## 🧹 Data Processing

Data processing is done using **Python (pandas)**.

Key steps:
1. Extract relevant tables from PDF/Excel sources
2. Standardize column names and region labels
3. Aggregate monthly investor data into yearly (December) snapshots
4. Merge all datasets into a single master table
5. Create derived metrics for analysis

---

## 🧾 Final Dataset Structure

Each row represents **one region in one year**.

| Column Name | Description |
|------------|------------|
| region | Indonesian region (6 regions) |
| year | Year (2020–2025) |
| investor_accounts | Number of retail investor accounts (SID) |
| population | Total population |
| internet_penetration | Percentage of internet users |
| gdp_per_capita | Regional GDP per capita |
| investors_per_1000 | Investors per 1,000 population |
| investor_growth_yoy | Year-over-year investor growth rate |

This long-format structure is optimized for BI tools and time-series analysis.

---

## 📈 Dashboard

The cleaned dataset is visualized using **Looker Studio**.

Dashboard features:
- Geographic distribution of retail investors
- Investor density normalized by population
- Year-over-year growth trends
- Correlation between investor participation and internet penetration / income
- Region-level comparison with interactive filters

---

## 🛠 Tools Used

- Python (pandas)
- Google Sheets
- Looker Studio
- Excel / PDF extraction tools (for raw data)

---

## ⚠️ Limitations

- Analysis is conducted at the **regional level**, not province level, due to data availability.
- Investor data reflects registered accounts, not active trading behavior.
- Correlation does not imply causation.

---

## 📌 Notes

This project is intended for academic and educational purposes.  
All data sources are cited and reproducible.

