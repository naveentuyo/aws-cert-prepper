# AWS Certified Cloud Practitioner (CLF-C02) — Realistic Practice Test
#
# Total Questions: 50
# Passing Score: 70% (35/50)
# Time Limit: 90 minutes
# Difficulty: Hard — Scenario-based questions matching real exam style

## Q1. A company has a Java web application. The company wants to use automated deployment to create the AWS environment and deploy new versions of its application. Which AWS service will meet these requirements?
- [ ] A) AWS CodeDeploy
- [ ] B) AWS CloudFormation
- [x] C) AWS Elastic Beanstalk
- [ ] D) Amazon EC2 Auto Scaling
### Explanation
AWS Elastic Beanstalk is a PaaS that both creates the AWS environment (load balancers, Auto Scaling groups, EC2 instances) AND deploys application code automatically. This is the key distinction — the question asks for a single service that does both. CloudFormation (B) provisions infrastructure but does not handle application deployment natively. CodeDeploy (A) deploys application code but does not create the environment. EC2 Auto Scaling (D) scales instances but does not deploy applications or create environments.
---

## Q2. A company is migrating its on-premises data center to AWS. The company's compliance team requires that all data remain encrypted at rest and that encryption keys be managed and rotated by the company, not by AWS. Which AWS service allows the company to manage its own encryption keys?
- [ ] A) AWS Certificate Manager
- [ ] B) AWS Secrets Manager
- [x] C) AWS KMS with customer managed keys
- [ ] D) Amazon S3 default encryption
### Explanation
AWS KMS with customer managed keys (CMKs) allows the company to create, manage, and rotate their own encryption keys while still using AWS infrastructure. Certificate Manager (A) manages SSL/TLS certificates, not data encryption keys. Secrets Manager (B) stores secrets like database credentials but is not a key management service. S3 default encryption (D) uses AWS-managed keys by default, which does not meet the requirement for the company to manage keys themselves.
---

## Q3. A startup is building a mobile application that requires user sign-up, sign-in, and access control. The application needs to support social identity providers such as Google and Facebook. Which AWS service should the startup use to manage user authentication?
- [ ] A) AWS IAM
- [ ] B) AWS IAM Identity Center
- [x] C) Amazon Cognito
- [ ] D) AWS Directory Service
### Explanation
Amazon Cognito is designed for mobile and web application user authentication, supporting user pools (sign-up/sign-in) and identity pools (federated access via Google, Facebook, etc.). IAM (A) manages AWS service access for internal users, not application end users. IAM Identity Center (B) provides SSO for AWS accounts using corporate identity providers, not social providers for mobile apps. Directory Service (D) integrates with Microsoft Active Directory for enterprise environments.
---

## Q4. A company runs a production workload on Amazon EC2 instances. The workload requires consistent performance and cannot tolerate interruptions. The company wants to reduce compute costs while maintaining availability. Which purchasing option should the company choose?
- [ ] A) Spot Instances
- [ ] B) On-Demand Instances
- [x] C) Reserved Instances or Savings Plans
- [ ] D) Dedicated Hosts
### Explanation
Reserved Instances or Savings Plans provide significant discounts (up to 72%) for steady-state, production workloads with a 1-year or 3-year commitment. The workload cannot tolerate interruptions, which eliminates Spot Instances (A) since they can be reclaimed with 2 minutes notice. On-Demand (B) provides no discount. Dedicated Hosts (D) are for licensing compliance or regulatory requirements, not cost optimization.
---

## Q5. A solutions architect needs to store objects that are frequently accessed for the first 30 days after creation, then rarely accessed for the next 90 days, and finally archived for long-term retention. The architect wants to minimize storage costs automatically. Which S3 feature should they configure?
- [ ] A) S3 Versioning
- [ ] B) S3 Intelligent-Tiering
- [x] C) S3 Lifecycle Policies
- [ ] D) S3 Cross-Region Replication
### Explanation
S3 Lifecycle Policies allow you to define rules that automatically transition objects between storage classes based on age — for example, Standard to Standard-IA after 30 days, then to Glacier after 120 days. This matches the exact requirement of time-based transitions. Intelligent-Tiering (B) moves objects based on access patterns, not predefined time schedules. Versioning (A) manages object versions. Cross-Region Replication (D) copies objects to another Region.
---

## Q6. A company has deployed a web application behind an Application Load Balancer across two Availability Zones. During a sudden traffic spike, users experience slow response times. Which AWS service should the company configure to automatically add EC2 instances when demand increases?
- [ ] A) Elastic Load Balancing
- [ ] B) Amazon CloudFront
- [x] C) Amazon EC2 Auto Scaling
- [ ] D) AWS Lambda
### Explanation
Amazon EC2 Auto Scaling automatically adjusts the number of EC2 instances based on demand, adding instances during traffic spikes and removing them when demand drops. The ALB is already in place distributing traffic — the missing piece is scaling the compute capacity behind it. ELB (A) distributes traffic but does not add instances. CloudFront (B) caches content at edge locations but doesn't scale backend compute. Lambda (D) is serverless and not applicable to an existing EC2-based architecture.
---

