# 🏎️ Azure Databricks & Spark Core: End-to-End Data Engineering with Formula 1 Racing Data

This repository contains an **enterprise-grade data engineering project** built using **Azure Databricks, PySpark, Delta Lake, Azure Data Factory, and Power BI** — leveraging real-world Formula 1 racing data. The project showcases the design and implementation of a **Lakehouse Architecture** and demonstrates **modern ELT practices** in the Azure cloud ecosystem.

> 🔧 This project is ideal for showcasing skills in **cloud-native big data processing, Delta Lake operations, PySpark transformations, workflow orchestration**, and **real-time reporting** using Power BI.

---

## 🚀 Project Objective

To build a **modular, scalable, and cloud-native data engineering pipeline** using Azure tools and open-source frameworks, solving a real-world problem: managing and analyzing Formula 1 racing data.

Key Objectives:
- Implement Delta Lake for data consistency and efficient incremental processing.
- Build robust PySpark transformation logic using Spark Core APIs.
- Automate workflows using Azure Data Factory pipelines.
- Visualize curated data via Power BI dashboards connected directly to Databricks.

---

## 🧰 Tech Stack & Services Used

| Tool/Service              | Purpose |
|--------------------------|---------|
| **Azure Databricks**     | Unified data analytics platform to develop PySpark notebooks, manage clusters, and run jobs. |
| **Apache Spark (PySpark)**| Distributed data processing framework for large-scale transformation. |
| **Delta Lake**           | ACID-compliant storage layer enabling updates, merges, time travel, and schema enforcement. |
| **Azure Data Lake Gen2** | Storage for raw and transformed datasets. |
| **Azure Key Vault**      | Secure access to secrets (e.g., credentials, mount configs). |
| **Azure Data Factory**   | Pipeline orchestration, job scheduling, and monitoring. |
| **Power BI**             | Business Intelligence dashboards for racing analytics. |
| **Unity Catalog**        | Centralized governance, access control, and lineage for Databricks data. |

---

## 🏗️ Architecture Overview

```plaintext
        ┌───────────────────────────┐
        │ Formula 1 Raw Data       │
        │ (CSV, JSON)              │
        └────────────┬──────────────┘
                     ▼
        ┌───────────────────────────┐
        │ Azure Data Lake Gen2      │
        │ - Raw Layer               │
        └────────────┬──────────────┘
                     ▼
        ┌───────────────────────────┐
        │ Azure Databricks          │
        │ - PySpark ETL             │
        │ - Delta Lake              │
        └────────────┬──────────────┘
                     ▼
        ┌───────────────────────────┐
        │ Azure Data Factory        │
        │ - Pipeline Orchestration  │
        └────────────┬──────────────┘
                     ▼
        ┌───────────────────────────┐
        │ Power BI                  │
        │ - Reporting Layer         │
        └───────────────────────────┘
🏁 Real-World Use Case: Formula 1 Racing Data
This project uses F1 telemetry and race data (drivers, constructors, circuits, lap times, results, pit stops, and status history) to simulate:

Incremental vs Full Loads

Schema evolution in Delta

Aggregation of race metrics

Dashboarding key performance indicators (KPI) for races and drivers

🔍 Key Skills & Concepts Covered
✅ Azure Databricks
Create and configure clusters & notebooks.

Manage Databricks jobs and job dependencies.

Access Azure Data Lake via mounting with Azure Key Vault.

Query data using Spark SQL and PySpark APIs.

✅ Spark Core / PySpark
Use DataFrame APIs for filtering, joining, aggregating, and transforming data.

Handle partitioning, window functions, and complex transformations.

Implement incremental loads using event timestamps and file metadata.

✅ Delta Lake
Merge, update, delete data with ACID guarantees.

Convert Parquet datasets into Delta format.

Implement Time Travel, Schema Evolution, and History Tracking.

✅ Azure Data Factory
Create pipelines to trigger and monitor Databricks notebooks.

Implement retry logic, failure handling, and conditional execution.

Parameterize notebooks for different stages (raw → silver → gold layers).

✅ Power BI
Directly connect Power BI to Databricks using SQL endpoints.

Build dashboards showcasing driver rankings, average lap times, and race performance metrics.

Perform DAX calculations and dataset modeling.

✅ Unity Catalog (Data Governance)
Set up metastore and catalogs for structured governance.

Implement fine-grained access control and auditing.

Capture data lineage for compliance and data discovery.

📁 f1-databricks-pipeline/
├── data/
│   ├── raw/                 # Raw F1 data files (CSV, JSON)
│   ├── silver/              # Cleaned & transformed data
│   └── gold/                # Final analytical layer
├── notebooks/
│   ├── ingestion/           # Raw data ingestion notebooks
│   ├── transformation/      # Data cleaning, joins, enrichments
│   ├── delta/               # Delta Lake operations (merge, time travel)
├── adf-pipelines/
│   └── json/                # ADF pipeline templates and configs
├── powerbi/
│   └── dashboards/          # PBIX files and dashboard screenshots
└── README.md

This project demonstrates:

✅ Real-world, production-ready data pipelines.

✅ Mastery of Spark Core, Delta Lake, and PySpark.

✅ Orchestration via Azure Data Factory.

✅ Governance with Unity Catalog.

✅ BI storytelling with Power BI dashboards.
