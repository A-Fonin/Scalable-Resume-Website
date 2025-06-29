# Scalable-Resume-Website
AWS Portfolio Capstone Project – EC2 to Serverless Migration

## 🧭 Overview

This project is a **cloud-native portfolio website** designed to showcase both my resume and AWS technical capabilities. It was developed as part of the **SAA1 Capstone Project** to demonstrate my ability to design, deploy, and migrate a monolithic application to a modern, serverless architecture using core AWS services.

The project mimics a real-world migration scenario where an on-premises, monolithic web application is re-architected for the cloud in two major phases:

- **Stage 1**: EC2-based, highly available deployment  
- **Stage 2**: Migration to a fully serverless, static site hosted on S3

---

## 🚀 Project Goals

- Deploy a scalable and fault-tolerant portfolio website using EC2, ALB, and Route 53
- Integrate cloud-native microservices using Lambda, API Gateway, DynamoDB, and EventBridge
- Secure the application using IAM roles, Security Groups, and best practices
- Migrate to a fully serverless static website hosted on S3 and served via CloudFront
- Demonstrate clean architectural design, automation, and documentation

---

## 🏗️ Architecture

### Stage 1 – EC2-Based Architecture

- **EC2 (Amazon Machine Image)**: Monolithic app launched via a public AMI
- **Auto Scaling Group** with Launch Template
- **Application Load Balancer (ALB)**
- **CloudFront** for global CDN caching
- **Route 53** for DNS resolution
- **VPC** with public/private subnets and NAT Gateway
- **Microservices Integration** via Lambda Function URLs and HTTP APIs

### Stage 2 – Serverless Architecture

- **S3 Static Website** hosting HTML/CSS/JS assets
- **CloudFront** distribution with custom domain
- **Route 53** DNS routing to CloudFront
- **Microservices** (unchanged from Stage 1):
  - Blog Post Service
  - Contact Form Submission
  - AWS Latest News Feed
  - View Counter

---

## 🧩 Technologies Used

- **Compute**: EC2, AWS Lambda
- **Networking**: VPC, ALB, Route 53
- **Storage**: S3, DynamoDB
- **Serverless Integration**: API Gateway (HTTP APIs), Lambda Function URLs, EventBridge
- **Security**: IAM, Security Groups, least privilege
- **Automation**: CloudFormation (for all microservices)
- **DevOps Tools**: Git, GitHub, VS Code

---

## 📂 Project Structure

```bash
.
├── cloudformation-templates/
│   ├── blog.yaml
│   ├── contactform.yaml
│   ├── viewcounter.yaml
│   └── awslatestnews.yaml
├── assets/
│   └── screenshots/
├── src/
│   ├── html/
│   ├── css/
│   └── js/
├── .gitignore
├── README.md
└── architecture-diagram.png