## Q7. A financial services company must ensure that all API calls made to their AWS account are logged for regulatory compliance. The logs must be stored for 7 years and be tamper-proof. Which combination of AWS services meets these requirements?
- [ ] A) Amazon CloudWatch Logs with a 7-year retention policy
- [x] B) AWS CloudTrail with logs delivered to an S3 bucket configured with Object Lock
- [ ] C) AWS Config with an Amazon RDS database for long-term storage
- [ ] D) AWS Trusted Advisor with Amazon S3 archival
### Explanation
AWS CloudTrail logs all API calls made in an AWS account. Delivering these logs to an S3 bucket with Object Lock (WORM — Write Once Read Many) ensures they are tamper-proof and retained for the required 7 years. CloudWatch Logs (A) monitors metrics and application logs but is not designed for API call auditing. AWS Config (C) tracks resource configuration changes, not API calls. Trusted Advisor (D) provides recommendations, not logging.
---

## Q8. A company is running a three-tier web application entirely on Amazon EC2 instances. The company wants to decouple the application tiers so that each tier can scale independently. Which AWS service should the company place between the tiers?
- [ ] A) Elastic Load Balancing
- [ ] B) Amazon SNS
- [x] C) Amazon SQS
- [ ] D) AWS Step Functions
### Explanation
Amazon SQS (Simple Queue Service) is a message queue that decouples application components, allowing each tier to process messages at its own pace and scale independently. If the backend is slow, messages queue up instead of causing failures. ELB (A) distributes incoming HTTP traffic but doesn't decouple application tiers asynchronously. SNS (B) is pub/sub for notifications, not queuing. Step Functions (D) orchestrates workflows but doesn't provide the buffering and decoupling that SQS does.
---

## Q9. A company has multiple AWS accounts for development, staging, and production. The security team wants to apply a policy that prevents any account from launching resources outside of the us-east-1 and eu-west-1 Regions. Which AWS feature should they use?
- [ ] A) IAM permission boundaries
- [ ] B) AWS Config rules
- [x] C) Service Control Policies (SCPs) in AWS Organizations
- [ ] D) Security group rules
### Explanation
Service Control Policies (SCPs) in AWS Organizations provide centralized control over the maximum available permissions across all accounts in the organization. An SCP can deny all actions outside specific Regions, applying to every user and role in every member account. IAM permission boundaries (A) apply to individual users/roles within a single account, not across the organization. Config rules (B) detect non-compliance but don't prevent actions. Security groups (D) control network traffic, not Region access.
---

## Q10. A company wants to host a static single-page application (SPA) built with React. The application must be globally available with low latency and support HTTPS. Which combination of AWS services provides the MOST cost-effective solution?
- [ ] A) Amazon EC2 instances behind an Application Load Balancer in multiple Regions
- [ ] B) AWS Elastic Beanstalk with a multi-Region deployment
- [x] C) Amazon S3 for hosting with Amazon CloudFront for global distribution and AWS Certificate Manager for HTTPS
- [ ] D) Amazon Lightsail with a CDN add-on
### Explanation
Hosting a static SPA on S3 is the most cost-effective approach — no servers to manage. CloudFront provides global CDN distribution with low latency, and ACM provides free SSL/TLS certificates for HTTPS. EC2 (A) and Elastic Beanstalk (B) are overkill and expensive for static content. Lightsail (D) is simpler than EC2 but still more expensive than S3 + CloudFront for static hosting.
---

## Q11. A company is running an application on Amazon EC2 that processes sensitive customer data. The company's security policy requires that the EC2 instance has no direct internet access, but the application needs to download software updates from the internet. Which solution meets these requirements?
- [ ] A) Attach an Elastic IP address to the instance
- [ ] B) Place the instance in a public subnet with a restrictive security group
- [x] C) Place the instance in a private subnet and route internet traffic through a NAT gateway
- [ ] D) Use AWS Direct Connect to access the internet
### Explanation
A NAT gateway allows instances in a private subnet to initiate outbound connections to the internet (for updates) while preventing inbound connections from the internet. The instance remains in a private subnet with no public IP, satisfying the security requirement. An Elastic IP (A) gives the instance a public address, allowing direct internet access. A public subnet (B) exposes the instance to the internet. Direct Connect (D) connects to on-premises, not the public internet.
---

## Q12. A company is evaluating whether to migrate to AWS. The CTO wants to understand the total cost of ownership (TCO) compared to their current on-premises infrastructure. Which factors should be included in the on-premises TCO calculation that would NOT apply to AWS? (Select TWO)
- [x] A) Data center facility costs including power, cooling, and physical space
- [ ] B) Application software licensing
- [x] C) Hardware procurement and refresh cycles every 3-5 years
- [ ] D) Employee salaries for application developers
- [ ] E) Network bandwidth costs
### Explanation
Data center facility costs (A) — power, cooling, physical space, and physical security — are eliminated when moving to AWS since AWS manages all facilities. Hardware procurement and refresh cycles (C) are also eliminated since AWS owns and maintains all physical hardware. Application licensing (B) may still apply on AWS. Developer salaries (D) remain regardless of infrastructure. Network bandwidth costs (E) exist in both models (on-premises ISP costs vs. AWS data transfer charges).
---

