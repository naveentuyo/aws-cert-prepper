# AWS Certified Cloud Practitioner (CLF-C02) — Practice Test 1
#
# Total Questions: 50
# Passing Score: 70% (35/50)
# Time Limit: 90 minutes

## Q1. Which AWS service allows you to provision a logically isolated section of the AWS Cloud where you can launch resources in a virtual network?
- [ ] A) AWS Direct Connect
- [ ] B) Amazon Route 53
- [x] C) Amazon VPC
- [ ] D) AWS Transit Gateway
### Explanation
Amazon VPC (Virtual Private Cloud) lets you create a logically isolated virtual network where you define IP ranges, subnets, route tables, and gateways. AWS Direct Connect (A) is a dedicated physical connection. Route 53 (B) is a DNS service. Transit Gateway (D) connects multiple VPCs and on-premises networks.
---

## Q2. A company wants to run batch processing jobs that can be interrupted without impacting business operations. Which EC2 pricing model offers the greatest cost savings?
- [ ] A) On-Demand Instances
- [ ] B) Reserved Instances
- [ ] C) Dedicated Hosts
- [x] D) Spot Instances
### Explanation
Spot Instances offer up to 90% discount compared to On-Demand pricing but can be interrupted with a 2-minute warning. They are ideal for fault-tolerant, flexible workloads like batch processing. On-Demand (A) has no discount. Reserved (B) requires commitment. Dedicated Hosts (C) are the most expensive option.
---

## Q3. Which AWS service is a fully managed data warehouse designed for large-scale data analytics?
- [x] A) Amazon Redshift
- [ ] B) Amazon DynamoDB
- [ ] C) Amazon RDS
- [ ] D) Amazon ElastiCache
### Explanation
Amazon Redshift is a fully managed, petabyte-scale data warehouse service designed for online analytical processing (OLAP). DynamoDB (B) is a NoSQL database. RDS (C) is a managed relational database. ElastiCache (D) is an in-memory caching service.
---

## Q4. Under the AWS Shared Responsibility Model, which of the following is AWS responsible for?
- [ ] A) Encrypting application data at rest
- [x] B) Physical security of data centers
- [ ] C) Managing IAM user permissions
- [ ] D) Configuring network ACLs
### Explanation
Physical security of data centers is an AWS responsibility. AWS manages the security OF the cloud, including hardware, facilities, and networking infrastructure. Encrypting application data (A), managing IAM permissions (C), and configuring network ACLs (D) are all customer responsibilities.
---

## Q5. A company needs to send transactional emails and SMS messages to customers at scale. Which AWS service should they use?
- [ ] A) Amazon SQS
- [x] B) Amazon SNS
- [ ] C) Amazon Kinesis
- [ ] D) AWS Step Functions
### Explanation
Amazon SNS (Simple Notification Service) is a pub/sub messaging service that sends notifications via email, SMS, HTTP/HTTPS, and other protocols. SQS (A) is a message queue for decoupling components. Kinesis (C) processes streaming data. Step Functions (D) orchestrates workflows.
---

## Q6. Which of the following best describes the AWS pricing principle of "pay-as-you-go"?
- [ ] A) You pay a fixed monthly fee regardless of usage
- [ ] B) You commit to a minimum usage level for a discount
- [x] C) You pay only for the resources you consume with no upfront costs
- [ ] D) You purchase hardware capacity in advance
### Explanation
Pay-as-you-go means you only pay for the individual services you need, for as long as you use them, without long-term contracts or upfront commitments. Fixed fees (A), minimum commitments (B), and advance purchases (D) describe traditional IT models.
---

## Q7. Which AWS service provides managed DDoS protection for your applications?
- [ ] A) Amazon GuardDuty
- [ ] B) Amazon Inspector
- [x] C) AWS Shield
- [ ] D) AWS WAF
### Explanation
AWS Shield provides DDoS protection. Shield Standard is automatically enabled at no cost. Shield Advanced provides enhanced protection with 24/7 DDoS response team access. GuardDuty (A) detects threats. Inspector (B) assesses vulnerabilities. WAF (D) protects against web exploits like SQL injection.
---

## Q8. A company wants to automate the deployment of infrastructure using code templates. Which AWS service should they use?
- [ ] A) AWS Elastic Beanstalk
- [x] B) AWS CloudFormation
- [ ] C) AWS CodeDeploy
- [ ] D) AWS OpsWorks
### Explanation
AWS CloudFormation is an infrastructure-as-code service that lets you model and provision AWS resources using JSON or YAML templates. Elastic Beanstalk (A) is a PaaS for deploying applications. CodeDeploy (C) automates application deployments. OpsWorks (D) is a configuration management service using Chef or Puppet.
---

## Q9. Which of the following is a benefit of using AWS Regions?
- [ ] A) All Regions share the same pricing
- [ ] B) Data is automatically replicated across all Regions
- [x] C) You can deploy applications closer to end users to reduce latency
- [ ] D) All AWS services are available in every Region
### Explanation
AWS Regions allow you to deploy applications geographically closer to your users, reducing latency. Pricing varies by Region (A). Data is NOT automatically replicated across Regions (B). Not all services are available in every Region (D).
---

## Q10. A company needs to store and retrieve any amount of data at any time from anywhere on the web. Which AWS service should they use?
- [x] A) Amazon S3
- [ ] B) Amazon EBS
- [ ] C) Amazon EFS
- [ ] D) AWS Storage Gateway
### Explanation
Amazon S3 (Simple Storage Service) is object storage designed for storing and retrieving any amount of data from anywhere on the web. EBS (B) provides block storage for EC2 instances. EFS (C) is a managed file system for EC2. Storage Gateway (D) is a hybrid storage service.
---

## Q11. Which AWS service provides a managed container orchestration service that supports Docker?
- [ ] A) AWS Lambda
- [ ] B) AWS Elastic Beanstalk
- [x] C) Amazon ECS
- [ ] D) Amazon Lightsail
### Explanation
Amazon ECS (Elastic Container Service) is a fully managed container orchestration service that supports Docker containers. Lambda (A) is serverless compute. Elastic Beanstalk (B) is a PaaS. Lightsail (D) provides simplified virtual private servers.
---

## Q12. A company wants to ensure that their S3 objects are not accidentally deleted. Which S3 feature should they enable?
- [x] A) S3 Versioning
- [ ] B) S3 Lifecycle Policies
- [ ] C) S3 Transfer Acceleration
- [ ] D) S3 Cross-Region Replication
### Explanation
S3 Versioning keeps multiple variants of an object in the same bucket, allowing you to recover from accidental deletions or overwrites. Lifecycle Policies (B) automate storage class transitions. Transfer Acceleration (C) speeds up uploads. Cross-Region Replication (D) copies objects to another Region.
---

## Q13. Which AWS service allows you to register and manage domain names?
- [ ] A) Amazon CloudFront
- [ ] B) Elastic Load Balancing
- [ ] C) AWS Global Accelerator
- [x] D) Amazon Route 53
### Explanation
Amazon Route 53 is a scalable DNS web service that provides domain name registration, DNS routing, and health checking. CloudFront (A) is a CDN. ELB (B) distributes traffic. Global Accelerator (C) optimizes network paths.
---

## Q14. A company is running a mission-critical application and needs 24/7 access to AWS support engineers via phone. What is the minimum AWS Support plan required?
- [ ] A) Basic
- [ ] B) Developer
- [x] C) Business
- [ ] D) Enterprise
### Explanation
The Business support plan provides 24/7 access to Cloud Support Engineers via phone, chat, and email. Basic (A) has no technical support. Developer (B) provides business-hours email support only. Enterprise (D) also includes phone support but is not the minimum required.
---

## Q15. Which of the following are components of the AWS Global Infrastructure? (Select TWO)
- [x] A) Availability Zones
- [ ] B) Security Groups
- [x] C) Edge Locations
- [ ] D) IAM Policies
- [ ] E) VPC Subnets
### Explanation
Availability Zones (A) and Edge Locations (C) are components of the AWS Global Infrastructure. AZs are isolated data center groups within Regions. Edge Locations are used by CloudFront and other services for content delivery. Security Groups (B), IAM Policies (D), and VPC Subnets (E) are customer-configured resources, not infrastructure components.
---

## Q16. Which AWS service provides a managed graph database?
- [ ] A) Amazon DynamoDB
- [x] B) Amazon Neptune
- [ ] C) Amazon DocumentDB
- [ ] D) Amazon Keyspaces
### Explanation
Amazon Neptune is a fully managed graph database service that supports property graph and RDF models. DynamoDB (A) is a key-value/document NoSQL database. DocumentDB (C) is a MongoDB-compatible document database. Keyspaces (D) is a managed Apache Cassandra-compatible database.
---

## Q17. A company wants to monitor API calls made within their AWS account for security and compliance. Which service should they use?
- [ ] A) Amazon CloudWatch
- [ ] B) AWS Config
- [x] C) AWS CloudTrail
- [ ] D) AWS Trusted Advisor
### Explanation
AWS CloudTrail records API calls made in your AWS account, providing a history of AWS API calls for auditing and compliance. CloudWatch (A) monitors performance metrics. Config (B) tracks resource configuration changes. Trusted Advisor (D) provides best-practice recommendations.
---

## Q18. Which of the following describes the concept of "high availability" in AWS?
- [ ] A) Running applications on the most powerful instance types
- [x] B) Designing systems to remain operational even when components fail
- [ ] C) Encrypting all data at rest and in transit
- [ ] D) Using the cheapest possible resources
### Explanation
High availability means designing systems that continue to operate even when individual components fail, typically by deploying across multiple Availability Zones. Powerful instances (A) relate to performance. Encryption (C) relates to security. Cheap resources (D) relate to cost optimization.
---

## Q19. A company needs a service to manage and rotate database credentials automatically. Which AWS service should they use?
- [ ] A) AWS KMS
- [ ] B) AWS Certificate Manager
- [x] C) AWS Secrets Manager
- [ ] D) Amazon Macie
### Explanation
AWS Secrets Manager helps you manage, retrieve, and rotate database credentials, API keys, and other secrets. KMS (A) manages encryption keys. Certificate Manager (B) manages SSL/TLS certificates. Macie (D) discovers sensitive data in S3.
---

## Q20. Which AWS service enables you to set up and govern a secure, multi-account AWS environment based on best practices?
- [ ] A) AWS Organizations
- [ ] B) AWS IAM
- [x] C) AWS Control Tower
- [ ] D) AWS Config
### Explanation
AWS Control Tower automates the setup and governance of a secure, multi-account AWS environment based on AWS best practices. Organizations (A) provides account management and consolidated billing but less automated governance. IAM (B) manages access within accounts. Config (D) tracks resource configurations.
---

## Q21. A company wants to use machine learning to add image recognition capabilities to their application without ML expertise. Which AWS service should they use?
- [x] A) Amazon Rekognition
- [ ] B) Amazon SageMaker
- [ ] C) AWS DeepLens
- [ ] D) Amazon Comprehend
### Explanation
Amazon Rekognition provides pre-trained image and video analysis capabilities without requiring ML expertise. SageMaker (B) is for building custom ML models. DeepLens (C) is a deep learning-enabled video camera. Comprehend (D) is for natural language processing, not image recognition.
---

## Q22. Which of the following is a design principle of the AWS Well-Architected Framework's Reliability pillar?
- [ ] A) Use the largest instance types available
- [x] B) Automatically recover from failure
- [ ] C) Minimize the number of AWS accounts
- [ ] D) Store all data in a single Availability Zone
### Explanation
Automatically recovering from failure is a key design principle of the Reliability pillar. This includes using health checks, auto-scaling, and multi-AZ deployments. Large instances (A) relate to performance. Minimizing accounts (C) is not a reliability principle. Single AZ (D) reduces reliability.
---

## Q23. A company needs to convert speech to text for their customer service application. Which AWS service should they use?
- [ ] A) Amazon Polly
- [ ] B) Amazon Lex
- [ ] C) Amazon Translate
- [x] D) Amazon Transcribe
### Explanation
Amazon Transcribe is an automatic speech recognition (ASR) service that converts speech to text. Polly (A) converts text to speech (the opposite). Lex (B) builds conversational chatbots. Translate (C) translates text between languages.
---

## Q24. Which AWS service provides a virtual desktop infrastructure (VDI) solution?
- [ ] A) Amazon AppStream 2.0
- [x] B) Amazon WorkSpaces
- [ ] C) Amazon Connect
- [ ] D) AWS Outposts
### Explanation
Amazon WorkSpaces is a managed Desktop-as-a-Service (DaaS) solution providing virtual desktops in the cloud. AppStream 2.0 (A) streams desktop applications, not full desktops. Connect (C) is a cloud contact center. Outposts (D) extends AWS infrastructure on-premises.
---

## Q25. Under the Shared Responsibility Model, who is responsible for managing the network configuration of an Amazon RDS database instance?
- [x] A) AWS manages the underlying network infrastructure; the customer configures security groups and network access
- [ ] B) The customer manages all networking
- [ ] C) AWS manages everything including security groups
- [ ] D) The internet service provider
### Explanation
For Amazon RDS, AWS manages the underlying infrastructure (hardware, OS patching, network infrastructure), while the customer is responsible for configuring security groups, network access (VPC, subnets), and database-level access controls. This is a shared responsibility.
---

