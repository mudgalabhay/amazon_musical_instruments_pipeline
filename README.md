# 🎵 Amazon Musical Instruments Pipeline

## 📌 Project Overview

The **Amazon Musical Instruments Pipeline** is a data integration project designed to demonstrate how to build a robust, end-to-end data migration pipeline. The goal is to extract data from a **PostgreSQL** source database, ingest it using **Airbyte**, and load it into a **Snowflake** data warehouse for analytics and reporting.

---

## 🛠️ Development Summary

### 🔹 Virtual Environment Setup

A Python virtual environment was created to isolate the project dependencies, ensuring consistency and easy management of the project environment.

### 🔹 Source Database: PostgreSQL

A local PostgreSQL database was spun up using Docker. Inside this database, a sample table was created, and a few records were inserted. This serves as the **source** of truth for the data pipeline.

### 🔹 Target Platform: Snowflake

A Snowflake instance was prepared by creating the necessary data warehouse, database, schema, and roles. No tables were created manually in advance—Airbyte automatically handled table creation during ingestion.

---

## 🔄 Data Pipeline Workflow

### 🔹 Why Airbyte?

Airbyte is an open-source data integration platform that allows effortless syncing between various sources and destinations. It was chosen for this project due to its ease of use, support for incremental syncs, and ability to handle schema changes dynamically.

### 🔹 Data Flow

The pipeline follows this architecture:

**PostgreSQL (Source) ➡️ Airbyte (Connector) ➡️ Snowflake (Target)**

* Airbyte runs locally using Docker.
* It is configured to fetch data from the PostgreSQL source.
* The destination is set up as a Snowflake account.
* Airbyte handles data syncing, schema management, and even creates the target table if it doesn’t already exist.

---

## ✅ Result

Once the pipeline is synced, the data is successfully transferred from the source PostgreSQL database to the target Snowflake table. The process supports incremental loading, which is useful for handling real-world dynamic datasets.

---

## 💬 Final Notes

This project showcases how modern data integration tools like Airbyte simplify the movement of data between systems. With minimal setup and no custom code, robust pipelines can be developed and scaled easily using open-source tools.

Thanks for checking out this project! 🎸🎧
