# AWS Key Topics — In-Depth Study Guide

---

## ⭐ AWS Pricing Models

AWS offers several pricing models, and the exam loves testing whether you know which one fits a given scenario.

### On-Demand Instances
- Pay by the hour or second (Linux = per second, Windows = per hour)
- No upfront commitment, no long-term contract
- Best for: unpredictable workloads, short-term projects, testing/development
- Most expensive per-hour rate, but most flexible
- You can start and stop anytime

### Reserved Instances (RIs)
- Commit to 1-year or 3-year term in exchange for a discount (up to 72% off On-Demand)
- Three payment options:
  - **All Upfront** — biggest discount, pay everything upfront
  - **Partial Upfront** — moderate discount, pay some upfront + monthly
  - **No Upfront** — smallest discount, pay monthly only
- Best for: steady-state, predictable workloads running 24/7
- Types:
  - **Standard RIs** — locked to a specific instance type, biggest discount
  - **Convertible RIs** — can change instance family/OS/tenancy, smaller discount

### Savings Plans
- Flexible alternative to Reserved Instances
- Commit to a consistent amount of compute usage (measured in $/hour) for 1 or 3 years
- Two types:
  - **Compute Savings Plans** — apply to any EC2 instance, Lambda, or Fargate usage regardless of Region, instance family, OS, or tenancy. Most flexible.
  - **EC2 Instance Savings Plans** — locked to a specific instance family in a specific Region, but flexible on size, OS, and tenancy. Bigger discount than Compute.
- Best for: organizations that want RI-level savings with more flexibility

### Spot Instances
- Purchase unused EC2 capacity at up to 90% discount
- AWS can reclaim them with a **2-minute warning** when capacity is needed
- Best for: fault-tolerant, flexible workloads — batch processing, data analysis, CI/CD, rendering
- NOT suitable for: databases, critical applications, anything that can't handle interruption

### Dedicated Hosts
- A physical EC2 server fully dedicated to your use
- Most expensive option
- Best for: regulatory/compliance requirements, software licensing that requires per-socket or per-core visibility (e.g., Windows Server, SQL Server, Oracle)
- You control instance placement on the physical server