## Q13. A company runs a web application that experiences unpredictable traffic patterns — sometimes thousands of requests per second, sometimes near zero. The company wants to minimize costs during idle periods while maintaining the ability to handle traffic bursts instantly. Which compute solution is MOST appropriate?
- [ ] A) Amazon EC2 On-Demand Instances with Auto Scaling
- [ ] B) Amazon EC2 Reserved Instances
- [x] C) AWS Lambda
- [ ] D) Amazon EC2 Spot Instances
### Explanation
AWS Lambda scales automatically from zero to thousands of concurrent executions and you pay nothing when there are no requests. This perfectly matches unpredictable traffic with idle periods. EC2 with Auto Scaling (A) still incurs costs for minimum running instances. Reserved Instances (B) require a commitment and run 24/7. Spot Instances (D) can be interrupted and still require running instances.
---

## Q14. A company has deployed an application across three Availability Zones in a single Region. A natural disaster destroys the entire Region. Which disaster recovery strategy would have protected the company?
- [ ] A) Deploying across more Availability Zones in the same Region
- [ ] B) Using Amazon S3 with versioning enabled
- [x] C) Deploying a standby environment in a second AWS Region
- [ ] D) Enabling Amazon EC2 Auto Scaling
### Explanation
Multi-Region deployment is the only strategy that protects against a complete Region failure. A standby environment in a second Region ensures business continuity even if an entire Region is lost. More AZs in the same Region (A) don't help if the entire Region fails. S3 versioning (B) protects against accidental deletions, not Region failures. Auto Scaling (D) adds capacity within a Region but doesn't protect against Region-level disasters.
---

## Q15. A company wants to give a third-party auditor temporary read-only access to specific AWS resources for a 2-week security review. The auditor should not need an IAM user account. Which approach follows AWS security best practices?
- [ ] A) Create an IAM user with read-only access and share the credentials
- [ ] B) Share the root account credentials with the auditor
- [x] C) Create an IAM role with read-only permissions and allow the auditor to assume it using cross-account access or federation
- [ ] D) Add the auditor to an IAM group with administrator access
### Explanation
Creating an IAM role with read-only permissions that the auditor assumes via cross-account access or federation follows the principle of least privilege and avoids creating long-term credentials. The role provides temporary credentials that expire automatically. Creating an IAM user (A) creates long-term credentials that must be manually revoked. Sharing root credentials (B) is a severe security violation. Administrator access (D) violates least privilege.
---

## Q16. A company is running a legacy application on a single Amazon EC2 instance with an attached Amazon EBS volume. The instance is in a single Availability Zone. The company wants to improve the durability of the data stored on the EBS volume. Which action should the company take?
- [ ] A) Increase the size of the EBS volume
- [x] B) Create automated EBS snapshots that are stored in Amazon S3
- [ ] C) Change the EBS volume type from gp2 to io2
- [ ] D) Enable EC2 Auto Scaling
### Explanation
EBS snapshots are stored in Amazon S3, which provides 99.999999999% durability across multiple AZs. Automated snapshots ensure data can be recovered even if the EBS volume or the entire AZ fails. Increasing volume size (A) doesn't improve durability. Changing volume type (C) affects performance, not durability. Auto Scaling (D) manages instance count, not data durability.
---

## Q17. A company has an application that needs to process messages in the exact order they are received, and each message must be processed exactly once. Which Amazon SQS feature meets these requirements?
- [ ] A) Standard queues with visibility timeout
- [ ] B) Dead-letter queues
- [x] C) FIFO (First-In-First-Out) queues
- [ ] D) Long polling
### Explanation
SQS FIFO queues guarantee that messages are processed in the exact order they are sent and that each message is delivered exactly once (exactly-once processing). Standard queues (A) provide best-effort ordering and at-least-once delivery, meaning messages can be delivered out of order or duplicated. Dead-letter queues (B) handle failed messages. Long polling (C) reduces empty responses but doesn't affect ordering.
---

## Q18. A company is running a database on Amazon RDS in a single Availability Zone. The company needs to improve availability so the database can survive an AZ failure with minimal downtime. Which RDS feature should they enable?
- [ ] A) Read Replicas
- [x] B) Multi-AZ deployment
- [ ] C) Automated backups
- [ ] D) Enhanced monitoring
### Explanation
RDS Multi-AZ deployment creates a synchronous standby replica in a different AZ. If the primary AZ fails, RDS automatically fails over to the standby with minimal downtime (typically 60-120 seconds). Read Replicas (A) are for read scaling and are asynchronous — they don't provide automatic failover for the primary database. Automated backups (C) enable point-in-time recovery but require manual restoration, causing longer downtime. Enhanced monitoring (D) provides metrics but doesn't improve availability.
---

