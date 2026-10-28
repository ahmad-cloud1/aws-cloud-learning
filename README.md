# ☁️ AWS Cloud Engineering Portfolio & Labs

Welcome to my cloud engineering repository. This space documents my transition into Cloud Engineering, showcasing production-ready architectures, Infrastructure as Code (IaC), automated CI/CD pipelines, and hands-on AWS lab environments. 

Rather than focusing on theoretical knowledge, this repository hosts functional code, deployment scripts, and architectural configurations designed according to the **AWS Well-Architected Framework**.

---

## 🛠️ Core Technical Stack

*   **Cloud Provider:** Amazon Web Services (AWS)
*   **Infrastructure as Code (IaC):** AWS CloudFormation, Bash Scripting
*   **CI/CD & Automation:** GitHub Actions, AWS CodePipeline
*   **Compute & OS:** Linux (Amazon Linux 2, Ubuntu), Amazon EC2, Auto Scaling, Elastic Load Balancing (ALB)
*   **Networking & Security:** Custom VPC, Public/Private Subnets, NAT Gateways, Security Groups, IAM Roles/Policies
*   **Storage & Databases:** Amazon S3 (Bucket Policies, Lifecycle Rules), Amazon RDS

---

## 🏗️ Featured Production-Ready Projects

### 🚀 Project 1: High-Availability Two-Tier Web Architecture via CloudFormation
*   **Directory:** [`/templates/ha-two-tier-vpc`](./)
*   **Architecture Components:** Custom VPC, 2x Public Subnets, 2x Private Subnets, Multi-AZ deployment, NAT Gateway, Application Load Balancer (ALB), Auto Scaling Group (ASG), Amazon RDS (MySQL).
*   **What this demonstrates:** 
    *   Writing declarative **AWS CloudFormation** templates to deploy repeatable infrastructure.
    *   Enforcing high availability and fault tolerance across multiple Availability Zones.
    *   Securing data by isolating the database tier in isolated private subnets.
    *   Configuring dynamic scaling policies based on CPU utilization.

### 🔄 Project 2: Automated CI/CD Pipeline for Linux/EC2 Deployments
*   **Directory:** [`/pipelines/ec2-app-deployment`](./)
*   **Architecture Components:** GitHub Actions / AWS CodePipeline, AWS CodeDeploy, Amazon S3, EC2, Linux Systemd.
*   **What this demonstrates:**
    *   Building automated **CI/CD pipelines** triggered on code push.
    *   Writing **Linux Bash scripts (`appspec.yml` hooks)** to automate application dependency installation, environment configuration, and service restarts.
    *   Managing secure cross-account/cross-service permissions utilizing **AWS IAM Roles**.

### 📦 Project 3: Secure Static Website Hosting & Asset Management
*   **Directory:** [`/storage/secure-s3-hosting`](./)
*   **Architecture Components:** Amazon S3, AWS CloudFront, S3 Bucket Policies, IAM Origin Access Control (OAC).
*   **What this demonstrates:**
    *   Configuring **Amazon S3** static website hosting with automated content synchronization.
    *   Securing the storage layer by blocking all public S3 access and forcing traffic exclusively through **Amazon CloudFront** using OAC.
    *   Implementing object lifecycle management rules to optimize cloud storage costs.

---

## 🐚 Linux & System Administration Utilities
*   **Directory:** [`/scripts/linux-sysadmin`](./)
*   A collection of shell scripts used to initialize and maintain EC2 instances:
    *   `bootstrap.sh`: Automates EC2 User Data initialization (updates packages, configures firewalls, installs Apache/Nginx).
    *   `cloudwatch-agent-config.sh`: Scripted installation and configuration of the CloudWatch agent to track custom Linux memory utilities.
    *   `backup-to-s3.sh`: Cron-compatible script that compresses local logs and syncs them directly to an encrypted S3 bucket.

---

## 📈 Technical Milestones & Roadmap
* [x] **IaC Native:** Migrated all manual console setups into structured CloudFormation templates.
* [x] **Linux Automation:** Eliminated manual instance configuration by relying entirely on Bash bootstrapping.
* [ ] **Next Goal:** Port existing CloudFormation templates into **Terraform** modules to demonstrate multi-provider IaC fluency.
* [ ] **Next Goal:** Introduce containerized workflows using Docker and AWS ECS (Fargate).

---


