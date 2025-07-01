## End-to-End Data Pipeline Architecture (Azure + Databricks + Power BI)
##### This project implements a modern data pipeline using Azure Data Factory, Azure Data Lake Gen2, Azure Databricks, Azure Synapse, and Power BI for efficient data ingestion, transformation, storage, and reporting.
#### Architecture Overview:
##### 1.Data Source (HTTP API or External System):
-- Data is fetched from an external data source such as a REST API or web service using HTTP protocols.
##### 2.Data Ingestion – Azure Data Factory:
-- Azure Data Factory (ADF) orchestrates the data pipeline by connecting to the source and moving raw data into the data lake.
##### 3.Raw Data Store – Data Lake Gen2:
-- The ingested raw data is stored in Azure Data Lake Storage Gen2 in its original format. This layer acts as the bronze layer in a medallion architecture.
##### 4.Data Transformation – Azure Databricks:
-- Databricks reads raw data from the data lake and performs necessary transformations using PySpark or SQL.
-- Cleaned and enriched data is then written back to the data lake (silver layer), ready for serving.
##### 5.Transformed Data Store – Data Lake Gen2:
-- This layer holds the transformed (processed) data, optimized for analytics and querying.
##### 6.Serving Layer – Azure Synapse Analytics:
-- Transformed data is loaded into Azure Synapse Analytics to enable efficient querying, serving as the gold layer.
##### 7.Reporting – Power BI:
-- Power BI connects to Synapse to visualize the processed data through dynamic dashboards and reports.

####  Medallion Architecture Layers:
##### 🥉 Bronze Layer – Raw data (stored in Data Lake Gen2).
##### 🥈Silver Layer – Cleaned/transformed data (stored in Data Lake Gen2).
##### 🥇 Gold Layer – Aggregated, analytics-ready data (served from Synapse).

####  Technologies Used:
##### Azure Data Factory – Orchestration
##### Azure Data Lake Gen2 – Storage (Raw + Transformed)
##### Azure Databricks – Data Processing
##### Azure Synapse – Data Serving/Analytics
##### Power BI – Data Visualization

### Flow Chart
![image](https://github.com/user-attachments/assets/b97b5120-d9b9-41c1-b55b-40b35e99a284)
![image](https://github.com/user-attachments/assets/b411f217-1e40-4880-ad5c-844ba121444b)
![image](https://github.com/user-attachments/assets/e65166b8-f284-4f35-a94a-4e6feb97a29d)



