# AWS Cloud Practitioner — Rapid Fire Cheatsheet

One-line triggers → answers. Scan this the night before. If you can match the keyword to the service, you pass.

---

## 🧠 Cloud Concepts

| Trigger | Answer |
|---|---|
| 6 advantages of cloud | Trade CapEx→OpEx, massive economies of scale, stop guessing capacity, speed/agility, stop running data centers, go global in minutes |
| IaaS / PaaS / SaaS | EC2 / Elastic Beanstalk / WorkSpaces, Rekognition |
| Elasticity | Scale up AND down automatically |
| Scalability | Ability to grow |
| High availability | Stay up during failure (multi-AZ) |
| Fault tolerance | Keep working through failure (redundancy) |
| Agility | Speed to build/deploy |
| Region | Geographic area, 2+ AZs |
| Availability Zone | 1+ data centers, isolated power/network |
| Edge Location | CloudFront cache point (400+) |
| Local Zone | Low-latency compute near metro areas |
| Outposts | AWS hardware in your data center |
| Wavelength | 5G edge compute |

---

## 🔐 Security & Compliance

### Shared Responsibility (memorize!)
- **AWS:** security OF the cloud → hardware, hypervisor, facilities, managed service internals
- **Customer:** security IN the cloud → data, IAM, OS patching (EC2), app code, network config, encryption choice
- Managed services (S3, DynamoDB, Lambda) → AWS patches. EC2 → you patch.

### IAM quick hits
| Trigger | Answer |
|---|---|
| Who can do what in AWS | IAM |
| Global service | IAM |
| Give EC2 access to S3 | IAM Role (never access keys) |
| Temporary credentials | IAM Role / STS |
| Collection of users | IAM Group (no nesting) |
| Deny vs Allow | Explicit Deny always wins |
| SSO across many AWS accounts | IAM Identity Center |
| End-user auth for your app | Cognito |
| Social login (Google/Facebook) | Cognito User Pool |
| Root user best practice | Enable MFA, lock away, never use daily |

### Security services (the confusing ones)
| Trigger | Service |
|---|---|
| Compliance reports (SOC, PCI, HIPAA BAA) | **Artifact** |
| Records resource config changes + rules | **Config** |
| Logs every API call (who did what) | **CloudTrail** |
| DDoS protection | **Shield** (Standard free, Advanced paid) |
| SQL injection / XSS | **WAF** |
| Threat detection via ML on logs | **GuardDuty** |
| Finds PII in S3 | **Macie** |
| Scans EC2/ECR/Lambda for vulns | **Inspector** |
| Central security findings dashboard | **Security Hub** |
| Create/manage encryption keys | **KMS** |
| SSL/TLS certs (free) | **ACM** |
| Store DB passwords, auto-rotate | **Secrets Manager** |
| Cheaper secret storage, no rotation | **Parameter Store** |
| Hardware security module | **CloudHSM** |
| Best-practice checks (5 categories) | **Trusted Advisor** |

---

## 💻 Compute

| Trigger | Service |
|---|---|
| Virtual servers | EC2 |
| Serverless functions, 15-min max | Lambda |
| Pay per request + duration | Lambda |
| Docker on AWS | ECS |
| Managed Kubernetes | EKS |
| Serverless containers | Fargate |
| PaaS for web apps (Java/.NET/etc.) | Elastic Beanstalk |
| Batch jobs at scale | AWS Batch |
| Hybrid/on-prem AWS hardware | Outposts |
| Edge compute at the ISP | Wavelength / Local Zones |

### EC2 pricing (huge exam topic)
| Trigger | Pricing |
|---|---|
| Unpredictable, short-term | **On-Demand** |
| Steady 24/7 for 1–3 years | **Reserved** (up to 72% off) |
| Flexible commitment across EC2/Lambda/Fargate | **Savings Plans** |
| Fault-tolerant, up to 90% off, 2-min warning | **Spot** |
| BYOL, per-socket licensing | **Dedicated Host** |
| Isolated hardware, less control | **Dedicated Instance** |

---

## 💾 Storage

