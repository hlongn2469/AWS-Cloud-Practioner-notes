# AWS Cloud-Practioner exam notes
============================================================================================

### There are 4 domains that the exam taker will be tested on

| [Cloud Concepts 26%](#Cloud-Concepts) | [Technology 33%](#Technology) | [Security and Compliance 25%](#Security-and-Compliance) | [Blling and Pricing 16%](#Billing-and-Pricing)|
|---------------------------------------------|------------------------------------------|-------------------------------------------------------------|-----------------------------------------------------------------|

## Cloud Concepts
- [ ] **Major advantages of cloud computing**:
  * High availability: Systems are designed to operate continuously without failure for a long time. These systems avoid loss of service by reducing or managing failures.
  * Elasticity: You can provision only what you need, and then grow and shrink based on demand.
  * Agility: All the services you have access to help you innovate faster, giving you speed to market. 
  * Durability: Your data will remain intact without corruption.

- [ ] **Cloud computing models**:
  * Infrastructure as a Service (IaaS): Building blocks (Eg. Web hosting, EC2)
  * Software as a Service (Saas): Complete application (Eg. Email)
  * Platform as a Service (PaaS): Used by developers (Eg. Storefront website)

- [ ] **Deployment models**:
  * Private Cloud (on-premises): Exists in internal data center and don't offer advantages of cloud computing
  * Public Cloud (AWS): Provides all advantages of cloud computing and users are not responsible for physical hardware
  * Hybrid Cloud: Highly sensitive data stored locally and application runs on AWS infrastructure. Communication between private and public cloud is through **AWS Direct Connect**

- [ ] **AWS Global Infrastructure**:
  * Group regions by geographical locations which is fully idenependent and service specific
  * Availibity Zones(AZs): consists of one or more data centers in each region
  * AZs are physically separated by using different power grids, connected through low-latency links, fault tolerant, and allows high availability.
  * Edge Location: Mini data centers that are used for cache content for fast delivery to users and reduce latency (time takes between user request and respones). Low latency > high latency
  * **Remember for Exam**
    1. Multi-AZ deployments provide high avalibility
    2. AZ has multiple data centers
    3. A region is global and has 2 or more Azs
    4. Edge locations ensure low latency by placing content closer to users

- [ ] **AWS Account**:
  * AWS management console: allows access to AWS acount and manage applications from web browser
  * Root user: Established when create AWS account and has authority within the account.
  * Service VPC (Virtual private cloud): Create secure and private networks
  * AWS Command Line Interface (CLI): Allows access to AWS account through command or terminal window
  * **Remember for Exam**
    1. Protect root user as they have certain authorities in AWS account

## Technology
- [ ] **AWS EC2**:
  * EC2: allows you to rent and manage virtual servers in the cloud
  * Use cases: deploy a database or web application
  * Connectivity: AWS managment console, SSH, EC2 instance connect, AWS systems manager
  * A public is needed to access an EC2 instance while private key is needed to access from your local machine
  * Pricing: 
    * On-demand: Pay for what you use 
    * Spot: Let you take advantage of unused EC2 capacity but need to request spot. Cheapest. 
    * Reserved Instances: reserve specific instance type in a particular region for 1 or 3 years
    * Dedicated Host: allows pay for a physical server that is fully dedicated to running your instances
    * Savings Plan: Allows commit to compute usage (measured per hour) for 1 or 3 years
  * Features: 
    * Elastic Load Balancing: automatically distributes incoming application traffic accross multiple EC2 instances
      * Classic
      * Application
      * Gateway
      * Network  
    * Auto Scaling: Adds or replaces EC2 instances automically across AZs based on need and changing demand to improve the availibility of application
      * Horizontal scaling: Adds or replaces EC2 instances
      * Vertical scaling: Upgrades existing instances
- [ ] **AWS Lambda**:
  * Lambda is a severless compute service that lets you run code without managing servers
  * Allows developers to focus on business logics
  * Use cases: Real-time file processing, Sending emails, backend business logics
  * Features:
    * Supports popular programming languages (Java, Go, PowerShell, Node.js, C#, Python, Ruby)
    * Execute code in response to events
    * Write code in your IDE or via console
    * 15-minute timeout
  * Pricing: Charge based on the duration and number of requests
    * Compute time
    * Request count
    * Always free
   
- [ ] **AWS Fargate**:
  * AWS Fargate is a serverless compute engine for containers
    * Allows you to manage containers like Docker
    * Scale automatically
    * Serverless
   
- [ ] **Amazon LightSail**:
  * Lightsail allows you to quickly launch all resources you need for small prjects
    * Deploy preconfigured applications like WordPress websites quickly
    * Simple screens for people with no cloud experience
    * Includes VM, SSD-based storage, data transfer, DNS management and static IP
    * Low predicitable monthly fee 

- [ ] **AWS Outposts**:
  * Allows you to run cloud services in your internal data center
    * Supports workloads that need to remain on-premises due to latency or data processing needs
    * AWS delivers and installs servers in your internal data center.
    * Used for a hybrid experience
    * Have access to the cloud services and APIs to develop apps on-premises

- [ ] **AWS Batch**:
  * Allows you to process large workloads in smaller chunks
    * Runs hundreds and thousands of smaller batch processing jobs
    * Dynamically provisions instances based on volume

  * **Remember for Exam**
    1. AWS Fargate is considered serverless and is used to manage containers.
    2. Amazon Lightsail is a compute service that is used to quickly launch preconfigured applications for small projects.
    3. AWS Outposts supports a hybrid deployment model.
    4. AWS Batch is a compute service that is used to process large workloads in smaller batches.
   
- [ ] **Storage Services: S3**:
  * An object storage service for the cloud that is highly available.
    * Objects (or files) are stored in buckets (or directories).
    * Objects can be public or private.
    * Essentially unlimited storage that can hold millions of objects per bucket.
    * You can upload objects via the console, the CLI, or programmatically from within code using SDKs. 
  * Storage classes:
    * Standard: General purpose storage used for frequently accessed data 
    * Intelligent-tiering: Automatically moves your data to most cost-effective storage class
    *  Standard IA: Data accessed less frequently but requires rapid access
    *  One Zone IA: Similar to Standard IA but data stored in single AZ
    *  Glacier: Long term-data storage and archival for lower costs
    *  Glacier Deep Dive: Like Glacier but with longer access time. Cheapest
    *  Outposts: provides object storage on premises
  * **Remember for Exam**
    * S3 is a regional service but has a global namespace
    * S3 offers unlimited storage with many storage classes 
   
- [ ] **EC2 storage options**:
  * Amazon EBS: storage device/volume that can be attached or removed from your instance. Use for long term, quickly accessible data or run a database on an instance
  * Instance store: Volumes are temporary
  * EFS: Only supports linux file systems
  * Storage Gateway: supports hybrid model

- [ ] **Content Delivery Services**:
  * Amazon CloudFront: allows global distribution of content with security features like DDoS protection and IP blocking
  * Global Accelerator: provides low latency to the CDN
  * S3 Transfer Accelerstion: provides fast transfer of files over long distance

- [ ] **Networking Services: VPC and subcomponents**:
  * Amazon VPC: foundational service that allows you to create a secure private network in the AWS cloud where you launch your resources.
  * An internet gateway allows traffic to the public internet and peering connects 2 VPCs together.

- [ ] **DNS**:
  * Domain name system: direct internet traffics by connecting domain name and web servers
  * Amazon Route 53:
    * Performs health checks on AWS resources
    * Supports hybrid model
  * AWS Direct connect:
    * Dedicated physical network connection from your on-premises data center to AWS.
    * Data travels via private network
    * Support hybrid model
  * AWS VPN
    * Site-to-Site VPN: creates a secure connection between your internal networks(Customer Gateway) and your AWS VPCs (via VPN and virtual private gateway). 
    * Data travels via public internet and is automatically encrypted
    * Support hybrid movel
    * Connect on-premises data to AWS 
    * ![AWS VPN model](https://github.com/hlongn2469/AWS-Cloud-Practioner-notes/blob/main/Screen%20Shot%202021-07-20%20at%209.41.04%20AM.png)

- [ ] **Utilizing databases**:
  * Relational: RDS, Aurora
    * RDS: Supports database engines: AMZ Aurora, PostgreSQL, MySQL, MariaDB, Oracle DB, SQL server
    * Aurora: Supports PostgreSQL and MySQL only and managed by RDS  
  * NoSQL: DynamoDB
    * Non-relational key-value database
  * Graph: Neptune
    *  Creates social media graphs
  * In-memory: ElastiCache
    * in-memory datastore 
  * Document: DocumentDB
    *  Non relational DB that stores documents and supports MongoDB
- [ ] **Exploring Migration and Transfer Services**:
  * Database Migration Service (DMS) migrate on-premises databases to AWS
    * EG: Migrate on-premises Oracle databases to Aurora MySQL
  * Server Migration Service (SMS) migrate on-premises servers to AWS
  * AWS Snow family: allows large data transfers of on-premises data to AWS using a physical device
    * Snowcone: 8 tb of usage storage
    * Snowballedge: Native services are supported such as EC2 and Lambda
    * Snowball: transfer petabytes of data and is cheaper than transferring over the internet
    * Snow Mobile: the largest member of the transport family and supports exabyte-scale data
    * Datasync: Transfer data online and can be used to replicate data cross-Region or cross-account
- [ ] **Leveraging Analytics Services**:
  * AMZ Redshift:
    *  Data warehousing solution that handles exabyte-scale data
    *  Use cases: data consolidation and Relational Databases
  * Anthena: 
    * Query Service for AMZ S3 using SQL
  * Glue: data preparation for analytics
  * Kinesis: analyze data and video streams in real time
  * Elastic MapReduce (EMR): Process large amount of data
  * Data pipeline: moves data between compute and storage services
- [ ] **Leveraging Machine Learning Services**:
  * Rekognition: automate image and video analysis
  * Comprehend: NLP service that finds relationships in text
  * Polly: turns text into speech
  * SageMaker: helps build, train, and deploy ML models
  * Translate: Provides language translation 
  * Lex: build conversational interfaces like chatbots
- [ ] **Understanding Developer Tools**:
  * Cloud9: offers an integrated development environment (IDE) that runs inside a web browser.
  * CodeCommit: offers a service similar to GitHub that works with Git repositories. 
  * CodeDeploy: allows you to deploy an application to servers running on-premises and in the cloud.
  * CodePipeline: allows you to implement a CI/CD pipeline.
- [ ] **Exploring Deployment and Infrastructure Management Services**:
  * CloudFormation: supports infrastructure automation using Infrastructure as Code (IaC).
  * Elastic Beanstalk: is only used to deploy applications to the AWS Cloud — it is not used to deploy applications on-premises.
  * OpsWorks: can deploy applications on-premises, and it also automates infrastructure management using Chef or Puppet.
- [ ] **Utilizing Messaging and Integration Services: SQS**:
  * SQS (Simple Queue Service): message queueing service that allows you to build loosely coupled system (FIFO order)
- [ ] **Utilizing Messaging and Integration Services: SNS and SES**:
  * SNS(Simple notification service) allows you to send emails and text messages from your applications.
    * Best for notification purposes 
  * SES(Simple email service) is an email service that allows you to send richly formatted HTML emails from your applications.
    * Best for marketing campaigns or profesional email  
- [ ] **Exploring Auditing, Monitoring, and Logging Services**:
  * CloudWatch is a collection of services that help you monitor and observe your cloud resources.
    * NOTE: Cloudwatch can monitor your EC2 instances and notify you when certain events occur.
  * CloudTrail tracks user activity and API calls within your account
    * NOTE: Things you can track with CloudTrail: username, event time and name, IP address, access key, Region, and error code. 
## Security and Compliance
- [ ] **Understanding the Shared Responsibility Model**:
  * There is a shared security responsibility between you and AWS:
    * AWS: responsible for security of cloud (AWS global infra, networking components, software, and building security)
    * You: responsible for security in the cloud(Application data, security config, patching, IAM, network traffic, and installed software)
- [ ] **Leveraging the Well-Architected Framework**:
  ![](https://github.com/hlongn2469/AWS-Cloud-Practioner-notes/blob/main/well-arch.png)
- [ ] 
   
## Billing and Pricing
