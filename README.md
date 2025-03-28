# AWS-3-Tier-Architecture-Deployment
## Description:
This project consist of hands-on walk through of a three-tier web architecture in AWS. We will be manually creating the necessary network, security, app, and database components and configurations in order to run this architecture in an available and scalable manner.
## Pre-requisites:
1. You have at least some foundational aws knowledge around VPC, EC2, RDS, S3, ELB and the AWS Console.
2. An AWS account.
3. IDE or text editor of your choice in order to make some changes in the files during the project.
## Architecture Overview:
![3 Tier Architecture](https://github.com/user-attachments/assets/06de2eb2-8bc1-43dd-9968-0076889c6307)
In this architecture, a public-facing Application Load Balancer forwards client traffic to our web tier EC2 instances. The web tier is running Nginx webservers that are configured to serve a React.js website and redirects our API calls to the application tier’s internal facing load balancer. The internal facing load balancer then forwards that traffic to the application tier, which is written in Node.js. The application tier manipulates data in an Aurora MySQL multi-AZ database and returns it to our web tier. Load balancing, health checks and autoscaling groups are created at each layer to maintain the availability of this architecture.
## Project Step by Step Instructions:
