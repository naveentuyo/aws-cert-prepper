# AWS Certified Cloud Practitioner (CLF-C02) — Practice Test 3
#
# Total Questions: 50
# Passing Score: 70% (35/50)
# Time Limit: 90 minutes

## Q1. A company wants to enforce that all IAM users use multi-factor authentication (MFA). Which AWS service should they configure?
- [ ] A) Amazon Cognito
- [ ] B) AWS Shield
- [x] C) AWS IAM
- [ ] D) AWS Directory Service
### Explanation
AWS IAM is where MFA is configured for IAM users. Administrators can create IAM policies requiring MFA for access. Cognito (A) is for application user authentication. Shield (B) is DDoS protection. Directory Service (D) integrates with Microsoft Active Directory.
---

## Q2. Which AWS service provides block-level storage volumes for use with Amazon EC2 instances?
- [ ] A) Amazon S3
- [x] B) Amazon EBS
- [ ] C) Amazon EFS
- [ ] D) AWS Storage Gateway
### Explanation
Amazon EBS (Elastic Block Store) provides persistent block-level storage volumes for EC2 instances. S3 (A) is object storage. EFS (C) is a managed file system. Storage Gateway (D) is a hybrid storage service.
---

## Q3. A company needs to translate text from one language to another within their application. Which AWS service should they use?
- [ ] A) Amazon Transcribe
- [ ] B) Amazon Comprehend
- [ ] C) Amazon Polly
- [x] D) Amazon Translate
### Explanation
Amazon Translate is a neural machine translation service for translating text between languages. Transcribe (A) converts speech to text. Comprehend (B) performs natural language processing. Polly (C) converts text to speech.
---

## Q4. Which of the following is a benefit of using multiple AWS Regions?
- [x] A) Disaster recovery and business continuity across geographic locations
- [ ] B) Automatic data synchronization between Regions at no cost
- [ ] C) Lower pricing in all Regions
- [ ] D) Simplified network configuration
### Explanation
Using multiple Regions provides disaster recovery and business continuity by distributing workloads across geographically separated locations. Data synchronization between Regions incurs costs (B). Pricing varies by Region (C). Multi-Region adds network complexity (D).
---

## Q5. A company wants to deploy a simple web application without managing servers, containers, or infrastructure. Which AWS service provides the easiest path?
- [ ] A) Amazon EC2
- [ ] B) Amazon ECS
- [x] C) AWS App Runner
- [ ] D) Amazon EKS
### Explanation
AWS App Runner is a fully managed service that makes it easy to deploy web applications and APIs from source code or container images without managing infrastructure. EC2 (A) requires server management. ECS (B) and EKS (D) require container orchestration knowledge.
---

## Q6. Which AWS service provides a managed file system that can be shared across multiple EC2 instances?
- [ ] A) Amazon S3
- [ ] B) Amazon EBS
- [x] C) Amazon EFS
- [ ] D) AWS Storage Gateway
### Explanation
Amazon EFS (Elastic File System) provides a fully managed, scalable file system that can be mounted on multiple EC2 instances simultaneously. S3 (A) is object storage. EBS (B) can only be attached to one EC2 instance at a time (except Multi-Attach io1/io2). Storage Gateway (D) is a hybrid storage service.
---

## Q7. A company wants to identify security vulnerabilities in their EC2 instances and container images. Which AWS service should they use?
- [ ] A) Amazon GuardDuty
- [ ] B) AWS WAF
- [x] C) Amazon Inspector
- [ ] D) AWS Shield
### Explanation
Amazon Inspector automatically assesses EC2 instances and container images for software vulnerabilities and unintended network exposure. GuardDuty (A) detects account-level threats. WAF (B) filters web traffic. Shield (D) protects against DDoS attacks.
---

## Q8. Which pricing model allows you to pay for compute capacity by the hour or second with no long-term commitments?
- [x] A) On-Demand Instances
- [ ] B) Reserved Instances
- [ ] C) Spot Instances
- [ ] D) Savings Plans
### Explanation
On-Demand Instances let you pay for compute capacity by the hour or second with no long-term commitments or upfront payments. Reserved Instances (B) and Savings Plans (D) require commitments. Spot Instances (C) offer discounts but can be interrupted.
---

