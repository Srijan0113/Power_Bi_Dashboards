# Nepal Economic & External Sector Analysis 🇳🇵

An interactive **Power BI dashboard analyzing major external-sector and economic indicators of Nepal**. The project brings together data on migration, remittance, foreign trade, tourism, and foreign exchange reserves and transforms it into an interactive analytical dashboard.

##  Project Objective

The goal of this project is to understand how major external-sector indicators of Nepal have changed over time and to present those trends in a clear, interactive Power BI dashboard.

The analysis covers:

- Migrant workers
- Remittance
- Imports and exports
- Trade balance
- Tourist arrivals
- Foreign exchange reserves

##  Tools Used

| Tool | Purpose |
|---|---|
| **Microsoft Excel** | Source data |
| **Power Query** | Data cleaning and transformation |
| **Power BI** | Data modeling and dashboard development |
| **DAX** | KPI and analytical measures |

##  Dashboard Pages

### 1. Executive Overview

A high-level summary of the major indicators using KPI cards and trend visuals.

Key metrics include:

- Total Remittance
- Total Exports
- Total Imports
- Trade Balance
- Latest FX Reserve
- Total Tourist Arrivals

### 2. Migration & Remittance

This page focuses on the relationship and trends between migration and remittance.

Visuals include:

- Migrant Workers Trend
- Remittance Trend
- Migrant Workers vs Remittance
- Remittance YoY Growth
- Migrant Workers by Year

**Data note:** The available remittance series used in this project begins in 2022.

### 3. Trade Analysis

This page analyzes Nepal's foreign trade performance.

Key areas include:

- Total Exports
- Total Imports
- Trade Balance
- Exports Trend
- Imports Trend
- Imports vs Exports
- Annual Trade Balance

### 4. Tourism & FX Reserves

This page focuses on tourism activity and foreign exchange reserves.

Key areas include:

- Total Tourist Arrivals
- Latest FX Reserve
- Tourist Arrivals Trend
- Annual Tourist Arrivals
- Foreign Exchange Reserve Trend

##  Data Cleaning & Transformation

The datasets were prepared using **Power Query** before analysis in Power BI.

Major transformation work included:

- Removing unnecessary rows and columns
- Cleaning and renaming columns
- Handling null and unnecessary values
- Correcting data types
- Reshaping monthly datasets
- Creating usable date fields
- Preparing datasets for time-series analysis
- Creating a common DateTable for consistent filtering
- Preparing data for DAX-based calculations

##  Data Model

A dedicated **DateTable** is used as the common date dimension for the dashboard.

This supports:

- Year and month analysis
- Date filtering
- Time-series visuals
- Year-over-year calculations
- Consistent date-based analysis across datasets

##  Key DAX Measures

The dashboard uses DAX measures for calculations including:

- Total Migrant Workers
- Total Remittance
- Total Imports
- Total Exports
- Trade Balance
- Total Tourist Arrivals
- Latest FX Reserve
- Remittance YoY Growth

##  Visualizations

The dashboard uses:

- KPI Cards
- Line Charts
- Clustered Column Charts
- Combo Charts
- Slicers

The visuals are designed to provide both an executive overview and more detailed trend analysis.

## 🖼️ Dashboard Preview

### Executive Overview

![Executive Overview](/images/Project2_Page1.png)

### Migration & Remittance

![Migration & Remittance](/images/Project2_Page2.png)

### Data Model

![Data Model](/images/Project_2_Model_view.png)

---

## 🗂️ Repository Structure

```text
Power-Bi/
│
├── DAX/
│
├── Power Query/
│
├── images/
│   └── Project_2_Model_view.png
│
├── Project_1/
│
├── Project_2/
│   ├── Nepal Economic and External Sector Analysis.pbix
│   ├── Nepal Economic and External Sector Analysis.pdf
│   ├── README.md
└── README.md
```

##  Data Sources

The datasets used in this project were obtained primarily from the **Nepal Rastra Bank (NRB) Database on the Nepalese Economy – External Sector**.

The NRB External Sector database provides data related to:

- Balance of Payments
- Remittance
- Foreign Exchange Reserves
- Foreign Trade
- Migrant Workers
- Tourist Arrivals

### Nepal Rastra Bank

**Database on the Nepalese Economy – External Sector**

https://www.nrb.org.np/database-on-nepalese-economy/external-sector/

**Database on the Nepalese Economy**

https://www.nrb.org.np/database-on-nepalese-economy/

### Nepal Tourism Board

Tourist arrival data and tourism statistics are also available from the Nepal Tourism Board.

**Nepal Tourism Board – Tourist Arrivals**

https://trade.ntb.gov.np/aboutus/tourist-arrivals/

**Nepal Tourism Statistics**

https://trade.ntb.gov.np/downloads-cat/nepal-tourism-statistics

---

##  Key Analytical Questions

The dashboard helps explore questions such as:

- How has the number of migrant workers changed over time?
- How has remittance changed over the available period?
- How do migrant-worker trends compare with remittance trends?
- How have Nepal's imports and exports changed?
- How has the trade balance evolved?
- How have tourist arrivals changed over time?
- How have foreign exchange reserves changed over time?

---

##  Data Limitations

- Different datasets cover different time periods.
- The remittance data used in the dashboard begins in 2022.
- The latest year may contain partial data depending on the source dataset.
- The available Balance of Payments/remittance data does not provide country-wise remittance values.
- Country-wise migrant-worker data and overall remittance data are therefore treated as separate analyses.

---

##  Future Improvements

Possible future enhancements include:

- Country-wise migrant-worker analysis
- More detailed trade-category analysis
- Additional tourism segmentation
- Automated data refresh
- More advanced DAX time-intelligence measures
- Additional Nepal economic indicators

---

## 👤\ Author

**Srijan Poudel**


##  Project Purpose

This project was developed as a portfolio data analytics project to demonstrate practical skills in:

**Data Cleaning → Data Transformation → Data Modeling → DAX → Power BI Visualization → Dashboard Development**