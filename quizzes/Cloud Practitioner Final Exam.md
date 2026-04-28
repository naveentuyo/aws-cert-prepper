# AWS Certified Cloud Practitioner (CLF-C02) — Final Exam
#
# Total Questions: 65
# Passing Score: 70% (46/65)
# Time Limit: 90 minutes
# Covers all four CLF-C02 domains:
#   Domain 1: Cloud Concepts (24%)
#   Domain 2: Security and Compliance (30%)
#   Domain 3: Cloud Technology and Services (34%)
#   Domain 4: Billing, Pricing, and Support (12%)

## Q1. A company is considering migrating to the AWS Cloud. Which of the following is one of the six advantages of cloud computing as defined by AWS? [Domain: 1]
- [ ] A) Maintain physical access to servers
- [ ] B) Trade variable expense for capital expense
- [x] C) Benefit from massive economies of scale
- [ ] D) Increase time to deploy new applications globally
### Explanation
"Benefit from massive economies of scale" is one of the six advantages. Because AWS aggregates usage from hundreds of thousands of customers, it achieves higher economies of scale, which translates to lower pay-as-you-go prices. Option B is backwards — cloud trades capital expense for variable expense. Options A and D are not cloud advantages.
---

## Q2. Which cloud computing model provides the customer with the MOST control over the underlying infrastructure? [Domain: 1]
- [x] A) Infrastructure as a Service (IaaS)
- [ ] B) Platform as a Service (PaaS)
- [ ] C) Software as a Service (SaaS)
- [ ] D) Function as a Service (FaaS)
### Explanation
IaaS provides the most control — you manage the OS, middleware, runtime, and applications while the provider manages the physical hardware and virtualization. PaaS (B) manages the OS and runtime for you. SaaS (C) manages everything. FaaS (D) is serverless with minimal control.
---

## Q3. A company wants to deploy resources in the AWS Cloud but is concerned about a single data center failure. How does AWS address this concern? [Domain: 1]
- [ ] A) By providing multiple AWS Regions in every country
- [x] B) By offering multiple Availability Zones within each Region
- [ ] C) By replicating all data across all Regions automatically
- [ ] D) By providing Dedicated Hosts for every customer
### Explanation
Each AWS Region contains multiple Availability Zones (AZs), which are physically separated data center groups with independent power, cooling, and networking. Deploying across multiple AZs protects against single data center failures. AWS does not have Regions in every country (A), does not auto-replicate across Regions (C), and Dedicated Hosts (D) don't address this concern.
---

## Q4. Which of the following describes the concept of elasticity in cloud computing? [Domain: 1]
- [ ] A) The ability to restrict access to resources based on user identity
- [x] B) The ability to automatically scale resources up and down based on demand
- [ ] C) The ability to deploy resources in multiple geographic locations
- [ ] D) The ability to recover from infrastructure failures
### Explanation
Elasticity is the ability to dynamically acquire resources when demand increases and release them when demand decreases. Access restriction (A) is security. Multi-geography deployment (C) is global reach. Failure recovery (D) is fault tolerance/reliability.
---

## Q5. A company wants to run applications in the AWS Cloud without managing servers, patching, or capacity planning. Which type of service model does this describe? [Domain: 1]
- [ ] A) Infrastructure as a Service
- [ ] B) Containers as a Service
- [x] C) Serverless computing
- [ ] D) Dedicated hosting
### Explanation
Serverless computing (e.g., AWS Lambda, Fargate) eliminates the need to manage servers, handle patching, or plan capacity. The cloud provider manages all infrastructure. IaaS (A) requires managing servers. Containers (B) may still require infrastructure management. Dedicated hosting (D) requires the most management.
---

## Q6. Under the AWS Shared Responsibility Model, which of the following is the customer ALWAYS responsible for? [Domain: 2]
- [ ] A) Physical security of AWS data centers
- [ ] B) Patching the hypervisor
- [x] C) Managing data encryption and IAM user permissions
- [ ] D) Maintaining the global network infrastructure
### Explanation
Customers are always responsible for managing their data (including encryption choices) and IAM user permissions — this is "security IN the cloud." AWS handles physical security (A), hypervisor patching (B), and global network infrastructure (D) — this is "security OF the cloud."
---

## Q7. Which AWS service enables you to manage users, groups, roles, and their permissions to access AWS resources? [Domain: 2]
- [x] A) AWS IAM
- [ ] B) Amazon Cognito
- [ ] C) AWS Shield
- [ ] D) AWS Organizations
### Explanation
AWS IAM (Identity and Access Management) is the service for managing users, groups, roles, and policies that control access to AWS resources. Cognito (B) manages application end-user authentication. Shield (C) provides DDoS protection. Organizations (D) manages multiple AWS accounts.
---

