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


## Technology

## Security and Compliance

## Billing and Pricing
