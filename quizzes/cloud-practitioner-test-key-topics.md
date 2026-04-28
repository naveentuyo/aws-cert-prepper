# AWS Key Topics — Practice Test
#
# Total Questions: 50
# Passing Score: 70% (35/50)
# Time Limit: 90 minutes
# Covers: Pricing, VPN, WorkSpaces, Migration, IAM, Artifact/Config/CloudTrail, CloudFront/WAF, Cognito, Fargate, ECS, EKS, Well-Architected

## Q1. A company runs a production workload 24/7 with predictable, steady-state usage. They want to reduce EC2 costs by committing to a 3-year term with the flexibility to change instance families and Regions. Which purchasing option provides this?
- [ ] A) Standard Reserved Instances
- [x] B) Compute Savings Plans
- [ ] C) Spot Instances
- [ ] D) Convertible Reserved Instances
### Explanation
Compute Savings Plans provide significant discounts for a 1- or 3-year commitment while offering the most flexibility — they apply to any EC2 instance family, Region, OS, tenancy, and also cover Lambda and Fargate usage. Standard RIs (A) are locked to a specific instance type and AZ. Convertible RIs (D) allow changing instance family but are less flexible than Compute Savings Plans and don't cover Lambda/Fargate. Spot Instances (C) can be interrupted and don't involve commitments.
---

## Q2. A company needs to connect their on-premises data center to AWS quickly with an encrypted connection. They cannot wait weeks for a physical line to be provisioned. Which service should they use?
- [ ] A) AWS Direct Connect
- [x] B) AWS Site-to-Site VPN
- [ ] C) Amazon VPC Peering
- [ ] D) AWS Transit Gateway
### Explanation
AWS Site-to-Site VPN creates an encrypted IPsec tunnel over the public internet and can be set up in minutes to hours. Direct Connect (A) provides a dedicated private connection but takes weeks to months to provision. VPC Peering (C) connects two VPCs, not on-premises to AWS. Transit Gateway (D) connects multiple VPCs and on-premises networks but is not itself a connection method.
---

## Q3. A company wants to provide remote employees with persistent virtual desktops they can access from any device, including personal laptops and Chromebooks. Which AWS service should they use?
- [ ] A) Amazon AppStream 2.0
- [ ] B) Amazon EC2
- [x] C) Amazon WorkSpaces
- [ ] D) Amazon Connect
### Explanation
Amazon WorkSpaces is a managed Desktop-as-a-Service (DaaS) that provides persistent virtual desktops accessible from any supported device. Files and settings are saved between sessions. AppStream 2.0 (A) streams individual applications, not full desktops. EC2 (B) requires manual setup and management of virtual desktops. Connect (D) is a cloud contact center service.
---

## Q4. Under the AWS Shared Responsibility Model, which of the following is exclusively a task that requires the root user account?
- [ ] A) Creating IAM users and groups
- [ ] B) Launching EC2 instances
- [x] C) Closing the AWS account
- [ ] D) Configuring security groups
### Explanation
Closing an AWS account is one of the few tasks that can only be performed by the root user. Creating IAM users (A), launching EC2 instances (B), and configuring security groups (D) can all be performed by IAM users with appropriate permissions. Other root-only tasks include changing the account name, changing the support plan, and restoring IAM permissions.
---

## Q5. A company's CISO needs to provide auditors with AWS's SOC 2 compliance report and sign a HIPAA Business Associate Agreement. Where can they find these documents?
- [ ] A) AWS Config
- [ ] B) AWS CloudTrail
- [x] C) AWS Artifact
- [ ] D) AWS Security Hub
### Explanation
AWS Artifact is a self-service portal for accessing AWS compliance reports (SOC 1/2/3, PCI DSS, ISO 27001) and agreements (HIPAA BAA, NDA). Config (A) tracks resource configurations. CloudTrail (B) logs API calls. Security Hub (D) aggregates security findings. None of these provide AWS's compliance certifications.
---

## Q6. A security team discovers that an S3 bucket was made public at 2:15 PM yesterday. They need to find out which IAM user made this change. Which AWS service provides this information?
- [ ] A) AWS Config
- [x] B) AWS CloudTrail
- [ ] C) AWS Artifact
- [ ] D) Amazon GuardDuty
### Explanation
AWS CloudTrail logs all API calls made in your AWS account, recording who performed the action, when, and from where. It would show the PutBucketPolicy or PutBucketAcl call with the IAM user identity and timestamp. Config (A) would show that the configuration changed but not necessarily who made the change. Artifact (C) provides compliance documents. GuardDuty (D) detects threats but doesn't provide the detailed API call history.
---