| Trigger | Service |
|---|---|
| Object storage, 11 9s durability | S3 |
| Block storage for EC2 | EBS (1 AZ, attach to 1 instance usually) |
| Shared file system for Linux (NFS) | EFS (multi-AZ, auto-scales) |
| Windows file server / Lustre HPC | FSx |
| Hybrid on-prem to AWS storage | Storage Gateway |
| 80 TB physical transfer | Snowball Edge |
| 8 TB portable | Snowcone |
| 100 PB truck | Snowmobile |
| Backup across services | AWS Backup |

### S3 storage classes (match the scenario)
| Scenario | Class |
|---|---|
| Default, frequent access | Standard |
| Unknown/changing access patterns | Intelligent-Tiering |
| Infrequent, ms retrieval | Standard-IA |
| Infrequent, single AZ (cheaper, less durable) | One Zone-IA |
| Archive, ms retrieval | Glacier Instant Retrieval |
| Archive, mins–hours retrieval | Glacier Flexible Retrieval |
| Cheapest, 12–48hr retrieval | Glacier Deep Archive |

---

## 🗄️ Databases

| Trigger | Service |
|---|---|
| Managed relational (MySQL, Postgres, Oracle, SQL Server, MariaDB) | RDS |
| 5x MySQL / 3x Postgres perf, cloud-native | Aurora |
| Serverless NoSQL, single-digit ms | DynamoDB |
| In-memory cache (Redis/Memcached) | ElastiCache |
| Data warehouse (petabyte analytics) | Redshift |
| Graph database | Neptune |
| Time-series | Timestream |
| Ledger (immutable, cryptographic) | QLDB |
| Document DB (MongoDB-compatible) | DocumentDB |
| DB migration with min downtime | DMS |
| Convert schema between engines | Schema Conversion Tool (SCT) |

---

## 🌐 Networking & Delivery

| Trigger | Service |
|---|---|
| Isolated virtual network | VPC |
| Controls traffic to instances (stateful) | Security Group |
| Controls traffic at subnet level (stateless) | NACL |
| Encrypted tunnel over internet | Site-to-Site VPN |
| Dedicated private line (not internet) | Direct Connect |
| CDN / cache at edge | CloudFront |
| Static/dynamic TCP/UDP routing, global IP | Global Accelerator |
| DNS | Route 53 |
| Distribute traffic in a Region | Elastic Load Balancer |
| HTTP/HTTPS L7 LB | ALB |
| TCP/UDP L4 ultra-low latency | NLB |
| Connect many VPCs | Transit Gateway |
| 1:1 VPC connection | VPC Peering |

---

## 📊 Management, Monitoring & Governance

| Trigger | Service |
|---|---|
| Metrics, logs, alarms, dashboards | CloudWatch |
| API call audit log | CloudTrail |
| Config history + compliance rules | Config |
| Infra as code (JSON/YAML) | CloudFormation |
| Multi-account landing zone | Control Tower |
| Consolidated billing + SCPs | Organizations |
| Patch, run commands, Session Manager | Systems Manager (SSM) |
| Distributed tracing | X-Ray |
| Config mgmt (Chef/Puppet) | OpsWorks |

---

## 🚀 Deployment & Developer Tools

| Trigger | Service |
|---|---|
| Git repos | CodeCommit |
| Build & test | CodeBuild |
| Deploy to EC2/Lambda/ECS | CodeDeploy |
| CI/CD orchestration | CodePipeline |
| All-in-one dev experience | CodeStar (legacy) / CodeCatalyst |
| Cloud IDE | Cloud9 |
| Mobile/web app backend | Amplify |

---

## 🤖 Analytics, ML & Integration

| Trigger | Service |
|---|---|
| Serverless SQL queries on S3 | Athena |
| Managed Hadoop/Spark | EMR |
| Real-time streaming | Kinesis |
| Managed Kafka | MSK |
| ETL | Glue |
| Build, train, deploy ML | SageMaker |
| Image/video analysis | Rekognition |
| Text-to-speech | Polly |
| Speech-to-text | Transcribe |
| Translate text | Translate |
| Chatbots (Alexa-style) | Lex |
| NLP (sentiment, entities) | Comprehend |
| Business intelligence dashboards | QuickSight |
| Pub/sub messaging | SNS |
| Message queue | SQS |
| Event bus | EventBridge |
| Workflow orchestration | Step Functions |
| Managed email | SES |

