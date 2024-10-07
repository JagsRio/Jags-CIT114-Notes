Auto Scaling and Monitoring

Elastic Load Balancing
ELB must:
+ Distribute incoming application or network traffic across multiple targets in a single AZ or across multiple AZs
+ Scale your load balancer as traffic to your application changes over time.

Types of Load Balancer
Application Load Balancer | Network Load Balancer | Classic Load Balancer
------------------------------ | --------------------- | --------- |
Load balancing HTTP and HTTPS traffic | Load balancing of TCP, UDP and TLS traffic | Load balancing of HTTP, HTTPS, TCP and SSL traffic |
Routes traffic to targets based on content of request | Routes traffic to targets based on IP protocol data | Load balancing across multiple EC2 instances
Provides advanced request routing targeted at the delivery of modern application architectures | Can handle millions of requests per second with ultra-low latencies and optimized for sudden and volatile traffic patterns | |
Operates at the application layer (OSI Model layer 7) | Operates at the transport layer (OSI Model layer 4) | Operates at both the application and transport layers

AWS ELB use cases
Highly available and fault-tolerant applications
Cotainerized applications
Elasticity and scalability
VPS
Hybrid environments
Invoke Lamda functions over HTTP(s)

Load balancer monitoring
+ Amazon CloudWatch metrics
+ Access logs
+ AWS CloudTrail logs


Amazon CloudWatch

Monitoring AWS resources
+ How do you know when you should launch more EC2 instances?
+ Is your application's performance or availablity being affected by a lack of sufficient capacity?
+ How much of your infrastructure is actually being used?

CloudWatch:
+ Monitors
	+ AWS resources
	+ Applications that run on AWS
+ Collects and tracks
	+ Standard metrics
	+ Custom metrics
+ Alarms
	+ Send notifications to Amazon SNS topic
	+ Perform EC2 Auto Scaling or Amazon EC2 actions
+ Events
	+ Define rules to match changes in AWS environment and route these events to target functions or streams for processing
