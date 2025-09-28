# Spotify End to End Data Engineering Project
In this project, we will create an ETL (Extract, Transform, Load) pipeline on AWS that leverages the Spotify API. The pipeline will extract data from Spotify, transform it into the required format, and store it within an AWS data repository.

### Introduction
This is an Extract, Transform, Load (ETL) project leveraging the Spotify API and AWS. The pipeline is designed to retrieve raw data, apply transformations, and load the final, useful results into an AWS data store.

### Architecture Diagram
![Architecture Diagram](https://github.com/datahub-by-urmi/spotify-etl-pipeline-project/blob/main/Spotify_ETL_architacture_diagram.png)

### About Dataset/API:
This project utilizes the Spotify Web API to retrieve and analyze metadata for approximately 78 top-performing songs, including their associated artists, albums, and audio features. The dataset provides a focused snapshot of music trends for analysis. [Spotify API](https://spotipy.readthedocs.io/en/2.25.1/)

### Services Used

1. **S3 (Simple Storage Service):**  Amazon S3 is a robust, highly scalable **object storage service.** It allows us to **store and retrieve any volume of data**, making it ideal for large media files and general data backups.

2. **AWS Lambda:**  A key **serverless computing** service that lets us **run our code without having to manage any servers**. It's often used to execute code automatically in response to events from other AWS services like S3 or DynamoDB.

3. **Cloud Watch:**  Amazon CloudWatch provides **essential monitoring** for the entire AWS environment. It allows us to gather **performance metrics** and **log files**, giving us the ability to **set up alarms** for automated alerts.

4. **Glue Crawler:**  This is a fully managed service that automatically analyzes your data sources. It **crawls the data**, identifies its format and **schema**, and then uses that information to automatically create entries in the **AWS Glue Data Catalog**.

5. **Data Catalog**  This service functions as a central, fully managed **metadata repository**. It simplifies the process of **discovering and managing data**, allowing you to easily integrate it with other AWS services like **Athena** for analysis.

6. **Amazon Athena**  An interactive query service that allows for easy **data analysis directly in Amazon S3** using **standard SQL**. It integrates seamlessly with the **Glue Data Catalog** to query structured data residing in S3 buckets.

### Install Packages: 
```
pip install pandas as pd
pip install numpy
pip install spotipy

```
### Project Execution Flow
Extract Data from API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load It -> Query Using Athena