---

## 💰 Billing, Pricing & Support

| Trigger | Service |
|---|---|
| Estimate costs before deploying | **Pricing Calculator** |
| Analyze historical spend, 12mo forecast | **Cost Explorer** |
| Set alerts when spend exceeds threshold | **Budgets** |
| Cost optimization recommendations | **Trusted Advisor** / **Compute Optimizer** |
| Consolidated billing discounts | **Organizations** |
| Flag unusual spending | **Cost Anomaly Detection** |
| Detailed line-item billing data | **Cost & Usage Report (CUR)** |

### Support plans (know the tiers)
| Plan | Key feature |
|---|---|
| **Basic** | Free, no tech support, 24/7 customer service, Trusted Advisor core checks |
| **Developer** | Business-hours email, 1 contact, 24hr response |
| **Business** | 24/7 phone/chat, unlimited contacts, all Trusted Advisor checks, 1hr for prod down |
| **Enterprise On-Ramp** | 30-min response for prod down, pooled TAM |
| **Enterprise** | 15-min response for business-critical down, dedicated TAM, concierge billing, IEM |

Key distinctions:
- **TAM (Technical Account Manager)** → Enterprise only (pooled on On-Ramp)
- **Concierge** → Enterprise
- **Third-party software support** → Business and up
- **Infrastructure Event Management (IEM)** → Enterprise (On-Ramp for additional fee)

---

## 🏛️ Well-Architected Framework — 6 Pillars

Mnemonic: **O**ld **S**chool **R**eliable **P**eople **C**hoose **S**ustainability
1. **Operational Excellence** — run & monitor, improve processes
2. **Security** — least privilege, encrypt everywhere, trace everything
3. **Reliability** — recover from failure, scale horizontally, multi-AZ
4. **Performance Efficiency** — right tool, use serverless/managed
5. **Cost Optimization** — pay for what you use, measure, tag
6. **Sustainability** — minimize environmental impact

---

## 🎯 High-Confusion Pairs (read twice)

- **Artifact vs Config vs CloudTrail** → Compliance *docs* / Your resource *configs* / *API* audit log
- **Shield vs WAF** → DDoS (L3/L4) / Web exploits (L7)
- **GuardDuty vs Inspector vs Macie** → Account threats / Vuln scans / PII in S3
- **CloudWatch vs CloudTrail** → Metrics & logs / API activity
- **SG vs NACL** → Stateful, instance-level, allow-only / Stateless, subnet-level, allow+deny
- **VPN vs Direct Connect** → Encrypted over internet / Dedicated private line
- **EBS vs EFS vs S3** → Block (1 EC2) / File (many EC2) / Object (anything)
- **RDS vs DynamoDB** → Relational / NoSQL key-value
- **Aurora vs RDS** → Cloud-native 5x perf / Standard engines
- **ECS vs EKS** → AWS-native / Kubernetes
- **SNS vs SQS** → Pub/sub push / Pull queue
- **Organizations vs Control Tower vs Identity Center** → Billing + SCPs / Landing zone automation / SSO
- **Cost Explorer vs Budgets vs Pricing Calculator** → Past & forecast / Alerts / Future estimate

---

## ⚡ Answer-in-5-seconds patterns

- "Minimal downtime DB migration" → DMS
- "Lift-and-shift servers" → Application Migration Service (MGN)
- "50TB physical transfer" → Snowball Edge
- "Encrypt data at rest with managed keys" → KMS
- "Auto-rotate RDS password" → Secrets Manager
- "Cache content globally" → CloudFront
- "Route users to nearest Region" → Route 53 (latency/geo) or Global Accelerator
- "Decouple microservices" → SQS / SNS / EventBridge
- "Run code without servers" → Lambda
- "Serverless containers" → Fargate
- "Business-critical 15-min response" → Enterprise Support
- "Where to get HIPAA BAA" → AWS Artifact
- "Who launched this EC2?" → CloudTrail
- "Is my S3 bucket encrypted?" → Config rule
- "Recommend idle resources to shut down" → Trusted Advisor / Compute Optimizer

Good luck. You've got this. 💪
