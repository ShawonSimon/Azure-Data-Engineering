# Data Engineering on Azure
This project demonstrates an end-to-end data engineering solution on Microsoft Azure, designed to handle the ingestion, transformation, and analysis of data from an on-premises SQL Server database to a comprehensive reporting platform in Power BI. The solution uses Azure Data Lake Storage Gen2, Azure Data Factory, Databricks, and Azure Synapse Analytics, with added security managed through Azure Key Vault.

# Project Overview
## Pipeline Components
1. Self-Hosted Integration Runtime (SHIR):
   
    - Used for secure data transfer from the on-premises SQL Server to Azure. The SHIR facilitates connectivity between the on-prem environment and Azure Data Factory.
2. Azure Data Factory (ADF):

    - Orchestrates the data pipeline by moving data from the on-premises SQL Server to Azure Data Lake Storage Gen2 via SHIR.
    - Performs data ingestion, using various activities to manage data flow and ensure seamless pipeline execution.
3. Azure Data Lake Storage Gen2:

    - Stores ingested data in Bronze, Silver, and Gold layers to manage raw, cleansed, and curated datasets, respectively.
4. Databricks:

    - Transforms data from the Silver layer to the Gold layer.
    - Handles complex transformations, cleansing, and data preparation for downstream analytics.
5. Azure Synapse Analytics:

    - Acts as the data warehouse, loading curated data from the Gold layer for advanced analytics.
    - Enables efficient query processing and serves as the source for Power BI reporting.
6. Azure Key Vault:

    - Manages and secures sensitive information such as database connection strings and API keys used throughout the pipeline.
7. Power BI:

    - Connects to Azure Synapse Analytics for data visualization and reporting, enabling insights and analysis of the ingested and transformed data.
