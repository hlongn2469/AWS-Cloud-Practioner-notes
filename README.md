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
## Security and Compliance

## Billing and Pricing