## Q8. A company wants to grant an EC2 instance permission to read from an S3 bucket. What is the AWS-recommended approach? [Domain: 2]
- [ ] A) Store IAM access keys in the application code
- [ ] B) Store IAM access keys in environment variables on the instance
- [x] C) Attach an IAM role to the EC2 instance
- [ ] D) Use the root account credentials
### Explanation
Attaching an IAM role to an EC2 instance provides temporary, automatically rotated credentials — this is the AWS best practice. Storing access keys in code (A) or environment variables (B) creates long-term credentials that can be leaked. Root credentials (D) should never be used for application access.
---

## Q9. Which security practices are recommended by AWS for securing an AWS account? (Select TWO) [Domain: 2]
- [x] A) Enable multi-factor authentication (MFA) on the root user
- [ ] B) Use the root user for daily administrative tasks
- [ ] C) Share IAM credentials among team members for convenience
- [x] D) Apply the principle of least privilege to all IAM policies
- [ ] E) Store access keys in application source code
### Explanation
Enabling MFA on the root user (A) and applying least privilege (D) are fundamental AWS security best practices. The root user should never be used for daily tasks (B). Credentials should never be shared (C) or stored in source code (E) — use IAM roles and Secrets Manager instead.
---

## Q10. Which AWS service provides managed DDoS protection? [Domain: 2]
- [ ] A) AWS WAF
- [x] B) AWS Shield
- [ ] C) Amazon GuardDuty
- [ ] D) Amazon Inspector
### Explanation
AWS Shield provides DDoS protection. Shield Standard is automatically enabled at no cost for all AWS customers. Shield Advanced provides enhanced protection with 24/7 DDoS response team access. WAF (A) protects against application-layer exploits like SQL injection. GuardDuty (C) detects account-level threats. Inspector (D) assesses software vulnerabilities.
---

## Q11. A company wants to protect their web application from SQL injection and cross-site scripting attacks. Which AWS service should they use? [Domain: 2]
- [x] A) AWS WAF
- [ ] B) AWS Shield
- [ ] C) Amazon Macie
- [ ] D) AWS Config
### Explanation
AWS WAF (Web Application Firewall) inspects HTTP/HTTPS requests and blocks common web exploits like SQL injection and XSS using managed or custom rules. Shield (B) protects against DDoS. Macie (C) discovers sensitive data in S3. Config (D) tracks resource configurations.
---

## Q12. Which AWS service continuously monitors for malicious activity and unauthorized behavior in your AWS accounts using machine learning? [Domain: 2]
- [ ] A) AWS Config
- [ ] B) Amazon Inspector
- [x] C) Amazon GuardDuty
- [ ] D) AWS Trusted Advisor
### Explanation
Amazon GuardDuty uses machine learning, anomaly detection, and integrated threat intelligence to continuously monitor for malicious activity. Config (A) tracks resource configurations. Inspector (B) assesses application vulnerabilities. Trusted Advisor (D) provides best-practice recommendations.
---

## Q13. A company needs to find AWS compliance reports such as SOC 2 and PCI DSS certifications. Where should they look? [Domain: 2]
- [ ] A) AWS Config
- [ ] B) AWS CloudTrail
- [x] C) AWS Artifact
- [ ] D) AWS Security Hub
### Explanation
AWS Artifact is a self-service portal for accessing AWS compliance reports (SOC 1/2/3, PCI DSS, ISO 27001, HIPAA BAA). Config (A) tracks your resource configurations. CloudTrail (B) logs API calls. Security Hub (D) aggregates your security findings.
---

## Q14. Which AWS service logs all API calls made in your AWS account, recording who did what, when, and from where? [Domain: 2]
- [ ] A) Amazon CloudWatch
- [x] B) AWS CloudTrail
- [ ] C) AWS Config
- [ ] D) AWS Artifact
### Explanation
AWS CloudTrail records all API calls in your account — the identity, action, time, and source IP. CloudWatch (A) monitors performance metrics. Config (C) tracks resource configuration changes over time. Artifact (D) provides compliance documents.
---

## Q15. Which AWS service continuously monitors and records the configuration of your AWS resources and can evaluate them against compliance rules? [Domain: 2]
- [x] A) AWS Config
- [ ] B) AWS CloudTrail
- [ ] C) Amazon CloudWatch
- [ ] D) AWS Artifact
### Explanation
AWS Config continuously records resource configurations and evaluates them against rules (e.g., "all S3 buckets must have encryption enabled"). CloudTrail (B) logs API calls. CloudWatch (C) monitors metrics. Artifact (D) provides compliance documents.
---

