# 🚀 BigQuery → MySQL Data Migration Pipeline (Python + Airflow)

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](#)
[![Airflow](https://img.shields.io/badge/Apache%20Airflow-Orchestration-orange.svg)](#)
[![BigQuery](https://img.shields.io/badge/Google-BigQuery-4285F4.svg)](#)
[![MySQL](https://img.shields.io/badge/MySQL-Target-4479A1.svg)](#)

## 📌 Overview
Production-ready pipeline to migrate/sync data from **Google BigQuery** to **MySQL** using **Python** ETL scripts orchestrated by **Apache Airflow**.

Supported load strategies:
- 🔄 **Truncate & Load** – full refresh of target table
- 📥 **CDC (Change Data Capture)** – incremental load using a `last_updated`/watermark column
- ✏️ **Update-Only** – update existing rows (no inserts)
- 🆕 **Create & Load** – auto-create target table from BigQuery schema, then load

Designed for: reliability, large datasets, zero/low hardcoding, and easy extensibility.

---

## 🏗️ Architecture


---

## ✨ Key Features
- ✅ Multiple load strategies (truncate, CDC, update-only, create+load)
- ✅ **Dynamic schema mapping** (BigQuery → MySQL; minimal hardcoding)
- ✅ **Batching + checkpointing** for large volumes
- ✅ **Idempotent** runs with natural-key or watermark logic
- ✅ **Robust logging & error handling**
- ✅ **Airflow DAGs** for scheduling, retries, SLAs, and alerting

---

## 🛠️ Tech Stack
- **Language:** Python 3.10+
- **Source:** Google BigQuery
- **Target:** MySQL 5.7/8.0
- **Orchestration:** Apache Airflow 2.x
- **Optional Staging:** Google Cloud Storage (GCS)

---

## 📂 Project Structure


        "path": ".checkpoints"       # local dir or mount
    }
}
