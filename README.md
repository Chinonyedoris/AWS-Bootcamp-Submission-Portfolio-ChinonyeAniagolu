# AWS-Bootcamp-Submission-Portfolio-ChinonyeAniagolu
Chinonyedoris.github.io.AWSCloud-Bootcamp-Submission/Portfolio
# This repository contains weekly deliverables from the AWS Cloud Bootcamp organized by CloudSec Network. Tasks include account setup, Identity Center configuration, and security role assignments.”


# Cloud Bootcamp Tasks – Week 1 to Week 9

Welcome to the official documentation of my AWS Bootcamp projects for **CloudSec Network (CSN)** covering deployment, monitoring, and securing static websites on AWS.

# Week 1 - AWS Account Setup
## Task
Set up an AWS account using a personal email address.

## Deliverable
Submitted below is a screenshot of my AWS Management Console showing proof of an active account.

## Status
✅ Completed

# Week 2 - AWS Identity Center & Permission Set Configuration

## Task
Set up AWS Identity Center:
- Created a new user
- Assigned the SecurityAudit permission set

## Deliverable
Screenshot below confirms the Identity Center setup and permission configuration.

## Status
✅ Completed

🚀 CloudSec Network Bootcamp – AWS Identity Center Setup ✅


As part of Week 2 of the CloudSec Network Bootcamp, I successfully configured AWS IAM Identity Center (formerly AWS SSO):

🔹 Set up a new user account
🔹 Assigned permission sets using SecurityAudit policies
🔹 Tested and submitted all deliverables via screenshot validation

This hands-on task deepened my understanding of:
🔐 Identity and access management (IAM)
🛡️ Security policies and permission sets
⚙️ Administrative cloud configurations

# 🚀 AWS Bootcamp Week 3 – EC2 Provisioning & Security

## 📌 Task Objective

Launch and configure a **Windows Server EC2 instance** using the **Amazon Windows Server 2025 Base AMI (or later)**, following these specifications:

- Deploy in a **public subnet**
- Configure **Security Group** to allow **RDP (port 3389)** only from your **public IP**
- Add a **Name tag** with value: `CSN-Bootcamp-Week3`

## 🛠️ Steps Performed

1. **Selected AMI**
   - Amazon Windows Server 2019 Base AMI

2. **Instance Configuration**
   - Instance type: `t2.micro` (Free Tier)
   - Network: Default VPC, Public Subnet
   - Enabled Auto-assign Public IP

3. **Security Group Setup**
   - Inbound rule:
     - Type: RDP
     - Port: 3389
     - Source: My IP Only

4. **Key Pair and Access**
   - Used existing or new key pair (.pem)
   - Retrieved password and connected via Remote Desktop

5. **Tagging**
   - Applied Name tag: `CSN-Bootcamp-Week3`

## ✅ Deliverables

- 📸 **Screenshot 1**: EC2 instance tagged `CSN-Bootcamp-Week3`
- 📸 **Screenshot 2**: Security Group with RDP (3389) open to your IP
- 📸 **Screenshot 3**: Successful Remote Desktop (RDP) login

## 📁 Project Structure (GitHub)

## ✅ AWS Bootcamp – Week 4: VPC & Subnet Configuration Achieved!

I successfully completed Week 4 of the CloudSec Network AWS Bootcamp, where I worked on simulating a multi-VPC architecture 🎯

### 🚀 Key Milestones:
🔹 Created two separate VPCs (VPC-A: 10.10.0.0/16 & VPC-B: 10.20.0.0/16)
🔹 Configured public & private subnets in both VPCs
🔹 Established VPC Peering between the two environments
🔹 Updated route tables to enable traffic flow
🔹 Captured console screenshots for validation and documentation
 
This hands-on experience strengthened my grasp of AWS Networking, Subnetting, and Cloud Infrastructure security. I'm one step closer to mastering AWS architecture! 🌐🔥

# 🚀 AWS Bootcamp Week 5 – Docker Container Deployment with ECS Fargate

