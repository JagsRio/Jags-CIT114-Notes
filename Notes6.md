# Amazon Compute Services
What I should know:

## Overview of different AWS Compute services in the cloud
+ Why to use Amazon Elastic Compute Cloud
+ Functionality in the EC2 Console
+ Perform basic functions in EC2 to build virtual computing environment.
+ Identify EC2 Cost optimization
+ When to use AWS Elastic Beanstalk
+ When to use AWS Lambda
+ How to run containerized applications in a cluster of managerd servers.

## AWS Compute Services
1. EC2 - provides resizable virtual machines
2. EC2 Auto Scaling - Application availablity
3. ECR Elastic Container Registry is used to store and retrieve Docker images
4. ECS Elastic Container Service is a container orchestration service that supports Docker
5. VMWare - Hybrid Cloud
6. AWS Elastic Beanstalk - provides a simple way to run and manage web applications
7. Lambda - serverless compute solution and you pay only for compute time you consume
8. Elastic Kubernetes Service - run managed Kubernetes on AWS
9. Many more...

## What to consider when using compute services:
What is the application design
What are the usage patterns
Which configuration settings you want to manage

Key choices when launching EC2 wizard:
1. AMI
2. Instance Typpe
3. Network settings
4. IAM role
5. User data
6. Storage options
7. Tags
8. Security group
9. Key pair

AMI
Amazon Machine Image is a template used to create an EC Instance (Windows or Linux)

Instance Type
Memory
CPU
Disk Space
Network performance
offers family, generation number, size

types/purpose | General Purpose | Computer Optimized | Memory Optimized | Accelerated Computing | Storage Optimized
Instance Types | a1, m4, m5, t2, t3 | c4, c5 | r4, r5, x1, z1 | f1, g3, g4, p2, p3 | d2, h1, i3
Use Case | Broad | High Performance | In-memory databases | Machine Learning | Distrubuted file Systems

Network settings
Identify the VPC and optionally the subnet
Should a public IP Address be automatically assigned?

IAM Role
Attach an appropriate IAM Role if the EC2 needs to interact with other AWS Services.

User data
User data scripts to customize the runtime environment of the instance.

Stoage options
Configure root volume
Attach additional storage volumes
Storage options
Elastic Block Store
	Durable block-level storage volumes
	Data will be available after stopping and starting the instance.
EC2 Instance Store
	Storage is provided on disk attached to the host computer of EC Instance.
	Data is lost after instance stops
Elastice File System and Simple Storage Service are other options for storage.

Tags
Tag is a label assigned to AWS resource consisting of key and value.
It is a way to attach metadata to an EC instance
Helps in Filtering, automation, cost allocation and access control

Security Groups
Security group is a set of firewall rules that control traffic to the instance.
It exists outside the instance's guest OS
Create rules and specify source and which ports to allow communications.

Key pair
A key pair consists of a public key and a private key
It enables secure connections to the instance
Windows AMI - use the private key to obtain the administrator password that you need to log in to your instance
Linux AMI - use the private key to use SSH to securely connect to your instance.

Every AWS account is allocated 5 elastic IP addresses
Instance metadata 
Amazon CloudWatch to monitor EC2 instances
	Basis monitoring - No cost and data sent every 5 minutes
	Detailed monitoring - Fixed monthly for 7 pre-selected metrics and sent every 1 minute

EC2 Cost Optinmization
On-Demand Instances
Dedicated Hosts
Dedicated Instances
Reserved Instances
Scheduled Reserved Instances
Spot Instances

Four pillars of cost optimization
Right size
Increase elasticity
Optimal pricing model
Optimize storage choices


