# End-to-End-Ecommerce-Big-Data-Engineering-Project-on-Azure-
This is an big data  end to end pipeline build with  azure services and data bricks  and other external resource :)


📌 ***Project Overview***

This project showcases a robust end-to-end data engineering pipeline developed on Microsoft Azure, leveraging the  E-Commerce Public Dataset. It follows the Medallion Architecture—structured into Bronze, Silver, and Gold layers—to deliver scalable, dependable, and analytics-ready data workflows from raw ingestion to curated insights.

<img width="768" height="512" alt="image" src="https://github.com/user-attachments/assets/08c48007-6ad0-4a5e-9b06-f4e88dfb2bfa" />


🚀 ***Workflow***

1. Data Ingestion
   
Raw data originates from two primary sources:

GitHub: CSV files accessed via HTTP connector
SQL Database: Subset of structured data retrieved using JDBC connection
These sources are ingested using Azure Data Factory (ADF) pipelines and landed into Azure Data Lake Storage Gen2 (ADLS Gen2) under the Bronze layer, 
serving as the raw data zone.

2. Data Transformation & Enrichment
   
Data processing is handled in Azure Databricks (Spark), where:
Raw datasets are cleaned, joined, and transformed
External enrichment data from MongoDB is integrated via Spark into the Bronze layer
The output is structured, high-quality Parquet files, stored in the Silver layer for analytical readiness.

3. Serving Layer
   
Using Azure Synapse Analytics (Serverless SQL Pool):
External tables and curated views are created from Silver layer data
These refined datasets are published into the Gold layer, representing business-ready information

4. Visualization & Consumption
   
Gold layer datasets are exposed for:
Business Intelligence dashboards via tools like Power BI and Tableau
Advanced analytics and data science workloads, enabling insights and decision-making

🏗️ ***Resource used***

Azure Data Factory (ADF) → Data ingestion pipelines.
Azure Data Lake Storage Gen2 (ADLS) → Bronze, Silver, Gold layers.
Azure Databricks → Data transformation and enrichment.
MongoDB (External) → Enrichment dataset.
Azure Synapse Analytics → Serverless SQL pool for querying and serving.


📂 ***Medallion Architecture***
adls_gen2/
├── bronze/   # Raw ingested data (CSV, JSON, MongoDB extracts)
├── silver/   # Cleaned, transformed, joined data (Parquet)
└── gold/     # Curated data served via Synapse (Views / Tables)


🔄 ***Data Pipeline Flow***

1. Data Ingestion

Raw CSV files hosted on GitHub accessed via HTTP connector
Structured data from SQL Database ingested via JDBC connection
Orchestrated using Azure Data Factory (ADF) pipelines
All raw data landed into Azure Data Lake Storage Gen2 (ADLS Gen2) under the Bronze layer

2. Data Transformation & Enrichment

Processed using Azure Databricks (Apache Spark) for:
Cleaning Joining Schema standardization
External enrichment data sourced from MongoDB
Enriched and structured data stored as Parquet files in the Silver layer

3. Serving Layer
   
Queried using Azure Synapse Analytics (Serverless SQL Pool)
Created external tables and curated views from Silver layer
Published business-ready datasets into the Gold layer


📸 ***Project Screenshots***

Azure Resources Overview

<img width="1891" height="793" alt="image" src="https://github.com/user-attachments/assets/26343163-f0ee-486f-9079-ce67a612766f" />

Medallion Architecture (Bronze, Silver, Gold Folders)

<img width="1900" height="829" alt="image" src="https://github.com/user-attachments/assets/b79dbef0-4a50-4412-9d80-f4fd96b84d0d" />

ADF Pipeline Workflow

<img width="1883" height="810" alt="image" src="https://github.com/user-attachments/assets/a1422eec-fb22-4e12-a9be-47d95f7ac299" />


Databricks Note book

<img width="1862" height="889" alt="image" src="https://github.com/user-attachments/assets/0e83b607-d165-4e98-8d6d-7dafbe835d57" />


Synapse Analytics Queries & Views

<img width="1904" height="888" alt="image" src="https://github.com/user-attachments/assets/33293310-f101-4ab5-8a37-c5c6610ac264" />


📊 ***Key Learnings***

Architected a full-stack Medallion Architecture using Azure-native services
Developed an automated ETL pipeline leveraging Azure Data Factory and Databricks (Spark)
Engineered a scalable serving layer with Azure Synapse Analytics (Serverless SQL Pool)
Executed end-to-end cloud-native data engineering workflows, from ingestion to visualization


📌***Technology Stack***

• Orchestration: Azure Data Factory
• Storage: Azure Data Lake Storage Gen2
• Processing: Azure Databricks (PySpark)
• Analytics: Azure Synapse Analytics
• Sources: MySQL, GitHub (CSV), MongoDB
• Languages: Python, SQL,Pyspak

📌 ***Next Steps***

• Connect pipelines to Power BI for dashboards and reports
• Automate pipelines using triggers in Azure Data Factory
• Implement basic CI/CD for pipeline deployment
