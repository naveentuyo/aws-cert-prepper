# AWS Certified Cloud Practitioner (CLF-C02) — Practice Test 2
#
# Total Questions: 50
# Passing Score: 70% (35/50)
# Time Limit: 90 minutes

## Q1. A company wants to centrally manage billing across multiple AWS accounts and apply volume discounts. Which service should they use?
- [ ] A) AWS Budgets
- [ ] B) AWS Cost Explorer
- [x] C) AWS Organizations
- [ ] D) AWS Control Tower
### Explanation
AWS Organizations enables consolidated billing across multiple AWS accounts, providing a single payment method and combined usage for volume discounts. Budgets (A) sets spending alerts. Cost Explorer (B) analyzes costs. Control Tower (D) sets up governance but relies on Organizations for billing.
---

## Q2. Which AWS service provides a fully managed in-memory data store compatible with Redis and Memcached?
- [ ] A) Amazon RDS
- [x] B) Amazon ElastiCache
- [ ] C) Amazon DynamoDB
- [ ] D) Amazon Redshift
### Explanation
Amazon ElastiCache provides fully managed in-memory data stores compatible with Redis and Memcached, delivering sub-millisecond latency. RDS (A) is a relational database. DynamoDB (C) is a NoSQL database. Redshift (D) is a data warehouse.
---

## Q3. A company needs to transfer 80 TB of data to AWS. Internet transfer would take weeks. Which service provides the fastest physical data transfer?
- [ ] A) AWS DataSync
- [ ] B) Amazon S3 Transfer Acceleration
- [x] C) AWS Snowball Edge
- [ ] D) AWS Direct Connect
### Explanation
AWS Snowball Edge is a physical data transport device for migrating large amounts of data (tens of terabytes to petabytes). For 80 TB, shipping a Snowball device is faster than network transfer. DataSync (A) and Transfer Acceleration (B) use the network. Direct Connect (D) requires setup time.
---

## Q4. Which AWS service uses machine learning to detect anomalous activity and potential threats in your AWS environment?
- [x] A) Amazon GuardDuty
- [ ] B) AWS WAF
- [ ] C) AWS Shield
- [ ] D) Amazon Inspector
### Explanation
Amazon GuardDuty uses machine learning, anomaly detection, and integrated threat intelligence to continuously monitor for malicious activity. WAF (B) filters web traffic. Shield (C) protects against DDoS. Inspector (D) assesses application vulnerabilities.
---

## Q5. Which of the following is an advantage of cloud computing over traditional on-premises infrastructure?
- [ ] A) Complete control over physical hardware
- [ ] B) Fixed monthly costs regardless of usage
- [ ] C) Longer procurement cycles for capacity planning
- [x] D) Ability to go global in minutes
### Explanation
The ability to go global in minutes is one of the six advantages of cloud computing. You can deploy applications in multiple Regions with a few clicks. Physical hardware control (A) is an on-premises advantage. Fixed costs (B) and long procurement (C) describe traditional IT drawbacks.
---

## Q6. A company wants to run a managed relational database that is compatible with MySQL but offers five times better performance. Which service should they use?
- [ ] A) Amazon RDS for MySQL
- [x] B) Amazon Aurora
- [ ] C) Amazon DynamoDB
- [ ] D) Amazon Redshift
### Explanation
Amazon Aurora is MySQL and PostgreSQL-compatible and offers up to 5x the throughput of standard MySQL. RDS for MySQL (A) runs standard MySQL without the Aurora performance enhancements. DynamoDB (C) is NoSQL. Redshift (D) is a data warehouse.
---

## Q7. Which AWS service allows you to create alarms that automatically trigger actions when a metric threshold is breached?
- [x] A) Amazon CloudWatch
- [ ] B) AWS CloudTrail
- [ ] C) AWS Config
- [ ] D) AWS X-Ray
### Explanation
Amazon CloudWatch monitors metrics and allows you to set alarms that trigger actions (like Auto Scaling or SNS notifications) when thresholds are breached. CloudTrail (B) logs API calls. Config (C) tracks resource configurations. X-Ray (D) traces distributed applications.
---