## Q19. A company wants to ensure that an Amazon S3 bucket can only be accessed from within their Amazon VPC, not from the public internet. Which feature should they configure?
- [ ] A) S3 bucket ACLs
- [ ] B) IAM policies with IP restrictions
- [x] C) A VPC endpoint for S3 with a bucket policy restricting access to the VPC endpoint
- [ ] D) S3 Transfer Acceleration
### Explanation
A VPC endpoint for S3 (gateway endpoint) allows private connectivity between the VPC and S3 without traversing the internet. Combined with a bucket policy that restricts access to only the VPC endpoint, this ensures the bucket is inaccessible from the public internet. Bucket ACLs (A) are legacy and don't support VPC-based restrictions. IAM policies with IP restrictions (B) can limit access but don't prevent internet traversal. Transfer Acceleration (D) speeds up uploads, unrelated to access control.
---

## Q20. A company has a monolithic application running on a single large EC2 instance. The application frequently crashes under heavy load. The company wants to improve reliability and scalability. Which architectural approach aligns with AWS best practices?
- [ ] A) Move to a larger EC2 instance type (vertical scaling)
- [ ] B) Add more EBS volumes to the instance
- [x] C) Refactor the application into microservices using containers or serverless components
- [ ] D) Enable detailed CloudWatch monitoring
### Explanation
Refactoring into microservices allows each component to scale independently, fail independently, and be deployed independently — dramatically improving both reliability and scalability. This is a core AWS Well-Architected best practice. Vertical scaling (A) has limits and still creates a single point of failure. More EBS volumes (B) don't address application architecture issues. CloudWatch monitoring (D) provides visibility but doesn't fix the underlying architectural problem.
---

## Q21. A company is using Amazon EC2 instances in a production environment. The security team discovers that several instances have security groups allowing inbound SSH access from 0.0.0.0/0 (anywhere). Which AWS service can automatically detect this misconfiguration and alert the team?
- [ ] A) Amazon CloudWatch
- [ ] B) AWS CloudTrail
- [x] C) AWS Config
- [ ] D) Amazon Inspector
### Explanation
AWS Config can evaluate resource configurations against desired rules (such as "no security groups should allow SSH from 0.0.0.0/0") and flag non-compliant resources automatically. It continuously monitors configurations and can trigger SNS notifications or auto-remediation. CloudWatch (A) monitors performance metrics, not configuration compliance. CloudTrail (B) logs API calls but doesn't evaluate configurations. Inspector (C) assesses software vulnerabilities on instances, not security group configurations.
---

## Q22. A company wants to deploy a containerized application. The development team is familiar with Docker but does not want to manage the underlying EC2 instances, Kubernetes clusters, or container orchestration infrastructure. Which combination of AWS services meets these requirements?
- [ ] A) Amazon EKS with self-managed node groups
- [x] B) Amazon ECS with AWS Fargate
- [ ] C) Amazon EC2 with Docker installed manually
- [ ] D) Amazon EKS with managed node groups
### Explanation
Amazon ECS with AWS Fargate provides serverless container execution — you define your containers and Fargate handles all the underlying infrastructure. No EC2 instances, clusters, or orchestration to manage. EKS with self-managed nodes (A) requires managing EC2 instances. EC2 with Docker (C) requires managing everything. EKS with managed node groups (D) still requires some cluster management and is Kubernetes-based, which adds complexity the team doesn't need.
---

## Q23. A company stores sensitive customer data in Amazon S3. A new regulation requires the company to discover and classify all personally identifiable information (PII) stored across their S3 buckets. Which AWS service is specifically designed for this?
- [ ] A) Amazon GuardDuty
- [x] B) Amazon Macie
- [ ] C) AWS Config
- [ ] D) Amazon Inspector
### Explanation
Amazon Macie uses machine learning to automatically discover, classify, and protect sensitive data like PII stored in Amazon S3. It can identify data types such as names, addresses, credit card numbers, and social security numbers across all your S3 buckets. GuardDuty (A) detects account-level threats, not data classification. Config (C) tracks resource configurations. Inspector (D) assesses software vulnerabilities on compute resources.
---

## Q24. A company is running a web application that serves users in North America and Europe. Users in Asia are reporting high latency. The company does not want to deploy additional infrastructure in Asia. Which AWS service can reduce latency for Asian users without deploying resources in an Asian Region?
- [x] A) Amazon CloudFront
- [ ] B) AWS Global Accelerator
- [ ] C) Amazon Route 53 latency-based routing
- [ ] D) Elastic Load Balancing
### Explanation
Amazon CloudFront caches content at edge locations worldwide, including many locations in Asia. It reduces latency by serving cached content from the nearest edge location without requiring the company to deploy any infrastructure in an Asian Region. Global Accelerator (B) optimizes network paths but still routes to the origin Region. Route 53 latency-based routing (C) requires infrastructure in multiple Regions to route to. ELB (D) operates within a single Region.
---