## Q26. Which AWS service can be used to create a hybrid cloud architecture by extending AWS infrastructure to on-premises locations?
- [ ] A) Amazon VPC
- [x] B) AWS Outposts
- [ ] C) AWS Direct Connect
- [ ] D) Amazon CloudFront
### Explanation
AWS Outposts extends AWS infrastructure, services, APIs, and tools to on-premises facilities for a truly consistent hybrid experience. VPC (A) is a virtual network in the cloud. Direct Connect (C) provides a dedicated network connection but doesn't extend AWS infrastructure on-premises. CloudFront (D) is a CDN.
---

## Q27. A company wants to analyze log data in real time. Which AWS service is BEST suited for ingesting and processing streaming data?
- [ ] A) Amazon SQS
- [ ] B) Amazon SNS
- [x] C) Amazon Kinesis
- [ ] D) AWS Batch
### Explanation
Amazon Kinesis is designed for real-time streaming data ingestion and processing. SQS (A) is a message queue for decoupling. SNS (B) is a pub/sub notification service. Batch (D) runs batch computing jobs, not real-time streaming.
---

## Q28. Which of the following is NOT a pillar of the AWS Well-Architected Framework?
- [ ] A) Cost Optimization
- [ ] B) Operational Excellence
- [x] C) Elasticity
- [ ] D) Security
### Explanation
Elasticity is not a pillar of the Well-Architected Framework. The six pillars are: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. Elasticity is a cloud computing concept but not a named pillar.
---

## Q29. A company needs to run a relational database but wants to avoid the overhead of database administration tasks like patching and backups. Which service should they use?
- [ ] A) Amazon EC2 with self-managed MySQL
- [x] B) Amazon RDS
- [ ] C) Amazon DynamoDB
- [ ] D) Amazon Redshift
### Explanation
Amazon RDS is a managed relational database service that handles routine tasks like patching, backups, and failover. EC2 with self-managed MySQL (A) requires manual administration. DynamoDB (C) is NoSQL, not relational. Redshift (D) is a data warehouse, not a general-purpose relational database.
---

## Q30. Which AWS service provides a way to assess the security and compliance of applications deployed on AWS?
- [ ] A) AWS Trusted Advisor
- [x] B) Amazon Inspector
- [ ] C) Amazon GuardDuty
- [ ] D) AWS Shield
### Explanation
Amazon Inspector automatically assesses applications for vulnerabilities and deviations from best practices, including common CVEs and network exposure. Trusted Advisor (A) provides broad best-practice recommendations. GuardDuty (C) detects threats at the account level. Shield (D) provides DDoS protection.
---

## Q31. A company wants to use a managed service to build, train, and deploy machine learning models. Which AWS service should they use?
- [ ] A) Amazon Rekognition
- [ ] B) Amazon Comprehend
- [x] C) Amazon SageMaker
- [ ] D) Amazon Lex
### Explanation
Amazon SageMaker is a fully managed service for building, training, and deploying ML models at scale. Rekognition (A) provides pre-built image/video analysis. Comprehend (B) provides pre-built NLP. Lex (D) builds conversational interfaces. SageMaker is for custom model development.
---

## Q32. Which AWS service provides a content delivery network (CDN) that caches content at edge locations worldwide?
- [x] A) Amazon CloudFront
- [ ] B) AWS Global Accelerator
- [ ] C) Amazon Route 53
- [ ] D) Elastic Load Balancing
### Explanation
Amazon CloudFront is AWS's CDN service that caches content at 400+ edge locations worldwide, reducing latency for end users. Global Accelerator (B) optimizes network paths but is not a CDN. Route 53 (C) is DNS. ELB (D) distributes traffic within a Region.
---

## Q33. A company wants to track resource configuration changes over time for compliance. Which AWS service should they use?
- [ ] A) AWS CloudTrail
- [ ] B) Amazon CloudWatch
- [ ] C) AWS Trusted Advisor
- [x] D) AWS Config
### Explanation
AWS Config continuously monitors and records AWS resource configurations and allows you to evaluate them against desired configurations over time. CloudTrail (A) logs API calls. CloudWatch (B) monitors performance metrics. Trusted Advisor (C) provides best-practice recommendations.
---