## Q8. Under the Shared Responsibility Model, which of the following is the customer responsible for when using AWS Lambda?
- [ ] A) Patching the underlying operating system
- [ ] B) Managing the physical servers
- [x] C) Managing the code and permissions for the Lambda function
- [ ] D) Maintaining the runtime environment
### Explanation
For AWS Lambda, the customer is responsible for the function code, IAM permissions, and configuration. AWS manages the underlying infrastructure, OS patching, and runtime environment. This is a key distinction — managed services shift more responsibility to AWS.
---

## Q9. A company needs to set up a private, dedicated network connection between their data center and AWS that does NOT traverse the public internet. Which service should they use?
- [ ] A) AWS Site-to-Site VPN
- [ ] B) Amazon CloudFront
- [x] C) AWS Direct Connect
- [ ] D) AWS Transit Gateway
### Explanation
AWS Direct Connect establishes a dedicated, private network connection from on-premises to AWS that does not use the public internet. Site-to-Site VPN (A) uses encrypted tunnels over the public internet. CloudFront (B) is a CDN. Transit Gateway (D) connects VPCs but is not a physical connection.
---

## Q10. Which of the following best describes Amazon S3 storage classes?
- [ ] A) Different sizes of storage volumes
- [x] B) Different pricing tiers optimized for various access patterns
- [ ] C) Different types of databases
- [ ] D) Different compute instance families
### Explanation
S3 storage classes (Standard, Standard-IA, One Zone-IA, Glacier, Glacier Deep Archive, Intelligent-Tiering) are pricing tiers optimized for different access patterns and cost requirements. They are not volume sizes (A), databases (C), or compute instances (D).
---

## Q11. A company wants to automatically scale their EC2 instances based on demand. Which AWS feature should they use?
- [ ] A) Elastic Load Balancing
- [ ] B) Amazon CloudFront
- [x] C) Amazon EC2 Auto Scaling
- [ ] D) AWS Lambda
### Explanation
Amazon EC2 Auto Scaling automatically adjusts the number of EC2 instances based on demand, scaling out during peaks and scaling in during low usage. ELB (A) distributes traffic but doesn't scale instances. CloudFront (B) is a CDN. Lambda (D) is serverless compute.
---

## Q12. Which AWS service provides a managed document database compatible with MongoDB?
- [ ] A) Amazon DynamoDB
- [ ] B) Amazon Neptune
- [ ] C) Amazon Keyspaces
- [x] D) Amazon DocumentDB
### Explanation
Amazon DocumentDB is a managed document database service compatible with MongoDB workloads. DynamoDB (A) is a key-value/document NoSQL database but not MongoDB-compatible. Neptune (B) is a graph database. Keyspaces (C) is Cassandra-compatible.
---

## Q13. A company wants to ensure their application can handle sudden traffic spikes without manual intervention. Which cloud computing concept does this describe?
- [x] A) Elasticity
- [ ] B) Durability
- [ ] C) Fault tolerance
- [ ] D) Encryption
### Explanation
Elasticity is the ability to automatically scale resources up or down based on demand without manual intervention. Durability (B) refers to data persistence. Fault tolerance (C) is the ability to continue operating during failures. Encryption (D) is a security mechanism.
---

## Q14. Which AWS service provides a serverless query service that allows you to analyze data directly in Amazon S3 using standard SQL?
- [x] A) Amazon Athena
- [ ] B) Amazon Redshift
- [ ] C) Amazon EMR
- [ ] D) AWS Glue
### Explanation
Amazon Athena is a serverless interactive query service that uses standard SQL to analyze data directly in S3 without loading it into a database. Redshift (B) requires data loading into a warehouse. EMR (C) uses Hadoop frameworks. Glue (D) is an ETL service.
---

