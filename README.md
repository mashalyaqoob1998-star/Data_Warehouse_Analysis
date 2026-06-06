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



gold.report_customers
gold.report_products
These views summarize detailed transaction data into analytics-ready outputs that can be used for dashboards, BI tools, or further SQL analysis.


