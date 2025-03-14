# **Building a Real-Time Data Pipeline for Netflix Data Analysis Using Azure**

## **Overview**
This project demonstrates an end-to-end **real-time data pipeline** for processing Netflix data using **Azure Data Factory (ADF), Databricks, and Delta Live Tables**. The goal is to implement a **scalable, automated, and optimized ETL workflow** that enables real-time data ingestion, transformation, and visualization.

## **Architecture**
The project follows the **Medallion Architecture**:
- **Bronze Layer**: Raw data ingestion from **GitHub** to **Azure Data Lake Storage (ADLS)** using **ADF**.
- **Silver Layer**: Data cleaning and transformation using **Databricks Auto-loader & PySpark**.
- **Gold Layer**: Optimized storage using **Delta Live Tables (DLT)**.

## **Tech Stack**
- **Azure Data Factory (ADF)** – ETL orchestration
- **Azure Databricks & PySpark** – Data transformation
- **Databricks Auto-loader** – Incremental data ingestion
- **Delta Live Tables (DLT)** – Optimized data storage
- **Azure Data Lake Storage (ADLS)** – Cloud storage

## **Implementation Steps**
### **Step 1: Setting Up Azure Resources**
1. Create an **Azure Resource Group**.
2. Deploy **Azure Data Lake Storage Gen2**.
3. Deploy **Azure Data Factory (ADF)**.
4. Set up **Azure Databricks** workspace and configure clusters.

### **Step 2: Data Ingestion Using ADF**
1. Create **Linked Services** for **GitHub (HTTP connector)** and **ADLS**.
2. Develop **parameterized ADF pipelines** for dynamic ingestion.
3. Implement **validation checks** before ingestion.
4. Use **Copy Activity** to move data from GitHub to ADLS (Bronze Layer).

### **Step 3: Data Processing in Databricks**
1. Create a **Databricks Notebook** for data transformation.
2. Use **Auto-loader** for **incremental ingestion**.
3. Apply **PySpark transformations** (filtering, joins, data cleansing).
4. Store **transformed data in the Silver Layer**.

### **Step 4: Implementing Delta Live Tables**
1. Enable **Delta Live Tables** in Databricks.
2. Create **ETL workflows** to transform **Silver to Gold Layer**.
3. Optimize storage with **schema evolution and indexing**.

## **How to Run the Project**
### **Prerequisites**
- An **Azure account** with access to **ADF, Databricks, ADLS, and Synapse**.
- **Databricks Cluster** (Runtime 9.1+ recommended).

### **Deployment Steps**
1. Clone this repository.
2. Import ADF pipeline JSONs into **Azure Data Factory**.
3. Run Databricks notebooks for data transformation.