## Q16. Which AWS service helps discover and protect sensitive data such as PII stored in Amazon S3? [Domain: 2]
- [ ] A) Amazon GuardDuty
- [x] B) Amazon Macie
- [ ] C) Amazon Inspector
- [ ] D) AWS Secrets Manager
### Explanation
Amazon Macie uses machine learning to discover, classify, and protect sensitive data like PII in S3. GuardDuty (A) detects account-level threats. Inspector (C) assesses software vulnerabilities. Secrets Manager (D) stores and rotates credentials.
---

## Q17. A company wants to create and manage encryption keys used to encrypt data across AWS services. Which service should they use? [Domain: 2]
- [ ] A) AWS Certificate Manager
- [x] B) AWS KMS
- [ ] C) AWS Secrets Manager
- [ ] D) Amazon Macie
### Explanation
AWS KMS (Key Management Service) creates and manages cryptographic keys for encrypting data. Certificate Manager (A) manages SSL/TLS certificates. Secrets Manager (C) stores secrets like database passwords. Macie (D) discovers sensitive data.
---

## Q18. Which AWS service provides a centralized view of security findings aggregated from GuardDuty, Inspector, Macie, and other services? [Domain: 2]
- [x] A) AWS Security Hub
- [ ] B) AWS Trusted Advisor
- [ ] C) Amazon CloudWatch
- [ ] D) AWS Config
### Explanation
AWS Security Hub aggregates security findings from multiple AWS services into a centralized dashboard with compliance checks. Trusted Advisor (B) provides best-practice recommendations. CloudWatch (C) monitors metrics. Config (D) tracks resource configurations.
---

## Q19. A company has a Java web application and wants a service that automatically handles infrastructure provisioning, load balancing, scaling, and deploys new application versions. Which service should they use? [Domain: 3]
- [ ] A) AWS CloudFormation
- [x] B) AWS Elastic Beanstalk
- [ ] C) Amazon EC2 Auto Scaling
- [ ] D) AWS CodeDeploy
### Explanation
AWS Elastic Beanstalk is a PaaS that creates the environment AND deploys application code automatically. CloudFormation (A) provisions infrastructure but doesn't deploy application code. Auto Scaling (C) scales instances but doesn't deploy apps. CodeDeploy (D) deploys code but doesn't create the environment.
---

## Q20. Which AWS service provides resizable compute capacity in the cloud as virtual servers? [Domain: 3]
- [x] A) Amazon EC2
- [ ] B) AWS Lambda
- [ ] C) Amazon S3
- [ ] D) Amazon RDS
### Explanation
Amazon EC2 (Elastic Compute Cloud) provides resizable virtual servers in the cloud. Lambda (B) is serverless compute. S3 (C) is object storage. RDS (D) is a managed database service.
---

## Q21. Which AWS service runs code in response to events without provisioning or managing servers, and you pay only for the compute time consumed? [Domain: 3]
- [ ] A) Amazon EC2
- [x] B) AWS Lambda
- [ ] C) Amazon ECS
- [ ] D) AWS Elastic Beanstalk
### Explanation
AWS Lambda is serverless compute — it runs code in response to events (S3 uploads, API calls, DynamoDB changes) with no server management. You pay per request and compute duration. EC2 (A) requires managing servers. ECS (C) orchestrates containers. Elastic Beanstalk (D) manages infrastructure but isn't serverless.
---

## Q22. A company wants to run Docker containers on AWS without managing the underlying EC2 instances. Which combination of services provides this? [Domain: 3]
- [ ] A) Amazon EKS with self-managed nodes
- [x] B) Amazon ECS with AWS Fargate
- [ ] C) Amazon EC2 with Docker installed
- [ ] D) AWS Elastic Beanstalk
### Explanation
Amazon ECS with Fargate provides serverless container execution — no EC2 instances to manage. EKS with self-managed nodes (A) requires managing EC2 instances. EC2 with Docker (C) requires managing everything. Elastic Beanstalk (D) is a PaaS, not specifically a container orchestration service.
---

## Q23. Which AWS service provides a managed Kubernetes service? [Domain: 3]
- [ ] A) Amazon ECS
- [x] B) Amazon EKS
- [ ] C) AWS Fargate
- [ ] D) AWS Lambda
### Explanation
Amazon EKS (Elastic Kubernetes Service) is a managed Kubernetes service. ECS (A) is AWS's proprietary container orchestration. Fargate (C) is a serverless compute engine for containers, not an orchestrator. Lambda (D) is serverless functions.
---

