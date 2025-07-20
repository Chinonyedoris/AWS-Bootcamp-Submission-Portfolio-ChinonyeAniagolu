# AWS-Bootcamp-Submission-Portfolio-ChinonyeAniagolu
Chinonyedoris.github.io.AWSCloud-Bootcamp-Submission/Portfolio
# This repository contains weekly deliverables from the AWS Cloud Bootcamp organized by CloudSec Network. Tasks include account setup, Identity Center configuration, and security role assignments.”
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

✅ AWS Bootcamp – Week 4: VPC & Subnet Configuration Achieved!

I successfully completed Week 4 of the CloudSec Network AWS Bootcamp, where I worked on simulating a multi-VPC architecture 🎯

🚀 Key Milestones:
🔹 Created two separate VPCs (VPC-A: 10.10.0.0/16 & VPC-B: 10.20.0.0/16)
🔹 Configured public & private subnets in both VPCs
🔹 Established VPC Peering between the two environments
🔹 Updated route tables to enable traffic flow
🔹 Captured console screenshots for validation and documentation

This hands-on experience strengthened my grasp of AWS Networking, Subnetting, and Cloud Infrastructure security. I'm one step closer to mastering AWS architecture! 🌐🔥