## Q7. A company wants to ensure that all their S3 buckets have encryption enabled and receive automatic alerts when a bucket is found without encryption. Which AWS service provides this continuous compliance monitoring?
- [x] A) AWS Config
- [ ] B) AWS CloudTrail
- [ ] C) AWS Artifact
- [ ] D) AWS Trusted Advisor
### Explanation
AWS Config continuously monitors resource configurations and evaluates them against rules (e.g., "s3-bucket-server-side-encryption-enabled"). When a bucket violates the rule, Config flags it as non-compliant and can trigger SNS notifications or auto-remediation. CloudTrail (B) logs API calls but doesn't evaluate compliance. Artifact (C) provides AWS's compliance documents. Trusted Advisor (D) provides broad recommendations but doesn't offer custom compliance rules.
---

## Q8. A company wants to reduce latency for users in Asia accessing their US-hosted website. They do not want to deploy infrastructure in Asia. Which AWS service caches content at edge locations to solve this?
- [ ] A) AWS Global Accelerator
- [x] B) Amazon CloudFront
- [ ] C) Elastic Load Balancing
- [ ] D) Amazon Route 53
### Explanation
Amazon CloudFront is a CDN that caches content at 400+ edge locations worldwide, including many in Asia. Users are served from the nearest edge location, dramatically reducing latency without deploying any infrastructure in Asia. Global Accelerator (A) optimizes network paths but still routes to the origin. ELB (C) operates within a single Region. Route 53 (D) is DNS and doesn't cache content.
---

## Q9. A company wants to protect their web application from SQL injection attacks. They need a solution that inspects HTTP requests before they reach the application. Which AWS service should they use?
- [ ] A) AWS Shield
- [x] B) AWS WAF
- [ ] C) Amazon GuardDuty
- [ ] D) Amazon Inspector
### Explanation
AWS WAF (Web Application Firewall) inspects incoming HTTP/HTTPS requests and can block SQL injection, cross-site scripting (XSS), and other Layer 7 attacks using managed or custom rules. Shield (A) protects against DDoS attacks at Layer 3/4, not application-layer exploits. GuardDuty (C) detects account-level threats. Inspector (D) scans for software vulnerabilities on instances.
---

## Q10. A mobile app startup needs to add user sign-up, sign-in, and social login (Google, Facebook) to their iOS application. Which AWS service is designed for this?
- [ ] A) AWS IAM
- [ ] B) AWS IAM Identity Center
- [x] C) Amazon Cognito
- [ ] D) AWS Directory Service
### Explanation
Amazon Cognito is designed for mobile and web application user authentication. User Pools handle sign-up/sign-in, and it natively supports social identity providers like Google, Facebook, Apple, and Amazon. IAM (A) manages AWS account access, not app users. IAM Identity Center (B) provides SSO for AWS accounts using corporate IdPs. Directory Service (D) integrates with Microsoft Active Directory.
---

## Q11. A company wants to run Docker containers on AWS without managing any EC2 instances, clusters, or orchestration infrastructure. Which combination of services provides this?
- [ ] A) Amazon EKS with self-managed node groups
- [x] B) Amazon ECS with AWS Fargate
- [ ] C) Amazon EC2 with Docker installed
- [ ] D) Amazon EKS with managed node groups
### Explanation
Amazon ECS with AWS Fargate provides fully serverless container execution. You define your containers in a task definition and Fargate handles all infrastructure — no EC2 instances to provision, patch, or scale. EKS with self-managed nodes (A) requires managing EC2 instances. EC2 with Docker (C) requires managing everything. EKS with managed node groups (D) still requires some cluster management.
---

## Q12. A company has Kubernetes expertise and wants to run their containerized workloads on AWS while maintaining the ability to migrate to another cloud provider in the future. Which AWS service should they use?
- [ ] A) Amazon ECS
- [x] B) Amazon EKS
- [ ] C) AWS Elastic Beanstalk
- [ ] D) Amazon Lightsail
### Explanation
Amazon EKS runs open-source Kubernetes, which is portable across cloud providers (GCP GKE, Azure AKS) and on-premises. This reduces vendor lock-in. ECS (A) is AWS-proprietary and not portable. Elastic Beanstalk (C) is a PaaS, not Kubernetes. Lightsail (D) provides simplified VPS.
---

