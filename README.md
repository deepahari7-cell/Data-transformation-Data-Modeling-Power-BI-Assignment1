# Data-transformation-Data-Modeling-Power-BI-Assignment1

Power BI Data Import, Transformation & Modeling Project
🧾 Overview

This project focuses on importing, transforming, and preparing data from multiple CSV files in Power BI using Power Query Editor.
The goal is to clean, format, and merge data for effective visualization and analysis.

All transformations are performed in Power Query Editor before loading the final dataset into Power BI.

📥 1. Import Data

Objective:
Bring all relevant CSV datasets into Power BI for data preparation.

Steps:

Import List of Orders.csv into Power BI.

Go to Home → Get Data → Text/CSV → List of Orders.csv.

Click Transform Data to open it in Power Query Editor.

Import the following additional CSV files into Power Query Editor:

Order Details.csv

Sales Target.csv
(Use the same import method for each.)

Expected Outcome:
All three datasets are now available in Power Query Editor for cleaning and transformation.

🔄 2. Data Transformation

Objective:
Clean and transform data fields to ensure consistency and readiness for modeling.

Tasks and Steps:
a) Restrict Rows

Limit the List of Orders table to only the first 500 rows:

In Power Query, go to Home → Keep Rows → Keep Top Rows → 500.

b) Set Data Types

Change Order Date → Date type.

Change Amount and Target → Fixed Decimal Number.

c) Format Text Columns

Format CustomerName to Proper Case:

Go to Transform → Format → Capitalize Each Word.

d) Create a Merged Column

Merge City and State into a new column Location (format: City, State):

Select both columns → Transform → Merge Columns → Separator: Comma + Space (", ") → New column name: Location.

e) Add a Custom Column – Profit Margin

Create Profit Margin (%) using:

= ([Profit] / [Amount]) * 100


Format this column as a percentage.

f) Add a Conditional Column – Profit Status

Create Profit Status with conditions:

If Profit < 0 → “Loss”

If Profit = 0 → “Break-Even”

If Profit > 0 → “Profit”

(Use Home → Add Column → Conditional Column)

Expected Outcome:
A clean, formatted dataset with meaningful calculated columns for financial analysis.

🔗 3. Merging Data (Joins)

Objective:
Combine related data across multiple tables for analysis.

Steps:

Merge List of Orders and Order Details on Order ID.

Go to Home → Merge Queries → Merge Queries as New.

Select Order ID as the matching column in both tables.

Name the new merged table: Orders Data.

Expected Outcome:
A unified table named Orders Data combining order-level and detail-level information.

⚠️ 4. Handling Missing & Duplicate Data

Objective:
Ensure data accuracy by dealing with null values and duplicates.

Steps:

Identify Missing Values:

Filter columns to check for null or blank entries.

Strategy:

Impute missing numeric values using averages or medians.

Replace missing text fields (e.g., Category) with “Unknown”.

Identify & Remove Duplicates:

Use Home → Remove Rows → Remove Duplicates.

Define duplicates based on Order ID or all columns, depending on context.

Expected Outcome:
A clean dataset free of missing or duplicated records.

🔍 5. Sorting and Filtering Data

Objective:
Enable exploratory analysis through sorting and filtering.

Steps:

Sort Orders by Date (Descending):

Click Order Date → Sort Descending.

Filter by State (e.g., Tamil Nadu):

Use the column filter or the Filter pane to view regional data.

Expected Outcome:
A filtered and sorted dataset that highlights recent orders and specific regional trends.

📈 6. Grouping and Aggregating Data

Objective:
Generate summary tables for performance analysis.

Tasks:
a) Order Details Summary

Duplicate Order Details → Group By using:

Count of Order ID

Average Profit by Category

Total Amount by Sub-Category

b) Sales Target Aggregation

Duplicate Sales Target table → Group By Month (Order Date) → Sum of Target.

Expected Outcome:
Aggregated views providing insights into order volume, profitability, and sales targets over time.

🧮 7. Data Modeling

Objective:
Establish relationships between datasets for dynamic reporting and analysis in Power BI.

Steps:

Create Relationships:

List of Orders ↔ Order Details via Order ID.

Order Details ↔ Sales Target via Category.

Activate Relationships:

Go to Model View → Manage Relationships.

Ensure both relationships are active.

Expected Outcome:
A connected data model allowing seamless cross-table analysis in Power BI reports.
