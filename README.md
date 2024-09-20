# Kinesis Demo Project

This is a demo project that showcases the deployment of an AWS architecture using CloudFormation. The architecture consists of the following components:

- **Kinesis Stream**: Acts as the entry point for incoming data.
- **Firehose**: Connected to the Kinesis stream, it ingests and delivers the data to an S3 bucket.
- **S3 Bucket**: Stores the data coming from Firehose.
- **Lambda Fanout**: Triggered by S3, this set of Lambda functions processes the data and prepares it for further actions.
- **RDS**: The processed data is added to an RDS database for persistence.
- **RDS Proxy**: An RDS proxy is placed in front of the RDS for connection management and improved efficiency.
  
---