## Q13. A solutions architect is designing a system that must continue operating even when individual components fail. Which pillar of the AWS Well-Architected Framework does this requirement fall under?
- [ ] A) Operational Excellence
- [ ] B) Security
- [x] C) Reliability
- [ ] D) Performance Efficiency
### Explanation
The Reliability pillar focuses on ensuring a workload performs its intended function correctly and consistently, including the ability to automatically recover from failure. Key principles include testing recovery procedures, scaling horizontally, and managing change through automation. Operational Excellence (A) focuses on running and monitoring systems. Security (B) focuses on protecting information. Performance Efficiency (D) focuses on using resources efficiently.
---

## Q14. A company wants to migrate 60 TB of data from their on-premises data center to AWS. Transferring over the internet would take several weeks. Which AWS service provides the fastest physical data transfer?
- [ ] A) AWS DataSync
- [ ] B) AWS Direct Connect
- [x] C) AWS Snowball Edge
- [ ] D) AWS Transfer Family
### Explanation
AWS Snowball Edge is a physical device with 80 TB usable storage designed for transferring large amounts of data. For 60 TB, shipping a Snowball device is significantly faster than network transfer. DataSync (A) transfers over the network. Direct Connect (B) requires weeks to provision and is a network connection, not a migration tool. Transfer Family (D) manages SFTP file transfers.
---

## Q15. A company is migrating an Oracle database to Amazon Aurora PostgreSQL. They need to convert the Oracle-specific stored procedures and schema to PostgreSQL format. Which AWS tool should they use?
- [ ] A) AWS Database Migration Service (DMS)
- [x] B) AWS Schema Conversion Tool (SCT)
- [ ] C) AWS Application Migration Service
- [ ] D) AWS Migration Hub
### Explanation
AWS Schema Conversion Tool (SCT) converts database schemas and code from one engine to another (e.g., Oracle stored procedures to PostgreSQL). This is required for heterogeneous migrations before using DMS to migrate the data. DMS (A) migrates the data but doesn't convert schemas. Application Migration Service (C) migrates servers, not databases. Migration Hub (D) tracks migration progress.
---

## Q16. An IAM user needs to allow an EC2 instance to read objects from an S3 bucket. What is the AWS-recommended approach?
- [ ] A) Store IAM access keys on the EC2 instance
- [ ] B) Embed credentials in the application code
- [x] C) Attach an IAM role with S3 read permissions to the EC2 instance
- [ ] D) Use the root account credentials
### Explanation
Attaching an IAM role to an EC2 instance (via an instance profile) provides temporary credentials that are automatically rotated — this is the AWS best practice. Storing access keys on the instance (A) or embedding them in code (B) creates long-term credentials that can be leaked. Using root credentials (D) is a severe security violation and never recommended.
---

## Q17. A company has a workload that runs for 2 hours every night and can tolerate interruptions. They want the absolute lowest compute cost. Which EC2 pricing model should they use?
- [ ] A) On-Demand Instances
- [ ] B) Reserved Instances
- [x] C) Spot Instances
- [ ] D) Savings Plans
### Explanation
Spot Instances offer up to 90% discount compared to On-Demand and are ideal for fault-tolerant workloads that can handle interruptions. Since this workload tolerates interruptions and runs briefly, Spot provides the lowest cost. On-Demand (A) has no discount. Reserved Instances (B) and Savings Plans (D) require commitments and are designed for steady-state usage, not 2-hour nightly jobs.
---

## Q18. A company wants to stream individual desktop applications to users without providing full virtual desktops. Which AWS service should they use?
- [x] A) Amazon AppStream 2.0
- [ ] B) Amazon WorkSpaces
- [ ] C) Amazon EC2
- [ ] D) AWS Outposts
### Explanation
Amazon AppStream 2.0 streams individual desktop applications to users through a web browser without providing a full desktop environment. WorkSpaces (B) provides full persistent virtual desktops, which is more than needed. EC2 (C) requires manual setup. Outposts (D) extends AWS infrastructure on-premises.
---