## Q9. A company needs to set up a DNS service to route end users to their application. Which AWS service should they use?
- [ ] A) Amazon CloudFront
- [ ] B) Elastic Load Balancing
- [ ] C) AWS Direct Connect
- [x] D) Amazon Route 53
### Explanation
Amazon Route 53 is a scalable DNS web service that routes end users to applications by translating domain names to IP addresses. CloudFront (A) is a CDN. ELB (B) distributes traffic across targets. Direct Connect (C) is a dedicated network connection.
---

## Q10. Which of the following is an example of a managed service where AWS handles the operating system patching?
- [ ] A) Amazon EC2
- [x] B) Amazon RDS
- [ ] C) Self-managed database on EC2
- [ ] D) Amazon EBS
### Explanation
Amazon RDS is a managed service where AWS handles OS patching, database engine patching, backups, and hardware maintenance. EC2 (A) and self-managed databases on EC2 (C) require the customer to patch the OS. EBS (D) is a storage service, not a compute/database service.
---

## Q11. A company wants to build a CI/CD pipeline to automate their software release process. Which AWS service provides continuous integration and continuous delivery?
- [x] A) AWS CodePipeline
- [ ] B) AWS CloudFormation
- [ ] C) AWS Config
- [ ] D) AWS Systems Manager
### Explanation
AWS CodePipeline is a fully managed CI/CD service that automates build, test, and deploy phases of your release process. CloudFormation (B) provisions infrastructure. Config (C) tracks resource configurations. Systems Manager (D) manages infrastructure operations.
---

## Q12. Which AWS service provides a way to connect your on-premises network to AWS using an encrypted VPN tunnel over the internet?
- [ ] A) AWS Direct Connect
- [x] B) AWS Site-to-Site VPN
- [ ] C) Amazon VPC Peering
- [ ] D) AWS Transit Gateway
### Explanation
AWS Site-to-Site VPN creates an encrypted tunnel between your on-premises network and AWS over the public internet. Direct Connect (A) is a dedicated physical connection that does not use the internet. VPC Peering (C) connects two VPCs. Transit Gateway (D) connects multiple VPCs and on-premises networks.
---

## Q13. A company wants to use a service that provides pre-built AI models for common use cases without requiring machine learning expertise. Which category of AWS services fits this need?
- [ ] A) AWS Compute services
- [x] B) AWS AI Services (Rekognition, Comprehend, Polly, etc.)
- [ ] C) AWS Database services
- [ ] D) AWS Storage services
### Explanation
AWS AI Services provide pre-built models for common use cases like image analysis (Rekognition), NLP (Comprehend), text-to-speech (Polly), and translation (Translate) without requiring ML expertise. Compute (A), Database (C), and Storage (D) are different service categories.
---

## Q14. Which of the following best describes the principle of least privilege?
- [ ] A) Granting all users administrator access for convenience
- [ ] B) Using the largest instance types for better security
- [x] C) Granting only the minimum permissions necessary to perform a task
- [ ] D) Encrypting all data at rest
### Explanation
The principle of least privilege means granting only the minimum permissions required to perform a specific task. This reduces the attack surface and limits potential damage. Admin access for all (A) violates this principle. Instance size (B) is unrelated. Encryption (D) is a separate security practice.
---

## Q15. A company needs to store archival data that is rarely accessed and can tolerate retrieval times of 12 hours. Which S3 storage class is MOST cost-effective?
- [ ] A) S3 Standard
- [ ] B) S3 Standard-Infrequent Access
- [ ] C) S3 Glacier Instant Retrieval
- [x] D) S3 Glacier Deep Archive
### Explanation
S3 Glacier Deep Archive is the lowest-cost S3 storage class, designed for long-term archival with retrieval times of 12-48 hours. Standard (A) and Standard-IA (B) are more expensive. Glacier Instant Retrieval (C) provides millisecond access at higher cost than Deep Archive.
---

## Q16. Which AWS service provides a managed service for running and scaling web applications and APIs built with containers or source code?
- [x] A) AWS App Runner
- [ ] B) Amazon EC2
- [ ] C) AWS CloudFormation
- [ ] D) Amazon Lightsail
### Explanation
AWS App Runner is a fully managed service for deploying containerized web applications and APIs without managing infrastructure. EC2 (B) requires server management. CloudFormation (C) is infrastructure-as-code. Lightsail (D) provides simplified VPS but still requires some management.
---

## Q17. A company wants to use a service that provides a single place to view and manage costs and usage across all their AWS accounts. Which service should they use?
- [ ] A) AWS Budgets
- [x] B) AWS Cost Explorer
- [ ] C) AWS Pricing Calculator
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Cost Explorer provides a comprehensive view of costs and usage across all AWS accounts with filtering, grouping, and forecasting capabilities. Budgets (A) sets alerts. Pricing Calculator (C) estimates future costs. Trusted Advisor (D) provides optimization recommendations.
---