## Q25. A company is using AWS and wants to ensure that no single person can make critical changes to production resources without approval from another team member. Which security practice should they implement?
- [ ] A) Enable MFA on all IAM users
- [ ] B) Use AWS CloudTrail to log all changes
- [x] C) Implement IAM policies that require approval workflows, combined with separation of duties
- [ ] D) Rotate all access keys every 30 days
### Explanation
Separation of duties ensures that no single person has enough access to make critical changes alone — for example, one person requests a change and another approves it. This can be implemented through IAM policies, approval workflows, and role-based access control. MFA (A) adds authentication security but doesn't prevent a single authorized user from making changes. CloudTrail (B) logs changes after the fact but doesn't prevent them. Key rotation (D) is a credential hygiene practice, not an authorization control.
---

## Q26. A company has an application that writes data to Amazon DynamoDB. During peak hours, the application experiences throttling errors because the provisioned write capacity is exceeded. The company wants to handle traffic spikes without manual intervention. Which DynamoDB feature should they enable?
- [ ] A) DynamoDB Streams
- [ ] B) DynamoDB Global Tables
- [x] C) DynamoDB On-Demand capacity mode
- [ ] D) DynamoDB Accelerator (DAX)
### Explanation
DynamoDB On-Demand capacity mode automatically scales read and write throughput based on actual traffic, eliminating throttling during unpredictable spikes without any capacity planning. Streams (A) capture data changes for event processing. Global Tables (B) provide multi-Region replication. DAX (D) is an in-memory cache for read acceleration, not write capacity.
---

## Q27. A company is running a critical application on AWS. The CTO wants a single dashboard that aggregates security findings from Amazon GuardDuty, Amazon Inspector, Amazon Macie, and AWS Firewall Manager. Which AWS service provides this centralized view?
- [ ] A) Amazon CloudWatch
- [ ] B) AWS Trusted Advisor
- [x] C) AWS Security Hub
- [ ] D) AWS Config
### Explanation
AWS Security Hub provides a centralized, comprehensive view of security findings aggregated from multiple AWS security services including GuardDuty, Inspector, Macie, Firewall Manager, and third-party tools. It prioritizes findings and provides compliance checks. CloudWatch (A) monitors performance metrics. Trusted Advisor (B) provides best-practice recommendations. Config (D) tracks resource configurations.
---

## Q28. A company has a workload that runs every night from 2:00 AM to 6:00 AM for batch data processing. The workload is consistent and runs every day. The company wants to minimize costs. Which EC2 purchasing option is MOST cost-effective?
- [ ] A) On-Demand Instances started and stopped via a schedule
- [x] B) Savings Plans (Compute) with scheduled usage
- [ ] C) Spot Instances
- [ ] D) Dedicated Instances
### Explanation
Savings Plans provide significant discounts (up to 72%) for consistent, predictable usage. Since this workload runs every night at the same time, it qualifies for Savings Plans pricing. On-Demand with scheduling (A) works but costs more. Spot Instances (C) could be interrupted during the batch window, risking incomplete processing. Dedicated Instances (D) are the most expensive option and unnecessary here.
---

## Q29. A company wants to migrate an on-premises Microsoft SQL Server database to AWS. The company wants to reduce licensing costs and is willing to make minor application changes. Which AWS service should they consider?
- [ ] A) Amazon RDS for SQL Server
- [x] B) Amazon Aurora PostgreSQL with the Babelfish feature
- [ ] C) Amazon DynamoDB
- [ ] D) Amazon Redshift
### Explanation
Amazon Aurora PostgreSQL with Babelfish understands T-SQL (SQL Server's dialect), allowing migration from SQL Server with minor application changes while eliminating SQL Server licensing costs entirely. RDS for SQL Server (A) still requires SQL Server licensing. DynamoDB (C) is NoSQL and would require significant application rewriting. Redshift (D) is a data warehouse, not a transactional database replacement.
---

## Q30. A company is using Amazon S3 to store application logs. The logs are written frequently but are only analyzed during monthly audits. After 1 year, the logs must be deleted. Which combination of S3 features minimizes cost while meeting these requirements?
- [ ] A) S3 Standard with manual deletion after 1 year
- [x] B) S3 Standard-Infrequent Access with a Lifecycle Policy to delete objects after 365 days
- [ ] C) S3 Glacier Deep Archive with Cross-Region Replication
- [ ] D) S3 Intelligent-Tiering with versioning enabled
### Explanation
S3 Standard-IA is cost-effective for data accessed infrequently (monthly audits) but available immediately when needed. A Lifecycle Policy automates deletion after 365 days, eliminating manual effort. S3 Standard (A) is more expensive for infrequent access. Glacier Deep Archive (C) has 12+ hour retrieval times, too slow for monthly audits. Intelligent-Tiering (D) adds monitoring costs and versioning is unnecessary for logs.
---

## Q31. A company is building a serverless API. The API must accept HTTPS requests, invoke an AWS Lambda function, and return the response to the client. Which AWS service acts as the front door for this API?
- [ ] A) Elastic Load Balancing
- [ ] B) Amazon CloudFront
- [x] C) Amazon API Gateway
- [ ] D) AWS AppSync
### Explanation
Amazon API Gateway is a fully managed service for creating, publishing, and securing REST and WebSocket APIs. It natively integrates with Lambda, handling HTTPS requests, invoking functions, and returning responses. ELB (A) distributes traffic to EC2/containers, not Lambda directly. CloudFront (B) is a CDN. AppSync (D) is specifically for GraphQL APIs, not general REST APIs.
---