## Q15. A company wants to restrict access to an S3 bucket so only specific IAM users can read objects. Which feature should they configure?
- [ ] A) S3 Versioning
- [ ] B) S3 Lifecycle Policies
- [x] C) S3 Bucket Policies
- [ ] D) S3 Transfer Acceleration
### Explanation
S3 Bucket Policies are JSON-based access policies that define who can access the bucket and what actions they can perform. Versioning (A) manages object versions. Lifecycle Policies (B) automate storage class transitions. Transfer Acceleration (D) speeds up uploads.
---

## Q16. Which of the following are benefits of AWS Cloud? (Select TWO)
- [ ] A) Requires long-term contracts for all services
- [x] B) Trade capital expense for variable expense
- [ ] C) Maintain physical access to data centers
- [x] D) Benefit from massive economies of scale
- [ ] E) Fixed capacity provisioning
### Explanation
Trading capital expense for variable expense (B) and benefiting from massive economies of scale (D) are two of the six advantages of cloud computing. AWS does not require long-term contracts (A). Customers do not access data centers (C). Cloud provides flexible, not fixed, capacity (E).
---

## Q17. Which AWS service provides a managed ETL (Extract, Transform, Load) service for preparing data for analytics?
- [ ] A) Amazon Athena
- [ ] B) Amazon Kinesis
- [x] C) AWS Glue
- [ ] D) Amazon Redshift
### Explanation
AWS Glue is a fully managed ETL service that makes it easy to prepare and load data for analytics. Athena (A) queries data in S3. Kinesis (B) processes streaming data. Redshift (D) is a data warehouse that stores and queries data.
---

## Q18. A company needs to deploy a web application quickly without worrying about the underlying infrastructure. Which AWS service provides a Platform-as-a-Service (PaaS) experience?
- [x] A) AWS Elastic Beanstalk
- [ ] B) Amazon EC2
- [ ] C) AWS CloudFormation
- [ ] D) Amazon VPC
### Explanation
AWS Elastic Beanstalk is a PaaS that automatically handles infrastructure provisioning, load balancing, scaling, and health monitoring. EC2 (B) requires managing infrastructure. CloudFormation (C) is infrastructure-as-code. VPC (D) is a networking service.
---

## Q19. Which AWS service helps you discover, classify, and protect sensitive data stored in Amazon S3?
- [ ] A) Amazon GuardDuty
- [ ] B) AWS Secrets Manager
- [ ] C) Amazon Inspector
- [x] D) Amazon Macie
### Explanation
Amazon Macie uses machine learning to automatically discover, classify, and protect sensitive data (like PII and financial data) in S3. GuardDuty (A) detects account-level threats. Secrets Manager (B) stores credentials. Inspector (C) assesses application vulnerabilities.
---

## Q20. A company is designing a disaster recovery strategy and needs to replicate data to a different geographic location. What should they do?
- [ ] A) Deploy across multiple Availability Zones in the same Region
- [x] B) Enable cross-Region replication for their data
- [ ] C) Use a single Availability Zone with backups
- [ ] D) Use larger instance types
### Explanation
Cross-Region replication copies data to a different geographic location, providing disaster recovery protection against Region-level failures. Multi-AZ (A) protects against AZ failures but not Region failures. Single AZ with backups (C) is less resilient. Larger instances (D) do not address disaster recovery.
---

## Q21. Which AWS service provides a managed service for running Apache Kafka?
- [ ] A) Amazon Kinesis
- [x] B) Amazon MSK
- [ ] C) Amazon SQS
- [ ] D) Amazon SNS
### Explanation
Amazon MSK (Managed Streaming for Apache Kafka) is a fully managed service for running Apache Kafka. Kinesis (A) is AWS's proprietary streaming service. SQS (C) is a message queue. SNS (D) is a pub/sub notification service.
---

