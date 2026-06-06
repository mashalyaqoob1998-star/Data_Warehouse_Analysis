# Data_Analysis_project
Data analysis project using SQL
# SQL Data Analytics Project

This repository contains a complete SQL analytics workflow built around a small data warehouse model. It includes source datasets, a SQL Server database initialization script, exploratory SQL queries, analytical reports, and supporting project documentation.

The project is useful for practicing end-to-end data analysis with SQL: loading dimensional and fact tables, exploring the database, calculating business metrics, analyzing trends, segmenting customers and products, and creating reusable reporting views.

## Project Overview

The database uses a `gold` schema with three main tables:

- `gold.dim_customers` - customer profile and demographic data
- `gold.dim_products` - product, category, cost, and product-line data
- `gold.fact_sales` - sales transactions with order, shipping, quantity, price, and revenue fields

The SQL scripts are organized as a learning path, starting with database setup and ending with analytical reporting views.

## Repository Structure

```text
sql-data-analytics-project/
|-- datasets/
|   |-- DataWarehouseAnalytics.bak
|   `-- flat-files/
|       |-- dim_customers.csv
|       |-- dim_products.csv
|       `-- fact_sales.csv
|-- docs/
|   |-- Project Roadmap.pdf
|   |-- Project Roadmap.png
|   `-- Project_Notes_Sketches.pdf
|-- scripts/
|   |-- 00_init_database.sql
|   |-- 01_database_exploration.sql
|   |-- 02_dimensions_exploration.sql
|   |-- 03_date_range_exploration.sql
|   |-- 04_measures_exploration.sql
|   |-- 05_magnitude_analysis.sql
|   |-- 06_ranking_analysis.sql
|   |-- 07_change_over_time_analysis.sql
|   |-- 08_cumulative_analysis.sql
|   |-- 09_performance_analysis.sql
|   |-- 10_data_segmentation.sql
|   |-- 11_part_to_whole_analysis.sql
|   |-- 12_report_customers.sql
|   `-- 13_report_products.sql
|-- LICENSE
`-- README.md
Requirements
Microsoft SQL Server
SQL Server Management Studio, Azure Data Studio, or another SQL client
Permission to run CREATE DATABASE, CREATE SCHEMA, CREATE TABLE, and BULK INSERT
Getting Started
Clone the repository:
git clone https://github.com/<your-username>/sql-data-analytics-project.git
cd sql-data-analytics-project
Open the project in your SQL client.

Create and load the database using:

scripts/00_init_database.sql
Important: this script drops and recreates the DataWarehouseAnalytics database if it already exists. Do not run it against a database that contains data you need to keep.

Update the BULK INSERT file paths in 00_init_database.sql if needed.
The script uses absolute file paths, so make sure they point to the CSV files on your machine. This repository stores the CSV files in:

datasets/flat-files/
Run the remaining scripts in order, or open individual scripts depending on the analysis you want to practice.
Script Guide
Script	Purpose
00_init_database.sql	Creates the database, schema, tables, and loads data
01_database_exploration.sql	Inspects tables and column metadata
02_dimensions_exploration.sql	Explores customer countries, product categories, subcategories, and product names
03_date_range_exploration.sql	Finds date ranges for orders and customer birthdates
04_measures_exploration.sql	Calculates core business metrics such as sales, quantity, orders, products, and customers
05_magnitude_analysis.sql	Compares metrics by country, gender, category, customer, and other dimensions
06_ranking_analysis.sql	Identifies top and bottom performers using ranking queries and window functions
07_change_over_time_analysis.sql	Analyzes sales performance across dates, months, and years
08_cumulative_analysis.sql	Calculates running totals and cumulative sales trends
09_performance_analysis.sql	Compares yearly product performance against averages and previous results
10_data_segmentation.sql	Segments products by cost and customers by spending behavior
11_part_to_whole_analysis.sql	Calculates category contribution to total sales
12_report_customers.sql	Creates a customer-level reporting view with KPIs and customer segments
13_report_products.sql	Creates a product-level reporting view with KPIs and product segments
Analysis Topics Covered
Database and schema exploration
Dimension analysis
Date range analysis
Business measures and KPIs
Magnitude analysis
Ranking analysis
Change-over-time trends
Cumulative metrics
Performance comparisons
Customer and product segmentation
Part-to-whole analysis
SQL reporting views
Example Business Questions
This project answers questions such as:

What are the total sales, total quantity sold, and total number of orders?
Which products generate the highest revenue?
Which product categories contribute the most to total sales?
How does sales performance change over time?
Which customers generate the most revenue?
How can customers be segmented by spending behavior?
Which products are high performers, mid-range performers, or low performers?
Reporting Views
The final scripts create reusable reporting views:

gold.report_customers
gold.report_products
These views summarize detailed transaction data into analytics-ready outputs that can be used for dashboards, BI tools, or further SQL analysis.


