# Spotify End-To-End Data Engineering Project

### Introduction
In this project, have built an ETL (Extract, Transform, Load) pipeline using Spotify API on AWS. The pipeline retrieves data from the Spotify API, transforms it to a desired format and loads it into AWS data store.

### Architecture
![Architecture Diagram](https://github.com/drashtikhakhi/spotify-pipeline-project/blob/main/Spotify-ETL-Architecture.png)

### About DataSet/API
This API contains information about music artist, albums and songs - [Spotify API](https://developer.spotify.com/documentation).

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups and static website files.
   
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets us run our code without managing servers. It is used to run code in response to events like changes in S3, DynamoDB or other AWS services.

3. **CloudWatch:** Cloud Watch is a monitoring service for AWS resources and the applications run on them. It is used to collect and track metrics, collect and monitor log files and set alarms.

4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls data sources, identifies data formats, and infer schemas to create an AWS Glue Data Catalog.

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. It is used with other AWS services such as Athena.

6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. It is used to analyze data in Glue Data Catalog or in other s3 buckets.

### Project Execution Flow
Extract data from API -> Lambda Trigger -> Run extract code -> Store raw data -> Trigger transform function -> Transform data and load it -> Query using Athena.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```
