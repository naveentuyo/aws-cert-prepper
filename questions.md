# Quiz Question Bank
# 
# FORMAT:
# Each question block starts with "## Q" followed by a number.
# Lines starting with "- [ ]" are answer choices (A, B, C, D, etc.)
# The correct answer(s) have "[x]" instead of "[ ]"
# The "### Explanation" section provides the detailed explanation.
# For multi-select questions, mark multiple choices with "[x]".
# Separate each question with "---"
#
# EXAMPLE:
#
#   [Q1] What does EC2 stand for?
#   [ ] A) Elastic Cloud Compute
#   [x] B) Elastic Compute Cloud
#   [ ] C) Easy Compute Cloud
#   [ ] D) Elastic Container Cloud
#   [Explanation] EC2 stands for Elastic Compute Cloud.
#

## Q1. A company wants to run applications in the AWS Cloud but does not want to manage the underlying infrastructure. Which AWS service should they use?
- [ ] A) Amazon EC2
- [x] B) AWS Elastic Beanstalk
- [ ] C) Amazon VPC
- [ ] D) AWS CloudFormation
### Explanation
AWS Elastic Beanstalk is a Platform-as-a-Service (PaaS) that automatically handles infrastructure provisioning, load balancing, scaling, and application health monitoring. Amazon EC2 requires managing the underlying infrastructure. Amazon VPC is a networking service. AWS CloudFormation is an infrastructure-as-code tool.
---

## Q2. Which AWS service provides a managed relational database that supports multiple database engines including MySQL, PostgreSQL, and Oracle?
- [ ] A) Amazon DynamoDB
- [ ] B) Amazon Redshift
- [ ] C) Amazon ElastiCache
- [x] D) Amazon RDS
### Explanation
Amazon RDS (Relational Database Service) is a managed service supporting MySQL, PostgreSQL, Oracle, SQL Server, MariaDB, and Amazon Aurora. DynamoDB is NoSQL. Redshift is a data warehouse. ElastiCache is an in-memory caching service.
---

## Q3. Which AWS service provides serverless compute for running code without provisioning servers?
- [ ] A) Amazon ECS
- [x] B) AWS Lambda
- [ ] C) Amazon EC2
- [ ] D) Amazon EKS
### Explanation
AWS Lambda is a serverless compute service that runs code in response to events without provisioning or managing servers. You pay only for compute time consumed. ECS and EKS are container orchestration services. EC2 requires provisioning virtual servers.
---

## Q4. Under the AWS Shared Responsibility Model, which of the following is the customer's responsibility?
- [ ] A) Physical security of data centers
- [ ] B) Patching the hypervisor
- [ ] C) Maintaining network infrastructure
- [x] D) Configuring security groups
### Explanation
Configuring security groups is a customer responsibility. Security groups act as virtual firewalls for EC2 instances, and customers must configure inbound/outbound rules. Physical security, hypervisor patching, and network infrastructure are all AWS responsibilities.
---

## Q5. Which of the following are advantages of the AWS Cloud? (Select TWO)
- [x] A) Eliminate guessing on capacity needs
- [x] B) Increase speed and agility
- [ ] C) Trade variable expense for fixed expense
- [ ] D) Require long-term contracts
- [ ] E) Maintain physical data center access
### Explanation
Eliminate guessing on capacity needs — cloud allows scaling up or down based on demand. Increase speed and agility — resources can be provisioned in minutes. Option C is backwards (cloud trades fixed for variable). Options D and E are not cloud advantages.
---