## Q22. Which of the following is an AWS global service that is NOT tied to a specific Region?
- [ ] A) Amazon EC2
- [ ] B) Amazon RDS
- [x] C) Amazon CloudFront
- [ ] D) Amazon VPC
### Explanation
Amazon CloudFront is a global service that operates across edge locations worldwide and is not tied to a specific Region. EC2 (A), RDS (B), and VPC (D) are all regional services that operate within a specific Region.
---

## Q23. A company wants to monitor their AWS spending and receive alerts when costs exceed a defined budget. Which service should they use?
- [x] A) AWS Budgets
- [ ] B) AWS Cost Explorer
- [ ] C) AWS Pricing Calculator
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Budgets allows you to set custom cost and usage budgets and receive alerts via email or SNS when thresholds are exceeded. Cost Explorer (B) analyzes past spending. Pricing Calculator (C) estimates future costs. Trusted Advisor (D) provides optimization recommendations.
---

## Q24. Which AWS service provides a managed NoSQL database with single-digit millisecond performance at any scale?
- [ ] A) Amazon RDS
- [ ] B) Amazon Redshift
- [x] C) Amazon DynamoDB
- [ ] D) Amazon Aurora
### Explanation
Amazon DynamoDB is a fully managed, serverless NoSQL database providing consistent single-digit millisecond performance at any scale. RDS (A) and Aurora (D) are relational databases. Redshift (B) is a data warehouse.
---

## Q25. A company wants to use AWS but is concerned about vendor lock-in. Which AWS service helps them run containers using open-source Kubernetes?
- [x] A) Amazon EKS
- [ ] B) Amazon ECS
- [ ] C) AWS Elastic Beanstalk
- [ ] D) Amazon Lightsail
### Explanation
Amazon EKS runs open-source Kubernetes, which is portable across cloud providers and on-premises, reducing vendor lock-in concerns. ECS (B) is AWS-proprietary. Elastic Beanstalk (C) is a PaaS. Lightsail (D) provides simplified virtual servers.
---

## Q26. Which AWS service allows you to create and manage cryptographic keys for encrypting data?
- [ ] A) AWS Certificate Manager
- [ ] B) AWS Secrets Manager
- [ ] C) Amazon Macie
- [x] D) AWS KMS
### Explanation
AWS KMS (Key Management Service) creates and manages cryptographic keys used to encrypt data across AWS services. Certificate Manager (A) manages SSL/TLS certificates. Secrets Manager (B) stores secrets like database credentials. Macie (C) discovers sensitive data in S3.
---

## Q27. A company needs to convert text into lifelike speech for their application. Which AWS service should they use?
- [x] A) Amazon Polly
- [ ] B) Amazon Transcribe
- [ ] C) Amazon Lex
- [ ] D) Amazon Comprehend
### Explanation
Amazon Polly converts text into lifelike speech using deep learning. Transcribe (B) converts speech to text (the opposite). Lex (C) builds conversational chatbots. Comprehend (D) performs natural language processing on text.
---

## Q28. Which of the following is a characteristic of Availability Zones?
- [ ] A) They are located in different countries
- [x] B) They are physically separated within a Region and connected by low-latency links
- [ ] C) They share the same power source for efficiency
- [ ] D) Each Region has exactly one Availability Zone
### Explanation
Availability Zones are physically separated facilities within a Region, each with independent power, cooling, and networking, connected by low-latency links. They are within the same Region, not different countries (A). They do NOT share power (C). Regions have multiple AZs (D).
---

## Q29. A company wants to build a chatbot for customer service. Which AWS service provides natural language understanding for building conversational interfaces?
- [ ] A) Amazon Polly
- [ ] B) Amazon Transcribe
- [x] C) Amazon Lex
- [ ] D) Amazon Comprehend
### Explanation
Amazon Lex provides natural language understanding (NLU) and automatic speech recognition (ASR) for building conversational interfaces like chatbots. Polly (A) converts text to speech. Transcribe (B) converts speech to text. Comprehend (D) analyzes text for sentiment and entities.
---

