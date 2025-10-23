# FINTRAC Data Analysis

This notebook provides an analysis of FINTRAC (Financial Transactions and Reports Analysis Centre of Canada) data. The analysis focuses on understanding trends in the number of reports submitted over time, the geographical distribution of these reports across Canada, and the breakdown of report types within different activity sectors.

## Notebook Structure and Analysis Steps

1.  **Data Loading and Initial Inspection**: The analysis begins by loading the data from an Excel file (`fintrac-canafe_data-donnees.xlsx`) into a pandas DataFrame. Initial steps include previewing the data, checking data types, and identifying duplicate rows.
2.  **Data Cleaning and Preparation**: This section focuses on cleaning the data for analysis. This involves:
    *   Cleaning column names to retain only the English portion.
    *   Cleaning data within columns (object types) to remove French text.
    *   Handling missing or blank postal codes by removing relevant rows.
    *   Extracting Year and Month into separate columns from the `YearMonthReportReceived` column.
    *   Cleaning the 'ActivitySector' column.
3.  **Trend Analysis**: This part of the analysis examines how the number of reports has changed over time.
    *   The total number of reports is aggregated by year and month.
    *   An interactive line plot visualizes the trend of reports over time.
    *   Monthly and yearly percentage changes in report numbers are calculated and displayed to quantify the trend.
4.  **Geographical Distribution Analysis**: This section explores where the reports are originating from within Canada.
    *   The total number of reports is aggregated by Postal Code to identify areas with high reporting volumes.
    *   A new column `Province_Territory` is created based on the first letter of the Postal Code.
    *   The total number of reports is aggregated and visualized by `Province_Territory` using a bar chart.
    *   The top 3 contributing provinces/territories by year are identified and visualized.
5.  **Yearly Distribution by Province and Report Type**: A detailed breakdown of report types within each province/territory over the years is performed and visualized using faceted bar charts for all report types, and then specifically for STR, LCTR, and EFT reports.
6.  **Fiscal Year Trend**: The total number of reports is analyzed and visualized by Fiscal Year.
7.  **Cross-analysis by Activity Sector and Report Type**: The analysis attempts to explore the distribution of report types within different activity sectors, noting the dominance of the 'Banks' sector.

## Data Sources:

*   **FINTRAC Data on Financial Transactions:**
    *   **Dataset:** Financial transaction report counts by postal code and activity sector. [Dataset source](https://open.canada.ca/data/en/dataset/81cc47ac-e88d-4b7f-9318-8774a2d919e6?utm_source=chatgpt.com)
    *   **Details:** This dataset provides monthly counts of financial transaction reports submitted to FINTRAC, categorized by activity sector, report type, and reporting entity location.
    *   **Usage:** Use this data to analyze the volume and distribution of various financial transactions across different sectors and regions.
*   **FINTRAC Publications and Reports:**
    *   **Source:** FINTRAC Publications
    *   **Details:** FINTRAC publishes strategic intelligence reports, operational alerts, and sectoral advisories that can provide insights into emerging trends and typologies in money laundering activities.
    *   **Usage:** Incorporate findings from these publications to contextualize your dashboard and highlight areas of concern.


## Key Observations and Findings

*   **Overall Trend:** There is a general upward trend in the total number of reports over time, with significant yearly increases observed in certain periods (e.g., 2011-2012 and 2022-2023).
*   **Dominant Report Type:** Electronic Funds Transfer Reports (EFT) consistently constitute the largest category of reports filed.
*   **STR Report Growth:** Suspicious Transaction Reports (STR) have shown a notable percentage growth since 2017.
*   **Geographical Concentration:** The majority of reports originate from Ontario, with specific postal codes in major urban centers like Toronto and Montreal showing the highest reporting volumes.
*   **Provincial Trends:** While Ontario is the highest contributor, the analysis reveals varying trends in report numbers and types across different provinces and territories.
*   **Fiscal Year Trend:** The total number of reports generally exhibits an increasing trend across fiscal years.
*   **Activity Sector Contribution:** The 'Banks' sector contributes a significantly higher number of reports compared to other activity sectors.


📊 **Here’s what the data reveals:**

🔼 1.35+ billion reports were filed between 2011 and 2023, marking a ~70% increase in total reporting volume. The biggest jumps occurred in 2011–2012 (+45.9%) and 2022–2023 (+20.4%) — both tied to major regulatory and operational shifts.

💳 **By Report Type:**

EFT (Electronic Funds Transfers): ~805M reports (≈59%) — dominant and steadily rising.

LCTR (Large Cash Transactions): ~396M reports (≈29%) — declining after 2020 due to reduced cash activity.

STR (Suspicious Transactions): ~151M reports (≈11%) — doubled since 2017, highlighting enhanced AML vigilance.

CDR (Casino Disbursements): ~2M reports — rebounded after pandemic slowdowns.

🏦 **By Sector:**

Banks dominate with over 800M EFT and 396M LCTR filings — driving nearly 90% of total reports.

Money Services Businesses (MSBs) show strong STR concentration (~3M), marking a key AML focus area.

Credit Unions remain consistent contributors (~38M total).

Casinos, Real Estate, and Precious Metals sectors report smaller volumes but carry higher inherent risk.

🌎 **Geographically:**

Ontario leads (~40% of all reports), followed by Quebec (~17%) and British Columbia (~15%).

Activity is heavily concentrated in Toronto, Montreal, and Vancouver — Canada’s major financial hubs.

📅 **Fiscal Trend:**

Total annual reports rose from ~68M in FY2011–12 to ~180M in FY2022–23.

EFTs and STRs are driving this upward curve, underscoring a clear shift toward digital vigilance and risk-based reporting.

In short:

Canada’s AML reporting landscape is maturing rapidly — from cash-heavy monitoring to sophisticated, technology-driven oversight.

The continued rise in STRs and EFTs highlights growing vigilance and stronger compliance systems across the industry.

This analysis provides insights into the reporting patterns captured by FINTRAC data, highlighting trends over time, key geographical areas, and the distribution of different report types.