## Q32. A company has a VPC with public and private subnets. An application in the private subnet needs to access Amazon DynamoDB without sending traffic over the public internet. Which solution provides private connectivity to DynamoDB?
- [ ] A) NAT gateway
- [x] B) VPC gateway endpoint for DynamoDB
- [ ] C) Internet gateway
- [ ] D) AWS Direct Connect
### Explanation
A VPC gateway endpoint provides private connectivity from a VPC to DynamoDB (and S3) without requiring an internet gateway, NAT device, or VPN connection. Traffic stays within the AWS network. A NAT gateway (A) routes traffic through the internet. An internet gateway (C) enables public internet access. Direct Connect (D) connects on-premises to AWS, not VPC to DynamoDB.
---

## Q33. A company is running a web application that stores user session data. The data must be accessible with sub-millisecond latency and must persist even if the application server is restarted. Which AWS service is BEST suited?
- [ ] A) Amazon S3
- [ ] B) Amazon RDS
- [x] C) Amazon ElastiCache for Redis
- [ ] D) Instance store volumes
### Explanation
Amazon ElastiCache for Redis provides sub-millisecond latency with data persistence (Redis supports snapshots and append-only file persistence). Session data survives application restarts since it's stored externally. S3 (A) has higher latency. RDS (B) provides millisecond latency, not sub-millisecond. Instance store volumes (D) are ephemeral — data is lost when the instance stops.
---

## Q34. A company wants to ensure that their AWS account cannot be used to launch any EC2 instances larger than t3.medium. Which AWS feature can enforce this restriction across all IAM users and roles in the account?
- [x] A) An IAM policy with a condition key restricting instance types
- [ ] B) AWS Config rules
- [ ] C) Amazon CloudWatch alarms
- [ ] D) Security group rules
### Explanation
An IAM policy with the ec2:InstanceType condition key can deny the RunInstances action for any instance type larger than t3.medium. Applied to all users/roles (or via an SCP), this prevents anyone from launching restricted instance types. Config rules (B) detect non-compliance after the fact but don't prevent launches. CloudWatch alarms (C) alert on metrics but don't enforce restrictions. Security groups (D) control network traffic, not instance types.
---

## Q35. A company is using AWS CloudFormation to manage their infrastructure. A developer accidentally deletes a CloudFormation stack, which terminates all associated resources including a production database. Which CloudFormation feature could have prevented this?
- [ ] A) Drift detection
- [ ] B) Change sets
- [x] C) Stack termination protection
- [ ] D) Stack rollback
### Explanation
CloudFormation stack termination protection prevents a stack from being accidentally deleted. When enabled, any attempt to delete the stack will fail until termination protection is explicitly disabled. Drift detection (A) identifies configuration changes made outside CloudFormation. Change sets (B) preview changes before applying them. Stack rollback (D) reverts failed updates but doesn't prevent deletion.
---

## Q36. A company has an application that needs to process 10,000 images per hour. Each image takes approximately 3 seconds to process. The workload is consistent throughout the day. The company wants the MOST cost-effective serverless solution. Which approach should they use?
- [x] A) AWS Lambda functions triggered by S3 upload events
- [ ] B) Amazon EC2 instances with Auto Scaling
- [ ] C) Amazon ECS on Fargate with scheduled tasks
- [ ] D) AWS Batch with On-Demand instances
### Explanation
Lambda is ideal here — 10,000 images × 3 seconds = 30,000 seconds of compute per hour. Lambda can process images in parallel as they're uploaded to S3, scaling automatically. At ~8.3 concurrent executions on average, this is well within Lambda's capabilities and cheaper than running EC2 instances 24/7. EC2 with Auto Scaling (B) requires managing instances. ECS on Fargate (C) has higher baseline costs. AWS Batch (D) is designed for large batch jobs, not event-driven processing.
---

## Q37. A company is evaluating AWS support plans. Their production workloads require a response time of less than 1 hour for system-impaired cases. They also need access to Infrastructure Event Management for planned events. What is the minimum support plan that meets BOTH requirements?
- [ ] A) Developer
- [ ] B) Business
- [x] C) Enterprise On-Ramp
- [ ] D) Enterprise
### Explanation
Enterprise On-Ramp provides less than 1-hour response for production system impaired cases AND includes Infrastructure Event Management (IEM) for planned events. Business (B) provides less than 1-hour response for production impaired cases but does NOT include IEM as a standard feature. Developer (A) only provides business-hours email support. Enterprise (D) meets all requirements but is more expensive than necessary — the question asks for the minimum plan.
---

