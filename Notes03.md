# AWS Global Infrastructure

### AWS Global Infrastructure modules teach you to identify 
+ AWS Regions
+ Availability Zones
+ Edge locations
+ AWS Services & Service Categories

> [!IMPORTANT]
>  _AWS Global Infrastructure is designed and built to deliver a flexible, reliable, scalable and secure cloud computing environment with high-quality global network performance._


+ => AWS Region
  + => Availability Zones
    + => Data Centers

## AWS Region
1. Is a geographical area
2. data replication across Regions is controlled by you
3. Communication between Regions uses AWS backbone network infrastructure.
4. Provides full redundancy and connectivity to the network
5. It typically consists of 2 or more Availability Zones
6. Regions may have restricted access

### Criteria for Selecting Regions 
+ Data governance & legal requirements
+ Proximity to customers
+ Some services may not be available
+ Costs may vary by Region

## Availability Zones (AZ)
### Each Region has multiple Availability Zones
1. Each AZ is a fully isolated partition of the AWS Infrastructure
2. AZ consist of discrete data centers typically at least 3
3. AZs are designed for fault isolation
4. AZs are connected among themselves using high-speed private networking
5. AWS recommends replication data and resources across AZs for resiliency
6. AZs have their own power infrastructure and physically separated from other AZs by several kilometers.
7. All AZs in a Regions are within 100 kilometers of each other.

> [!Note]
> Customer can only choose AZ - choosing Data Center is not allowed to keep the location of actual data center unknown and secure.


## Data Centers
+ AWS data centers are designed for security
+ Data centers house all the data and it is where the data processing occurs.
+ Each data center has redundant power, networking, connectivity and is housed in a separate facility
+ A data center can have anywhere from 50,000 to 80,000 servers in a single location.


## Points of Preference
+ AWS provides a global network of over 180 Points of Presence locations.
+ These consists of 176 edge locations and 11 Regional edge caches
+ Amazon CloudFront - A global Content Delivery Network (CDN) that delivers content to end users with reduced latency
+ Regional edge caches is used for content which is accessed less frequently.
+ Points of presence continuously measure internet connectivity, performance and computing to find the best possible way to route traffic requests

### Benefits
+ Elasticity and scalability
  + Elastic infrastructure- dynamic adoption of capacity
  + Scalable infrastructure- adapts to accommodate growth

+ Fault-tolerance
  + Continuous operating properly in the presence of failure
  + Built-in redundancy of components

+ High Availability
  + High level of operational performance
  + Minimized downtime
  + No human infrastructure
 

## AWS Services
>> AWS offers a broad set of global cloud-based products that can be used as building blocks for common cloud architectures.

### COMPUTE
### Cloud providers offers a wide variety of compute services allowing you to develop, deploy, run, and scale your applications and workloads in the cloud. Some of the AWS Compute services include:
+ Amazon Elastic Compute Cloud (Amazon EC2) provides resizable compute capacity as virtual machines in the cloud.
+ Amazon EC2 Auto Scaling enables you to automatically add or remove EC2 instances according to conditions that you define.
+ Amazon Elastic Container Service (Amazon ECS) is a highly scalable, high-performance container orchestration service that supports Docker containers.
+ Amazon Elastic Container Registry (Amazon ECR) is a fully-managed Docker container registry that makes it easy for developers to store, manage, and deploy Docker container images.
+ AWS Elastic Beanstalk is a service for deploying and scaling web applications and services on familiar servers such as Apache and Microsoft Internet Information Services (IIS).
+ AWS Lambda enables you to run code without provisioning or managing servers. You pay only for the compute time that you consume. There is no charge when your code is not running.
+ Amazon Elastic Kubernetes Service (Amazon EKS) makes it easy to deploy, manage, and scale containerized applications that use Kubernetes on AWS.
+ AWS Fargate is a compute engine for Amazon ECS that allows you to run containers without having to manage servers or clusters.

### Storage
### Cloud providers offer a range of services for you to store, access, govern, and analyze your data to so you can reduce your costs, increase agility, and accelerate innovation. Some of the AWS Storage services include:
+ Amazon Simple Storage Service (Amazon S3) is an object storage service that offers scalability, data availability, security, and performance.
+ Amazon Elastic Block Store (Amazon EBS) is high-performance block storage that is designed for use with Amazon EC2 for both throughput and transaction intensive workloads
+ Amazon Elastic File System (Amazon EFS) provides a scalable, fully managed elastic Network File System (NFS) file system for use with AWS Cloud services and on-premises resources.
+ Amazon Simple Storage Service Glacier is a secure, durable, and extremely low-cost Amazon S3 cloud storage class for data archiving and long-term backup.rity, availability, performance, global coverage, and manageability.

### Database
### Cloud based managed database services support businesses by providing flexible and low cost database options with robust enterprise features. Some of the AWS Database services include:
+ Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups.
+ Amazon Aurora is a MySQL and PostgreSQL-compatible relational database. It is up to five times faster than standard MySQL databases and three times faster than standard PostgreSQL databases. 
+ Amazon Redshift enables you to run analytic queries against petabytes of data that is stored locally in Amazon Redshift, and directly against exabytes of data that are stored in Amazon S3. It delivers fast performance at any scale.
+ Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale, with built-in security, backup and restore, and in-memory caching.

### Network & Content Delivery
### Networks are the backbone cloud service providers use to deliver content and run workloads all around the globe. Some of the AWS Network & Content Delivery services include:
+ Amazon Virtual Private Cloud (Amazon VPC) enables you to provision logically isolated sections of the AWS Cloud.
+ Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and Lambda functions.
+ Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and application programming interfaces (APIs) to customers globally, with low latency and high transfer speeds.
+ AWS Transit Gateway is a service that enables customers to connect their Amazon Virtual Private Clouds (VPCs) and their on-premises networks to a single gateway.
+ Amazon Route 53 is a scalable cloud Domain Name System (DNS) web service designed to give you a reliable way to route end users to internet applications. It translates names (like www.example.com) into the numeric IP addresses (like 192.0.2.1) that computers use to connect to each other.
+ AWS Direct Connect provides a way to establish a dedicated private network connection from your data center or office to AWS, which can reduce network costs and increase bandwidth throughput.
+ AWS VPN provides a secure private tunnel from your network or device to the AWS global network.
