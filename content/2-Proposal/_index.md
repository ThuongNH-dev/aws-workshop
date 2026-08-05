---
title: "Proposal"
date: 2026-05-18
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Splitly – Group Expense Sharing Platform
## An AWS-based solution for managing, sharing, and settling group expenses

### 1. Executive Summary
Splitly is a group expense management and sharing platform developed to help users track shared expenses, calculate balances, and manage settlement between members in a transparent and convenient way.

The system is built using a modern web architecture with React + Vite for the user interface, Node.js/Express for the backend service, and MongoDB Atlas as the database. The infrastructure is deployed on AWS, using Amazon EC2 to run both the backend and frontend, Amazon S3 to store receipts and supporting images, Amazon CloudWatch to monitor the system, and Amazon VPC together with Security Groups to ensure secure network connectivity.

The platform provides core features such as group management, expense recording and sharing, balance calculation, payment tracking, and electronic receipt storage. The architecture is designed to be scalable and suitable for small to medium-sized user groups.

### 2. Problem Statement
#### Current Problem

Group expense management is still mostly handled manually through spreadsheets or chat messages. As the number of members and expenses increases, tracking who has paid, who still owes money, and how much needs to be settled becomes complicated and error-prone.

Some common difficulties include:
- Managing many expenses within the same group.
- Calculating balances between members takes time and is easy to get wrong.
- There is no centralized storage for receipts when they need to be checked again.
- There is no clear mechanism for tracking payment status between debtors and recipients.
- It is difficult to monitor system activity and handle incidents after deployment.

#### The Solution

Splitly is built on AWS to digitalize group expense management. The system provides group management, expense recording, balance calculation, payment tracking, and receipt storage in one centralized platform, while using AWS services to ensure deployment, storage, and monitoring are handled efficiently.

#### Benefits and Return on Investment (ROI)

Deploying Splitly brings several benefits:
- Reduces the time needed to calculate and reconcile balances between members.
- Minimizes errors in expense splitting and settlement.
- Increases transparency through centralized transaction and payment status history.
- Supports electronic receipt storage, making lookup and verification easier.
- Improves system visibility through Amazon CloudWatch, helping with operations and incident handling.

### 3. Solution Architecture
The project uses a monolithic application architecture for the application layer, deployed centrally on AWS cloud infrastructure with 3 main layers:

### Presentation Layer – Frontend

* The React/Vite frontend is built into static files (HTML, CSS, and JavaScript).
* These files are stored directly on the EC2 server and served by the Nginx web server.
* When users access the website through the Elastic IP on port 80, Nginx loads and returns the interface to the browser.

### Application Layer – Backend

* Both the Node.js backend and the Nginx web server that serves the frontend are deployed on the same Amazon EC2 instance.
* The EC2 instance is located in a Public Subnet inside a VPC in the ap-southeast-1 Region.
* A Web Security Group controls which ports are allowed to access the EC2 instance, opening port 80 for web traffic and port 22 for SSH administration.
* The Internet Gateway creates a two-way connection between EC2 and the Internet.
* Nginx also acts as a Reverse Proxy to route REST API requests from the `/api` path to the backend running on port 5000, which is managed by PM2.
* This application layer also integrates directly with third-party Internet services such as VNPay and Gmail SMTP.

### Data Layer

* Business data such as user information, groups, expenses, payment transactions, complaints, and notifications is stored securely in the external database management system MongoDB Atlas.
* Payment receipt images or files are uploaded and stored separately in an Amazon S3 Receipts Bucket.
* MongoDB stores only metadata such as file name, object key, URL, or processing status, instead of storing physical files directly, in order to optimize cost and performance.

### Security, Monitoring and Cost Management

* **IAM Role:** EC2 is assigned an IAM Role to allow uploading files to the S3 Receipts Bucket and sending data to CloudWatch, ensuring security because no Access Key or Secret Key needs to be stored on the server.
* **Configuration Management:** Sensitive information such as MongoDB URI, JWT secret, Gmail configuration, and VNPay keys is configured through environment variables stored securely in the `.env` file on EC2.
* **Monitoring:** Amazon CloudWatch is used to collect basic metrics and system logs, track EC2 and application status, and trigger alerts through Amazon SNS when errors or threshold violations occur.
* **Cost Management:** AWS Budgets continuously monitors resource spending and automatically sends alerts via email or SNS if the project’s estimated budget is exceeded.