## Q30. Which AWS service provides recommendations to help reduce costs by identifying idle and underutilized resources?
- [x] A) AWS Trusted Advisor
- [ ] B) AWS Config
- [ ] C) Amazon CloudWatch
- [ ] D) AWS CloudTrail
### Explanation
AWS Trusted Advisor provides cost optimization recommendations, including identifying idle resources like unattached EBS volumes, idle load balancers, and underutilized EC2 instances. Config (B) tracks configurations. CloudWatch (C) monitors metrics. CloudTrail (D) logs API calls.
---

## Q31. A company needs to store data that is accessed once per quarter but requires millisecond retrieval when accessed. Which S3 storage class is MOST cost-effective?
- [ ] A) S3 Standard
- [ ] B) S3 Standard-Infrequent Access
- [x] C) S3 Glacier Instant Retrieval
- [ ] D) S3 Glacier Deep Archive
### Explanation
S3 Glacier Instant Retrieval is designed for data accessed approximately once per quarter with millisecond retrieval, at a lower cost than Standard-IA. S3 Standard (A) is for frequently accessed data. Standard-IA (B) is for monthly access patterns. Glacier Deep Archive (D) has retrieval times of 12+ hours.
---

## Q32. Which AWS service provides a managed service for running serverless applications that coordinate multiple AWS services into workflows?
- [ ] A) AWS Lambda
- [x] B) AWS Step Functions
- [ ] C) Amazon SQS
- [ ] D) Amazon EventBridge
### Explanation
AWS Step Functions is a serverless orchestration service that lets you coordinate multiple AWS services into workflows using visual state machines. Lambda (A) runs individual functions. SQS (C) is a message queue. EventBridge (D) is an event bus.
---

## Q33. A company wants to ensure that all data stored in Amazon S3 is encrypted. Which is the simplest way to achieve this?
- [ ] A) Use client-side encryption for every upload
- [x] B) Enable default encryption on the S3 bucket
- [ ] C) Use AWS CloudTrail to monitor encryption
- [ ] D) Create an IAM policy to encrypt data
### Explanation
Enabling default encryption on an S3 bucket ensures all new objects are automatically encrypted at rest using SSE-S3 or SSE-KMS. Client-side encryption (A) requires application changes. CloudTrail (C) monitors API calls, not encryption. IAM policies (D) control access, not encryption.
---

## Q34. Which AWS service provides a fully managed service for deploying, managing, and scaling containerized applications using Kubernetes?
- [ ] A) Amazon ECS
- [x] B) Amazon EKS
- [ ] C) AWS Fargate
- [ ] D) AWS App Runner
### Explanation
Amazon EKS (Elastic Kubernetes Service) is a fully managed Kubernetes service for deploying and scaling containerized applications. ECS (A) is AWS's proprietary container orchestration. Fargate (C) is a serverless compute engine for containers. App Runner (D) is for simpler container/source deployments.
---

## Q35. A company needs to comply with regulations that require data to remain within a specific country. How does AWS help meet this requirement?
- [x] A) By offering Regions in multiple countries, allowing customers to choose where data is stored
- [ ] B) By automatically replicating data across all Regions
- [ ] C) By encrypting all data by default
- [ ] D) By providing dedicated hardware in every country
### Explanation
AWS offers Regions in multiple countries, and data does not leave a Region unless explicitly configured. This allows customers to meet data residency requirements. AWS does NOT automatically replicate across Regions (B). Encryption (C) addresses security, not residency. AWS doesn't have dedicated hardware in every country (D).
---

## Q36. Which AWS service provides a way to distribute incoming application traffic across multiple targets in multiple Availability Zones?
- [ ] A) Amazon Route 53
- [ ] B) Amazon CloudFront
- [x] C) Elastic Load Balancing
- [ ] D) AWS Global Accelerator
### Explanation
Elastic Load Balancing (ELB) automatically distributes incoming traffic across multiple targets (EC2 instances, containers, IP addresses) in one or more Availability Zones. Route 53 (A) is DNS. CloudFront (B) is a CDN. Global Accelerator (D) optimizes network paths globally.
---

