# Indian Crop Production Analysis Dashboard

An interactive Power BI dashboard exploring crop production, cultivated area, and yield trends across Indian states and districts, built on the ICRISAT District Level Database.

## Dataset

- **Source:** ICRISAT District Level Database (District-level agricultural statistics for India)
- **Coverage:** ~311 districts across 20 states, years 1966–2017
- **Scope of this dashboard:** 8 major crops — Rice, Wheat, Maize, Cotton, Sugarcane, Groundnut, Soyabean, Sunflower — selected out of the full ~25-crop dataset to keep the model focused
- Metrics per crop: Area (1000 ha), Production (1000 tons), Yield (Kg per ha)

## What was done

- **Data cleaning (Power Query):** removed empty/junk columns, replaced the dataset's `-1` missing-value sentinel with proper nulls, corrected data types
- **Data reshaping:** unpivoted wide per-crop columns into a normalized long format, then split and re-pivoted into a clean Crop / Area / Production / Yield structure
- **Data modeling:** star schema with a central `Fact_CropProduction` table related to `Dim_Crop` and `Dim_Year` dimension tables
- **DAX measures:** Total Production, Total Area, Avg Yield, District Count, and Year-over-Year Production Growth %
- **Report:** two pages — a national/state overview (KPI cards, production trend line, top-crop bar chart, state map, slicers) and a state-to-district drill-down (drillable column chart, crop × year matrix)

## Tools used

Power BI Desktop, Power Query (M), DAX, Excel (intermediate data prep)

## Notes / limitations

- This dashboard covers a subset of crops (8 of ~25 available) and does not represent the complete ICRISAT dataset.
- Figures shown are drawn directly from the ICRISAT District Level Database as published; no independent verification of the underlying agricultural statistics was performed.
- Built as a personal/resume project to practice Power BI, Power Query, and data modeling — not intended as an authoritative agricultural research or policy tool.

## License / Usage

This project is shared **for educational and portfolio purposes only**. The underlying ICRISAT data belongs to its original publisher (ICRISAT) — please refer to their terms for any reuse of the raw data itself. The dashboard, queries, and code in this project may be freely referenced for learning purposes; no warranty of accuracy or fitness for any particular purpose is provided.
## Overview
<img width="1192" height="667" alt="Overview" src="https://github.com/user-attachments/assets/fb86fd72-f8bf-4f62-b0b3-c2c32df4c4ee" />
## State and District Level Drilldown
<img width="1197" height="668" alt="State and District Drilldown" src="https://github.com/user-attachments/assets/3da9d4a0-da61-49f1-8cdf-86b635ed4c56" />