## Q18. Which of the following is a responsibility of AWS under the Shared Responsibility Model? (Select TWO)
- [ ] A) Managing customer application code
- [x] B) Maintaining the physical network infrastructure
- [ ] C) Configuring customer VPC security groups
- [x] D) Ensuring the availability of AWS Regions and Availability Zones
- [ ] E) Managing customer encryption keys
### Explanation
AWS is responsible for maintaining physical network infrastructure (B) and ensuring the availability of Regions and AZs (D). Customer application code (A), VPC security groups (C), and customer encryption keys (E) are customer responsibilities.
---

## Q19. A company needs a service to orchestrate multiple AWS Lambda functions into a workflow. Which service should they use?
- [ ] A) Amazon SQS
- [x] B) AWS Step Functions
- [ ] C) Amazon SNS
- [ ] D) Amazon EventBridge
### Explanation
AWS Step Functions coordinates multiple Lambda functions and other AWS services into serverless workflows using visual state machines. SQS (A) is a message queue. SNS (C) is pub/sub notifications. EventBridge (D) is an event bus for routing events.
---

## Q20. Which AWS service provides a managed service for running relational databases that automatically handles hardware provisioning, setup, patching, and backups?
- [x] A) Amazon RDS
- [ ] B) Amazon DynamoDB
- [ ] C) Amazon EC2
- [ ] D) Amazon Redshift
### Explanation
Amazon RDS is a managed relational database service that handles hardware provisioning, database setup, patching, and backups. DynamoDB (B) is NoSQL. EC2 (C) requires self-managing everything. Redshift (D) is a data warehouse, not a general-purpose relational database.
---

## Q21. A company wants to detect and respond to security events across their AWS accounts. Which service provides centralized security findings?
- [ ] A) Amazon CloudWatch
- [ ] B) AWS CloudTrail
- [x] C) AWS Security Hub
- [ ] D) AWS Config
### Explanation
AWS Security Hub provides a centralized view of security findings across AWS accounts, aggregating alerts from GuardDuty, Inspector, Macie, and other services. CloudWatch (A) monitors metrics. CloudTrail (B) logs API calls. Config (D) tracks resource configurations.
---

## Q22. Which of the following describes the AWS Well-Architected Tool?
- [x] A) A service that helps review workloads against AWS best practices across the six pillars
- [ ] B) A tool for estimating AWS costs
- [ ] C) A service for deploying infrastructure as code
- [ ] D) A monitoring service for AWS resources
### Explanation
The AWS Well-Architected Tool helps you review your workloads against the six pillars of the Well-Architected Framework and provides recommendations for improvement. It is not a cost estimator (B), deployment tool (C), or monitoring service (D).
---

## Q23. A company needs to store key-value data with consistent single-digit millisecond latency for their gaming application. Which database service should they use?
- [ ] A) Amazon RDS
- [ ] B) Amazon Redshift
- [x] C) Amazon DynamoDB
- [ ] D) Amazon Neptune
### Explanation
Amazon DynamoDB is a fully managed NoSQL key-value database providing consistent single-digit millisecond performance, ideal for gaming applications. RDS (A) is relational. Redshift (B) is a data warehouse. Neptune (D) is a graph database.
---

## Q24. Which AWS service allows you to connect multiple VPCs and on-premises networks through a central hub?
- [ ] A) Amazon VPC Peering
- [ ] B) AWS Direct Connect
- [x] C) AWS Transit Gateway
- [ ] D) Amazon Route 53
### Explanation
AWS Transit Gateway acts as a central hub that connects multiple VPCs and on-premises networks, simplifying network architecture. VPC Peering (A) connects only two VPCs. Direct Connect (B) is a physical connection. Route 53 (D) is DNS.
---

## Q25. A company wants to use a service that automatically optimizes S3 storage costs by moving objects between access tiers. Which storage class should they use?
- [ ] A) S3 Standard
- [ ] B) S3 Standard-Infrequent Access
- [x] C) S3 Intelligent-Tiering
- [ ] D) S3 Glacier
### Explanation
S3 Intelligent-Tiering automatically moves objects between frequent and infrequent access tiers based on changing access patterns, optimizing costs without performance impact. Standard (A) and Standard-IA (B) require manual tier management. Glacier (D) is for archival data.
---

