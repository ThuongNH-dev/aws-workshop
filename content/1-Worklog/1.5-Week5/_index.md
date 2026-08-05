---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Objectives of Week 5:

* Learn about the AWS Shared Responsibility Model.
* Study AWS Identity and Access Management (IAM).
* Practice user, group, and permission management in AWS.
* Learn authentication, authorization, and encryption key management mechanisms in AWS.
* Explore AWS services for centralized administration and security.
* Analyze the business requirements of the Group Expense Management System.
* Identify the main features and project scope.
* Draft the overall system architecture to be deployed on AWS.

### Tasks for This Week:

| Day | Tasks | Start Date | End Date | References |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | ------------------------------------------------------------ |
| Mon | - Study the AWS Shared Responsibility Model <br> - Learn AWS IAM: <br>  + Root Account <br>  + IAM User <br>  + IAM Group <br>  + IAM Policy <br>  + IAM Role <br> - **Practice:** <br>  + Create IAM Groups and IAM Users <br>  + Create IAM Roles <br>  + Assume Roles <br> - Analyze the business requirements of the Group Expense Management System. <br> - Identify the main functional modules of the system. | 15/06/2026 | 15/06/2026 | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Tue | - Learn IAM authorization mechanisms <br> - Study IAM Conditions: <br>  + IP Address restriction <br>  + Time-based access restriction <br> - **Practice:** <br>  + Create EC2 Administrator User <br>  + Create RDS Administrator User <br>  + Create Administrator Group <br>  + Configure Switch Role <br> - Design the Use Case Diagram. <br> - Identify actors and major business workflows. | 16/06/2026 | 16/06/2026 | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Wed | - Learn Permission Boundary <br> - Study the Least Privilege Principle <br> - **Practice:** <br>  + Create restricted IAM Policies <br>  + Create limited IAM Users <br>  + Verify restricted user permissions <br> - Analyze the AWS deployment architecture. <br> - Select appropriate AWS services for the system. | 17/06/2026 | 17/06/2026 | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Thu | - Learn Access Keys and AWS CLI Authentication <br> - Learn IAM Roles for Amazon EC2 <br> - Study Amazon Cognito: <br>  + User Pool <br>  + Identity Pool <br> - **Practice:** <br>  + Authenticate using Access Keys <br>  + Attach IAM Roles to EC2 <br> - Design the high-level system architecture. <br> - Identify Frontend, Backend, and Cloud components. | 18/06/2026 | 18/06/2026 | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Fri | - Learn AWS Organizations <br> - Learn Service Control Policies (SCP) <br> - Learn AWS Identity Center (SSO) <br> - Learn AWS KMS and Customer Managed Keys (CMK) <br> - Learn AWS Security Hub and AWS security best practices <br> - Prepare for MongoDB Atlas database design and Backend architecture implementation in Week 6. | 19/06/2026 | 19/06/2026 | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |

### Week 5 Achievements:

* Understood the AWS Shared Responsibility Model and the responsibilities between AWS and customers.

* Understood the architecture and access management mechanism of AWS IAM.

* Learned the key IAM components:

  * Root Account
  * IAM User
  * IAM Group
  * IAM Policy
  * IAM Role

* Understood the Least Privilege Principle.

* Understood Explicit Deny and IAM Policy evaluation order.

* Learned how to use IAM Conditions to control access:

  * IP Address restriction
  * Time-based access restriction

* Understood the Assume Role and Switch Role mechanisms in AWS.

* Learned the purpose and usage of Permission Boundaries for limiting IAM User permissions.

* Understood Access Key authentication and its associated security risks.

* Understood the advantages of using IAM Roles for EC2 instead of Access Keys.

* Learned the functionality of Amazon Cognito:

  * User Pool
  * Identity Pool

* Understood how to manage multiple AWS accounts using AWS Organizations.

* Learned the role of Service Control Policies (SCP) in centralized governance.

* Understood Single Sign-On (SSO) using AWS Identity Center.

* Learned how to manage encryption keys using AWS KMS and Customer Managed Keys (CMK).

* Understood the security monitoring and compliance capabilities of AWS Security Hub.

* Completed hands-on labs:

  * Create IAM Users and IAM Groups
  * Create IAM Roles and Assume Roles
  * Create EC2 and RDS administrator users
  * Configure IAM Conditions
  * Configure Switch Roles
  * Create Permission Boundaries
  * Authenticate using Access Keys
  * Attach IAM Roles to EC2

* Gained the ability to design and implement identity and access management models on AWS.

* Completed the business requirement analysis for the Group Expense Management System.

* Identified the core features of the system:

  * Group management
  * Member management
  * Expense management
  * Balance tracking
  * Statistics and reporting

* Completed the Use Case analysis and major business workflows.

* Designed the high-level AWS system architecture.

* Identified the overall deployment model, including the Frontend, Backend, and Cloud infrastructure.

* Prepared for MongoDB Atlas database design and Backend architecture development.