## Q24. Which AWS service provides object storage with 99.999999999% (11 nines) durability? [Domain: 3]
- [x] A) Amazon S3
- [ ] B) Amazon EBS
- [ ] C) Amazon EFS
- [ ] D) AWS Storage Gateway
### Explanation
Amazon S3 provides 99.999999999% durability for objects stored across multiple AZs. EBS (B) provides block storage for EC2. EFS (C) provides managed file storage. Storage Gateway (D) is a hybrid storage service.
---

## Q25. A company needs to store objects that are infrequently accessed but must be available within milliseconds when needed. Which S3 storage class is MOST cost-effective?
- [ ] A) S3 Standard
- [x] B) S3 Standard-Infrequent Access
- [ ] C) S3 Glacier Instant Retrieval
- [ ] D) S3 Glacier Deep Archive
### Explanation
S3 Standard-IA is designed for data accessed less frequently but requiring rapid access (millisecond retrieval) at lower cost than Standard. S3 Standard (A) is more expensive for infrequent access. Glacier Instant Retrieval (C) is for data accessed roughly once per quarter. Glacier Deep Archive (D) has 12+ hour retrieval times.
---

## Q26. A company needs to store archival data that is rarely accessed and can tolerate retrieval times of 12 hours or more. Which S3 storage class provides the lowest cost?
- [ ] A) S3 Standard-Infrequent Access
- [ ] B) S3 One Zone-Infrequent Access
- [ ] C) S3 Glacier Instant Retrieval
- [x] D) S3 Glacier Deep Archive
### Explanation
S3 Glacier Deep Archive is the lowest-cost storage class, designed for long-term archival with retrieval times of 12-48 hours. Standard-IA (A) and One Zone-IA (B) are for infrequent but faster access. Glacier Instant Retrieval (C) provides millisecond access at higher cost.
---

## Q27. Which S3 feature automatically moves objects between storage classes based on changing access patterns to optimize costs?
- [ ] A) S3 Versioning
- [ ] B) S3 Lifecycle Policies
- [x] C) S3 Intelligent-Tiering
- [ ] D) S3 Cross-Region Replication
### Explanation
S3 Intelligent-Tiering automatically moves objects between frequent and infrequent access tiers based on actual access patterns. Lifecycle Policies (B) move objects based on predefined time rules, not access patterns. Versioning (A) manages object versions. Cross-Region Replication (D) copies objects to another Region.
---

## Q28. Which AWS service provides block-level storage volumes for use with Amazon EC2 instances?
- [ ] A) Amazon S3
- [x] B) Amazon EBS
- [ ] C) Amazon EFS
- [ ] D) Amazon FSx
### Explanation
Amazon EBS (Elastic Block Store) provides persistent block-level storage volumes attached to EC2 instances. S3 (A) is object storage. EFS (C) is a managed NFS file system. FSx (D) provides managed file systems (Windows File Server, Lustre).
---

## Q29. Which AWS service provides a managed relational database that supports MySQL, PostgreSQL, Oracle, SQL Server, and MariaDB?
- [x] A) Amazon RDS
- [ ] B) Amazon DynamoDB
- [ ] C) Amazon Redshift
- [ ] D) Amazon ElastiCache
### Explanation
Amazon RDS (Relational Database Service) supports multiple relational database engines. DynamoDB (B) is NoSQL. Redshift (C) is a data warehouse. ElastiCache (D) is in-memory caching.
---

## Q30. Which AWS service is a fully managed NoSQL database that provides single-digit millisecond performance at any scale?
- [ ] A) Amazon RDS
- [x] B) Amazon DynamoDB
- [ ] C) Amazon Redshift
- [ ] D) Amazon Aurora
### Explanation
Amazon DynamoDB is a fully managed, serverless NoSQL key-value database with consistent single-digit millisecond performance. RDS (A) and Aurora (D) are relational databases. Redshift (C) is a data warehouse.
---

## Q31. Which AWS database service is MySQL and PostgreSQL-compatible and offers up to five times better performance than standard MySQL?
- [ ] A) Amazon RDS for MySQL
- [x] B) Amazon Aurora
- [ ] C) Amazon DynamoDB
- [ ] D) Amazon Neptune
### Explanation
Amazon Aurora is MySQL and PostgreSQL-compatible, offering up to 5x MySQL throughput and 3x PostgreSQL throughput. RDS for MySQL (A) runs standard MySQL. DynamoDB (C) is NoSQL. Neptune (D) is a graph database.
---

