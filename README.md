# Retail360 — End-to-End Retail Data Engineering Platform

![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-Data%20Engineering-blue)
![PySpark](https://img.shields.io/badge/PySpark-ETL-orange)
![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-yellow)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-Lakehouse-green)

## 📌 Project Overview

Retail360 is an end-to-end retail data engineering project built using Microsoft Fabric.

The project demonstrates how raw retail data can be ingested, transformed through a Medallion Architecture, modelled for analytics, and consumed through an executive Power BI dashboard.

> **Note:** This project uses synthetic retail data for demonstrating the complete engineering workflow.

---

## 🏗️ Architecture

```text
                Retail Source Data
                       │
                       ▼
              ┌─────────────────┐
              │  Bronze Layer   │
              │  Raw Delta Data │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │  Silver Layer   │
              │ Data Cleaning   │
              │ Transformation  │
              │ Validation      │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │   Gold Layer    │
              │ Business-ready  │
              │     Tables      │
              └────────┬────────┘
                       │
                       ▼
             ┌──────────────────┐
             │ Semantic Model   │
             │    Direct Lake   │
             └────────┬─────────┘
                      │
                      ▼
             ┌──────────────────┐
             │    Power BI      │
             │ Executive        │
             │ Dashboard        │
             └──────────────────┘

🛠️ Technology Stack
Microsoft Fabric
Fabric Lakehouse
OneLake
Apache Spark / PySpark
Delta Lake
Fabric Data Pipelines
Direct Lake
Power BI
DAX
GitHub
🥉 Bronze Layer

The Bronze layer stores raw retail source data with minimal transformation.

Source datasets
Customers
Products
Stores
Sales

The raw datasets were converted into Delta tables inside the Bronze Lakehouse.

🥈 Silver Layer

The Silver layer performs data cleaning and transformation.

Transformations
Data type standardization
Null handling
Duplicate handling
Invalid record handling
Date standardization
Data validation
Customer and product enrichment
Derived business columns

The cleaned data is stored as Delta tables in the Silver Lakehouse.

🥇 Gold Layer

The Gold layer contains analytics-ready business datasets.

Gold tables
gold_sales
daily_sales
category_sales
store_sales
segment_sales
overall_kpi

These tables are designed for reporting and analytical workloads.

⚙️ Data Pipeline

The project includes a master Fabric Data Pipeline:

Silver_Transformation
          │
        Success
          ▼
Gold_Transformation

The pipeline provides dependency-based orchestration between transformation notebooks.

High-concurrency Spark configuration is used to optimize notebook execution within the Fabric environment.

📊 Power BI Dashboard

The project includes an executive retail analytics dashboard with:

Total Sales
Total Orders
Total Customers
Average Order Value
Sales Trend
Category Performance
Store Performance
Customer Segment Analysis
Interactive Slicers
Store-level Drillthrough
🧠 Key Data Engineering Concepts Demonstrated
Medallion Architecture
Lakehouse Architecture
Delta Lake
PySpark ETL
Data Cleaning
Data Quality Validation
Spark-based Transformations
Pipeline Orchestration
High Concurrency Spark
Semantic Modelling
Direct Lake
DAX Measures
Business Intelligence
📁 Project Structure
Retail360-Fabric-Data-Engineering/
│
├── notebooks/
│   ├── Retail360_Silver_Transform
│   └── Retail360_Gold_Transform
│
├── pipelines/
│   └── Retail360_Master_Pipeline
│
├── documentation/
│   ├── architecture
│   └── data_dictionary
│
├── screenshots/
│   └── dashboard
│
└── README.md
🎯 Business Objective

The objective of Retail360 is to demonstrate how a retail organization can transform raw operational data into trusted analytical datasets and business insights using a modern cloud data platform.

👨‍💻 Author

Haven Mehta

BCA | Aspiring Data Engineer

Focus Areas
Microsoft Fabric
Azure Data Engineering
PySpark
SQL
Power BI
Cloud Data Platforms
⭐ Project Status

Completed — Portfolio / Learning Project

Future projects will extend these concepts using larger publicly available datasets and more advanced production-oriented data engineering patterns.