## Q19. A company wants to track the progress of migrating multiple servers and databases to AWS using different migration tools. Which AWS service provides a centralized dashboard for this?
- [ ] A) AWS Application Migration Service
- [ ] B) AWS Database Migration Service
- [x] C) AWS Migration Hub
- [ ] D) AWS CloudFormation
### Explanation
AWS Migration Hub provides a central dashboard to track the progress of migrations across multiple AWS tools (Application Migration Service, DMS, etc.). It aggregates status from all migration tools into one view. Application Migration Service (A) and DMS (B) perform specific migrations but don't provide a unified tracking dashboard. CloudFormation (D) provisions infrastructure.
---

## Q20. Which IAM feature allows a user in one AWS account to temporarily access resources in a different AWS account without creating a new IAM user?
- [ ] A) IAM Groups
- [x] B) IAM Roles with cross-account access
- [ ] C) IAM Access Keys
- [ ] D) IAM Permission Boundaries
### Explanation
IAM Roles with cross-account access allow users in one account to assume a role in another account, receiving temporary credentials. No new IAM user is needed in the target account. Groups (A) organize users within a single account. Access Keys (C) are long-term credentials tied to a specific user. Permission Boundaries (D) set maximum permissions for a user/role but don't enable cross-account access.
---

## Q21. A company is choosing between AWS Site-to-Site VPN and AWS Direct Connect. Which statement is true?
- [ ] A) VPN provides a dedicated physical connection
- [ ] B) Direct Connect is encrypted by default
- [x] C) VPN uses the public internet with encryption, while Direct Connect uses a dedicated private line
- [ ] D) VPN takes weeks to provision while Direct Connect is instant
### Explanation
Site-to-Site VPN creates encrypted IPsec tunnels over the public internet (quick setup). Direct Connect provides a dedicated private physical connection that does NOT traverse the internet (takes weeks to provision). VPN is not a dedicated physical connection (A). Direct Connect is NOT encrypted by default (B) — you can add VPN on top for encryption. VPN is fast to set up, not weeks (D).
---

## Q22. A company wants to minimize environmental impact while running their cloud workloads. Which pillar of the Well-Architected Framework addresses this concern?
- [ ] A) Cost Optimization
- [ ] B) Reliability
- [ ] C) Performance Efficiency
- [x] D) Sustainability
### Explanation
The Sustainability pillar focuses on minimizing the environmental impact of running cloud workloads. Key principles include maximizing utilization, right-sizing resources, using energy-efficient processors (like Graviton), and leveraging managed/serverless services. Cost Optimization (A) focuses on avoiding unnecessary costs. Reliability (B) focuses on failure recovery. Performance Efficiency (C) focuses on using resources efficiently for performance.
---

## Q23. A company needs to migrate their on-premises VMware servers to AWS EC2 with minimal downtime using continuous replication. Which AWS service should they use?
- [x] A) AWS Application Migration Service (MGN)
- [ ] B) AWS Database Migration Service
- [ ] C) AWS Snowball Edge
- [ ] D) AWS DataSync
### Explanation
AWS Application Migration Service (MGN) performs lift-and-shift migrations by continuously replicating source servers to AWS, then performing a cutover with minimal downtime. DMS (B) migrates databases, not servers. Snowball Edge (C) is for physical data transfer. DataSync (D) transfers files, not entire server workloads.
---

## Q24. A company uses Amazon Cognito User Pools for their mobile app. They now need authenticated users to directly access an S3 bucket to upload profile photos. Which Cognito feature provides temporary AWS credentials for this?
- [ ] A) Cognito User Pools
- [x] B) Cognito Identity Pools (Federated Identities)
- [ ] C) Cognito Sync
- [ ] D) Cognito Hosted UI
### Explanation
Cognito Identity Pools provide temporary AWS credentials (via STS) that allow authenticated users to directly access AWS services like S3. The user authenticates via User Pool, then exchanges the JWT token with Identity Pool for temporary AWS credentials mapped to an IAM role. User Pools (A) handle authentication but don't provide AWS credentials. Sync (C) synchronizes user data across devices. Hosted UI (D) is a sign-in interface.
---

