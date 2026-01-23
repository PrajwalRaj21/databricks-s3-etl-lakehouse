# 🚀 Databricks ETL Pipeline with Amazon S3 (Lakehouse Architecture)

## 📌 Project Overview

This project demonstrates a **job-ready batch ETL pipeline** built using **Databricks, PySpark, Delta Lake, and Amazon S3**. The pipeline ingests raw CSV data from S3, processes it through a **Bronze → Silver → Gold** lakehouse architecture, and produces analytics-ready datasets.


---

## 🏗 Architecture

```
Local CSV Files
      ↓
Amazon S3 (Raw Zone)
      ↓
Databricks Job (PySpark)
      ↓
Delta Lake (Bronze / Silver / Gold)
      ↓
SQL / BI / Analytics
```

---

## 🛠 Tech Stack

* Databricks
* Apache Spark (PySpark)
* Delta Lake
* Amazon S3
* Spark SQL
* Databricks Jobs

---

## 📂 Repository Structure

```
Databricks_S3_ETL_Lakehouse/
│
├── notebooks/
│   └── etl_orders_customers_products.py
│
├── data/
│   ├── orders.csv
│   ├── customers.csv
│   └── products.csv
│
├── architecture/
│   └── etl_architecture.png
│
└── README.md
```

---

## 📥 Data Sources

The pipeline ingests the following CSV files stored in Amazon S3:

* `orders.csv`
* `customers.csv`
* `products.csv`

### S3 Folder Layout

```
s3://<your-bucket-name>/raw/
├── orders/orders.csv
├── customers/customers.csv
└── products/products.csv
```

---

## 🔄 ETL Pipeline Design

### 🥉 Bronze Layer (Raw Ingestion)

* Reads CSV files directly from Amazon S3
* Stores raw data as **Delta tables**
* Preserves original schema and values

### 🥈 Silver Layer (Clean & Enriched)

* Applies data quality checks (null handling, schema validation)
* Joins orders with customers and products
* Applies business transformations

### 🥇 Gold Layer (Analytics Ready)

* Aggregates business metrics
* Produces reporting-ready datasets
* Exposed via SQL tables for BI tools

---

## ⚙️ Automation

* The ETL pipeline is executed using **Databricks Jobs**
* Can be scheduled to run daily or hourly
* Includes retry logic and failure monitoring

---

## 🧪 Example Transformations

* Filtering invalid records
* Joining fact and dimension tables
* Aggregating product-level metrics

---

## 🧠 Key Concepts Demonstrated

* Batch ETL pipelines
* Lakehouse architecture
* Incremental data ingestion
* Separation of compute and storage
* SQL + PySpark interoperability

---

## 📄 Resume Highlights

* Built an automated batch ETL pipeline ingesting CSV data from Amazon S3 into Databricks
* Implemented Bronze–Silver–Gold lakehouse architecture using Delta Lake
* Performed data cleansing, joins, and aggregations using PySpark
* Automated pipeline execution using Databricks Jobs

---

## 🚀 Future Enhancements

* Incremental file ingestion
* Schema evolution handling
* Data quality monitoring tables
* Streaming ingestion using Kafka
* dbt integration on Databricks

---

## 👤 Author

**Prajwal Raj Giri**
Aspiring Data Engineer | Data Science & AI Enthusiast

---

⭐ If you find this project useful, consider starring the repository!
