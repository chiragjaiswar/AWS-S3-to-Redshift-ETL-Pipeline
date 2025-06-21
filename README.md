# AWS S3 to Redshift ETL Pipeline 🚀

![AWS S3 to Redshift ETL Pipeline](https://img.shields.io/badge/repo-AWS_S3_to_Redshift_ETL_Pipeline-blue.svg)
[![Releases](https://img.shields.io/badge/releases-latest-brightgreen)](https://github.com/chiragjaiswar/AWS-S3-to-Redshift-ETL-Pipeline/releases)

Welcome to the AWS S3 to Redshift ETL Pipeline repository! This project showcases an automated, serverless ETL pipeline built on AWS. It transforms CSV data ingested into S3, using AWS Lambda to trigger an AWS Glue workflow that includes crawlers and Spark ETL jobs. The processed data is then loaded into Amazon Redshift, with real-time notifications sent via Amazon SNS through EventBridge.

## Table of Contents

- [Features](#features)
- [Architecture](#architecture)
- [Setup](#setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Features

- **Serverless Architecture**: This pipeline uses AWS services to minimize server management.
- **Data Transformation**: CSV data is transformed efficiently using AWS Glue and PySpark.
- **Real-Time Notifications**: Get instant updates via Amazon SNS when data processing occurs.
- **Event-Driven**: The pipeline responds to events, triggering processes automatically.
- **Scalable**: Designed to handle large datasets without performance issues.

## Architecture

The architecture of the ETL pipeline consists of several AWS services working together:

1. **Amazon S3**: The source of CSV data.
2. **AWS Lambda**: Triggers the ETL process when new data arrives in S3.
3. **AWS Glue**: Manages data cataloging and transformation tasks.
   - **Crawlers**: Automatically discover data and create table schemas.
   - **ETL Jobs**: Execute data transformation using PySpark.
4. **Amazon Redshift**: Stores the processed data for analysis.
5. **Amazon SNS**: Sends notifications about the ETL process.
6. **Amazon EventBridge**: Manages events and routes them to the appropriate services.

![Architecture Diagram](https://example.com/path/to/architecture-diagram.png)

## Setup

To set up this ETL pipeline, follow these steps:

### Prerequisites

- An AWS account
- AWS CLI installed and configured
- Basic knowledge of AWS services

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/chiragjaiswar/AWS-S3-to-Redshift-ETL-Pipeline.git
   cd AWS-S3-to-Redshift-ETL-Pipeline
   ```

2. **Create S3 Bucket**:
   Create an S3 bucket to store your CSV files.
   ```bash
   aws s3 mb s3://your-bucket-name
   ```

3. **Deploy AWS Lambda Function**:
   Use the AWS Console or CLI to create a Lambda function. Upload the function code from the repository.

4. **Set Up AWS Glue**:
   - Create a Glue Crawler to catalog your data.
   - Create Glue ETL jobs to transform your data.

5. **Configure Amazon Redshift**:
   Set up a Redshift cluster to load your processed data.

6. **Set Up Amazon SNS**:
   Create an SNS topic for notifications.

7. **Configure EventBridge**:
   Set up rules to trigger your Lambda function based on S3 events.

## Usage

Once the setup is complete, you can start using the ETL pipeline:

1. **Upload CSV Files**:
   Place your CSV files in the S3 bucket.

2. **Trigger the Pipeline**:
   The Lambda function will automatically trigger the Glue workflow.

3. **Monitor Notifications**:
   Check your email or SNS dashboard for notifications regarding the ETL process.

## Contributing

Contributions are welcome! If you want to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [AWS Documentation](https://aws.amazon.com/documentation/)
- [Apache Spark](https://spark.apache.org/)
- [Amazon Redshift](https://aws.amazon.com/redshift/)

For the latest releases, please visit our [Releases](https://github.com/chiragjaiswar/AWS-S3-to-Redshift-ETL-Pipeline/releases) section. You can download and execute the files available there.

Thank you for your interest in the AWS S3 to Redshift ETL Pipeline!