## Q34. Which of the following is a benefit of consolidated billing in AWS Organizations?
- [ ] A) It provides free AWS support for all accounts
- [x] B) It combines usage across accounts to qualify for volume pricing discounts
- [ ] C) It automatically encrypts all data across accounts
- [ ] D) It eliminates the need for IAM in member accounts
### Explanation
Consolidated billing combines usage from all accounts in an organization, which can qualify for volume pricing discounts (e.g., S3 tiered pricing, EC2 Reserved Instance sharing). It does not provide free support (A), automatic encryption (C), or eliminate IAM (D).
---

## Q35. A company needs to host a static website with high availability and low cost. Which AWS service is the MOST cost-effective?
- [ ] A) Amazon EC2
- [ ] B) AWS Elastic Beanstalk
- [x] C) Amazon S3
- [ ] D) Amazon Lightsail
### Explanation
Amazon S3 can host static websites (HTML, CSS, JavaScript) at very low cost with 99.999999999% durability. EC2 (A) and Elastic Beanstalk (B) are overkill for static content. Lightsail (D) is simpler than EC2 but still more expensive than S3 for static hosting.
---

## Q36. Which AWS service allows you to run code in response to events without provisioning or managing servers?
- [ ] A) Amazon ECS
- [ ] B) Amazon EC2
- [x] C) AWS Lambda
- [ ] D) Amazon EKS
### Explanation
AWS Lambda is a serverless compute service that runs code in response to events (S3 uploads, DynamoDB changes, API Gateway requests) without provisioning servers. ECS (A) and EKS (D) are container orchestration services. EC2 (B) requires provisioning virtual servers.
---

## Q37. A company wants to receive recommendations for cost optimization, security, and performance. Which AWS service provides these?
- [x] A) AWS Trusted Advisor
- [ ] B) AWS Config
- [ ] C) Amazon CloudWatch
- [ ] D) AWS Systems Manager
### Explanation
AWS Trusted Advisor provides real-time guidance across five categories: cost optimization, performance, security, fault tolerance, and service limits. Config (B) tracks resource configurations. CloudWatch (C) monitors metrics. Systems Manager (D) manages infrastructure operations.
---

## Q38. Which of the following describes an AWS Region?
- [ ] A) A single data center with redundant power
- [ ] B) A global network of caching servers
- [x] C) A separate geographic area containing multiple Availability Zones
- [ ] D) A virtual private network within AWS
### Explanation
An AWS Region is a separate geographic area that contains multiple isolated Availability Zones. A single data center (A) describes part of an AZ. A caching network (B) describes edge locations. A virtual network (D) describes a VPC.
---

## Q39. A company needs to enforce governance policies across multiple AWS accounts, such as restricting which services can be used. Which feature should they use?
- [ ] A) IAM Policies
- [x] B) Service Control Policies (SCPs)
- [ ] C) Security Groups
- [ ] D) Network ACLs
### Explanation
Service Control Policies (SCPs) in AWS Organizations allow you to centrally control the maximum available permissions across multiple AWS accounts. IAM Policies (A) apply within a single account. Security Groups (C) and Network ACLs (D) are network-level controls, not governance tools.
---

## Q40. Which AWS service provides a fully managed message queuing service for decoupling application components?
- [ ] A) Amazon SNS
- [ ] B) Amazon Kinesis
- [x] C) Amazon SQS
- [ ] D) AWS EventBridge
### Explanation
Amazon SQS (Simple Queue Service) is a fully managed message queuing service that decouples and scales microservices and distributed systems. SNS (A) is pub/sub notifications. Kinesis (B) is for real-time streaming data. EventBridge (D) is a serverless event bus.
---

## Q41. A company wants to migrate a large on-premises Oracle database to AWS with minimal code changes. Which AWS service should they consider?
- [ ] A) Amazon DynamoDB
- [x] B) Amazon RDS for Oracle
- [ ] C) Amazon Redshift
- [ ] D) Amazon ElastiCache
### Explanation
Amazon RDS for Oracle provides a managed Oracle database environment, allowing migration with minimal code changes since the database engine remains the same. DynamoDB (A) is NoSQL and would require significant code changes. Redshift (C) is a data warehouse. ElastiCache (D) is an in-memory cache.
---

## Q42. Which of the following is a responsibility of the customer under the AWS Shared Responsibility Model? (Select TWO)
- [x] A) Patching the guest operating system on EC2 instances
- [ ] B) Managing the physical hardware in AWS data centers
- [ ] C) Maintaining the global network infrastructure
- [x] D) Managing application-level firewall rules
- [ ] E) Patching the hypervisor
### Explanation
Patching the guest OS on EC2 (A) and managing application-level firewall rules (D) are customer responsibilities. AWS manages physical hardware (B), global network infrastructure (C), and hypervisor patching (E).
---

