---
title: "Workshop"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Deploying the Splitly Application on AWS Using CloudFormation and EC2

#### Overview

In this workshop, we will deploy the **Splitly** application on AWS using **AWS CloudFormation** to automatically provision the required infrastructure.

After the infrastructure is created, we will connect to the **Amazon EC2** instance through **AWS Systems Manager Session Manager** and deploy both the backend and frontend of the application.

The main activities in this workshop include:

+ Using **AWS CloudFormation** to deploy the infrastructure.
+ Connecting to the EC2 instance using **Session Manager**.
+ Cloning the Splitly source code from GitHub.
+ Installing dependencies and building the backend.
+ Running the backend using **PM2**.
+ Building the frontend.
+ Configuring **Nginx** to serve the frontend and forward API requests to the backend.
+ Testing the status and operation of the entire system.
+ Deleting the CloudFormation stack after completing the workshop to avoid unnecessary charges.

#### Content

1. [Workshop Overview](5.1-workshop-overview/)
2. [Prerequisites](5.2-Prerequiste/)
3. [DeployCode-WebServer](5.3-deploycode-webserver/)
4. [System Testing](5.4-test/)
5. [Resource Cleanup](5.5-cleanup/)
