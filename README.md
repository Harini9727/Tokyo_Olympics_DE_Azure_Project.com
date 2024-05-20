 1. Project Setup and Data Source Preparation
- Data Source Identification: The data for the project is sourced from Kaggle, specifically the Tokyo Olympics dataset, which is initially stored on GitHub for easier access and management.
- Azure Data Factory (ADF): The first step involves setting up Azure Data Factory, a tool used for data integration. ADF is used to create a data pipeline that automates the extraction of data from the GitHub repository and loads it into Azure Data Lake Storage.

 2. Data Loading to Azure Data Lake Storage
- Creation of Storage Accounts: Before loading the data, a storage account within Azure Data Lake is created to store both raw and transformed data.
- Data Ingestion: Using Azure Data Factory, pipelines are constructed to move data from GitHub (considered as a raw data source) to Azure Data Lake Storage. This involves configuring the data factory to connect to GitHub via HTTP, fetching the data, and then storing it in a structured format in the data lake.

 3. Data Transformation Using Azure Databricks
- Setup Azure Databricks Workspace: This service provides a collaborative environment for data scientists and engineers to perform complex data transformations using Apache Spark.
- Data Transformation: The raw data loaded into the data lake is pulled into Databricks, where various transformation tasks are performed. These tasks include cleaning the data, renaming columns, changing data types, and more, to prepare the data for analysis.
- Loading Transformed Data: After transformations, the data is loaded back into Azure Data Lake Storage, but into a separate folder for transformed data to distinguish it from the raw data.

 4. Data Analysis with Azure Synapse Analytics
- Synapse Analytics Setup: Azure Synapse Analytics is utilized for running SQL queries on the transformed data. This service integrates big data and data warehousing solutions, enabling complex analytical queries.
- SQL Queries and Analysis: In Synapse Analytics, SQL queries are executed to derive insights from the data, such as calculating the total number of medals won by each country, the average number of entries by gender, etc.


