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

### Compute
+ Compute services help you make the most of your data. They support research and big data processing. AWS compute services cover virtual machines, containers, serverless computing, and more.

### Storage
+ AWS storage solutions provide reliable, scalable, and secure storage for backup, disaster recovery, and business continuity.

### Databases
+ aWS databases are built for different data models and use cases and offer speed, reliability, availability, and security.

### Networking
+ AWS networking and content delivery are designed to ensure that AWS has the networking capabilities required to run any workload in the cloud with security, availability, performance, global coverage, and manageability.
