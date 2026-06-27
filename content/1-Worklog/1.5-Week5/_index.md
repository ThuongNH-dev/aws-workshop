---
title: "Week 5 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---

### Week 5 Objectives:

* Learn about the AWS Shared Responsibility Model.
* Learn about AWS Identity and Access Management (IAM).
* Practice managing users, groups, and permissions in AWS.
* Learn about authentication, authorization, and encryption key management services on AWS.
* Explore centralized account management and security services in AWS.

### Tasks to be carried out this week:

| Day | Tasks                                                                                                                                                                                                                                                                                                                      | Start Date | Completion Date | Resources                                                          |
| --- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------ |
| Mon | - Learn about the AWS Shared Responsibility Model <br> - Learn about AWS IAM components: <br>  + Root Account <br>  + IAM User <br>  + IAM Group <br>  + IAM Policy <br>  + IAM Role <br> - **Hands-on Lab:** <br>  + Create IAM Groups and IAM Users <br>  + Create IAM Roles <br>  + Assume Roles                        | 15/06/2026 | 15/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Tue | - Learn about IAM authorization mechanisms <br> - Learn about IAM Conditions: <br>  + IP Address Restrictions <br>  + Time-based Access Restrictions <br> - **Hands-on Lab:** <br>  + Create EC2 Administrator User <br>  + Create RDS Administrator User <br>  + Create Administrator Group <br>  + Configure Switch Role | 16/06/2026 | 16/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Wed | - Learn about Permission Boundaries <br> - Learn about the Principle of Least Privilege <br> - **Hands-on Lab:** <br>  + Create Permission Boundary Policies <br>  + Create Restricted IAM Users <br>  + Verify Permission Restrictions                                                                                    | 17/06/2026 | 17/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Thu | - Learn about Access Keys and AWS CLI Authentication <br> - Learn about IAM Roles for Amazon EC2 <br> - Learn about Amazon Cognito: <br>  + User Pools <br>  + Identity Pools <br> - **Hands-on Lab:** <br>  + Use Access Keys <br>  + Attach IAM Roles to EC2 Instances                                                   | 18/06/2026 | 18/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| Fri | - Learn about AWS Organizations <br> - Learn about Service Control Policies (SCP) <br> - Learn about AWS Identity Center (SSO) <br> - Learn about AWS KMS and Customer Managed Keys (CMK) <br> - Learn about AWS Security Hub and AWS security best practices                                                              | 19/06/2026 | 19/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |

### Week 5 Achievements:

* Understand the AWS Shared Responsibility Model and the division of security responsibilities between AWS and customers.

* Understand the architecture and access management mechanisms of AWS IAM.

* Gain knowledge of the core IAM components:

  * Root Account
  * IAM User
  * IAM Group
  * IAM Policy
  * IAM Role

* Understand the Principle of Least Privilege and its importance in access management.

* Understand the IAM policy evaluation logic and the priority of Explicit Deny over Allow permissions.

* Learn how to use IAM Conditions to control access based on:

  * IP address restrictions
  * Time-based access restrictions

* Understand the concepts of Assume Role and Switch Role in AWS environments.

* Understand the purpose and usage of Permission Boundaries to limit the maximum permissions granted to IAM Users.

* Learn how Access Keys are used for programmatic access and understand the associated security considerations.

* Understand the advantages of using IAM Roles for Amazon EC2 instead of embedding Access Keys.

* Gain an understanding of Amazon Cognito components:

  * User Pool
  * Identity Pool

* Understand how AWS Organizations can be used to centrally manage multiple AWS accounts.

* Learn the role of Service Control Policies (SCPs) in governance and account-level permission management.

* Understand how Single Sign-On (SSO) can be implemented using AWS Identity Center.

* Learn how AWS KMS manages encryption keys and understand the use of Customer Managed Keys (CMKs).

* Understand the purpose of AWS Security Hub and its role in monitoring security compliance and best practices.

* Successfully complete hands-on labs including:

  * Creating IAM Users and IAM Groups
  * Creating and assuming IAM Roles
  * Creating EC2 and RDS administrator users
  * Configuring IAM Conditions
  * Configuring Switch Role
  * Creating Permission Boundaries
  * Using Access Keys
  * Assigning IAM Roles to EC2 instances

* Be able to design and implement identity and access management strategies following AWS security best practices.