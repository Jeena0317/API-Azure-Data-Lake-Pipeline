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

1. Clone the Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
2. Set Up Azure Data Lake Storage

Create a storage account and containers: Bronze, Silver, Gold

Use access keys or service principal, store them securely (avoid hardcoding)

3. Configure Azure Data Factory

Connect to the API using the REST connector

Enable pagination, retries, and incremental ingestion

4. Set Up Databricks

Mount Azure Data Lake storage

Use notebooks for flattening JSON and incremental ETL

Store secrets securely using Databricks Secret Scopes

5. Run the Pipeline

Trigger the ADF pipeline → fetch API data → write to Bronze

Transform and flatten data in Databricks → write to Silver/Gold

⚡ Best Practices

Never commit secrets to GitHub; always use secure storage

Incremental ingestion improves performance and reduces costs

Monitor pipeline logs to handle failed API requests efficiently

💼 Skills Demonstrated

Real-world API ingestion pipelines

Integration of REST APIs with cloud storage

Fault tolerance and retry mechanisms

JSON flattening and incremental ETL

📚 References

Azure Data Factory REST Connector

Azure Data Lake Storage Gen2

Databricks Notebook Best Practices

I can also make a version with a screenshot of your pipeline diagram and sample notebook outputs so it
