# Azure Data Factory & Databricks End-to-End Pipeline (Medallion Architecture)

## 📌 Overview
This project demonstrates an **end-to-end data engineering pipeline** using **Azure Data Factory (ADF)**, **Azure Databricks**, and **Azure Data Lake Storage Gen2 (ADLS)**.  
It implements the **Medallion Architecture** (Bronze → Silver → Gold) to ingest, process, and store trip transaction & ratings data for analytics.

![Project Architecture](images/project_architecture.png)

---

## 🚀 Use Case
- **Optimized Ride Analytics** – Identify top-rated drivers, peak demand periods, and travel patterns.
- **Real-Time Data Processing & Alerts** – Automated ingestion with notifications via Azure Logic Apps.
- **Structured Storage** – Data stored in Delta tables for time travel, schema evolution, and efficient querying.

---

## 🏗 Architecture
1. **Bronze Layer** – Raw data from Azure SQL Database copied to ADLS via ADF.
2. **Silver Layer** – Data cleaned, transformed, and structured in Databricks.
3. **Gold Layer** – Aggregated, analytics-ready data stored in Delta format for BI/ML.

---

## 🛠 Services Used
- **Azure SQL Database** – Source transactional & ratings data.
- **Azure Data Factory** – Orchestrates data movement & transformations.
- **Azure Data Lake Storage Gen2** – Stores raw & processed data.
- **Azure Databricks** – Processes data with PySpark using Medallion Architecture.
- **Azure Logic Apps** – Sends email alerts after pipeline completion.

---

## 📂 Project Workflow
1. **Data Ingestion** – ADF pipelines replicate SQL DB tables to ADLS Bronze folders.
2. **Transformation** – Databricks notebooks process Bronze → Silver → Gold.
3. **Automation** – ADF orchestrates notebook execution & triggers Logic App alerts.
4. **Storage** – Delta tables stored in ADLS for analytics.

---

## 📊 Datasets
- **Trip Transactions** – Trip details, timestamps, distance, and fares.
- **Ride Ratings** – Driver ratings and customer satisfaction scores.

---

## ⚙️ Prerequisites
- Azure Subscription
- Azure SQL Database with sample data
- ADLS Gen2 Storage Account
- Databricks Workspace & Cluster
- Azure Data Factory instance
- Logic Apps for notifications

---

## 📜 Execution Steps
1. Create Azure Resource Group, SQL DB, ADLS Gen2, Databricks, and ADF.
2. Upload raw CSV data into **bronze** folder in ADLS.
3. Configure **ADF Dataflows** for Trip Transactions & Rewards Points.
4. Implement **Incremental Loads** using ADF filter expressions.
5. Build **Databricks Notebooks** for Bronze, Silver, and Gold processing.
6. Schedule and monitor pipelines in ADF.
7. Verify processed data in ADLS and Databricks tables.

---

## 🏆 Key Features
- **Delta Lake Storage** with ACID transactions & schema enforcement.
- **Incremental Data Loads** for efficiency.
- **Automated Notifications** after pipeline runs.
- **Time Travel Queries** for historical data analysis.


