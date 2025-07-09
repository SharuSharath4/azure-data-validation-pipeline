# azure-data-validation-pipeline

This project implements an event-driven CSV data validation pipeline using Azure services and Databricks. When a CSV file lands in an ADLS container, a Storage Event Trigger activates an Azure Data Factory pipeline that processes the file in Databricks. The pipeline validates the schema (fetched from Azure SQL), checks for duplicate rows, and ensures date formats are correct. Files are then routed to staging or rejected folders based on the outcome.

## Technologies Used
- Azure Blob Storage (ADLS Gen2)
- Azure Data Factory (ADF)
- Azure Databricks (PySpark)
- Azure SQL Database
- Azure Storage Event Triggers

## Features
- CSV ingestion and mount in Databricks
- Schema validation against SQL table
- Duplicate and date format checks
- Routing to `/staging` or `/rejected` folders
