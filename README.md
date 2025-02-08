# Serverless Web Application on AWS

This repository contains a project that demonstrates how to set up a **Serverless Web Application** using AWS services. The application follows a serverless architecture, reducing the need for managing and provisioning servers.

## Architecture Overview

The application utilizes the following AWS services:
- **AWS Lambda**: A compute service that runs code without provisioning servers.
- **Amazon DynamoDB**: A fully managed NoSQL database service.
- **Amazon S3 Bucket**: A storage service to host static files like HTML, CSS, and JavaScript.
- **Amazon CloudFront**: A Content Delivery Network (CDN) service to speed up the distribution of your content globally.
- **Amazon Route 53**: A scalable DNS service to route end-user requests.

### Project Flow:
1. **Users** access the web application through a browser.
2. **Route 53** directs the traffic to **CloudFront**.
3. **CloudFront** serves the static content from **S3 Bucket**.
4. **Lambda** executes backend logic and interacts with **DynamoDB** for data storage.

## Prerequisites

- **AWS Account**: You need an AWS account to deploy the infrastructure and services.
- **AWS CLI**: AWS Command Line Interface for managing AWS resources.
- **Node.js**: For running the Lambda functions if applicable.
- **AWS SDK**: To interact with AWS services in your code.

## Setup Guide

### 1. Deploying the AWS Resources
- **Lambda Function**: Deploy a Lambda function to process requests. You can set it up using the AWS Management Console or AWS SAM (Serverless Application Model).
- **DynamoDB**: Create a DynamoDB table to store data.
- **S3 Bucket**: Upload your static assets (HTML, CSS, JS files) to S3.
- **Route 53**: Configure Route 53 to route your domain's traffic to CloudFront.

### 2. Lambda Function Configuration
Set up your Lambda function to interact with DynamoDB and process requests. You can use the AWS SDK to interact with DynamoDB tables.

### 3. S3 and CloudFront Configuration
- Upload your frontend files (e.g., index.html, style.css) to the S3 bucket.
- Set up CloudFront to distribute content from your S3 bucket globally.

## Deployment

Follow these steps to deploy the application:

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/your-repository.git
    ```

2. Set up AWS resources:
    - Configure AWS CLI:
        ```bash
        aws configure
        ```

    - Deploy Lambda functions, DynamoDB, S3, and CloudFront using the provided templates or manually through the AWS Console.

## Usage

1. Open your browser and navigate to the domain configured with Route 53 and CloudFront.
2. The application will interact with Lambda and DynamoDB to serve dynamic data while static assets are served from S3.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- AWS for providing the infrastructure and services.
- Serverless framework for simplifying the deployment of Lambda functions.