## Q32. A developer needs to store session data for a web application with sub-millisecond latency. Which AWS service is BEST suited?
- [ ] A) Amazon RDS
- [ ] B) Amazon S3
- [x] C) Amazon ElastiCache
- [ ] D) Amazon Redshift
### Explanation
Amazon ElastiCache provides in-memory caching (Redis or Memcached) with sub-millisecond response times, ideal for session data. RDS (A) has higher latency. S3 (B) is object storage. Redshift (D) is a data warehouse for analytics.
---

## Q33. Which of the following are components of Amazon VPC? (Select TWO)
- [x] A) Subnets
- [ ] B) Edge Locations
- [x] C) Security Groups
- [ ] D) Availability Zones
- [ ] E) CloudFront Distributions
### Explanation
Subnets (A) and Security Groups (C) are components you configure within a VPC. Subnets divide the VPC's IP range, and Security Groups act as virtual firewalls for instances. Edge Locations (B) are part of CloudFront's CDN. Availability Zones (D) are part of the global infrastructure, not VPC components. CloudFront Distributions (E) are CDN configurations.
---

## Q34. Which AWS service provides a content delivery network (CDN) that caches content at edge locations worldwide to reduce latency?
- [ ] A) AWS Global Accelerator
- [ ] B) Amazon Route 53
- [x] C) Amazon CloudFront
- [ ] D) Elastic Load Balancing
### Explanation
Amazon CloudFront caches content at 400+ edge locations worldwide, reducing latency for end users. Global Accelerator (A) optimizes network paths but isn't a CDN. Route 53 (B) is DNS. ELB (D) distributes traffic within a Region.
---

## Q35. Which AWS service automatically distributes incoming application traffic across multiple targets such as EC2 instances in multiple Availability Zones?
- [ ] A) Amazon Route 53
- [x] B) Elastic Load Balancing
- [ ] C) Amazon CloudFront
- [ ] D) AWS Auto Scaling
### Explanation
Elastic Load Balancing (ELB) automatically distributes incoming traffic across multiple targets in one or more AZs. Route 53 (A) is DNS. CloudFront (C) is a CDN. Auto Scaling (D) adjusts the number of instances but doesn't distribute traffic.
---

## Q36. A company needs a dedicated, private network connection from their on-premises data center to AWS that does NOT traverse the public internet. Which service should they use?
- [x] A) AWS Direct Connect
- [ ] B) AWS Site-to-Site VPN
- [ ] C) Amazon VPC Peering
- [ ] D) AWS Transit Gateway
### Explanation
AWS Direct Connect provides a dedicated private physical connection from on-premises to AWS. Site-to-Site VPN (B) uses encrypted tunnels over the public internet. VPC Peering (C) connects two VPCs. Transit Gateway (D) connects multiple VPCs but isn't a physical connection.
---

## Q37. Which AWS service provides a scalable DNS web service that routes end users to applications?
- [x] A) Amazon Route 53
- [ ] B) Amazon CloudFront
- [ ] C) Elastic Load Balancing
- [ ] D) AWS Global Accelerator
### Explanation
Amazon Route 53 is a scalable DNS service that translates domain names to IP addresses and routes users to applications. CloudFront (B) is a CDN. ELB (C) distributes traffic across targets. Global Accelerator (D) optimizes network paths.
---

## Q38. A company wants to automate the provisioning of AWS infrastructure using JSON or YAML templates. Which service should they use?
- [x] A) AWS CloudFormation
- [ ] B) AWS Elastic Beanstalk
- [ ] C) AWS CodeDeploy
- [ ] D) AWS OpsWorks
### Explanation
AWS CloudFormation is an infrastructure-as-code service that provisions resources using JSON or YAML templates in a repeatable, automated manner. Elastic Beanstalk (B) is a PaaS. CodeDeploy (C) deploys application code. OpsWorks (D) is a configuration management service.
---

## Q39. Which AWS service monitors AWS resources, collects metrics, sets alarms, and can trigger automated actions?
- [x] A) Amazon CloudWatch
- [ ] B) AWS CloudTrail
- [ ] C) AWS Config
- [ ] D) AWS X-Ray
### Explanation
Amazon CloudWatch monitors resources and applications, collecting metrics (CPU, memory, etc.), setting alarms, and triggering actions like Auto Scaling. CloudTrail (B) logs API calls. Config (C) tracks resource configurations. X-Ray (D) traces distributed applications.
---

## Q40. A company wants to receive alerts when their AWS spending exceeds a defined budget. Which service should they use?
- [x] A) AWS Budgets
- [ ] B) AWS Cost Explorer
- [ ] C) AWS Pricing Calculator
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Budgets lets you set custom cost and usage budgets and receive alerts via email or SNS when thresholds are exceeded. Cost Explorer (B) analyzes past spending. Pricing Calculator (C) estimates future costs. Trusted Advisor (D) provides optimization recommendations.
---