### 3.1 Current Architecture
![Architecture](/images/2-Proposal/Architecture_Final.png)

### AWS Services Used

* **Amazon S3:** Stores receipt files uploaded by users.
* **Amazon EC2:** Runs the backend API and processes system business logic.
* **AWS IAM:** Grants EC2 permission to access required AWS resources.
* **Amazon CloudWatch:** Collects logs, monitors EC2, and detects incidents.
* **Amazon SNS:** Sends email or alert notifications from CloudWatch and AWS Budgets.
* **AWS Budgets:** Tracks spending and warns when the budget is exceeded.

### Component Design

* **Web Interface & Proxy:** The frontend application (React/Vite) is built into static files and served directly by the Nginx server running on Amazon EC2. Nginx also acts as a Reverse Proxy to route API requests from users to the backend.

* **Business Processing (Backend):** Amazon EC2, sharing the same server with the web interface, runs the backend API through Node.js/PM2 and handles authentication, group management, expenses, payments, receipts, disputes, and notifications.

* **Data Storage:** MongoDB Atlas stores the core data including user information, groups, expenses, settlements, disputes, and notifications.

* **Receipt Storage:** Amazon S3 (Receipts Bucket) stores receipt images and uploaded files, reducing local storage usage on EC2.

* **Network Connectivity:** Amazon VPC, Public Subnet, Internet Gateway, and Elastic IP form the network foundation, supporting EC2 access from users, file uploads to S3, connectivity to MongoDB Atlas, and requests to external services such as VNPay and Gmail SMTP.

* **System Security:** The Web Security Group acts as a firewall, restricting which ports and network sources can access EC2, for example allowing only port 80 for web traffic and 22 for SSH administration.

* **Configuration & Secret Management:** Sensitive system information such as MongoDB URI, JWT Secret, Gmail credentials, and VNPay keys is stored through environment variables in the `.env` file directly on EC2.

* **Access Control:** An AWS IAM Role grants least-privilege permissions to the EC2 server so it can access the S3 Receipts Bucket and CloudWatch securely without storing Access Keys on the server.

* **System Monitoring:** Amazon CloudWatch runs in the background to collect application logs, monitor EC2 resource status such as CPU, RAM, and Disk, and create alerts when incidents are detected.

* **Alert Delivery:** Amazon SNS acts as the delivery channel, sending email or notification messages from CloudWatch and AWS Budgets to the administrator.

* **Cost Management:** AWS Budgets continuously tracks AWS infrastructure spending and triggers alerts when usage reaches or exceeds the configured budget threshold.

### 3.2 Proposed Future Architecture

The figure below describes the upgraded architecture proposed for Splitly in the future. This architecture is not part of the current deployment scope, but it is intended as the next development stage of the system.

![Architecture_Update](/images/2-Proposal/Architecture_Update.png)

In the proposed architecture, the frontend application is separated from the backend server. The React/Vite frontend is built into static files and stored in an Amazon S3 Frontend Bucket. Amazon CloudFront is used to distribute the frontend content to users, reducing latency and improving page load speed.

Amazon Route 53 is used to manage the domain name and route users to the system. AWS WAF is placed in front of CloudFront to protect the application from common web attacks. AWS Certificate Manager is used to manage SSL/TLS certificates, allowing the system to provide secure HTTPS connections.

The backend application continues to be deployed on an Amazon EC2 instance in the Public Subnet of Amazon VPC. The backend is responsible for business logic, REST API services, MongoDB Atlas integration, and uploading receipt files to the Amazon S3 Receipts Bucket.

Amazon S3 Receipts Bucket is used separately to store receipt images and uploaded files. Separating the Frontend Bucket and Receipts Bucket makes data management clearer and allows appropriate access policies for each resource type.

Amazon CloudWatch is used to collect infrastructure metrics and application logs. Amazon SNS is responsible for sending operational alerts to the administrator, while AWS Budgets monitors resource spending and sends notifications when the spending level approaches or exceeds the configured budget.

AWS IAM is used to manage access permissions between EC2 and AWS services. EC2 is assigned an IAM Role so the backend can access S3 and CloudWatch without storing Access Keys and Secret Access Keys directly on the server.

### 3.3 Expected Improvements

Compared with the current architecture, the proposed future architecture brings the following improvements:

+ **Frontend and backend separation:** Static frontend files are moved from EC2 to Amazon S3, allowing EC2 to focus on API processing and backend business logic.

+ **Better performance:** Amazon CloudFront caches and delivers frontend content through edge locations, reducing page load time for users.

+ **Custom domain support:** Amazon Route 53 allows users to access Splitly through a domain name instead of directly using the Elastic IP address.

+ **HTTPS support:** AWS Certificate Manager manages SSL/TLS certificates, helping encrypt data transmitted between users and the system.

+ **Improved web application security:** AWS WAF helps filter and control requests before they reach CloudFront and downstream components.

+ **Reduced EC2 load:** Serving the frontend through Amazon S3 and CloudFront reduces the amount of traffic and work the EC2 server has to handle.

+ **Clearer storage management:** The Frontend Bucket is used for static interface files, while the Receipts Bucket is used separately for user-uploaded files.

+ **Better scalability:** The frontend and backend can be upgraded or scaled independently depending on system usage.

+ **Improved monitoring:** Amazon CloudWatch, Amazon SNS, and AWS Budgets help the team track system status, receive incident alerts, and control costs more effectively.

This architecture creates a foundation for future expansion of Splitly, such as adding an Application Load Balancer, Auto Scaling, Amazon Cognito, AWS Lambda, or CI/CD deployment pipelines.

### 4. Technical Implementation
Clone the source code from GitHub to the EC2 server and configure sensitive environment variables in the `.env` file. Install and build the frontend (React/Vite), and configure Nginx to serve static files and act as a reverse proxy. Build the backend (Node.js/Express) and keep it running with PM2; connect the backend successfully to MongoDB, the S3 Receipts Bucket, and third-party services (VNPay, Gmail). Finally, test the API, receipt upload functionality, log monitoring, and bring the system into production.

### Technical Requirements (Updated Version)

#### Architecture and Infrastructure

The system is deployed in the AWS Singapore Region (ap-southeast-1). The entire application (frontend and backend) is stored and operated centrally on a single Amazon EC2 instance inside the Public Subnet of a VPC.

#### Technologies

* **Frontend:** React, TypeScript, and Vite.
* **Backend:** Node.js, Express, and TypeScript, providing REST APIs.
* **Web Server & Process Manager:** Nginx is used as the Web Server and Reverse Proxy; PM2 is used to manage and automatically restart the backend process.

#### Source Code Management and Deployment

The source code is managed on GitHub. The deployment process, including dependency installation and code building, is performed directly on the EC2 environment through the command line.

#### Data and Storage

Core business data is securely stored in MongoDB Atlas. Static files such as images and receipts uploaded by users are pushed to Amazon S3 Receipts Bucket to optimize storage.

#### Network and Connectivity

The EC2 instance communicates with the Internet through an Internet Gateway and Elastic IP. Security Groups are configured to allow port 80 (HTTP) for web traffic and port 22 (SSH) for administration. Nginx routes traffic by serving static frontend files or proxying API requests to the backend running on internal port 5000.

#### Security and Access Control

Sensitive information such as Database URI, JWT Secret, and integration keys is protected through environment variables stored in the `.env` file. The EC2 instance is assigned an IAM Role to access the S3 Receipts Bucket and CloudWatch following the principle of least privilege.

#### Monitoring and Alerts

Amazon CloudWatch is configured to collect server metrics and application logs. Amazon SNS works as the notification channel and sends alerts to the administrator when the system encounters incidents or when resources become overloaded.

#### Cost Management

AWS Budgets continuously monitors the cost of the AWS ecosystem and automatically sends alerts when spending reaches or exceeds the configured budget limit.

#### Non-functional Requirements

The system is deployed in the Singapore region to optimize performance and reduce latency for users in Vietnam. The EC2-based architecture is fully suitable for a student project budget and can be scaled up in RAM or CPU if traffic increases.

### 5. Timeline & Milestones
The project is implemented in 4 main phases over approximately 3 months to ensure development, testing, and deployment are carried out systematically.

#### Phase 1 – Requirements Analysis and System Design (Week 5 - Week 6)

* Analyze the business requirements of the group expense management system.
* Design the overall AWS architecture.
* Design the MongoDB Atlas database.
* Build the user interface and backend architecture.

#### Phase 2 – Feature Development (Week 7 - Week 8)

