# Acme Analytics Regional Sales Analysis
## Project Summary
This project dives into Acme Co.’s 2014–2018 USA sales dataset through:
* **Data Profiling & Cleaning:** Verified schema, handled missing budgets, and corrected data types.
* **Univariate & Bivariate Analysis:** Explored distributions (revenue, margin, unit price), product/channel/region breakdowns, and customer segments.
* **Trend & Seasonality:** Charted monthly and yearly sales patterns, highlighting recurring surges and dips.
* **Outlier Detection:** Identified extreme transactions at both ends of the revenue and unit-price spectra.
* **Correlation & Segmentation:** Assessed relationships between key metrics and clustered customers by revenue vs. profit margin.
## Problem Statement
Analyze Acme Co.’s 2014–2018 sales data to identify key revenue and profit drivers across products, channels, and regions; uncover seasonal trends and outliers; and align performance against budgets. Use these insights to optimize pricing, promotions, and market expansion for sustainable growth and reduced concentration risk.
* **Business Questions**
  - Inconsistent revenue and profit performance across U.S. regions
  - Lack of visibility into seasonal swings, top SKUs and channel profitability
## Objectives
Deliver actionable insights from Acme Co.’s 2014–2018 sales data to:
* Identify top-performing products, channels, and regions driving revenue and profit
* Uncover seasonal trends and anomalies for optimized planning
* Spot pricing and margin risks from outlier transactions
* Inform pricing, promotion, and market-expansion strategies

These findings will guide the design of a Power BI dashboard to support strategic decision-making and sustainable growth.
## Entity Relationship Diagram
```mermaid
erDiagram
    SALES_ORDERS }o--|| CUSTOMERS : places
    SALES_ORDERS }o--|| PRODUCTS : includes
    SALES_ORDERS }o--|| REGIONS : delivers_to
    REGIONS }o--o{ STATE_REGIONS : part_of
    PRODUCTS ||--o{ BUDGETS_2017 : has

    CUSTOMERS {
        int Customer_Index
        string Customer_Names
    }

    PRODUCTS {
        int Index
        string Product_Name
    }

    REGIONS {
        int id
        string name
        string state_code
    }

    SALES_ORDERS {
        string OrderNumber
        date OrderDate
        int Customer_Name_Index
        int Product_Description_Index
        int Delivery_Region_Index
        int Order_Quantity
        float Unit_Price
        float Line_Total
    }

    STATE_REGIONS {
        string State_Code
        string State
        string Region
    }

    BUDGETS_2017 {
        string Product_Name
        float Budget
    }
```
## Project Workflow
* **Define Busines Objective:** Understand the core problem and expected business outcomes.
* **Collect & Consolidate Data:** Gather multi-source sales data and understand schema.
* **Data Loading & Initial Exploration:** Load into Colab/Jupyter Notebook for initial profiling and data understanding using Python.
* **Pre-processing & Cleaning:** Handle nulls, join tables, format dates and normalize columns.
* **Exploratory Data Analysis (EDA):** Visualize trends, compare performance, and extract key insights.
* **Dashboarding & Recommendations:** Build Power BI dashboard and present strategic findings.
## Exploratory Data Analysis
## Key Insights
### Executive Overview & Trends
### Product & Channel Performance
### Geographic & Customer Insights
## Recommendations
