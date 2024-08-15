# spotify-etl 🎧

![spotify](https://github.com/user-attachments/assets/af6fdf6f-2692-4b6b-95b9-fd76c4eb302e)

## Overview 📝
This project implements an ETL (Extract, Transform, Load) pipeline for processing Spotify data. The pipeline is designed to extract data from the Spotify API, transform it using AWS Lambda functions, and load it into AWS S3 for storage and analysis. AWS Glue and AWS Athena are then used for schema inference and analytics.

## ETL Pipeline Components 🚀

### Extract 📡
- **Spotify API**: Data is extracted from the Spotify API using Python scripts.
- **AWS Lambda**: An AWS Lambda function triggers the data extraction process.
- **AWS CloudWatch**: Scheduled daily triggers for the extraction process.

### Transform 🔄
- **AWS Lambda**: Another Lambda function is responsible for transforming the raw data.
- **AWS Glue**: The transformed data is cataloged using AWS Glue, which also provides schema inference.

### Load 📂
- **AWS S3**: Raw data is stored in an S3 bucket, and transformed data is saved in another S3 bucket for further processing.
- **AWS Athena**: Data is queried and analyzed using AWS Athena.

## Pipeline Flow 🔗
1. **Trigger**: AWS CloudWatch triggers the ETL process daily. ⏰
2. **Extraction**: Data is extracted from the Spotify API via an AWS Lambda function and stored in S3. 🗂️
3. **Transformation**: Another Lambda function transforms the raw data and stores the processed data in S3. 🔄
4. **Schema Inference**: AWS Glue Crawlers infer the schema of the transformed data. 🧠
5. **Analytics**: AWS Athena is used for running queries on the transformed data for analysis. 📊

## Technologies Used 💻
- **Python**: Core programming language for the Lambda functions. 🐍
- **AWS Lambda**: For both data extraction and transformation processes. 🛠️
- **AWS S3**: Storage solution for both raw and transformed data. ☁️
- **AWS Glue**: Data Catalog for managing and discovering data. 🗂️
- **AWS Athena**: For querying the transformed data. 🔍
- **AWS CloudWatch**: Scheduled triggers to automate the ETL process. ⏰