## Q25. A company is running containers on Amazon ECS with the EC2 launch type. They want to eliminate the need to manage and patch the underlying EC2 instances. What should they do?
- [ ] A) Switch to Amazon EKS
- [x] B) Switch to the Fargate launch type
- [ ] C) Enable Auto Scaling for the EC2 instances
- [ ] D) Use AWS Systems Manager Patch Manager
### Explanation
Switching to the Fargate launch type eliminates all EC2 instance management — Fargate handles provisioning, scaling, and patching of the underlying infrastructure. Switching to EKS (A) still requires managing worker nodes unless also using Fargate. Auto Scaling (C) manages instance count but you still patch them. Patch Manager (D) automates patching but you still manage the instances.
---

## Q26. A company wants to enforce multi-factor authentication for all IAM users who access the AWS Management Console. Which AWS service should they configure?
- [ ] A) Amazon Cognito
- [x] B) AWS IAM
- [ ] C) AWS Shield
- [ ] D) AWS WAF
### Explanation
AWS IAM is where MFA is configured for IAM users. Administrators can create IAM policies that deny console access unless MFA is present using the aws:MultiFactorAuthPresent condition key. Cognito (A) manages application end users, not AWS console users. Shield (C) is DDoS protection. WAF (D) protects web applications.
---

## Q27. A company has a web application behind Amazon CloudFront. They want to block requests from specific countries and also protect against SQL injection. Which combination of services achieves both?
- [x] A) CloudFront geo-restriction for country blocking and AWS WAF for SQL injection protection
- [ ] B) AWS Shield for both country blocking and SQL injection
- [ ] C) Security groups for country blocking and Amazon Inspector for SQL injection
- [ ] D) Network ACLs for country blocking and AWS Config for SQL injection
### Explanation
CloudFront has built-in geo-restriction to block or allow traffic from specific countries. AWS WAF attaches to CloudFront and inspects requests for SQL injection using managed rules. Shield (B) protects against DDoS, not SQL injection or geo-blocking. Security groups (C) don't support country-based rules. Network ACLs (D) work at the subnet level, not by country. Inspector and Config don't inspect HTTP traffic.
---

## Q28. A company is running a workload that requires a physical server dedicated entirely to them for software licensing compliance. Which EC2 purchasing option should they use?
- [ ] A) Reserved Instances
- [ ] B) Spot Instances
- [x] C) Dedicated Hosts
- [ ] D) On-Demand Instances
### Explanation
Dedicated Hosts provide a physical EC2 server fully dedicated to your use, giving visibility into sockets and physical cores — required for per-socket or per-core software licensing (e.g., Windows Server, SQL Server, Oracle). Reserved Instances (A) and On-Demand (D) run on shared hardware. Spot Instances (B) also run on shared hardware and can be interrupted.
---

## Q29. A company wants to identify resources in their AWS account that are shared with external entities, such as S3 buckets accessible from outside the account. Which IAM feature helps with this?
- [ ] A) IAM Policy Simulator
- [x] B) IAM Access Analyzer
- [ ] C) IAM Credential Report
- [ ] D) IAM Permission Boundaries
### Explanation
IAM Access Analyzer identifies resources shared with external entities by analyzing resource-based policies (S3 bucket policies, KMS key policies, IAM roles, etc.) and flagging any that grant access outside your account or organization. Policy Simulator (A) tests policy effects. Credential Report (C) lists all IAM users and their credential status. Permission Boundaries (D) set maximum permissions.
---

## Q30. A company needs to migrate a MySQL database to Amazon RDS MySQL with minimal downtime. The source database must remain operational during migration. Which AWS service should they use?
- [x] A) AWS Database Migration Service (DMS)
- [ ] B) AWS Schema Conversion Tool (SCT)
- [ ] C) AWS Application Migration Service
- [ ] D) AWS Snowball Edge
### Explanation
AWS DMS migrates databases with minimal downtime by continuously replicating changes from the source to the target while the source remains operational. Since this is a homogeneous migration (MySQL to MySQL), SCT (B) is not needed — SCT is for converting schemas between different engines. Application Migration Service (C) migrates servers, not databases. Snowball Edge (D) is for physical data transfer.
---

