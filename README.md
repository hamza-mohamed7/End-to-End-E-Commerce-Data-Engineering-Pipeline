# End-to-End-E-Commerce-Data-Engineering-Pipeline

## Project Overview

This project is an end-to-end batch ETL pipeline for an e-commerce system.

The goal of this project is to extract data from MariaDB, store it in HDFS, transform it using PySpark, and load the final analytics tables into Hive.

## Pipeline Architecture

Python
↓
MariaDB
↓
Apache NiFi
↓
HDFS
↓
PySpark
↓
Analytics Tables
↓
Hive

## Technologies Used

- Python
- MariaDB
- Apache NiFi
- HDFS
- PySpark
- Hive
- SQL

## Project Steps

### 1. Data Generation

I used Python to generate e-commerce data and store it in MariaDB.

The database contains:

- Customers
- Products
- Orders
- Order Items
- Payments

### 2. Data Extraction

I used Apache NiFi to extract data from MariaDB and store it in HDFS as a staging zone.

The NiFi flow is:

ExecuteSQL → UpdateAttribute → ConvertRecord → PutHDFS

### 3. Data Transformation

I used PySpark to read the data from HDFS, clean it, and apply business transformations.

I also created a sales dataset and calculated the sales amount.

### 4. Analytics

I created analytics tables for:

- Fact Sales
- Daily Sales
- Customer Sales
- Product Sales

I also calculated different sales metrics such as total sales, total quantity, average order value, and sales by country and category.

### 5. Data Warehouse

I used Hive to create the `ecommerce_dw` database and load the analytics tables.

### 6. Data Validation

Finally, I used Hive SQL queries to validate the loaded data and check the results.

## Project Documentation

The complete project documentation is available in this repository.

## Author

Hamza Mohamed Ali
