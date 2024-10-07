# Auto Scaling and Monitoring

### How does load balancing work?
Load balancing is handled by a tool or application called a load balancer. A load balancer can be either hardware-based or software-based. Hardware load balancers require the installation of a dedicated load balancing device; software-based load balancers can run on a server, on a virtual machineLinks to an external site., or in the cloudLinks to an external site.. Content delivery networks (CDN)Links to an external site. often include load balancing features.

### Static load balancing algorithms
Static load balancing algorithms distribute workloads without taking into account the current state of the system. A static load balancer will not be aware of which servers are performing slowly and which servers are not being used enough. Instead it assigns workloads based on a predetermined plan. Static load balancing is quick to set up, but can result in inefficiencies.

### Dynamic load balancing algorithms
Dynamic load balancing algorithms take the current availability, workload, and health of each server into account. They can shift traffic from overburdened or poorly performing servers to underutilized servers, keeping the distribution even and efficient. However, dynamic load balancing is more difficult to configure. A number of different factors play into server availability: the health and overall capacity of each server, the size of the tasks being distributed, and so on.

There are several types of dynamic load balancing algorithms, including least connection, weighted least connection, resource-based, and geolocation-based load balancing.

## Elastic Load Balancing
### ELB must:
+ Distribute incoming application or network traffic across multiple targets in a single AZ or across multiple AZs
+ Scale your load balancer as traffic to your application changes over time.


## Types of Load Balancer
Application Load Balancer | Network Load Balancer | Classic Load Balancer
------------------------------ | --------------------- | --------- |
Load balancing HTTP and HTTPS traffic | Load balancing of TCP, UDP and TLS traffic | Load balancing of HTTP, HTTPS, TCP and SSL traffic |
Routes traffic to targets based on content of request | Routes traffic to targets based on IP protocol data | Load balancing across multiple EC2 instances
Provides advanced request routing targeted at the delivery of modern application architectures | Can handle millions of requests per second with ultra-low latencies and optimized for sudden and volatile traffic patterns | |
Operates at the application layer (OSI Model layer 7) | Operates at the transport layer (OSI Model layer 4) | Operates at both the application and transport layers

## AWS ELB use cases
+ Highly available and fault-tolerant applications
+ Cotainerized applications
+ Elasticity and scalability
+ VPS
+ Hybrid environments
+ Invoke Lamda functions over HTTP(s)

Load balancer monitoring
+ Amazon CloudWatch metrics
+ Access logs
+ AWS CloudTrail logs


## Amazon CloudWatch

### Monitoring AWS resources
+ How do you know when you should launch more EC2 instances?
+ Is your application's performance or availablity being affected by a lack of sufficient capacity?
+ How much of your infrastructure is actually being used?

### CloudWatch:
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


## EC2 Auto Scaling
Scaling is the ability to increase or decrease compute capacity of your application.

### EC2 Auto scaling :
+ Helps you maintain application availability
+ Enables you to automatically add or remove EC2 instances
+ Detect impaired EC2 instances and unhealthy applications and replacesthe instances automatically
+ Provides several scaling options - Manual, scheduled, dynamic or on-demand and predictive.

