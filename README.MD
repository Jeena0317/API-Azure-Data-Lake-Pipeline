🟡 API → Azure Data Lake Pipeline
🧩 Use Case

This project demonstrates how to ingest live data from a public API (such as weather, currency, COVID-19, or cryptocurrency data) into Azure Data Lake using a robust ETL pipeline.

The pipeline ensures:

Fault-tolerant ingestion

Incremental data processing

Proper handling of complex JSON data

🛠️ Tools

Azure Data Factory (ADF) – REST connector for API ingestion

Azure Data Lake Storage (ADLS) – Data storage and staging

Databricks – Data transformation, JSON flattening, and incremental processing

✅ Features Implemented

API Pagination – Automatically retrieves all pages of data from the API

Error Handling & Retries – Implements retry logic for failed requests

JSON Flattening – Converts nested JSON responses into tabular format

Incremental Ingestion – Only ingests new or updated data to minimize storage and processing time

💼 Skills Demonstrated

Building real-world ingestion pipelines

Integrating REST APIs with cloud storage

Implementing fault tolerance and retry mechanisms

⚙️ Setup Instructions

Clone the Repository

git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

Set up Azure Data Lake Storage

Create a storage account and containers for Bronze, Silver, and Gold layers

Configure access keys or service principal securely (avoid hardcoding secrets)

Configure Azure Data Factory (ADF)

Connect to your API using the REST connector

Set up pagination, error handling, and incremental ingestion

Set up Databricks

Mount Azure Data Lake storage to Databricks

Use notebooks for JSON flattening and incremental processing

Store secrets securely using Databricks Secret Scopes

Run the Pipeline

Trigger the ADF pipeline → fetch API data → write to ADLS Bronze

Transform and flatten data in Databricks → write to Silver/Gold

⚡ Notes

Do not store secrets in notebooks or commits – use Databricks Secret Scopes or Azure Key Vault

Monitor pipeline logs for failed requests and retry automatically

Incremental ingestion ensures efficient storage and compute usage

📚 References

Azure Data Factory REST Connector

Databricks Notebooks

Azure Data Lake Storage Gen2

Working with nested JSON data and incremental ETL