## Q41. A company wants to analyze their AWS spending patterns over the past 12 months and forecast future costs. Which tool should they use?
- [ ] A) AWS Budgets
- [x] B) AWS Cost Explorer
- [ ] C) AWS Pricing Calculator
- [ ] D) AWS Billing Dashboard
### Explanation
AWS Cost Explorer provides detailed visualizations of spending patterns over time (up to 12 months historical + 12 months forecast) with filtering by service, account, and tags. Budgets (A) sets alerts. Pricing Calculator (C) estimates costs before deployment. Billing Dashboard (D) shows current month summary.
---

## Q42. A startup wants to estimate the cost of running their planned architecture on AWS before migrating. Which tool should they use?
- [ ] A) AWS Cost Explorer
- [x] B) AWS Pricing Calculator
- [ ] C) AWS Budgets
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Pricing Calculator lets you model your architecture and estimate costs before deploying. Cost Explorer (A) analyzes historical spending. Budgets (C) sets spending alerts. Trusted Advisor (D) provides recommendations for existing resources.
---

## Q43. Which of the following are functions of AWS Trusted Advisor? (Select TWO)
- [x] A) Identifying idle and underutilized resources to reduce costs
- [ ] B) Automatically patching EC2 instances
- [x] C) Checking for security groups with unrestricted access
- [ ] D) Deploying infrastructure as code
- [ ] E) Migrating databases to AWS
### Explanation
Trusted Advisor checks for cost optimization opportunities like idle resources (A) and security issues like unrestricted security groups (C). It provides recommendations across five categories: cost optimization, performance, security, fault tolerance, and service limits. It does not patch instances (B), deploy infrastructure (D), or migrate databases (E).
---

## Q44. Which EC2 pricing model offers up to 90% discount but instances can be interrupted with a 2-minute warning?
- [ ] A) On-Demand Instances
- [ ] B) Reserved Instances
- [x] C) Spot Instances
- [ ] D) Dedicated Hosts
### Explanation
Spot Instances use unused EC2 capacity at up to 90% discount but can be reclaimed by AWS with 2 minutes notice. Best for fault-tolerant workloads like batch processing. On-Demand (A) has no discount. Reserved (B) requires commitment. Dedicated Hosts (D) are for licensing compliance.
---

## Q45. A company runs a production database 24/7 with steady-state usage and wants to reduce costs with a 1-year or 3-year commitment. Which pricing option provides the best savings?
- [ ] A) On-Demand Instances
- [x] B) Reserved Instances or Savings Plans
- [ ] C) Spot Instances
- [ ] D) Dedicated Instances
### Explanation
Reserved Instances and Savings Plans provide up to 72% discount for steady-state workloads with 1-year or 3-year commitments. On-Demand (A) has no discount. Spot (C) can be interrupted — unsuitable for production databases. Dedicated Instances (D) are for compliance, not cost optimization.
---

## Q46. Which AWS support plan provides access to a designated Technical Account Manager (TAM)?
- [ ] A) Basic
- [ ] B) Developer
- [ ] C) Business
- [x] D) Enterprise
### Explanation
Only the Enterprise support plan includes a designated TAM. Basic (A) has no technical support. Developer (B) provides business-hours email support. Business (C) provides 24/7 phone support but no TAM.
---

## Q47. Which AWS service enables consolidated billing for multiple AWS accounts and allows applying Service Control Policies across the organization?
- [x] A) AWS Organizations
- [ ] B) AWS Control Tower
- [ ] C) AWS IAM
- [ ] D) AWS Budgets
### Explanation
AWS Organizations provides consolidated billing across multiple accounts and Service Control Policies (SCPs) for centralized governance. Control Tower (B) automates multi-account setup but relies on Organizations. IAM (C) manages access within a single account. Budgets (D) sets spending alerts.
---

## Q48. A company needs to migrate 50 TB of data to AWS. Internet transfer would take weeks. Which service provides the fastest physical data transfer?
- [ ] A) AWS DataSync
- [ ] B) AWS Direct Connect
- [x] C) AWS Snowball Edge
- [ ] D) Amazon S3 Transfer Acceleration
### Explanation
AWS Snowball Edge is a physical device (80 TB capacity) for transferring large amounts of data. For 50 TB, shipping a device is faster than network transfer. DataSync (A) and Transfer Acceleration (D) use the network. Direct Connect (B) requires weeks to provision.
---