## Q38. A company has a web application that uses Amazon RDS MySQL. The application is read-heavy, with 90% of database queries being SELECT statements. The database is becoming a bottleneck. Which solution improves read performance without changing the application's write path?
- [ ] A) Enable Multi-AZ deployment
- [x] B) Create one or more RDS Read Replicas and direct read traffic to them
- [ ] C) Upgrade to a larger RDS instance type
- [ ] D) Migrate to Amazon DynamoDB
### Explanation
RDS Read Replicas handle read traffic separately from the primary instance, offloading the 90% read workload. The application directs SELECT queries to replicas while writes continue to the primary. Multi-AZ (A) provides failover for availability, not read scaling — the standby cannot serve read traffic. Upgrading instance type (C) is more expensive and has limits. Migrating to DynamoDB (D) requires significant application changes since it's NoSQL.
---

## Q39. A company wants to deploy an application that must comply with data sovereignty requirements in Germany. The application data must never leave German borders. Which AWS approach ensures compliance?
- [ ] A) Use Amazon CloudFront with a European edge location
- [ ] B) Use AWS Global Accelerator with European endpoints
- [x] C) Deploy all resources in the eu-central-1 (Frankfurt) Region and ensure no cross-Region replication is configured
- [ ] D) Use a VPN connection from Germany to any AWS Region
### Explanation
The eu-central-1 Region is located in Frankfurt, Germany. Data stored in an AWS Region does not leave that Region unless explicitly configured (e.g., cross-Region replication). By deploying exclusively in eu-central-1 and avoiding cross-Region features, data sovereignty is maintained. CloudFront (A) caches data at edge locations that may be outside Germany. Global Accelerator (B) routes traffic globally. A VPN (D) doesn't control where data is stored.
---

## Q40. A company is running a legacy application that requires a fixed IP address for whitelisting by a third-party partner. The application runs on EC2 instances behind an Auto Scaling group. Which load balancer type provides static IP addresses?
- [ ] A) Application Load Balancer (ALB)
- [x] B) Network Load Balancer (NLB)
- [ ] C) Classic Load Balancer
- [ ] D) Gateway Load Balancer
### Explanation
Network Load Balancer provides static IP addresses (one per AZ) and supports Elastic IP addresses, making it suitable for IP whitelisting by third parties. ALB (A) uses dynamic IP addresses that can change. Classic Load Balancer (C) also uses dynamic IPs and is legacy. Gateway Load Balancer (D) is for deploying third-party virtual appliances, not general application load balancing.
---

## Q41. A company wants to track which AWS services are costing the most and identify unexpected cost increases. They want to receive an alert if any service's daily cost exceeds $500. Which combination of AWS tools should they use?
- [ ] A) AWS Pricing Calculator and Amazon SNS
- [x] B) AWS Cost Explorer for analysis and AWS Budgets for alerts
- [ ] C) AWS Trusted Advisor and AWS CloudTrail
- [ ] D) Amazon CloudWatch and AWS Config
### Explanation
AWS Cost Explorer provides detailed cost breakdowns by service, account, and time period to identify which services cost the most and spot unexpected increases. AWS Budgets can set daily cost thresholds and send alerts via email or SNS when exceeded. Pricing Calculator (A) estimates future costs, not actual spending. Trusted Advisor (C) provides general recommendations. CloudWatch (D) monitors resource metrics, not billing.
---

## Q42. A company has an application that needs to send the same message to multiple subscribing services simultaneously — an email notification service, a logging service, and an analytics service. Which AWS messaging pattern is MOST appropriate?
- [ ] A) Amazon SQS standard queue
- [x] B) Amazon SNS topic with multiple subscriptions
- [ ] C) Amazon Kinesis Data Streams
- [ ] D) AWS Step Functions
### Explanation
Amazon SNS uses a pub/sub (publish/subscribe) pattern where a single message published to a topic is delivered simultaneously to all subscribers. Each subscribing service (email, logging, analytics) receives its own copy of the message. SQS (A) is point-to-point — one consumer processes each message. Kinesis (C) is for streaming data processing. Step Functions (D) orchestrates sequential/parallel workflows, not message fan-out.
---

## Q43. A company is running a production database on Amazon RDS. The database administrator accidentally runs a DELETE query that removes critical data. The company needs to restore the database to its state from 2 hours ago. Which RDS feature enables this?
- [ ] A) Multi-AZ failover
- [ ] B) Read Replicas
- [x] C) Automated backups with point-in-time recovery
- [ ] D) Manual snapshots
### Explanation
RDS automated backups with point-in-time recovery allow you to restore a database to any second within the retention period (up to 35 days), including exactly 2 hours ago. Multi-AZ (A) provides failover for infrastructure failures but replicates the DELETE to the standby immediately. Read Replicas (B) also replicate the DELETE since they follow the primary. Manual snapshots (D) only capture the state at the time they were taken, which may not be exactly 2 hours ago.
---