## Q37. A company wants to use a service that automatically classifies data and provides natural language processing capabilities. Which AWS service should they use?
- [ ] A) Amazon Rekognition
- [ ] B) Amazon Polly
- [x] C) Amazon Comprehend
- [ ] D) Amazon Transcribe
### Explanation
Amazon Comprehend uses NLP to extract insights from text, including sentiment analysis, entity recognition, and topic modeling. Rekognition (A) analyzes images and video. Polly (B) converts text to speech. Transcribe (D) converts speech to text.
---

## Q38. Which of the following is a valid use case for Amazon CloudFront?
- [ ] A) Running serverless functions
- [ ] B) Storing relational data
- [x] C) Caching and delivering static and dynamic web content globally with low latency
- [ ] D) Managing DNS records
### Explanation
Amazon CloudFront is a CDN that caches and delivers content (static and dynamic) from edge locations worldwide, reducing latency. Serverless functions (A) are Lambda. Relational data (B) is RDS. DNS management (D) is Route 53.
---

## Q39. A company needs to ensure that deleted S3 objects can be recovered for 30 days. Which combination of features should they enable?
- [ ] A) S3 Lifecycle Policies and Cross-Region Replication
- [x] B) S3 Versioning and Lifecycle Policies to expire delete markers after 30 days
- [ ] C) S3 Transfer Acceleration and encryption
- [ ] D) S3 Intelligent-Tiering and access logging
### Explanation
S3 Versioning retains previous versions of objects (including deleted ones), and Lifecycle Policies can be configured to permanently delete old versions after 30 days. Transfer Acceleration (C) speeds uploads. Intelligent-Tiering (D) optimizes storage costs.
---

## Q40. Which AWS service provides a managed service for creating and publishing APIs at any scale?
- [x] A) Amazon API Gateway
- [ ] B) AWS AppSync
- [ ] C) Elastic Load Balancing
- [ ] D) Amazon CloudFront
### Explanation
Amazon API Gateway is a fully managed service for creating, publishing, maintaining, and securing APIs at any scale. AppSync (B) is specifically for GraphQL APIs. ELB (C) distributes traffic. CloudFront (D) is a CDN.
---

## Q41. A company wants to use infrastructure as code to provision AWS resources in a repeatable manner. Which AWS service should they use?
- [ ] A) AWS CodePipeline
- [ ] B) AWS CodeDeploy
- [x] C) AWS CloudFormation
- [ ] D) AWS CodeBuild
### Explanation
AWS CloudFormation lets you model and provision AWS resources using JSON or YAML templates in a repeatable, automated manner. CodePipeline (A) is for CI/CD pipelines. CodeDeploy (B) automates application deployments. CodeBuild (D) compiles source code.
---

## Q42. Which of the following describes the AWS Free Tier?
- [ ] A) All AWS services are free for the first year
- [x] B) Certain AWS services offer free usage up to specified limits, some for 12 months and some always free
- [ ] C) Only EC2 and S3 are included in the Free Tier
- [ ] D) The Free Tier requires a minimum annual commitment
### Explanation
The AWS Free Tier includes three types of offers: 12-month free tier (e.g., EC2, S3), always free (e.g., Lambda, DynamoDB), and short-term trials. Not all services are free (A). It includes many services beyond EC2 and S3 (C). No commitment is required (D).
---

## Q43. A company needs to process and analyze clickstream data in real time. Which AWS service is BEST suited?
- [ ] A) Amazon SQS
- [x] B) Amazon Kinesis Data Streams
- [ ] C) Amazon SNS
- [ ] D) AWS Batch
### Explanation
Amazon Kinesis Data Streams is designed for real-time data streaming and processing, ideal for clickstream analytics. SQS (A) is a message queue, not optimized for real-time streaming. SNS (C) is for notifications. Batch (D) is for batch processing, not real-time.
---