## Q26. Which AWS support plan is available to all AWS customers at no additional cost?
- [x] A) Basic
- [ ] B) Developer
- [ ] C) Business
- [ ] D) Enterprise
### Explanation
The Basic support plan is included for all AWS customers at no additional cost. It includes access to documentation, whitepapers, support forums, and AWS Trusted Advisor core checks. Developer (B), Business (C), and Enterprise (D) are paid plans.
---

## Q27. A company needs to process large-scale batch computing jobs such as financial risk modeling. Which AWS service is designed for this?
- [ ] A) AWS Lambda
- [x] B) AWS Batch
- [ ] C) Amazon SQS
- [ ] D) AWS Step Functions
### Explanation
AWS Batch efficiently runs hundreds of thousands of batch computing jobs by dynamically provisioning the optimal quantity and type of compute resources. Lambda (A) has execution time limits. SQS (C) is a message queue. Step Functions (D) orchestrates workflows.
---

## Q28. Which of the following is a feature of Amazon VPC that acts as a virtual firewall at the subnet level?
- [ ] A) Security Groups
- [x] B) Network ACLs
- [ ] C) IAM Policies
- [ ] D) AWS WAF
### Explanation
Network ACLs (Access Control Lists) act as a virtual firewall at the subnet level, controlling inbound and outbound traffic. Security Groups (A) operate at the instance level. IAM Policies (C) control AWS service access. WAF (D) protects web applications.
---

## Q29. A company wants to use AWS to host a WordPress website with minimal operational overhead. Which service provides the simplest solution?
- [ ] A) Amazon EC2
- [ ] B) AWS Elastic Beanstalk
- [x] C) Amazon Lightsail
- [ ] D) Amazon ECS
### Explanation
Amazon Lightsail provides simplified virtual private servers with pre-configured WordPress blueprints, making it the easiest way to host WordPress on AWS. EC2 (A) requires more configuration. Elastic Beanstalk (B) is for custom applications. ECS (D) is for containers.
---

## Q30. Which AWS service provides a way to automate security assessments of applications deployed on AWS?
- [x] A) Amazon Inspector
- [ ] B) AWS Trusted Advisor
- [ ] C) Amazon GuardDuty
- [ ] D) AWS Config
### Explanation
Amazon Inspector automatically assesses applications for vulnerabilities and deviations from best practices. Trusted Advisor (B) provides broad recommendations. GuardDuty (C) detects threats at the account level. Config (D) tracks resource configuration changes.
---

## Q31. A company wants to use a managed service to run Apache Spark for big data processing. Which AWS service should they use?
- [x] A) Amazon EMR
- [ ] B) Amazon Athena
- [ ] C) Amazon Redshift
- [ ] D) AWS Glue
### Explanation
Amazon EMR (Elastic MapReduce) provides a managed platform for running Apache Spark, Hadoop, and other big data frameworks. Athena (B) queries S3 with SQL. Redshift (C) is a data warehouse. Glue (D) is an ETL service.
---

## Q32. Which of the following describes the concept of "fault tolerance" in cloud computing?
- [ ] A) The ability to scale resources based on demand
- [x] B) The ability of a system to continue operating properly when one or more components fail
- [ ] C) The ability to deploy resources globally
- [ ] D) The ability to encrypt data at rest
### Explanation
Fault tolerance is the ability of a system to continue operating properly even when one or more components fail, typically through redundancy and failover mechanisms. Scaling (A) is elasticity. Global deployment (C) is reach. Encryption (D) is security.
---

## Q33. A company needs to store session state for a web application with microsecond latency. Which AWS service is BEST suited?
- [ ] A) Amazon RDS
- [ ] B) Amazon S3
- [x] C) Amazon ElastiCache for Redis
- [ ] D) Amazon DynamoDB
### Explanation
Amazon ElastiCache for Redis provides in-memory caching with microsecond latency, ideal for session state management. RDS (A) has higher latency. S3 (B) is object storage. DynamoDB (D) provides single-digit millisecond latency, which is slower than ElastiCache's microsecond performance.
---

## Q34. Which AWS service enables you to create reusable templates to model and provision AWS resources?
- [ ] A) AWS CodePipeline
- [x] B) AWS CloudFormation
- [ ] C) AWS CodeDeploy
- [ ] D) AWS Elastic Beanstalk
### Explanation
AWS CloudFormation uses JSON or YAML templates to model and provision AWS resources in a repeatable, automated manner. CodePipeline (A) automates release pipelines. CodeDeploy (C) automates application deployments. Elastic Beanstalk (D) is a PaaS.
---

