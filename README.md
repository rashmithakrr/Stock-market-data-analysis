# 📈 Real-Time Stock Market Data Pipeline on AWS

This project demonstrates the implementation of a real-time data streaming and analytics pipeline using Kafka, AWS EC2, S3, Glue, Athena, and QuickSight.

The objective is to simulate stock market data ingestion using Apache Kafka, process and store it on AWS S3, catalogue and query it using Athena, and finally visualize it with Amazon QuickSight.

---

## 🧰 Tech Stack

- **Apache Kafka** – Real-time data streaming engine
- **AWS EC2** – Kafka broker and producer/consumer host
- **Python** – Data processing and automation
- **AWS S3** – Scalable object storage for raw and processed data
- **AWS Glue** – Crawlers for schema detection and catalog creation
- **AWS Athena** – Serverless SQL querying on S3 data
- **Amazon QuickSight** – Business intelligence and interactive dashboard visualization

---

## 🚀 Project Workflow Overview

### 1. **Kafka Streaming on EC2**
Kafka was deployed on an AWS EC2 instance to simulate real-time streaming. Sample stock market data was ingested and sent through Kafka topics using Python-based producers. This allowed streaming the data in a near real-time fashion.

### 2. **Storing Data in S3**
The Kafka consumer running on EC2 received the streamed messages and saved them in JSON format to an Amazon S3 bucket. S3 acted as the centralized data lake for further processing and analysis.

### 3. **Data Cataloging with AWS Glue**
An AWS Glue crawler was used to scan the JSON files in the S3 bucket and automatically infer the schema. Glue then created a table in the AWS Glue Data Catalog, making the data queryable in Athena without any manual schema definitions.

### 4. **Querying with Amazon Athena**
Using the table created by the Glue crawler, SQL queries were run directly in Amazon Athena. Athena allowed on-demand analysis of the stock data using familiar SQL syntax, with no need for infrastructure provisioning.

### 5. **Data Visualization with QuickSight**
The queried data from Athena was connected to Amazon QuickSight. Dashboards were created to visualize trends, price movements, and other key metrics using line charts, bar charts, and filters. This provided interactive and shareable business intelligence capabilities over the processed stock market data.

---

## 🌐 Outcome

This project successfully demonstrates how to build a scalable, serverless data pipeline for real-time analytics on AWS using open-source tools and cloud-native services. It highlights seamless integration between Kafka and AWS services, enabling efficient data flow from ingestion to visualization.

---

## 📌 Key Benefits

- Real-time data simulation and ingestion
- Serverless querying without managing databases
- Automatic schema inference and cataloging
- Interactive, dynamic dashboards for insights
- Modular architecture easily extensible to other use cases

---




