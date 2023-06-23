# Spotify Data Pipeline ETL Project

### Description
In this project, we built an ETL (Extract, Transform, Load) pipeline on AWS using Spotify API.The Pipeline will retrieve data from the Spotify API, transform it to the desired format, and load it with AWS data store.    

### Architecture
![Architecture Diagram](https://github.com/deepakydv26/spotify-data-pipeline-etl-project/blob/main/Project-Arc.jpg)

### About Dataset/API
This API contains information about music artist, album and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)
### Technology Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on the web. It is commonly used to store and distribute large media files, data backups, and static website files.
2.  **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDB, or other AWS services. 
3. **Cloud Watch:** Amazon CloudWatch is a monitoring service for AWS resources and the applications you run on them. You can use CloudWatch to collect and track metrics, collect and monitor log files, and set alarms. 
4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources, identifies data formats, and infers schemas to create an AWS Glue Data Catalog. 
5. **Data atalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in A You can use the Glue Dat log with other AWS services, such as Athena. 
6. **Amazon Athena:** is an interactive query service th makes it easy to analyze data in Amazon S3 using standard can use Athena to analyze data in your Glue Data Catalog or in other S3 buckets.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 Hour) -> Run Extract Code -> Store RAW data -> Trigger Transform Function -> Transform Data and Load it -> Query using Athena