### Dedicated Instances
- Instances that run on hardware dedicated to a single customer
- Less control than Dedicated Hosts (you don't see the physical server)
- Cheaper than Dedicated Hosts but more expensive than shared tenancy

### Free Tier
- Three types of offers:
  - **12-Month Free** — available for 12 months after account creation (e.g., 750 hrs/month EC2 t2.micro, 5 GB S3)
  - **Always Free** — never expires (e.g., 1 million Lambda requests/month, 25 GB DynamoDB)
  - **Short-Term Trials** — free for a limited period when you first use a service

### Key Exam Concepts
- "Steady-state, predictable" → Reserved Instances or Savings Plans
- "Can tolerate interruptions" → Spot Instances
- "Unpredictable, short-term" → On-Demand
- "Licensing compliance" → Dedicated Hosts
- "Lowest cost for fault-tolerant batch jobs" → Spot Instances
- "Flexibility across instance families and Regions" → Compute Savings Plans

---

## Amazon VPN

AWS provides two VPN services for connecting on-premises networks to AWS securely over the internet.

### AWS Site-to-Site VPN
- Creates an **encrypted IPsec tunnel** between your on-premises network and your AWS VPC
- Traffic goes over the **public internet** but is encrypted end-to-end
- Components:
  - **Virtual Private Gateway (VGW)** — the VPN endpoint on the AWS side, attached to your VPC
  - **Customer Gateway (CGW)** — represents your on-premises VPN device (router/firewall)
  - **VPN Connection** — two redundant IPsec tunnels between VGW and CGW (for high availability)
- Supports static routing or dynamic routing (BGP)
- Setup time: minutes to hours (much faster than Direct Connect)
- Bandwidth: limited by your internet connection speed, typically up to 1.25 Gbps per tunnel
- Best for: quick, encrypted connectivity to AWS when you don't need dedicated bandwidth

### AWS Client VPN
- Managed VPN service for **individual users** (remote workers) to connect to AWS or on-premises resources
- Based on OpenVPN — users install a VPN client on their laptop/device
- Supports Active Directory and certificate-based authentication
- Best for: remote employees who need secure access to resources in a VPC

### VPN vs. Direct Connect — Key Differences
| Feature | Site-to-Site VPN | AWS Direct Connect |
|---------|-----------------|-------------------|
| Connection | Over public internet (encrypted) | Dedicated private line (not internet) |
| Setup time | Minutes to hours | Weeks to months |
| Bandwidth | Up to 1.25 Gbps/tunnel | 1 Gbps, 10 Gbps, or 100 Gbps |
| Latency | Variable (internet-dependent) | Consistent, low latency |
| Cost | Lower | Higher |
| Encryption | Built-in IPsec | Not encrypted by default (can add VPN on top) |

### Exam Tips
- "Encrypted connection over the internet" → Site-to-Site VPN
- "Dedicated, private connection NOT over the internet" → Direct Connect
- "Quick setup, lower cost" → VPN
- "Consistent performance, high bandwidth" → Direct Connect
- You can use BOTH together — VPN over Direct Connect for encrypted dedicated connectivity

---

## Amazon WorkSpaces

Amazon WorkSpaces is a managed **Desktop-as-a-Service (DaaS)** solution.

### What It Does
- Provides fully managed, persistent **virtual desktops** in the cloud
- Users get a Windows or Linux desktop they can access from any supported device (laptop, tablet, thin client, Chromebook)
- Each WorkSpace is a dedicated virtual machine with persistent storage — your files and settings are saved between sessions

### Key Features
- **Persistent storage** — each WorkSpace has a root volume (OS) and user volume (data) backed by EBS
- **Protocol** — uses WSP (WorkSpaces Streaming Protocol) or PCoIP for streaming the desktop
- **Directory integration** — integrates with AWS Directory Service, Microsoft Active Directory, or AD Connector
- **Multi-factor authentication** — supports MFA via RADIUS
- **Encryption** — supports encryption of volumes at rest and in transit
- **Auto Stop/Start** — WorkSpaces can automatically stop after a period of inactivity to save costs

### Pricing
- **Monthly** — flat monthly fee, always-on (best for full-time users)
- **Hourly** — small monthly fee + per-hour charge when running (best for part-time or occasional users)
- You choose the bundle (CPU, RAM, storage) — ranges from Value (1 vCPU, 2 GB RAM) to Performance/Power/PowerPro

### Use Cases
- Remote workforce — provide secure desktops without shipping hardware
- BYOD (Bring Your Own Device) — corporate desktop on personal devices
- Temporary workers/contractors — spin up and tear down desktops quickly
- Data security — data stays in the cloud, never on the local device

### WorkSpaces vs. AppStream 2.0
- **WorkSpaces** = full persistent desktop (like a virtual PC)
- **AppStream 2.0** = streams individual applications (not a full desktop), non-persistent by default

---

## Amazon Migration Services

AWS provides several services for different migration scenarios.

### AWS Migration Hub
- **Central tracking dashboard** for all your migrations
- Tracks progress of migrations across multiple AWS migration tools
- Does not perform migrations itself — it aggregates status from other tools

### AWS Application Migration Service (AWS MGN)
- Formerly CloudEndure Migration
- **Lift-and-shift** migration of servers (physical, virtual, or cloud) to AWS
- Continuously replicates source servers to AWS, then performs a cutover with minimal downtime
- Supports Windows and Linux
- Best for: migrating existing servers to EC2 without modifying the application

### AWS Database Migration Service (DMS)
- Migrates databases to AWS with minimal downtime
- Source database remains operational during migration
- Supports:
  - **Homogeneous** migrations (e.g., Oracle → Oracle, MySQL → MySQL)
  - **Heterogeneous** migrations (e.g., Oracle → Aurora, SQL Server → PostgreSQL) — requires AWS Schema Conversion Tool (SCT) first
- Can also be used for continuous data replication

### AWS Schema Conversion Tool (SCT)
- Converts database schemas from one engine to another (e.g., Oracle stored procedures → PostgreSQL)
- Used in combination with DMS for heterogeneous migrations
- Free to use

### AWS Snow Family (Physical Data Transfer)
- For migrating **massive amounts of data** where network transfer is too slow or expensive
- **Snowcone** — 8 TB usable storage, smallest device, portable (fits in a backpack)
- **Snowball Edge** — 80 TB usable storage, comes in Storage Optimized and Compute Optimized variants, can run EC2 instances and Lambda locally
- **Snowmobile** — 100 PB capacity, literally a shipping container on a truck, for exabyte-scale migrations

### AWS DataSync
- Automated data transfer service for moving data between on-premises storage and AWS (S3, EFS, FSx)
- Uses a software agent installed on-premises
- Transfers over the internet or Direct Connect
- Best for: ongoing data transfers, not one-time massive migrations

### AWS Transfer Family
- Managed file transfer service supporting SFTP, FTPS, and FTP protocols
- Transfers files directly into/out of S3 or EFS
- Best for: organizations that have existing file transfer workflows using SFTP

### Exam Tips
- "Lift-and-shift servers" → Application Migration Service (MGN)
- "Migrate databases" → Database Migration Service (DMS)
- "50+ TB physical transfer" → Snowball Edge
- "Exabyte-scale" → Snowmobile
- "Track migration progress" → Migration Hub
- "Convert database schema" → Schema Conversion Tool (SCT)

---

## ⭐ AWS IAM (Identity and Access Management)

IAM is one of the most heavily tested topics on the CLP exam. Know it cold.

### What IAM Is
- A **global service** (not tied to any Region)
- Controls **who** (authentication) can do **what** (authorization) in your AWS account
- Free to use — no additional charges for IAM

### Core Components

#### Root User
- The email address used to create the AWS account
- Has **unrestricted access** to everything in the account
- Best practice: **never use the root user for daily tasks**
- Lock it down with MFA immediately
- Only use root for tasks that specifically require it (e.g., changing account settings, closing the account, changing the support plan)

#### IAM Users
- Represents a **person or application** that interacts with AWS
- Has permanent long-term credentials (username/password for console, access keys for CLI/API)
- Best practice: create individual users, never share credentials

#### IAM Groups
- A **collection of IAM users**
- Attach policies to a group, and all users in the group inherit those permissions
- A user can belong to multiple groups
- Groups cannot contain other groups
- Groups are for organizing users and simplifying permission management

#### IAM Roles
- An identity with permissions that is **assumed temporarily**
- No permanent credentials — provides temporary security credentials via STS (Security Token Service)
- Use cases:
  - **EC2 instance roles** — allow an EC2 instance to access other AWS services (e.g., S3) without embedding access keys
  - **Cross-account access** — allow users in Account A to access resources in Account B
  - **Federated access** — allow external users (corporate AD, Google, etc.) to access AWS
  - **Service roles** — allow AWS services to act on your behalf (e.g., Lambda accessing DynamoDB)
- Best practice: **always prefer roles over access keys**

#### IAM Policies
- JSON documents that define permissions
- Structure:
  ```json
  {
    "Version": "2012-10-17",
    "Statement": [
      {
        "Effect": "Allow",
        "Action": "s3:GetObject",
        "Resource": "arn:aws:s3:::my-bucket/*"
      }
    ]
  }
  ```
- **Effect** — Allow or Deny
- **Action** — what API calls are permitted (e.g., s3:GetObject, ec2:RunInstances)
- **Resource** — which AWS resources the policy applies to (ARN)
- Types:
  - **AWS Managed Policies** — pre-built by AWS (e.g., AmazonS3ReadOnlyAccess)
  - **Customer Managed Policies** — created by you, reusable across users/groups/roles
  - **Inline Policies** — embedded directly in a single user, group, or role (not reusable)
- **Deny always wins** — if any policy denies an action, it's denied regardless of other Allow statements

### Multi-Factor Authentication (MFA)
- Adds a second layer of authentication beyond username/password
- Supported devices: virtual MFA (Google Authenticator, Authy), hardware MFA key (YubiKey), hardware MFA device
- Best practice: enable MFA on the root user AND all IAM users with console access

### IAM Access Analyzer
- Identifies resources shared with external entities (e.g., S3 buckets accessible from outside your account)
- Helps you verify that your policies grant only intended access

### IAM Identity Center (formerly AWS SSO)
- Centralized access management for multiple AWS accounts
- Supports federation with corporate identity providers (SAML 2.0, OIDC)
- Provides single sign-on to AWS accounts and business applications
- Best for: organizations with multiple AWS accounts that want centralized user management

### Key Exam Concepts
- "Temporary credentials" → IAM Roles
- "Allow EC2 to access S3" → IAM Role (instance profile), NOT access keys
- "Centrally manage access across multiple accounts" → IAM Identity Center
- "Principle of least privilege" → grant only the minimum permissions needed
- "Global service" → IAM (not tied to a Region)
- "Deny always wins" over Allow

---

## ⭐ Artifact vs. Config vs. CloudTrail

These three services are frequently confused on the exam. Here's how to tell them apart.

### AWS Artifact
- **What it is:** A self-service portal for accessing AWS **compliance reports and agreements**
- **What it provides:**
  - Third-party audit reports (SOC 1, SOC 2, SOC 3, PCI DSS, ISO 27001, HIPAA, etc.)
  - AWS compliance certifications
  - Business Associate Agreements (BAA) for HIPAA
  - Non-Disclosure Agreements (NDA)
- **What it does NOT do:** It does not monitor, audit, or configure anything in your account
- **Think of it as:** A document library of AWS's compliance paperwork
- **Exam trigger:** "Where can I find AWS compliance reports?" or "HIPAA BAA" or "SOC 2 audit report" → **Artifact**

### AWS Config
- **What it is:** A service that **continuously monitors and records the configuration** of your AWS resources
- **What it does:**
  - Records configuration changes over time (e.g., "security group SG-123 was modified at 3:00 PM")
  - Evaluates configurations against **rules** (e.g., "all S3 buckets must have encryption enabled")
  - Provides a **configuration timeline** showing how a resource changed over time
  - Can trigger **auto-remediation** when a rule is violated (e.g., automatically re-enable encryption)
- **What it does NOT do:** It does not log API calls (that's CloudTrail) or provide compliance certifications (that's Artifact)
- **Think of it as:** A continuous compliance auditor that watches your resource configurations
- **Exam trigger:** "Track resource configuration changes" or "ensure compliance with internal policies" or "detect misconfigured security groups" → **Config**

### AWS CloudTrail
- **What it is:** A service that **logs all API calls** made in your AWS account
- **What it does:**
  - Records who did what, when, and from where (user, action, time, source IP)
  - Logs management events (e.g., creating an EC2 instance, modifying a security group) by default
  - Can log data events (e.g., S3 object-level operations, Lambda invocations) when enabled
  - Delivers logs to S3 and optionally to CloudWatch Logs
  - Enabled by default for management events (90-day history viewable in console)
- **What it does NOT do:** It does not evaluate whether configurations are compliant (that's Config) or provide compliance reports (that's Artifact)
- **Think of it as:** A security camera recording every action taken in your AWS account
- **Exam trigger:** "Who launched this instance?" or "audit API calls" or "investigate a security incident" → **CloudTrail**

### Side-by-Side Comparison

| Feature | Artifact | Config | CloudTrail |
|---------|----------|--------|------------|
| Purpose | Compliance documents | Resource configuration monitoring | API call logging |
| Answers | "Is AWS compliant with X?" | "Are MY resources configured correctly?" | "Who did what and when?" |
| Scope | AWS's compliance posture | Your resource configurations | Your API activity |
| Output | PDF reports, agreements | Configuration snapshots, compliance rules | JSON log files of API calls |
| Proactive/Reactive | Reference documents | Proactive (rules + remediation) | Reactive (audit trail) |

---

## ⭐ Amazon CloudFront and AWS WAF

These two services are often tested together because they work together to deliver and protect web content.

### Amazon CloudFront
- **What it is:** AWS's Content Delivery Network (CDN)
- **How it works:**
  1. User requests content (image, video, HTML, API response)
  2. Request goes to the nearest **edge location** (400+ worldwide)
  3. If the content is cached at the edge → served immediately (cache hit)
  4. If not cached → CloudFront fetches it from the **origin** (S3, EC2, ALB, or any HTTP server), caches it, then serves it
- **Key concepts:**
  - **Origin** — where the original content lives (S3 bucket, EC2 instance, ALB, custom HTTP server)
  - **Distribution** — the CloudFront configuration that maps to your origin
  - **Edge Location** — the physical location where content is cached (NOT the same as a Region or AZ)
  - **TTL (Time to Live)** — how long content stays cached before CloudFront checks the origin for updates
  - **Origin Access Control (OAC)** — restricts S3 bucket access so content can ONLY be accessed through CloudFront, not directly via S3 URL
- **Features:**
  - HTTPS support with free SSL/TLS certificates via ACM
  - Custom domain names (CNAME)
  - Geo-restriction — block or allow access from specific countries
  - Lambda@Edge / CloudFront Functions — run code at edge locations for customization
  - Real-time logging and metrics
- **Global service** — not tied to any Region
- **Pricing:** Pay for data transfer out + number of HTTP requests

### AWS WAF (Web Application Firewall)
- **What it is:** A firewall that protects web applications from common web exploits
- **How it works:**
  - You create **Web ACLs** (Access Control Lists) containing **rules**
  - Rules inspect incoming HTTP/HTTPS requests and allow, block, or count them
  - Attaches to: **CloudFront, ALB, API Gateway, or AppSync**
- **What it protects against:**
  - SQL injection
  - Cross-site scripting (XSS)
  - IP-based attacks (block specific IPs or IP ranges)
  - Rate-based attacks (rate limiting — e.g., block IPs making more than 2,000 requests in 5 minutes)
  - Geographic restrictions
  - Bot traffic
- **Rule types:**
  - **AWS Managed Rules** — pre-built rule sets maintained by AWS (e.g., OWASP Top 10, SQL injection, known bad inputs)
  - **Custom Rules** — rules you write based on your specific needs
  - **Marketplace Rules** — third-party rule sets from AWS Marketplace
- **WAF vs. Shield:**
  - WAF = Layer 7 (application layer) protection against web exploits
  - Shield = Layer 3/4 (network/transport layer) protection against DDoS attacks
  - They complement each other — use both for comprehensive protection

### How They Work Together
```
User → CloudFront Edge Location → WAF inspects request → If allowed → Origin (S3/EC2/ALB)
                                  → If blocked → 403 Forbidden
```
WAF rules are evaluated at the CloudFront edge, so malicious traffic is blocked before it ever reaches your origin servers. This reduces load on your infrastructure and blocks attacks at the edge.

### Exam Tips
- "Reduce latency globally" → CloudFront
- "Cache content at edge locations" → CloudFront
- "Protect against SQL injection / XSS" → WAF
- "Rate limiting" → WAF
- "DDoS protection" → Shield (not WAF)
- "Block traffic from specific countries" → CloudFront geo-restriction OR WAF geographic rules
- "Serve S3 content only through CloudFront" → Origin Access Control (OAC)

---

## Amazon Cognito

### What It Is
- A service for adding **user authentication and authorization to web and mobile applications**
- Manages application end users — NOT AWS account users (that's IAM)

### Two Main Components

#### User Pools
- A **user directory** for your application
- Handles sign-up, sign-in, password recovery, email/phone verification
- Supports:
  - Username/password authentication
  - Social identity providers (Google, Facebook, Apple, Amazon)
  - SAML 2.0 and OIDC enterprise identity providers
  - Multi-factor authentication (MFA)
  - Customizable sign-up/sign-in UI
- Returns **JSON Web Tokens (JWTs)** after successful authentication
- Think of it as: "Who is this user?"

#### Identity Pools (Federated Identities)
- Provides **temporary AWS credentials** to users so they can access AWS services directly (e.g., S3, DynamoDB)
- Users can be authenticated (via User Pool, social provider, etc.) or unauthenticated (guest access)
- Maps users to IAM roles with specific permissions
- Think of it as: "What can this user access in AWS?"

### Common Pattern
```
User signs in → Cognito User Pool authenticates → Returns JWT token
                                                → JWT exchanged with Identity Pool
                                                → Identity Pool returns temporary AWS credentials
                                                → User accesses S3/DynamoDB directly
```

### Cognito vs. IAM vs. IAM Identity Center
| Feature | Cognito | IAM | IAM Identity Center |
|---------|---------|-----|-------------------|
| For | App end users (customers) | AWS account users (employees) | Multi-account AWS access |
| Social login | Yes (Google, Facebook) | No | No |
| Scale | Millions of users | Thousands of users | Thousands of users |
| Use case | Mobile/web app auth | AWS service access | SSO across AWS accounts |

### Exam Tips
- "Mobile app user sign-up/sign-in" → Cognito
- "Social identity providers (Google, Facebook)" → Cognito
- "Temporary AWS credentials for app users" → Cognito Identity Pools
- "AWS employee access management" → IAM or IAM Identity Center

---

## AWS Fargate

### What It Is
- A **serverless compute engine for containers**
- Works with both Amazon ECS and Amazon EKS
- You define your containers — Fargate handles all the underlying infrastructure

### How It Works
- You create a **task definition** (ECS) or **pod spec** (EKS) that describes your containers (image, CPU, memory, networking)
- Fargate provisions the compute, runs your containers, and scales automatically
- No EC2 instances to manage, patch, or scale
- Each task/pod runs in its own isolated environment (kernel-level isolation)

### Pricing
- Pay for the vCPU and memory your containers actually use, per second
- No charges for idle capacity — you only pay when containers are running
- More expensive per-unit than EC2 but eliminates operational overhead

### Fargate vs. EC2 Launch Type
| Feature | Fargate | EC2 Launch Type |
|---------|---------|----------------|
| Infrastructure management | None (serverless) | You manage EC2 instances |
| Scaling | Automatic | You configure Auto Scaling for instances |
| Pricing | Per task (vCPU + memory) | Per EC2 instance (running or not) |
| Patching | AWS handles everything | You patch the OS |
| Best for | Variable workloads, small teams | Large steady-state workloads, cost optimization at scale |

### Exam Tips
- "Run containers without managing servers" → Fargate
- "Serverless containers" → Fargate
- "Reduce operational overhead for containers" → Fargate
- Fargate is NOT a standalone service — it's a launch type for ECS and EKS

---

## Amazon ECS (Elastic Container Service)

### What It Is
- AWS's **proprietary container orchestration service**
- Manages the deployment, scaling, and operation of Docker containers
- Tightly integrated with the AWS ecosystem (IAM, CloudWatch, ALB, etc.)

### Key Concepts
- **Cluster** — a logical grouping of tasks or services (the environment where containers run)
- **Task Definition** — a blueprint for your application (like a docker-compose file) — defines container image, CPU, memory, ports, environment variables, volumes
- **Task** — a running instance of a task definition (one or more containers running together)
- **Service** — maintains a desired number of tasks running and handles load balancing, rolling updates, and auto-recovery

### Launch Types
- **Fargate** — serverless, no EC2 management (see above)
- **EC2** — you manage a fleet of EC2 instances that run your containers
- You can mix both in the same cluster

### Networking
- **awsvpc mode** — each task gets its own Elastic Network Interface (ENI) with a private IP, just like an EC2 instance
- Integrates with ALB/NLB for load balancing

### Exam Tips
- "AWS-native container orchestration" → ECS
- "Docker containers on AWS" → ECS (or EKS)
- "Simpler than Kubernetes" → ECS
- ECS is AWS-proprietary — if the question mentions Kubernetes, it's EKS

---

## Amazon EKS (Elastic Kubernetes Service)

### What It Is
- A **managed Kubernetes service** on AWS
- Runs the open-source Kubernetes control plane — you don't manage the master nodes
- Compatible with standard Kubernetes tooling (kubectl, Helm, etc.)

### Key Concepts
- **Control Plane** — managed by AWS (API server, etcd, scheduler, controller manager) — runs across multiple AZs for high availability
- **Worker Nodes** — EC2 instances or Fargate that run your containerized workloads
- **Pods** — the smallest deployable unit in Kubernetes (one or more containers)
- **Node Groups** — groups of EC2 instances that serve as worker nodes
  - **Managed Node Groups** — AWS manages provisioning and lifecycle of nodes
  - **Self-Managed Node Groups** — you manage the EC2 instances yourself
  - **Fargate Profiles** — serverless, no nodes to manage

### ECS vs. EKS
| Feature | ECS | EKS |
|---------|-----|-----|
| Orchestrator | AWS proprietary | Open-source Kubernetes |
| Complexity | Simpler | More complex, more powerful |
| Portability | AWS-only | Portable across clouds and on-premises |
| Tooling | AWS-native (task definitions) | Kubernetes ecosystem (kubectl, Helm) |
| Best for | Teams already on AWS, simpler workloads | Teams with Kubernetes expertise, multi-cloud strategy |

### Exam Tips
- "Managed Kubernetes" → EKS
- "Portable across cloud providers" → EKS (Kubernetes is open-source)
- "Reduce vendor lock-in for containers" → EKS
- "Simpler container management, AWS-native" → ECS

---

## ⭐ AWS Well-Architected Framework

The Well-Architected Framework is a set of best practices for designing and operating reliable, secure, efficient, cost-effective, and sustainable systems in the cloud. It has **six pillars**.

### Pillar 1: Operational Excellence
- **Focus:** Running and monitoring systems to deliver business value, and continually improving processes
- **Key principles:**
  - Perform operations as code (infrastructure as code)
  - Make frequent, small, reversible changes
  - Refine operations procedures frequently
  - Anticipate failure (run game days, chaos engineering)
  - Learn from all operational failures
- **AWS services:** CloudFormation, CloudWatch, Config, CloudTrail, Systems Manager, X-Ray

### Pillar 2: Security
- **Focus:** Protecting information, systems, and assets through risk assessment and mitigation
- **Key principles:**
  - Implement a strong identity foundation (least privilege, MFA)
  - Enable traceability (log everything with CloudTrail)
  - Apply security at all layers (edge, VPC, subnet, instance, OS, application)
  - Automate security best practices
  - Protect data in transit and at rest
  - Keep people away from data (reduce manual access)
  - Prepare for security events (incident response plans)
- **AWS services:** IAM, Organizations (SCPs), CloudTrail, GuardDuty, Security Hub, WAF, Shield, KMS, Macie, Inspector

### Pillar 3: Reliability
- **Focus:** Ensuring a workload performs its intended function correctly and consistently
- **Key principles:**
  - Automatically recover from failure
  - Test recovery procedures
  - Scale horizontally to increase aggregate workload availability
  - Stop guessing capacity (use Auto Scaling)
  - Manage change in automation
- **AWS services:** CloudWatch, Auto Scaling, ELB, RDS Multi-AZ, S3 (11 9s durability), Route 53 (health checks)

### Pillar 4: Performance Efficiency
- **Focus:** Using computing resources efficiently to meet system requirements and maintaining that efficiency as demand changes
- **Key principles:**
  - Democratize advanced technologies (use managed services)
  - Go global in minutes (deploy in multiple Regions)
  - Use serverless architectures
  - Experiment more often
  - Consider mechanical sympathy (use the right tool for the job)
- **AWS services:** Auto Scaling, Lambda, CloudFront, ElastiCache, RDS Read Replicas, EBS volume types

### Pillar 5: Cost Optimization
- **Focus:** Avoiding unnecessary costs and understanding where money is being spent
- **Key principles:**
  - Implement cloud financial management
  - Adopt a consumption model (pay only for what you use)
  - Measure overall efficiency
  - Stop spending money on undifferentiated heavy lifting (use managed services)
  - Analyze and attribute expenditure (tagging, Cost Explorer)
- **AWS services:** Cost Explorer, Budgets, Trusted Advisor, Reserved Instances, Savings Plans, Spot Instances, S3 Lifecycle Policies, right-sizing with Compute Optimizer

### Pillar 6: Sustainability
- **Focus:** Minimizing the environmental impact of running cloud workloads
- **Key principles:**
  - Understand your impact
  - Establish sustainability goals
  - Maximize utilization (right-size resources)
  - Anticipate and adopt new, more efficient offerings
  - Use managed services (AWS optimizes shared infrastructure)
  - Reduce the downstream impact of your workloads
- **AWS services:** Compute Optimizer, Auto Scaling, Graviton instances (energy-efficient ARM processors), serverless (Lambda, Fargate)

### AWS Well-Architected Tool
- A **free service** in the AWS Console
- Helps you review your workloads against the six pillars
- Generates a report with identified risks and improvement recommendations
- Not an automated scanner — it's a questionnaire-based review

### Exam Tips
- Know all **six pillar names** and what each focuses on
- "Run workloads effectively, gain operational insights" → Operational Excellence
- "Protect information and systems" → Security
- "Recover from failure, scale to meet demand" → Reliability
- "Use resources efficiently" → Performance Efficiency
- "Avoid unnecessary costs" → Cost Optimization
- "Minimize environmental impact" → Sustainability
- The exam may describe a scenario and ask which pillar it relates to — focus on the primary concern in the question

---

*Last updated: April 2026*