## Q35. A company wants to restrict which AWS Regions their developers can launch resources in. Which feature should they use?
- [ ] A) IAM User Policies
- [x] B) Service Control Policies (SCPs) in AWS Organizations
- [ ] C) Security Groups
- [ ] D) Network ACLs
### Explanation
SCPs in AWS Organizations can restrict which Regions are available for resource deployment across all accounts in the organization. IAM Policies (A) can restrict Regions within a single account but SCPs provide organization-wide enforcement. Security Groups (C) and Network ACLs (D) are network controls.
---

## Q36. Which of the following is a valid use case for AWS Lambda?
- [ ] A) Running a 24/7 web server
- [x] B) Processing an image uploaded to S3
- [ ] C) Hosting a relational database
- [ ] D) Providing block storage for EC2
### Explanation
AWS Lambda is ideal for event-driven tasks like processing an S3 upload. Lambda functions have a maximum execution time of 15 minutes, making them unsuitable for 24/7 servers (A). Hosting databases (C) requires persistent compute. Block storage (D) is EBS.
---

## Q37. A company wants to use a service that provides real-time recommendations based on user behavior. Which AWS service should they consider?
- [ ] A) Amazon Comprehend
- [x] B) Amazon Personalize
- [ ] C) Amazon Rekognition
- [ ] D) Amazon Polly
### Explanation
Amazon Personalize uses machine learning to deliver real-time personalized recommendations based on user behavior. Comprehend (A) is for NLP. Rekognition (C) is for image/video analysis. Polly (D) converts text to speech.
---

## Q38. Which AWS service provides a way to manage access to AWS services and resources securely using policies?
- [x] A) AWS IAM
- [ ] B) Amazon Cognito
- [ ] C) AWS Shield
- [ ] D) Amazon GuardDuty
### Explanation
AWS IAM (Identity and Access Management) enables you to manage access to AWS services and resources securely using users, groups, roles, and policies. Cognito (B) manages application user identities. Shield (C) is DDoS protection. GuardDuty (D) detects threats.
---

## Q39. A company needs to ensure their application automatically recovers from an Availability Zone failure. Which architecture pattern should they implement?
- [ ] A) Single AZ deployment with larger instances
- [ ] B) Single Region, single AZ with manual failover
- [x] C) Multi-AZ deployment with Elastic Load Balancing and Auto Scaling
- [ ] D) On-premises backup with manual restoration
### Explanation
Multi-AZ deployment with ELB and Auto Scaling ensures automatic failover and recovery when an AZ fails. Single AZ deployments (A, B) create single points of failure. On-premises backup (D) requires manual intervention and increases recovery time.
---

## Q40. Which AWS service provides a managed service for creating and running data pipelines for data-driven workflows?
- [ ] A) Amazon Kinesis
- [ ] B) AWS Step Functions
- [x] C) AWS Data Pipeline
- [ ] D) Amazon SQS
### Explanation
AWS Data Pipeline is a managed service for creating and running data-driven workflows, moving and transforming data between AWS services. Kinesis (A) processes streaming data. Step Functions (B) orchestrates serverless workflows. SQS (D) is a message queue.
---

## Q41. Which of the following describes the AWS Shared Responsibility Model?
- [ ] A) AWS is responsible for all security in the cloud
- [ ] B) The customer is responsible for all security in the cloud
- [x] C) AWS is responsible for security OF the cloud; the customer is responsible for security IN the cloud
- [ ] D) Security responsibilities are determined by the support plan
### Explanation
The Shared Responsibility Model divides security: AWS secures the underlying infrastructure (security OF the cloud), while customers secure their data, applications, and configurations (security IN the cloud). It is not solely AWS (A) or customer (B) responsibility, and support plans (D) don't determine this.
---

## Q42. A company wants to use a service that provides a managed message broker compatible with Apache ActiveMQ and RabbitMQ. Which service should they use?
- [ ] A) Amazon SQS
- [ ] B) Amazon SNS
- [x] C) Amazon MQ
- [ ] D) Amazon Kinesis
### Explanation
Amazon MQ is a managed message broker service compatible with Apache ActiveMQ and RabbitMQ, ideal for migrating existing messaging applications. SQS (A) and SNS (B) are AWS-native messaging services. Kinesis (D) is for streaming data.
---

