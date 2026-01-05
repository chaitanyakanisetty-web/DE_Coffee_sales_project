Coffee Sales ETL Pipeline: Cloud Composer & GCP
📌 Project Overview
This project demonstrates a production-ready ETL (Extract, Transform, Load) Pipeline built using Apache Airflow on Google Cloud Composer. The pipeline automates the cleaning and normalization of messy retail sales data, transforming raw Excel records into a structured CSV format ready for downstream analytics and BI tools.

By leveraging Cloud Composer (GKE-based), the solution ensures high availability, scalability, and seamless integration with the Google Cloud ecosystem.

🏗️ System Architecture
The data flows through the following stages:

Storage (Landing Zone): Raw Coffe_sales.xlsx is uploaded to a Google Cloud Storage (GCS) bucket.

Orchestration (Cloud Composer): An Airflow DAG triggers on a daily schedule.

Transformation (Compute): A Python task executes a specialized cleaning script that handles deduplication, currency formatting, and datetime feature engineering.

Storage (Curated Zone): The cleaned data is saved back to GCS as a structured .csv file.

🛠️ Tech Stack
Orchestration: Apache Airflow (Google Cloud Composer)

Language: Python 3.10+

Data Processing: Pandas, NumPy

Cloud Provider: Google Cloud Platform (GCS, IAM, Cloud Logging)