This project is part of the CloudSec Network AWS Cloud Computing Bootcamp. In Week 5, the goal was to deploy a **Grafana Docker container** to **Amazon ECS using Fargate**.

---

## 📌 Project Overview

- **Task:** Deploy Grafana via Docker using Amazon ECS (Fargate).
- **Objective:** Use container orchestration to run a monitoring dashboard tool (Grafana) without managing servers.
- **Container Image:** `grafana/grafana`
- **Port:** 3000 (default Grafana UI port)

---

## ⚙️ Tools & Technologies

- **AWS ECS (Fargate)**
- **Docker**
- **IAM**
- **VPC/Subnet**
- **Security Groups**
- **Elastic Network Interface (ENI)**

---

## 📝 Deployment Steps

### 1. ECS Task Definition
- Created a new **Fargate Task Definition** named `grafana-task-definition`
- Defined container image: `grafana/grafana`
- Set **port mapping**: `3000:3000`

### 2. ECS Cluster
- Created ECS cluster named `grafana-cluster` (Fargate launch type)
- Deployed task into a **public subnet**

### 3. Networking & Security
- Configured a **Security Group** allowing **inbound TCP traffic on port 3000**
- Restricted access to **my public IP**
- Assigned task a public IP via ENI

### 4. Task Execution
- Launched task and confirmed **RUNNING** status
- Accessed the Grafana UI via:

> Default credentials: `admin` / `admin`

---

## 📷 Screenshots

> _Located in the `/screenshots` folder_

- ✅ ECS Cluster
- ✅ Task Definition Details
- ✅ Security Group Rules
- ✅ Grafana Login Page (Browser)

---

## ✅ Results

Successfully deployed Grafana in a containerized environment using AWS ECS Fargate. This project demonstrates my understanding of:

- Cloud-native deployments
- Docker containerization
- ECS Task Definition and Cluster setup
- Networking and secure access

---

## 📎 Resources