## Q43. Which AWS service allows you to run code for virtually any type of application with no administration, automatically scaling from a few requests per day to thousands per second?
- [x] A) AWS Lambda
- [ ] B) Amazon EC2
- [ ] C) Amazon ECS
- [ ] D) AWS Elastic Beanstalk
### Explanation
AWS Lambda automatically scales from zero to thousands of concurrent executions with no administration required. EC2 (B) requires instance management. ECS (C) requires container orchestration. Elastic Beanstalk (D) manages infrastructure but is not serverless.
---

## Q44. A company wants to tag their AWS resources to track costs by department. Which AWS feature supports this?
- [ ] A) AWS Organizations
- [x] B) Cost Allocation Tags
- [ ] C) AWS Budgets
- [ ] D) AWS Trusted Advisor
### Explanation
Cost Allocation Tags allow you to tag AWS resources and then use those tags to filter and group costs in Cost Explorer and billing reports by department, project, or any custom category. Organizations (A) manages accounts. Budgets (C) sets alerts. Trusted Advisor (D) provides recommendations.
---

## Q45. Which of the following is a benefit of using Amazon CloudFront with an S3 origin?
- [ ] A) It reduces the cost of S3 storage
- [x] B) It reduces latency by caching content at edge locations closer to users
- [ ] C) It encrypts S3 objects automatically
- [ ] D) It provides database caching
### Explanation
CloudFront caches S3 content at edge locations worldwide, reducing latency for end users. It doesn't reduce S3 storage costs (A) or encrypt objects (C). Database caching (D) is provided by ElastiCache.
---

## Q46. A company needs to grant temporary AWS credentials to users who sign in through a corporate identity provider using SAML 2.0. Which service supports this?
- [x] A) AWS IAM Identity Center (SSO)
- [ ] B) AWS IAM Access Keys
- [ ] C) Amazon Cognito
- [ ] D) AWS Directory Service
### Explanation
AWS IAM Identity Center (formerly AWS SSO) enables federated access using corporate identity providers via SAML 2.0 to grant temporary credentials. IAM Access Keys (B) are long-term credentials. Cognito (C) is for application end-user authentication. Directory Service (D) provides managed Microsoft AD.
---

## Q47. Which of the following describes the six advantages of cloud computing as defined by AWS? (Select TWO)
- [x] A) Stop guessing capacity
- [ ] B) Increase fixed costs
- [ ] C) Decrease speed and agility
- [x] D) Benefit from massive economies of scale
- [ ] E) Require long-term contracts
### Explanation
Stop guessing capacity (A) and benefit from massive economies of scale (D) are two of the six advantages. The others are: trade fixed expense for variable expense, increase speed and agility, stop spending money running data centers, and go global in minutes. Increased fixed costs (B), decreased agility (C), and long-term contracts (E) are not advantages.
---

## Q48. A company wants to monitor the health and performance of their AWS resources and set up dashboards. Which service should they use?
- [ ] A) AWS CloudTrail
- [ ] B) AWS Config
- [x] C) Amazon CloudWatch
- [ ] D) AWS Trusted Advisor
### Explanation
Amazon CloudWatch monitors AWS resources and applications, collecting metrics, creating dashboards, and setting alarms. CloudTrail (A) logs API calls. Config (B) tracks resource configurations. Trusted Advisor (D) provides best-practice recommendations.
---

## Q49. Which AWS service provides a managed service for creating, publishing, maintaining, and securing REST and WebSocket APIs?
- [x] A) Amazon API Gateway
- [ ] B) Elastic Load Balancing
- [ ] C) Amazon CloudFront
- [ ] D) AWS AppSync
### Explanation
Amazon API Gateway is a fully managed service for creating and managing REST and WebSocket APIs at any scale. ELB (B) distributes traffic. CloudFront (C) is a CDN. AppSync (D) is specifically for GraphQL APIs.
---

## Q50. A company is evaluating AWS and wants to understand the total cost of ownership compared to on-premises. Which factor makes cloud computing more cost-effective for variable workloads?
- [ ] A) Higher upfront hardware investment
- [ ] B) Fixed monthly pricing regardless of usage
- [x] C) Pay only for what you use, scaling up and down with demand
- [ ] D) Longer procurement cycles for new capacity
### Explanation
Cloud computing's pay-as-you-go model means you only pay for resources consumed, scaling dynamically with demand. This eliminates over-provisioning for peak capacity. Higher upfront costs (A) and fixed pricing (B) describe traditional IT. Longer procurement (D) is a disadvantage of on-premises.
---