* Develop the Frontend using React + Vite.
* Develop APIs using Node.js and Express.
* Integrate MongoDB Atlas.
* Build the core features:

  * Authentication
  * Group Management
  * Expense Management
  * Settlement
  * Receipt Upload

#### Phase 3 – AWS Deployment (Week 9 - Week 10)

* Create Amazon EC2 instances.
* Configure VPC, Security Group, and Elastic IP.
* Deploy the Backend and Frontend to EC2.
* Create an Amazon S3 Bucket for receipt storage.
* Configure IAM Role.
* Set up CloudWatch Monitoring.

#### Phase 4 – Testing and Finalization (Week 11 - Week 12)

* Test system functions.
* Test APIs.
* Test receipt upload functionality.
* Check logging and monitoring.
* Optimize AWS costs.
* Complete documentation and the final report.

### 6. Budget Estimation
The system is designed for a small-scale learning and testing purpose, therefore the project prioritizes AWS Free Tier services and low-cost AWS services whenever possible.

### Expected Infrastructure Costs

* **Amazon EC2:** $0.00/month (using a t3.micro instance under AWS Free Tier, 750 hours/month. Used to run both Nginx and the Node.js backend).

* **Amazon S3 Standard:** $0.10/month (estimated 5 GB of storage for the Receipts Bucket, with around 2,000 PUT/GET requests).

* **Amazon CloudWatch:** $0.03/month (pushing basic EC2 monitoring metrics and storing application logs).

* **Amazon SNS:** $0.00/month (estimated 100 alert emails per month, fully within Free Tier).

* **Amazon VPC:** $0.00/month (includes 1 VPC, Public Subnet, Internet Gateway, Route Table, and Security Group).

* **Elastic IP:** $3.65/month (AWS charges $0.005/hour for public IPv4 addresses, including the Elastic IP attached to EC2).

* **AWS IAM:** $0.00/month (managing IAM Roles and access permissions for the system).

**Estimated Total Cost:** About $3.78/month, equivalent to $45.36/12 months.

During development, the team plans to maximize the use of AWS Free Tier, combined with storing security-related configuration directly on the server through the `.env` file, in order to minimize operating costs. After the system becomes stable, the actual cost will be monitored continuously via AWS Budgets and can be recalculated using the AWS Pricing Calculator if real user traffic exceeds the initial estimate.

### 7. Risk Assessment
#### Risk Matrix
- **EC2 failure:** High impact, low probability.
- **MongoDB Atlas connection loss:** High impact, low probability.
- **Receipt upload failure:** Medium impact, low probability.
- **Secret information leak:** High impact, medium probability.
- **Incorrect Security Group configuration:** High impact, low probability.
- **Exceeding AWS Free Tier budget:** Medium impact, medium probability.

#### Mitigation Strategies
- Set up CloudWatch and SNS to monitor EC2 health.
- Set up AWS Budgets to alert when costs exceed the threshold.
- Use IAM Roles instead of Access Keys when accessing AWS services.
- Configure Security Groups with the principle of least privilege, opening only the necessary ports.
- Regularly check the connection between EC2 and MongoDB Atlas.

#### Contingency Plans
- Restart or redeploy EC2 from source code when an incident occurs.
- Restore receipt data from Amazon S3.
- Restore configuration from the GitHub repository.
- Switch to MongoDB Atlas Backup if the database has an issue.
- Adjust service configuration or limit resources if the cost exceeds the budget.

### 8. Expected Outcomes
#### Technical Outcomes

- Successfully build the Splitly system running stably on AWS, supporting group management, expense management, settlement, and receipt storage.
- Deploy the application on Amazon EC2, store receipts in Amazon S3, and connect to MongoDB Atlas for data management.
- Set up Amazon CloudWatch, Amazon SNS, and AWS Budgets to monitor the system, send alerts, and control operating costs.
- Apply IAM Roles and Security Groups to improve security, while ensuring the system can scale in the future.

#### Value Delivered

- Helps users manage group spending transparently and reduces mistakes during calculation and settlement.
- Supports centralized receipt storage, making lookup and verification easier when needed.
- Provides a platform that can continue expanding with AWS services such as CloudFront, Route 53, AWS WAF, Auto Scaling, or CI/CD in future development stages.
- Serves as a real product for learning, research, and a possible foundation for future group finance management projects.