## Q44. Which AWS service provides a way to manage SSL/TLS certificates for use with AWS services?
- [ ] A) AWS KMS
- [x] B) AWS Certificate Manager
- [ ] C) AWS Secrets Manager
- [ ] D) AWS IAM
### Explanation
AWS Certificate Manager (ACM) provisions, manages, and deploys SSL/TLS certificates for use with AWS services like ELB and CloudFront. KMS (A) manages encryption keys. Secrets Manager (C) stores secrets. IAM (D) manages access permissions.
---

## Q45. A company wants to migrate their on-premises VMware workloads to AWS. Which service simplifies this migration?
- [ ] A) AWS DataSync
- [ ] B) AWS Snowball
- [x] C) AWS Application Migration Service
- [ ] D) AWS Transfer Family
### Explanation
AWS Application Migration Service (formerly CloudEndure Migration) simplifies lift-and-shift migrations by automatically converting source servers to run natively on AWS. DataSync (A) transfers data. Snowball (B) is for physical data transport. Transfer Family (D) manages file transfers via SFTP/FTPS.
---

## Q46. Which pillar of the AWS Well-Architected Framework focuses on protecting information, systems, and assets?
- [ ] A) Operational Excellence
- [x] B) Security
- [ ] C) Reliability
- [ ] D) Cost Optimization
### Explanation
The Security pillar focuses on protecting information, systems, and assets through risk assessments and mitigation strategies, including identity management, detective controls, infrastructure protection, data protection, and incident response.
---

## Q47. A company wants to run a workload for exactly 1 year with steady-state usage. Which pricing model provides the best balance of savings and flexibility?
- [ ] A) On-Demand Instances
- [ ] B) Spot Instances
- [x] C) Savings Plans (1-year, No Upfront)
- [ ] D) Dedicated Hosts
### Explanation
Savings Plans (1-year, No Upfront) provide significant discounts over On-Demand with flexibility across instance families and Regions, without requiring upfront payment. On-Demand (A) has no discount. Spot (B) can be interrupted. Dedicated Hosts (D) are for licensing compliance.
---

## Q48. Which AWS service provides a fully managed service for creating data lakes and analyzing data across multiple sources?
- [x] A) AWS Lake Formation
- [ ] B) Amazon Redshift
- [ ] C) Amazon Athena
- [ ] D) AWS Glue
### Explanation
AWS Lake Formation simplifies the process of building, securing, and managing data lakes. Redshift (B) is a data warehouse. Athena (C) queries data in S3. Glue (D) is an ETL service that can be used with Lake Formation but doesn't manage the full data lake lifecycle.
---

## Q49. A company needs to ensure high availability for their web application. Which approach aligns with AWS best practices?
- [ ] A) Deploy all resources in a single Availability Zone
- [ ] B) Use only the largest instance types
- [ ] C) Disable Auto Scaling to maintain consistent performance
- [x] D) Deploy resources across multiple Availability Zones with load balancing
### Explanation
Deploying across multiple AZs with load balancing ensures that if one AZ fails, traffic is routed to healthy instances in other AZs. Single AZ (A) creates a single point of failure. Large instances (B) don't ensure availability. Disabling Auto Scaling (C) reduces resilience.
---

## Q50. Which of the following describes the AWS Cloud Adoption Framework (AWS CAF)?
- [ ] A) A pricing model for AWS services
- [ ] B) A tool for monitoring AWS resources
- [x] C) A framework that provides guidance for organizations planning cloud adoption
- [ ] D) A managed database service
### Explanation
The AWS Cloud Adoption Framework provides guidance and best practices to help organizations develop an efficient cloud adoption strategy across six perspectives: Business, People, Governance, Platform, Security, and Operations. It is not a pricing model (A), monitoring tool (B), or database service (D).
---