## Q49. A company wants to migrate an on-premises MySQL database to Amazon RDS with minimal downtime while the source database remains operational. Which service should they use?
- [x] A) AWS Database Migration Service (DMS)
- [ ] B) AWS Application Migration Service
- [ ] C) AWS Snowball Edge
- [ ] D) AWS Schema Conversion Tool
### Explanation
AWS DMS migrates databases with minimal downtime by continuously replicating changes while the source remains operational. Application Migration Service (B) migrates servers, not databases. Snowball (C) is for physical data transfer. SCT (D) converts schemas between different database engines but doesn't migrate data.
---

## Q50. Which of the following are pillars of the AWS Well-Architected Framework? (Select TWO)
- [x] A) Reliability
- [ ] B) Elasticity
- [ ] C) Scalability
- [x] D) Sustainability
- [ ] E) Automation
### Explanation
Reliability (A) and Sustainability (D) are two of the six pillars. The full list is: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. Elasticity (B), Scalability (C), and Automation (E) are cloud computing concepts but not named pillars.
---

## Q51. Which pillar of the Well-Architected Framework focuses on protecting information, systems, and assets?
- [ ] A) Operational Excellence
- [x] B) Security
- [ ] C) Reliability
- [ ] D) Cost Optimization
### Explanation
The Security pillar focuses on protecting information and systems through identity management, detective controls, infrastructure protection, data protection, and incident response. Operational Excellence (A) focuses on operations. Reliability (C) focuses on failure recovery. Cost Optimization (D) focuses on avoiding unnecessary costs.
---

## Q52. A company needs to design a highly available architecture that can survive an Availability Zone failure. Which approach aligns with AWS best practices?
- [ ] A) Deploy all resources in a single AZ with larger instance types
- [x] B) Deploy resources across multiple Availability Zones with load balancing
- [ ] C) Deploy all resources in one Region with no redundancy
- [ ] D) Use Dedicated Hosts in a single AZ
### Explanation
Deploying across multiple AZs with load balancing ensures that if one AZ fails, traffic is routed to healthy instances in other AZs. Single AZ deployments (A, C) create single points of failure. Dedicated Hosts (D) don't address availability.
---

## Q53. Under the Shared Responsibility Model, who is responsible for patching the guest operating system on an Amazon EC2 instance?
- [ ] A) AWS
- [x] B) The customer
- [ ] C) Both AWS and the customer equally
- [ ] D) The internet service provider
### Explanation
The customer is responsible for patching the guest OS on EC2 instances. AWS manages the underlying infrastructure (hardware, hypervisor), while customers manage everything they put on the infrastructure — OS patches, application software, and security configuration.
---

## Q54. A company wants to add user sign-up, sign-in, and social login (Google, Facebook) to their mobile application. Which AWS service should they use?
- [ ] A) AWS IAM
- [x] B) Amazon Cognito
- [ ] C) AWS IAM Identity Center
- [ ] D) AWS Directory Service
### Explanation
Amazon Cognito is designed for mobile and web application user authentication, supporting user pools (sign-up/sign-in) and social identity providers (Google, Facebook, Apple). IAM (A) manages AWS account access. IAM Identity Center (C) provides SSO for AWS accounts. Directory Service (D) integrates with Microsoft AD.
---

## Q55. Which of the following is an AWS global service that is NOT tied to a specific Region?
- [ ] A) Amazon EC2
- [ ] B) Amazon RDS
- [x] C) AWS IAM
- [ ] D) Amazon VPC
### Explanation
AWS IAM is a global service — users, groups, roles, and policies are not tied to a specific Region. EC2 (A), RDS (B), and VPC (D) are all regional services.
---

## Q56. A company wants to use machine learning to analyze images for content moderation without building custom ML models. Which AWS service should they use?
- [x] A) Amazon Rekognition
- [ ] B) Amazon SageMaker
- [ ] C) Amazon Comprehend
- [ ] D) Amazon Textract
### Explanation
Amazon Rekognition provides pre-built image and video analysis including content moderation without requiring ML expertise. SageMaker (B) is for building custom ML models. Comprehend (C) is for natural language processing. Textract (D) extracts text from documents.
---

## Q57. Which AWS service converts speech to text and supports features like speaker identification?
- [ ] A) Amazon Polly
- [x] B) Amazon Transcribe
- [ ] C) Amazon Lex
- [ ] D) Amazon Translate
### Explanation
Amazon Transcribe converts audio to text with features like speaker diarization (identifying who said what). Polly (A) converts text to speech (the opposite). Lex (C) builds conversational chatbots. Translate (D) translates text between languages.
---

