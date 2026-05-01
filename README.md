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
## 📊 Interactive Executive Dashboard & Advanced Visualization

I enhanced this project by designing a dynamic, single-page Executive Dashboard to translate backend data into actionable business insights.

### Key Visualization & Dashboard Features Added:

* **Dynamic KPI Summary Cards:** * Designed clean, high-level metric tiles at the top of the dashboard for **Total Revenue** ($1.78M), **Total Profit** ($439.8K), and **Average Profit Margin** (24.77%).
  * Connected shapes using plain-cell reference bridges to mirror the Pivot Cache dynamically.

* **Interactive Slicers (Cross-Filtering):**
  * Integrated **Category**, **Region**, and **Month Name** slicers.
  * Configured **Report Connections** across multiple Pivot Tables, allowing stakeholders to instantly filter the entire dashboard with a single click.

* **Advanced Chart Formatting & Cleanliness:**
  * **Seasonal Trend Analysis:** Line chart visualizing monthly sales performance from January to December (filtered out blank date records).
  * **Regional Performance:** Cleaned horizontal bar chart isolating key business territories by filtering out "Unknown" data artifacts.
  * **Category Profitability & Customer Behaviour:** Dual-axis and clustered visualizations to show profit margins and buying patterns across weekdays vs. weekends.

### 🛠️ Technical Skills Demonstrated:
* Data visualization design principles (cohesive color themes, layout hierarchy).
* Advanced Pivot Table calculations and Pivot Chart generation.
* Dashboard interactivity via Slicers and connected Pivot Cache.
* Data cleaning directly within visual filters for accurate executive reporting.
## Tools Used
* **Excel (Power Query):** Data Extraction, Transformation, and Feature Engineering.
* **Excel (Pivot Tables & Charts):** Advanced Data Analysis and Visualization.
* **Git/GitHub:** Version control and portfolio documentation.
