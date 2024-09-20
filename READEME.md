# Kinesis Demo Project

This is a demo project that showcases the deployment of an AWS architecture using CloudFormation. The architecture consists of the following components:

- **Kinesis Stream**: Acts as the entry point for incoming data.
- **Firehose**: Connected to the Kinesis stream, it ingests and delivers the data to an S3 bucket.
- **S3 Bucket**: Stores the data coming from Firehose.
- **Lambda Fanout**: Triggered by S3, this set of Lambda functions processes the data and prepares it for further actions.
- **RDS**: The processed data is added to an RDS database for persistence.
- **RDS Proxy**: An RDS proxy is placed in front of the RDS for connection management and improved efficiency.

This guide covers how to deploy and manage this setup using CloudFormation with the `aws-cf` CLI.

# CloudFormation Deployment using `aws-cf`

This guide covers how to deploy and manage your CloudFormation templates using the `aws-cf` CLI. 

## Deploying Specific Services

To deploy a specific service using `aws-cf`, run the following command:

aws-cf deploy -s <SERVICE>

Replace `<SERVICE>` with the name of the service you want to deploy.

## Deploying All Services

To deploy all services at once, use the following command:

aws-cf deploy

This will deploy all services defined in your CloudFormation templates.

## Checking Differences for a Specific Service

To see the differences between the current CloudFormation template and the deployed stack for a specific service, run:

aws-cf diff -s <SERVICE>

Replace `<SERVICE>` with the service name.

## Checking Differences for All Services

To see differences for all services, use the following command:

aws-cf diff

This will display a diff for all services compared to their currently deployed CloudFormation stacks.

---
