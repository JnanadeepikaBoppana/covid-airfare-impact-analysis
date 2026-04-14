# covid-airfare-impact-analysis
Analysis of COVID-19's impact on U.S. domestic airfare prices (Q4 2019 – Q4 2020) using Tableau

COVID-19 Impact on U.S. Domestic Airfare Prices

Course: Data Visualization | Master of Science in Business Analytics
Tool: Tableau | Data Source: Bureau of Transportation Statistics (BTS)
Period Analyzed: Q4 2019 – Q4 2020


Project Overview
This project analyzes how the COVID-19 pandemic affected domestic airline fares across the United States. Using quarterly airfare data from the Bureau of Transportation Statistics (BTS) combined with state-level COVID-19 case data, the project uncovers the relationship between rising case counts and falling airfare prices across 5 quarters.
The analysis covers the period just before COVID hit (Q4 2019) through the end of 2020, capturing the full initial impact of the pandemic on the U.S. airline industry.

Key Findings
QuarterAvg FareCOVID 7-Day Avg CasesQ4 2019$391.9087 (Pre-COVID baseline)Q1 2020$367.70137 (Early spread)Q2 2020$277.53582 (Peak lockdown)Q3 2020$269.21413 (Partial reopening)Q4 2020$296.34498 (Second wave)

29.2% fare drop from Q4 2019 to Q2 2020 — the steepest single decline, coinciding with peak lockdowns
Negative correlation of -0.625 between COVID-19 case counts and airfare prices — as cases rose, fares fell significantly
Fares never recovered to pre-COVID levels in 2020 — by Q4 2020, fares were still 24.4% below Q4 2019
Georgia had the highest fares during peak COVID ($391 avg in Q2 2020), likely due to reduced route competition
Internal Medicine and Emergency specialties drove the highest readmission volumes in associated healthcare data


Tableau Dashboard
The project includes an interactive Tableau Story with 4 visualizations:

Average Flight Fares in U.S. States — Geographic view of fare levels across states by quarter
COVID-19 Cases vs Flight Fares — Dual-axis time series showing the inverse relationship between cases and fares
COVID-19 Quarterly Case Trends — 7-day rolling average of COVID cases across the 5 quarters
Quarterly Heat Map — State-by-quarter heat map showing both COVID case intensity and fare price changes


To view the dashboard: Download COVID_Airfare_Dashboard.twbx and open it in Tableau Desktop or Tableau Public.


Data Sources
FileDescriptiondata/raw/AverageFare_Q4_2019.csvBTS raw airfare data — Q4 2019data/raw/AverageFare_Q1_2020.csvBTS raw airfare data — Q1 2020data/raw/AverageFare_Q2_2020.csvBTS raw airfare data — Q2 2020data/raw/AverageFare_Q3_2020.csvBTS raw airfare data — Q3 2020data/raw/AverageFare_Q4_2020.csvBTS raw airfare data — Q4 2020data/processed/Cleaned_Airfare_2019_2020_FIXED.csvCleaned and combined airfare data across all 5 quartersdata/processed/COVID_Airfare_Analysis_Final.csvFinal dataset — airfare data merged with state-level COVID-19 daily case data
Original BTS Data: BTS Average Domestic Airfare by Origin City
COVID-19 Case Data: State-level daily confirmed cases and 7-day rolling averages

Data Notes

Passenger column in the dataset reflects 2024 passenger volume benchmarks from BTS (used for airport ranking purposes only) — it does not represent actual 2020 quarterly passenger counts and is not used in any analysis or visualization
The enhanced dataset covers 10 U.S. states: CA, FL, GA, IL, MI, NC, NY, OH, PA, TX — states for which both airfare and COVID case data were available and matched
Raw BTS files contain airports ranked by 2024 total domestic passenger volume


Data Preparation

Raw data downloaded from BTS — 5 separate quarterly CSV files
Cleaned and combined in Excel — removed empty rows, standardized column names, merged all quarters into a single file
Enhanced with COVID data — daily state-level COVID-19 case data joined to quarterly airfare data by state
Visualized in Tableau — 4 interactive dashboards compiled into a Tableau Story


Limitations

Analysis is limited to 10 states due to COVID data availability at the time of the project
Airfare data is aggregated at the state level for the COVID analysis; airport-level detail is preserved in the cleaned source file
Passenger volume data from BTS reflects 2024 benchmarks and cannot be used to measure actual 2020 travel demand changes
Data covers Q4 2019 through Q4 2020 only — long-term recovery trends beyond 2020 are not included


Tools Used
ToolPurposeMicrosoft ExcelData cleaning, combining quarterly filesTableau DesktopDashboard creation and visualizationBTS Consumer Airfare ReportPrimary data source

Repository Structure
covid-airfare-impact-analysis/
│
├── README.md
├── data/
│   ├── raw/                        # Original BTS quarterly files
│   │   ├── AverageFare_Q4_2019.csv
│   │   ├── AverageFare_Q1_2020.csv
│   │   ├── AverageFare_Q2_2020.csv
│   │   ├── AverageFare_Q3_2020.csv
│   │   └── AverageFare_Q4_2020.csv
│   └── processed/                  # Cleaned and analysis-ready files
│       ├── Cleaned_Airfare_2019_2020_FIXED.csv
│       └── COVID_Airfare_Analysis_Final.csv
├── dashboard/
│   └── COVID_Airfare_Dashboard.twbx
└── assets/
    └── screenshots/                # Dashboard screenshots (add manually)

How to Run

Download the repository
Open dashboard/COVID_Airfare_Dashboard.twbx in Tableau Desktop or Tableau Public
The workbook is self-contained — no additional data connection setup needed
Navigate through the Story tabs to explore each visualization


Project completed as part of the Data Visualization course — MS Business Analytics