## Q43. Which AWS service provides a managed Kubernetes service?
- [ ] A) Amazon ECS
- [x] B) Amazon EKS
- [ ] C) AWS Fargate
- [ ] D) AWS Elastic Beanstalk
### Explanation
Amazon EKS (Elastic Kubernetes Service) is a fully managed Kubernetes service. ECS (A) is AWS's proprietary container orchestration service. Fargate (C) is a serverless compute engine for containers. Elastic Beanstalk (D) is a PaaS, not a Kubernetes service.
---

## Q44. A company wants to estimate the cost of their planned AWS architecture before deployment. Which tool should they use?
- [ ] A) AWS Cost Explorer
- [ ] B) AWS Budgets
- [x] C) AWS Pricing Calculator
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Pricing Calculator allows users to estimate the cost of AWS services before using them by modeling their architecture. Cost Explorer (A) analyzes historical spending. Budgets (B) sets spending alerts. Trusted Advisor (D) provides optimization recommendations for existing resources.
---

## Q45. Which AWS service enables you to run containers without managing servers or clusters?
- [x] A) AWS Fargate
- [ ] B) Amazon ECS on EC2
- [ ] C) Amazon EC2
- [ ] D) Amazon EKS on EC2
### Explanation
AWS Fargate is a serverless compute engine for containers that works with both ECS and EKS, eliminating the need to manage servers or clusters. ECS on EC2 (B) and EKS on EC2 (D) require managing the underlying EC2 instances. EC2 (C) is not a container service.
---

## Q46. A company needs to identify which AWS resources are generating the most cost. Which tool provides this visibility?
- [ ] A) AWS Budgets
- [x] B) AWS Cost Explorer
- [ ] C) AWS Pricing Calculator
- [ ] D) AWS Billing Dashboard
### Explanation
AWS Cost Explorer provides detailed visualizations and analysis of AWS spending patterns, allowing you to filter by service, account, tag, and more to identify cost drivers. Budgets (A) sets alerts. Pricing Calculator (C) estimates future costs. Billing Dashboard (D) shows a high-level current month summary.
---

## Q47. Which of the following best describes Amazon Aurora?
- [ ] A) A NoSQL database service
- [ ] B) A data warehouse service
- [x] C) A MySQL and PostgreSQL-compatible relational database with up to 5x better performance
- [ ] D) An in-memory caching service
### Explanation
Amazon Aurora is a MySQL and PostgreSQL-compatible relational database built for the cloud, offering up to 5x the throughput of standard MySQL and 3x of PostgreSQL. It is not NoSQL (A), a data warehouse (B), or a caching service (D).
---

## Q48. A company wants to protect their web application from SQL injection and cross-site scripting attacks. Which AWS service should they use?
- [x] A) AWS WAF
- [ ] B) AWS Shield
- [ ] C) Amazon GuardDuty
- [ ] D) Amazon Inspector
### Explanation
AWS WAF (Web Application Firewall) protects web applications from common exploits like SQL injection and cross-site scripting (XSS). Shield (B) protects against DDoS attacks. GuardDuty (C) detects threats at the account level. Inspector (D) assesses application vulnerabilities.
---

## Q49. Which AWS service provides a managed Apache Hadoop framework for processing large amounts of data?
- [ ] A) Amazon Athena
- [ ] B) Amazon Redshift
- [x] C) Amazon EMR
- [ ] D) AWS Glue
### Explanation
Amazon EMR (Elastic MapReduce) provides a managed Hadoop framework for processing vast amounts of data using open-source tools like Apache Spark, Hive, and Presto. Athena (A) queries S3 data with SQL. Redshift (B) is a data warehouse. Glue (D) is an ETL service.
---

## Q50. Which of the following describes the concept of "elasticity" in cloud computing?
- [ ] A) The ability to restrict access to resources
- [ ] B) The ability to withstand component failures
- [ ] C) The ability to deploy resources in multiple Regions
- [x] D) The ability to acquire resources when needed and release them when no longer needed
### Explanation
Elasticity is the ability to dynamically acquire resources as demand increases and release them when demand decreases, automatically scaling to match workload requirements. Access restriction (A) relates to security. Withstanding failures (B) is fault tolerance. Multi-Region deployment (C) relates to global reach.
---