## Q31. Which of the following are key principles of the Security pillar of the Well-Architected Framework? (Select TWO)
- [x] A) Implement a strong identity foundation with least privilege
- [ ] B) Use the largest instance types for better security
- [x] C) Enable traceability by logging all actions
- [ ] D) Store all data in a single Region for easier management
- [ ] E) Grant all developers administrator access for productivity
### Explanation
Implementing least privilege (A) and enabling traceability through logging (C) are core Security pillar principles. Larger instances (B) don't improve security. Storing data in a single Region (D) is a data residency decision, not a security principle. Granting admin access to all developers (E) directly violates least privilege.
---

## Q32. A company has remote employees who need to connect to resources inside their AWS VPC from their personal laptops using a VPN client. Which AWS service provides this?
- [ ] A) AWS Site-to-Site VPN
- [x] B) AWS Client VPN
- [ ] C) AWS Direct Connect
- [ ] D) Amazon VPC Peering
### Explanation
AWS Client VPN is a managed VPN service for individual users to connect to AWS resources from their devices using an OpenVPN-based client. Site-to-Site VPN (A) connects entire networks (data center to VPC), not individual users. Direct Connect (C) is a dedicated physical connection. VPC Peering (D) connects two VPCs.
---

## Q33. A company wants to avoid unnecessary costs by identifying idle EC2 instances, underutilized EBS volumes, and unused Elastic IP addresses. Which AWS service provides these cost optimization recommendations?
- [x] A) AWS Trusted Advisor
- [ ] B) AWS Config
- [ ] C) Amazon CloudWatch
- [ ] D) AWS CloudTrail
### Explanation
AWS Trusted Advisor provides cost optimization recommendations including identifying idle EC2 instances, underutilized EBS volumes, unassociated Elastic IPs, and idle load balancers. Config (B) tracks resource configurations. CloudWatch (C) monitors metrics but doesn't provide cost recommendations. CloudTrail (D) logs API calls.
---

## Q34. A company is designing their architecture and wants to use serverless services wherever possible to reduce operational overhead. Which pillar of the Well-Architected Framework recommends this approach?
- [ ] A) Reliability
- [ ] B) Security
- [x] C) Performance Efficiency
- [ ] D) Cost Optimization
### Explanation
The Performance Efficiency pillar recommends using serverless architectures and managed services to democratize advanced technologies and reduce operational overhead. While serverless also helps with Cost Optimization (D), the principle of "use serverless architectures" and "democratize advanced technologies" is explicitly part of Performance Efficiency. Reliability (A) focuses on failure recovery. Security (B) focuses on protecting information.
---

## Q35. A company needs to transfer files from on-premises to Amazon S3 using SFTP. Their existing workflows rely on SFTP and cannot be changed. Which AWS service supports this?
- [ ] A) AWS DataSync
- [ ] B) AWS Snowball Edge
- [x] C) AWS Transfer Family
- [ ] D) Amazon S3 Transfer Acceleration
### Explanation
AWS Transfer Family provides managed SFTP, FTPS, and FTP endpoints that transfer files directly into S3 or EFS. Existing SFTP workflows can point to the Transfer Family endpoint without changes. DataSync (A) uses its own agent and protocol. Snowball Edge (B) is physical data transfer. S3 Transfer Acceleration (D) speeds up HTTP-based uploads, not SFTP.
---

## Q36. A company wants to restrict S3 bucket access so content can ONLY be served through their CloudFront distribution, not directly via the S3 URL. Which CloudFront feature enables this?
- [ ] A) Lambda@Edge
- [ ] B) CloudFront signed URLs
- [x] C) Origin Access Control (OAC)
- [ ] D) CloudFront geo-restriction
### Explanation
Origin Access Control (OAC) restricts the S3 bucket so that only CloudFront can access it. Direct access to the S3 URL is blocked. Lambda@Edge (A) runs code at edge locations. Signed URLs (B) restrict access to specific users/time periods. Geo-restriction (D) blocks access from specific countries.
---

## Q37. A company has 5 AWS accounts and wants a single invoice while still seeing cost breakdowns per account. Which AWS service provides this?
- [x] A) AWS Organizations with consolidated billing
- [ ] B) AWS Budgets
- [ ] C) AWS Cost Explorer
- [ ] D) AWS Control Tower
### Explanation
AWS Organizations with consolidated billing provides a single invoice for all member accounts while maintaining per-account cost visibility. The management account receives one bill with breakdowns. Budgets (B) sets spending alerts. Cost Explorer (C) analyzes costs but doesn't consolidate billing. Control Tower (D) provides governance but relies on Organizations for billing.
---

