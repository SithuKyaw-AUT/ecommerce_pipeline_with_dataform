# E-commence Data Pipeline using Dataform
This project is an analytical data pipeline for a fictional e-commerce database. It includes SQL queries for generating key business insights such as total orders, revenue, inventory, and customer information. This project could serve as a foundational data engineering or data analytics project for e-commerce platforms.

# Project Overview
The e-commerce data analytics project is designed to help stakeholders gain insights into business performance through various summary statistics and metrics. This project organizes data related to orders, inventory, products, distribution centers, and users, and provides SQL-based summaries for key performance indicators (KPIs).

# Key Metrics Calculated
The project generates the following key metrics:
- Total Orders: Count of all orders in the system.
- Total Revenue: Total revenue generated from successful orders.
- Total Sales: Total quantity of products sold.
- Total Canceled Orders: Count of all orders that were canceled.
- Total Inventory Items: Sum of all items available in inventory.
- Average Order Value (AOV): Average revenue generated per order.
- Unique Products Sold: Count of distinct products sold.
- Top Products by Quantity Sold: List of top-selling products based on quantity sold.
- Inventory by Distribution Center: Inventory count for each distribution center.

# Database Diagram
The following diagram illustrates the database structure:
![E-commence database schema](https://github.com/SithuKyaw-AUT/ecommence_pipeline_with_dataform/blob/main/ecommence.png)

# Tools
- BigQuery
- Dataform
- Looker Studio

# Project Flow
1. Data Ingestion and Setup
This project uses data from the BigQuery public dataset thelook_ecommerce. The required tables from the thelook_ecommerce dataset are copied to a dedicated dataset, source_data. These tables include users, orders, order_items, products, inventory_items, and distribution_centers. Then, sqlx files for each table in Dataform are defined and set up configurations to import data from source_data for transformation and testing.
2. Data Validation and Quality Testing
Tests in Dataform are defined to ensure data quality by adding assertions for each table. 
3. Data Transformation
Data are transformed by using SQL queries in Dataform and saved in the transformed_data dataset.
4. Data Aggregation for Reporting
SQL queries are written to aggregate data and prepare summarized tables for the key metrics.
5. Export Data for Visualization
The transformed tables and views are exported to BigQuery so they are accessible in Looker Studio. The BigQuery dataset is connected with Looker Studio to create a dashboard.
6. Dashboard Creation in Looker Studio
The E-commence dashboard is created in Looker Studio.

# E-commence Dashboard
![E-commence dashboard](https://github.com/SithuKyaw-AUT/ecommence_pipeline_with_dataform/blob/main/dashboard.png)

# Future Enhancements
To expand on this project, consider implementing the following features:
- Automated ETL Pipelines: Integrate the queries into an ETL tool to automate data extraction, transformation, and loading.
- Time-based Analysis: Calculate KPIs over different time periods (e.g., weekly, monthly).
- Customer Segmentation: Segment users based on purchase history, demographics, or activity.
- Inventory Forecasting: Use historical sales data to predict future inventory needs.


