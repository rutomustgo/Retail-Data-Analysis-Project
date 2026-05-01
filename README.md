# Retail-Data-Analysis-Project
Data cleaning, transformation, and interactive dashboard project using Power Query and Excel.
# Retail Data Analysis & Interactive Dashboard

## Project Overview
This project focuses on extracting, cleaning, transforming, and analyzing raw retail sales data to derive actionable business insights. Using **Excel** and **Power Query**, I built an end-to-end data pipeline to resolve data quality issues and engineered new columns for advanced time-series and profitability analysis.

---

## The ETL & Data Cleaning Pipeline
The raw dataset required comprehensive cleaning to guarantee data integrity and accuracy before visualization. 

### 1. Data Validation & Extraction
* **Null Value Handling:** Filtered out records with missing data in critical transactional fields (`Sales`, `Quantity`, `Profit`) to prevent calculation distortion.
* **Format Standardization:** Removed unwanted characters (such as double quotation marks from text strings) to clean the dataset categories.
* **Data Type Enforcement:** Explicitly set data types for dates, text dimensions, and numerical decimals to protect against downstream math errors.

### 2. Feature Engineering & Calculated Columns
To allow deeper analytical insights, I transformed the raw transactional data by building out the following fields in Power Query:

#### Financial & Operational Metrics:
* `Cost`: Calculated via `[Sales] - [Profit]` to measure complete business overhead.
* `Profit Margin`: Calculated via `[Profit] / [Sales]` to evaluate category performance.
* `Unit Price`: Calculated via `[Sales] / [Quantity]`.

#### Customer & Transactional Segmentation:
* `Order Size`: Grouped orders into `"Bulk Purchase"`, `"Medium Order"`, or `"Small Order"` based on quantity thresholds.
* `Day Type`: Categorized transactions as either `"Weekday"` or `"Weekend"`.
* `Margin Health`: Flagged sales into `"Low Margin"`, `"Normal Margin"`, or `"High Margin"`.
* `Transaction Tier`: Classified total transaction value into Tier 1, Tier 2, and Tier 3.

#### Time Intelligence (For Seasonal Trends):
* Extracted `Day Name`, `Month Name`, `Quarter`, and `Year` to drive period-over-period performance metrics.

---

## Next Phase: Visual Dashboard
With the data fully cleaned and enriched, the next phase of this project involves loading the dataset into Excel to create:
* **Pivot Tables** to summarize key business metrics by Region, Category, and Time.
* **Interactive Slicers** allowing users to filter by segment and date.
* **Dynamic Charts** for executive-level reporting.

---

## Tools Used
* **Excel (Power Query):** Data Extraction, Transformation, and Feature Engineering.
* **Excel (Pivot Tables & Charts):** Advanced Data Analysis and Visualization.
* **Git/GitHub:** Version control and portfolio documentation.