## Q38. A company is running Amazon ECS tasks and needs each task to have its own private IP address and security group, similar to an EC2 instance. Which ECS networking mode provides this?
- [ ] A) Bridge mode
- [ ] B) Host mode
- [x] C) awsvpc mode
- [ ] D) None mode
### Explanation
The awsvpc networking mode gives each ECS task its own Elastic Network Interface (ENI) with a private IP address, allowing you to apply security groups directly to individual tasks. Bridge mode (A) uses Docker's built-in virtual network. Host mode (B) shares the host's network. None mode (D) disables networking.
---

## Q39. A company wants to adopt a consumption-based pricing model where they only pay for what they use and stop spending money on undifferentiated heavy lifting. Which Well-Architected pillar promotes these principles?
- [ ] A) Operational Excellence
- [ ] B) Reliability
- [ ] C) Performance Efficiency
- [x] D) Cost Optimization
### Explanation
The Cost Optimization pillar explicitly promotes adopting a consumption model (pay only for what you use) and stopping spending on undifferentiated heavy lifting (use managed services instead of building your own). Operational Excellence (A) focuses on operations and monitoring. Reliability (B) focuses on failure recovery. Performance Efficiency (C) focuses on efficient resource use for performance.
---

## Q40. A company needs to provide temporary workers with virtual desktops for a 3-month project. They want to minimize costs by only paying when the desktops are actively being used. Which Amazon WorkSpaces pricing model should they choose?
- [x] A) Hourly billing
- [ ] B) Monthly billing
- [ ] C) Reserved pricing
- [ ] D) Spot pricing
### Explanation
WorkSpaces hourly billing charges a small monthly fee plus a per-hour charge only when the desktop is running. For temporary workers who don't use desktops 24/7, this is more cost-effective than monthly billing (B), which charges a flat rate regardless of usage. WorkSpaces does not offer Reserved (C) or Spot (D) pricing models.
---

## Q41. A company wants to ensure that IAM policies in their account grant only the intended access and don't accidentally allow external entities to access resources. Which IAM tool should they use for ongoing monitoring?
- [ ] A) IAM Credential Report
- [ ] B) IAM Policy Simulator
- [x] C) IAM Access Analyzer
- [ ] D) AWS CloudTrail
### Explanation
IAM Access Analyzer continuously monitors resource-based policies and identifies any resources shared with external entities, providing ongoing monitoring for unintended access. Credential Report (A) is a one-time snapshot of user credentials. Policy Simulator (B) tests specific policies manually. CloudTrail (D) logs API calls but doesn't analyze policy intent.
---

## Q42. A company is running containers on Amazon EKS and wants to eliminate the need to manage worker node EC2 instances. Which compute option should they use with EKS?
- [ ] A) Managed node groups
- [ ] B) Self-managed node groups
- [x] C) Fargate profiles
- [ ] D) Spot Instance node groups
### Explanation
Fargate profiles with EKS allow you to run Kubernetes pods without managing any EC2 worker nodes — Fargate handles all infrastructure. Managed node groups (A) simplify node management but you still have EC2 instances. Self-managed nodes (B) require full EC2 management. Spot Instance node groups (D) reduce cost but still require managing instances.
---

## Q43. A company needs to migrate an exabyte of data to AWS. Which AWS Snow Family device is designed for this scale?
- [ ] A) AWS Snowcone
- [ ] B) AWS Snowball Edge
- [x] C) AWS Snowmobile
- [ ] D) AWS DataSync
### Explanation
AWS Snowmobile is a 45-foot shipping container that can transfer up to 100 PB per device, designed for exabyte-scale migrations. Snowcone (A) handles 8 TB. Snowball Edge (B) handles 80 TB. DataSync (D) transfers data over the network, not physically.
---

## Q44. A company wants to centrally manage single sign-on access for employees across 20 AWS accounts using their existing corporate Active Directory. Which AWS service should they use?
- [ ] A) Amazon Cognito
- [x] B) AWS IAM Identity Center
- [ ] C) AWS Directory Service
- [ ] D) AWS IAM
### Explanation
AWS IAM Identity Center (formerly AWS SSO) provides centralized SSO access across multiple AWS accounts and integrates with corporate identity providers like Active Directory. Cognito (A) is for application end users, not AWS account access. Directory Service (C) provides managed AD but doesn't provide SSO across AWS accounts. IAM (D) manages access within a single account.
---