## Q44. A company wants to run a machine learning inference workload that requires GPU-based compute. The workload runs continuously and is latency-sensitive. Which EC2 instance family is designed for this use case?
- [ ] A) T3 (general purpose, burstable)
- [ ] B) R6g (memory optimized)
- [ ] C) C6g (compute optimized)
- [x] D) P4d or Inf2 (accelerated computing)
### Explanation
P4d (GPU-based) and Inf2 (AWS Inferentia-based) instances are in the accelerated computing family, specifically designed for ML inference and training workloads requiring GPU or custom ML accelerators. T3 (A) is burstable general purpose. R6g (B) is memory optimized for in-memory databases. C6g (C) is compute optimized for CPU-intensive tasks but lacks GPU acceleration.
---

## Q45. A company has multiple development teams, each with their own AWS account. The finance team wants a single invoice for all accounts and the ability to see cost breakdowns by team. Which AWS service provides this?
- [x] A) AWS Organizations with consolidated billing
- [ ] B) AWS Cost Explorer with tags
- [ ] C) AWS Budgets with multiple budget alerts
- [ ] D) AWS Control Tower
### Explanation
AWS Organizations with consolidated billing provides a single invoice for all member accounts while maintaining cost visibility per account (which maps to each team). The management account receives one bill with per-account breakdowns. Cost Explorer with tags (B) works within a single account. Budgets (C) sets alerts but doesn't consolidate billing. Control Tower (D) provides governance but relies on Organizations for billing consolidation.
---

## Q46. A company is designing a system where an order placed on a website triggers a series of steps: validate payment, update inventory, send confirmation email, and notify the warehouse. Each step depends on the previous step's success. Which AWS service is BEST suited to orchestrate this workflow?
- [ ] A) Amazon SQS
- [ ] B) Amazon SNS
- [x] C) AWS Step Functions
- [ ] D) Amazon EventBridge
### Explanation
AWS Step Functions orchestrates multi-step workflows with conditional logic, error handling, and retry capabilities. It visually coordinates the sequential steps (validate → update → email → notify) where each step depends on the previous one's success. SQS (A) is a message queue without orchestration logic. SNS (B) fans out messages simultaneously, not sequentially. EventBridge (D) routes events but doesn't manage complex sequential workflows with dependencies.
---

## Q47. A company is using Amazon EC2 instances and wants to ensure that their instances are launched only from approved, hardened Amazon Machine Images (AMIs). Which approach enforces this?
- [ ] A) Use AWS Config to monitor instance types
- [x] B) Create an IAM policy with a condition that restricts ec2:RunInstances to specific AMI IDs
- [ ] C) Enable Amazon Inspector on all instances
- [ ] D) Use security groups to restrict access
### Explanation
An IAM policy with the ec2:ImageId condition key can restrict the RunInstances action to only approved AMI IDs, preventing anyone from launching instances with unapproved images. Config (A) can detect non-compliant instances after launch but doesn't prevent it. Inspector (C) scans for vulnerabilities but doesn't control which AMIs are used. Security groups (D) control network traffic, not instance launch parameters.
---

## Q48. A company has a web application that stores user-uploaded files in Amazon S3. The company wants to ensure that files are automatically scanned for malware before being made available to other users. Which approach should they use?
- [ ] A) Enable S3 server-side encryption
- [ ] B) Use S3 bucket policies to restrict access
- [x] C) Use S3 event notifications to trigger a Lambda function that scans files with Amazon GuardDuty Malware Protection or a third-party scanning tool
- [ ] D) Enable S3 versioning
### Explanation
S3 event notifications can trigger a Lambda function when a new object is uploaded. The function can invoke GuardDuty Malware Protection or a third-party antivirus tool to scan the file before making it available. Encryption (A) protects data at rest but doesn't detect malware. Bucket policies (B) control access but don't scan content. Versioning (D) maintains file versions but doesn't scan for malware.
---

## Q49. A company is running a microservices architecture on AWS. One service is experiencing intermittent failures, and the team needs to trace requests across multiple services to identify the bottleneck. Which AWS service provides distributed tracing?
- [ ] A) Amazon CloudWatch Logs
- [ ] B) AWS CloudTrail
- [x] C) AWS X-Ray
- [ ] D) AWS Config
### Explanation
AWS X-Ray provides distributed tracing for microservices architectures, allowing you to trace requests as they travel through multiple services, identify bottlenecks, and pinpoint the source of errors and latency. CloudWatch Logs (A) stores log data but doesn't trace requests across services. CloudTrail (B) logs API calls, not application-level request flows. Config (D) tracks resource configurations.
---

## Q50. A company wants to adopt AWS but their CISO is concerned about meeting compliance requirements for PCI DSS, HIPAA, and SOC 2. Where can the company find documentation of AWS's compliance certifications and audit reports?
- [ ] A) AWS Trusted Advisor
- [ ] B) AWS Config compliance dashboard
- [x] C) AWS Artifact
- [ ] D) AWS Security Hub
### Explanation
AWS Artifact is a self-service portal that provides on-demand access to AWS compliance reports and certifications, including PCI DSS, HIPAA, SOC 1/2/3, ISO 27001, and more. These are third-party audit reports that demonstrate AWS's compliance posture. Trusted Advisor (A) provides best-practice recommendations. Config compliance dashboard (B) shows your resource compliance, not AWS's certifications. Security Hub (D) aggregates security findings for your account.
---
