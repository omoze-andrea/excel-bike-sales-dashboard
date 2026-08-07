# Bike Sales Performance & Customer Demographics Dashboard

## Project Overview
This project analyzes customer demographic data—including income levels, age brackets, commute distances, education, and marital status—to evaluate key drivers behind bike purchases. Built in Microsoft Excel, the final deliverable features an interactive dashboard with connected slicers for dynamic filtering.

## Dashboard Preview
![Bike Sales Dashboard](./bike_sales_dashboard.gif)

## Data Cleaning & Transformation Pipeline
Before constructing the dashboard, the raw dataset underwent data cleaning and preparation in Excel:
1. **Duplicate Removal:** Removed duplicate rows to prevent skewed aggregations.
2. **Standardization:** Normalized abbreviations across columns (e.g., converted `M`/`S` to `Married`/`Single` and `M`/`F` to `Male`/`Female`).
3. **Currency Formatting:** Formatted income fields into standard currency with thousand separators and zero decimal places.
4. **Feature Engineering (Age Grouping):** Binned continuous ages into categorical cohorts (`Adolescent`, `Middle Age`, `Old`) using nested `IF` logic:
   `=IF(L2>54, "Old", IF(L2>=31, "Middle Age", IF(L2<31, "Adolescent", "Invalid")))`

##  Key Insights & Findings
* **Income Level:** Higher-income individuals show a significantly higher conversion rate for purchasing bikes across both genders.
* **Target Demographic:** The **Middle Age** cohort (ages 31–54) represents the primary buying audience.
* **Commute Sensitivity:** Purchase rates peak among customers with short commutes (0–1 miles) and drop off significantly past 5 miles.

## 📁Repository Structure
* `Excel Project Dataset.xlsx` — Full interactive workbook (Data, Pivot Tables, Dashboard).
* `bike_sales_dashboard.gif` — Animated preview of the interactive dashboard layout.