## Q45. A company is designing a system and wants to make frequent, small, reversible changes and perform operations as code. Which Well-Architected pillar promotes these practices?
- [x] A) Operational Excellence
- [ ] B) Security
- [ ] C) Reliability
- [ ] D) Cost Optimization
### Explanation
The Operational Excellence pillar promotes performing operations as code (infrastructure as code), making frequent small reversible changes, refining procedures frequently, and anticipating failure. Security (B) focuses on protecting information. Reliability (C) focuses on failure recovery. Cost Optimization (D) focuses on avoiding unnecessary costs.
---

## Q46. A company is using the AWS Free Tier. Which of the following is an "Always Free" offer that never expires?
- [ ] A) 750 hours/month of EC2 t2.micro
- [ ] B) 5 GB of S3 Standard storage
- [x] C) 1 million AWS Lambda requests per month
- [ ] D) 750 hours/month of RDS db.t2.micro
### Explanation
1 million Lambda requests per month is an Always Free offer that never expires, regardless of how long the account has been open. EC2 t2.micro (A), S3 5 GB (B), and RDS db.t2.micro (D) are all 12-Month Free Tier offers that expire 12 months after account creation.
---

## Q47. A company has deployed AWS WAF on their Application Load Balancer. They want to automatically block IP addresses that make more than 5,000 requests in a 5-minute period. Which WAF rule type should they create?
- [ ] A) AWS Managed Rules
- [ ] B) Custom string match rule
- [x] C) Rate-based rule
- [ ] D) Geographic match rule
### Explanation
WAF rate-based rules automatically count requests from each IP address and block those exceeding the defined threshold within a time window. This is designed for rate limiting and basic DDoS mitigation. Managed Rules (A) are pre-built rule sets for common threats. String match rules (B) inspect request content. Geographic rules (D) block by country.
---

## Q48. A company wants to use both VPN and Direct Connect to connect their on-premises data center to AWS. The VPN should serve as a backup when Direct Connect is unavailable. What is this architecture called?
- [ ] A) Multi-Region deployment
- [x] B) VPN as a Direct Connect backup (hybrid connectivity with failover)
- [ ] C) VPC Peering
- [ ] D) Transit Gateway multicast
### Explanation
Using VPN as a backup for Direct Connect is a common hybrid connectivity pattern. Direct Connect provides the primary dedicated connection with consistent performance, while Site-to-Site VPN provides encrypted backup connectivity over the internet if Direct Connect fails. Multi-Region (A) is about deploying across Regions. VPC Peering (C) connects VPCs. Transit Gateway multicast (D) is for multicast traffic distribution.
---

## Q49. A company is evaluating ECS vs. EKS for their container workloads. Their team has no Kubernetes experience and wants the simplest AWS-native solution. Which service should they choose?
- [x] A) Amazon ECS
- [ ] B) Amazon EKS
- [ ] C) Amazon EC2 with Docker
- [ ] D) AWS Elastic Beanstalk
### Explanation
Amazon ECS is AWS's proprietary container orchestration service that is simpler to learn and deeply integrated with the AWS ecosystem. It uses task definitions (similar to docker-compose) rather than Kubernetes manifests. EKS (B) requires Kubernetes expertise. EC2 with Docker (C) requires managing everything manually. Elastic Beanstalk (D) is a PaaS, not a container orchestration service.
---

## Q50. A company wants to ensure that their AWS architecture follows best practices across all six pillars. They want a structured review process with actionable recommendations. Which AWS tool provides this?
- [ ] A) AWS Trusted Advisor
- [x] B) AWS Well-Architected Tool
- [ ] C) AWS Config
- [ ] D) AWS Systems Manager
### Explanation
The AWS Well-Architected Tool is a free service that provides a structured questionnaire-based review of your workloads against all six pillars of the Well-Architected Framework, generating a report with identified risks and improvement recommendations. Trusted Advisor (A) provides automated checks across five categories but is not a structured architectural review. Config (C) tracks resource configurations. Systems Manager (D) manages infrastructure operations.
---
