# End-to-End-Ecommerce-Big-Data-Engineering-Project
This is an end-to-end big data pipeline built using Azure services, Databricks, and external data sources :)

---

## 📌 **Project Overview**

This project demonstrates a complete, cloud-native **big data engineering pipeline** built on **Microsoft Azure**, using the [Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). It follows the **Medallion Architecture** structured into **Bronze**, **Silver**, and **Gold** layers to ensure scalable, modular, and analytics-ready data processing.

The pipeline begins with raw data ingestion from **GitHub** and a **SQL database** using **Azure Data Factory**, storing it in **Azure Data Lake Storage Gen2**. It then leverages **Azure Databricks (Apache Spark)** for transformation, cleansing, and enrichment, including integration of external data from **MongoDB**. The refined datasets are served through **Azure Synapse Analytics (Serverless SQL Pool)**, enabling powerful querying and downstream consumption.

Final outputs are made available for **BI dashboards** (Power BI, Tableau) and **data science workloads**, delivering actionable insights and supporting real-time decision-making.


![Architecture Diagram](https://github.com/user-attachments/assets/08c48007-6ad0-4a5e-9b06-f4e88dfb2bfa)

---

## 🔄 Workflow

**1. Data Ingestion**
- **Sources**:  
  - GitHub (CSV files via HTTP connector)  
  - SQL Database (via JDBC connection)  
- **Tool Used**: Azure Data Factory (ADF)  
- **Landing Zone**: Azure Data Lake Storage Gen2 (**Bronze layer**)

### **2. Data Transformation & Enrichment**
- **Tool Used**: Azure Databricks (Apache Spark)  
- **Processes**:  
  - Cleaning, joining, schema standardization  
  - Enrichment using external data from **MongoDB**  
- **Output Format**: Parquet files stored in the **Silver layer**

### **3. Serving Layer**
- **Tool Used**: Azure Synapse Analytics (Serverless SQL Pool)  
- **Processes**:  
  - External tables and curated views created from Silver  
  - Published datasets into the **Gold layer**


---

## 🏗️ Resources Used

- **Azure Data Factory (ADF)** → Data ingestion pipelines  
- **Azure Data Lake Storage Gen2 (ADLS)** → Bronze, Silver, Gold layers  
- **Azure Databricks** → Data transformation and enrichment  
- **MongoDB (External)** → Enrichment dataset  
- **Azure Synapse Analytics** → Serverless SQL pool for querying and serving  

-----

## 📂 **Medallion Architecture**

```bash
adls_gen2/
├── bronze/   # Raw ingested data (CSV, JSON, MongoDB extracts)
├── silver/   # Cleaned, transformed, joined data (Parquet)
└── gold/     # Curated data served via Synapse (Views / Tables)

```
-----

##🔄 **Data Pipeline Flow**

1. **Data Ingestion**
uploded the data to the sources (MYSQL DB AND MONGO DB) using python scripts
Raw CSV files hosted on GitHub accessed via HTTP connector
Structured data from SQL Database ingested via JDBC connection
Orchestrated using Azure Data Factory (ADF) pipelines
All raw data landed into Azure Data Lake Storage Gen2 (ADLS Gen2) under the Bronze layer

2. **Data Transformation & Enrichment**

Processed using Azure Databricks (Apache Spark) for:
Cleaning Joining Schema standardization
External enrichment data sourced from MongoDB
Enriched and structured data stored as Parquet files in the Silver layer

3. **Serving Layer**
   
Queried using Azure Synapse Analytics (Serverless SQL Pool)
Created external tables and curated views from Silver layer
Published business-ready datasets into the Gold layer

----

##📸 **Project Screenshots**

**Azure Resources Overview**

<img width="1891" height="793" alt="image" src="https://github.com/user-attachments/assets/26343163-f0ee-486f-9079-ce67a612766f" />

**Medallion Architecture (Bronze, Silver, Gold Folders)**

<img width="1900" height="829" alt="image" src="https://github.com/user-attachments/assets/b79dbef0-4a50-4412-9d80-f4fd96b84d0d" />

**ADF Pipeline Workflow**

<img width="1883" height="810" alt="image" src="https://github.com/user-attachments/assets/a1422eec-fb22-4e12-a9be-47d95f7ac299" />


**Databricks Note book**

<img width="1862" height="889" alt="image" src="https://github.com/user-attachments/assets/0e83b607-d165-4e98-8d6d-7dafbe835d57" />


**Synapse Analytics Queries & Views**

<img width="1904" height="888" alt="image" src="https://github.com/user-attachments/assets/33293310-f101-4ab5-8a37-c5c6610ac264" />

----
##📊 **Key Learnings**

Architected a full-stack Medallion Architecture using Azure-native services
Developed an automated ETL pipeline leveraging Azure Data Factory and Databricks (Spark)
Engineered a scalable serving layer with Azure Synapse Analytics (Serverless SQL Pool)
Executed end-to-end cloud-native data engineering workflows, from ingestion to visualization
Applied the Medallion Architecture across Bronze, Silver, and Gold layers
Secured integrations between Azure services using App Registration and Role-Based Access Control (RBAC)
Implemented data quality checks and schema normalization for reliable processing
Explored NoSQL (MongoDB) for business enrichment and external data integration
Worked with Synapse Serverless SQL Pools and OPENROWSET for querying external data efficiently

---

##📌**Technology Stack**

• Orchestration: Azure Data Factory 
• Storage: Azure Data Lake Storage Gen2 
• Processing: Azure Databricks (PySpark) 
• Analytics: Azure Synapse Analytics 
• Sources: MySQL, GitHub (CSV), MongoDB 
• Languages: Python, SQL, PySpark


---
##📌**Next Steps**

• Connect pipelines to Power BI for dashboards and reports
• Automate pipelines using triggers in Azure Data Factory 
• Implement basic CI/CD for pipeline deployment

---