- [Grafana Docker Image](https://hub.docker.com/r/grafana/grafana)
- [AWS ECS Documentation](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html)

---
# 🚀 Week 6: Deploying Metabase with RDS on AWS ECS

This project contains the setup for deploying the Metabase dashboard on Amazon ECS (Fargate) and connecting it to an Amazon RDS PostgreSQL database.

## 📌 Tools Used
- AWS ECS (Fargate)
- AWS RDS (PostgreSQL)
- Docker (Metabase image)
- Security Groups, IAM, and VPC

## 🔧 Architecture
- ECS (Fargate) service runs the official `metabase/metabase` Docker image.
- RDS (PostgreSQL) stores Metabase metadata.
- Both are deployed in the same VPC with configured security groups.

## 🛡️ Security Group Rules
- **RDS Inbound:** TCP 5432 from ECS security group
- **ECS Outbound:** TCP 5432 to RDS

## 🌐 Access URL
Once deployed, Metabase is available
## 📸 Screenshots
- ✅ ECS Task Running
- ✅ RDS PostgreSQL Instance
- ✅ Security Group Rules (Port 5432)
- ✅ Metabase Login Page

## 💻 Environment Variables in ECS
```env
   MB_DB_TYPE=postgres
MB_DB_DBNAME=metabase
MB_DB_PORT=5432
MB_DB_USER=admin
MB_DB_PASS=yourpassword
MB_DB_HOST=<rds-endpoint>

## ✅ Week 7: Monitoring & Observability with CloudWatch

### 🎯 Task Overview
Deploy a containerized application on ECS using Fargate and monitor its performance using Amazon CloudWatch.

### 🛠️ Steps
1. **Deploy to ECS:**
   - Go to **ECS** → Create Cluster (Fargate)
   - Create Task Definition (e.g., Nginx/Grafana)
   - Assign CPU & Memory
   - Run service in a public subnet

2. **Create CloudWatch Dashboard:**
   - Navigate to **CloudWatch → Dashboards**
   - Add widgets:
     - ECS → CPUUtilization
     - ECS → MemoryUtilization

3. **Test & Simulate Load:**
   - Use tools like `curl` or [Loader.io](https://loader.io) to simulate traffic

### 📸 Deliverables
- ECS task/service running
- Task definition (CPU/Memory config)
- CloudWatch metrics dashboard
- (Optional) Simulated load screenshot

---

## ✅ Week 8: Deploy Static Website with S3 & CloudFront

### 🎯 Task Overview
Deploy a resume or portfolio static website using Amazon S3 and serve it securely using CloudFront.

### 🛠️ Steps
1. **Create S3 Bucket:**
   - Enable static website hosting
   - Upload `index.html`, `about.html`, etc.
   - Remove "Block All Public Access"

2. **Set Bucket Policy:**
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Sid": "PublicReadGetObject",
    "Effect": "Allow",
    "Principal": "*",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::your-bucket-name/*"
  }]
}

3. **Create CloudFront Distribution:**

Set S3 static site as the origin

Enable public access

Wait for distribution deployment


📸 Deliverables

Screenshot: S3 static site settings

Screenshot: Bucket policy config

Screenshot: CloudFront distribution setup

Screenshot: Live website via CloudFront


### ✅ Week 9: Securing Custom Domains with HTTPS

🎯 Task Overview

Register a free domain, set it up using Route 53, secure it with ACM (SSL), and link it to CloudFront with HTTPS support.

🛠️ Steps

1. Register Domain:

Go to freenom.com

Register a domain (e.g., myproject.tk)


2. Route 53 Setup:

Create a Hosted Zone

Copy NS records to Freenom’s nameservers


3. ACM Certificate:

Request a Public SSL certificate

Validate using DNS validation (CNAME)

Attach to CloudFront


4. Update CloudFront:

Add custom domain and SSL certificate

Confirm site loads over HTTPS


## 📸 Deliverables

Route 53 Hosted Zone setup

ACM certificate validation

CloudFront with domain & HTTPS

Final secure site screenshot


### 🌐 Tools Used

AWS ECS (Fargate)

CloudWatch

Amazon S3

CloudFront

Route 53

ACM (Certificate Manager)

Freenom

## Weekly Task 10 is about creating an Event-Driven Workflow with AWS Lambda.

## Here’s how you can complete it step-by-step:

## Step 1 – Create an S3 Bucket Log in to your AWS Management Console. Search for S3 and click Create bucket. Name the bucket (e.g., lambda-trigger-bucket), choose a region, and leave other settings as default. Click Create bucket. 

## Step 2 – Write Your Lambda Function In the AWS Console, go to Lambda → Create function. Choose Author from scratch. Name it (e.g., S3FileUploadHandler). Select Python or Node.js as the runtime. Create the function. 

## Step 3 – Create an S3 Event Trigger Go to your S3 bucket → Properties → Event notifications. Click Create event notification. Name it (e.g., OnFileUpload). Event type: PUT (Object Created). Destination: Select Lambda function → your function. Save changes. 

## Step 4 – Add Permissions In Lambda, under Configuration → Permissions, ensure your function has: AWSLambdaBasicExecutionRole Permission to read from S3 (s3:GetObject) If sending email via SES, ses:SendEmail 

## Step 5 – Optional Email Notification with SES 

If required by your task:

Go to Amazon SES → Verify your email. Add SES send code in your Lambda function to email a confirmation after file upload.

## Step 6 – Test the Workflow Upload a file to the S3 bucket. Check CloudWatch Logs for Lambda execution results. Take screenshots of: S3 bucket with event trigger. Lambda code/configuration. 

















## 🙌 Author

**Chinonye Doris Aniagolu**  
📧 [chinonyedoris@gmail.com](mailto:chinonyedoris@gmail.com)  
🌐 [GitHub Portfolio](https://chinonyedoris.github.io/AWS-Bootcamp-Submission-Portfolio-ChinonyeAniagolu/)  
🔗 [LinkedIn](https://linkedin.com/in/chinonyedoris-aniagolu-250603225)

---