## Q58. A company needs to host a static website with the MOST cost-effective solution. Which AWS service should they use?
- [ ] A) Amazon EC2
- [x] B) Amazon S3
- [ ] C) AWS Elastic Beanstalk
- [ ] D) Amazon Lightsail
### Explanation
Amazon S3 can host static websites (HTML, CSS, JavaScript) at very low cost with high durability. EC2 (A) and Elastic Beanstalk (C) are overkill for static content. Lightsail (D) is simpler than EC2 but still more expensive than S3.
---

## Q59. Which of the following are advantages of the AWS Cloud? (Select TWO)
- [x] A) Stop guessing capacity
- [ ] B) Increase fixed infrastructure costs
- [x] C) Increase speed and agility
- [ ] D) Require long-term contracts for all services
- [ ] E) Maintain physical data center access
### Explanation
"Stop guessing capacity" (A) — cloud allows scaling based on demand. "Increase speed and agility" (C) — resources can be provisioned in minutes. Fixed costs (B) describe traditional IT. Long-term contracts (D) are not required. Physical access (E) is not a cloud advantage.
---

## Q60. Which of the following is a responsibility of AWS under the Shared Responsibility Model? (Select TWO)
- [ ] A) Configuring customer security groups
- [x] B) Managing the physical infrastructure of data centers
- [ ] C) Managing customer IAM policies
- [x] D) Patching the underlying host operating system for managed services like RDS
- [ ] E) Encrypting customer application data
### Explanation
AWS manages physical infrastructure (B) and patches the host OS for managed services like RDS (D). Configuring security groups (A), managing IAM policies (C), and encrypting application data (E) are customer responsibilities.
---

## Q61. A company wants to track which AWS services are costing the most and tag resources by department for cost allocation. Which AWS features should they use?
- [ ] A) AWS Budgets and AWS Shield
- [x] B) AWS Cost Explorer and Cost Allocation Tags
- [ ] C) AWS Trusted Advisor and AWS Config
- [ ] D) AWS CloudTrail and Amazon CloudWatch
### Explanation
Cost Explorer provides detailed cost breakdowns by service, and Cost Allocation Tags let you tag resources by department/project for granular cost tracking. Budgets (A) sets alerts but doesn't provide detailed analysis. Trusted Advisor (C) provides recommendations. CloudTrail (D) logs API calls.
---

## Q62. A company needs a fully managed message queuing service to decouple application components so each tier can scale independently. Which service should they use?
- [x] A) Amazon SQS
- [ ] B) Amazon SNS
- [ ] C) Amazon Kinesis
- [ ] D) AWS Step Functions
### Explanation
Amazon SQS (Simple Queue Service) is a message queue that decouples components, allowing each to process at its own pace. SNS (B) is pub/sub for fan-out notifications. Kinesis (C) processes real-time streaming data. Step Functions (D) orchestrates workflows.
---

## Q63. A company wants to send the same notification to multiple subscribers simultaneously — email, SMS, and an HTTP endpoint. Which AWS service supports this fan-out pattern?
- [ ] A) Amazon SQS
- [x] B) Amazon SNS
- [ ] C) Amazon Kinesis
- [ ] D) AWS EventBridge
### Explanation
Amazon SNS (Simple Notification Service) uses a pub/sub pattern where a message published to a topic is delivered to all subscribers simultaneously. SQS (A) is point-to-point queuing. Kinesis (C) processes streaming data. EventBridge (D) routes events but is not designed for multi-protocol fan-out.
---

## Q64. A company wants to set up and govern a secure, multi-account AWS environment based on best practices with pre-configured guardrails. Which service should they use?
- [ ] A) AWS Organizations
- [x] B) AWS Control Tower
- [ ] C) AWS IAM
- [ ] D) AWS Config
### Explanation
AWS Control Tower automates the setup and governance of a multi-account environment with pre-configured guardrails (preventive and detective). Organizations (A) provides account management but less automated governance. IAM (C) manages access within accounts. Config (D) tracks resource configurations.
---

## Q65. Which of the following best describes the AWS Free Tier?
- [ ] A) All AWS services are free for the first 12 months
- [x] B) Certain services offer free usage up to specified limits — some for 12 months, some always free, and some as short-term trials
- [ ] C) Only EC2 and S3 are included in the Free Tier
- [ ] D) The Free Tier requires a minimum annual spending commitment
### Explanation
The AWS Free Tier includes three types: 12-Month Free (e.g., 750 hrs/month EC2 t2.micro), Always Free (e.g., 1M Lambda requests/month, 25 GB DynamoDB), and Short-Term Trials. Not all services are free (A). Many services beyond EC2/S3 are included (C). No commitment is required (D).
---
