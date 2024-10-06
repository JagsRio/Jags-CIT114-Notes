# Cloud Architecture

## AWS Well-Architected Framework
AWS Well-Architected Framework provides a consistent set of best practice for customers to evaluate architectures, and also provides a set of questions to evaluate the architecture and its alignment to AWS's best practices.

## Six Pillars of AWS Well-Architected Framework
| Name | Description |
|------------------------------|-------------------------|
Operational Excellence | The ability to support development and run workloads effectively, gain insight into their operations, and to continuously improve supporting processes and procedures to deliver business value. 
Security | The security pillar describes how to take advantage of cloud technologies to protect data, systems, and assets in a way that can improve your security posture |
Reliability | The reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistently when it’s expected to |
Performance Efficiency | The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve
Cost Optimization | The ability to run systems to deliver business value at the lowest price point
Sustainability | The ability to continually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing the total resources required

### Common terms
+ Component
+ Workload
+ Architecture
+ Milestones
+ Technology portfolio

> "Everything Fails, all the time." - Werner Vogels, CTO, Amazon.com

> “Good intentions never work, you need good mechanisms to make anything happen” — Jeff Bezos. 

## General Design Principles
+ Stop guessing your capacity needs
+ Test systems at production scale
+ Automate to make architectural experimentation easier
+ Allow for evolutionary architectures
+ Drive architecturs using data
+ Improve through game days


## Six pillars of Framework
### 1. Operational Excellence
+ Design Principles
	+ Perform operations as code
	+ Make frequent, small reversible changes
	+ Refine operations procedures frequently
	+ Anticipate failure
	+ Learn from all operational failures
+ Definition
	+ Organization
	+ Prepare
	+ Operate
	+ Evolve

### 2. Security
+ Design Principles
	+ Implement a strong identity foundatin
	+ Enable traceability
	+ Apply security at all layers
	+ Automate security best practices
	+ Protect data in transit and at rest
	+ Keep people away from data
	+ Prepare for security events

+ Definition
	+ Security 
	+ Identity and Access Management 
	+ Detection 
	+ Infrastructure Protection 
	+ Data Protection 
	+ Incident Response 


### 3. Reliability
+ Design Principles
	+ Automatically recover from failure
	+ Test recovery procedures
	+ Scale horizontally to increase aggregate workload availability
	+ Stop guessing capacity
	+ Manage change in automation

+ Definition
	+ Foundations
	+ Workload Architecture 
	+ Change Management 
	+ Failure Management


### 4. Performance Efficiency
+ Design Principles
	+ Democratize advanced technologies
	+ Go global in minutes
	+ Use serverless architectures 
	+ Experiment more often
	+ Consider mechanical sympathy

+ Design
	+ Selection 
	+ Review 
	+ Monitoring 
	+ Tradeoffs


### 5. Cost Optimization
+ Design Principles
	+ Implement Cloud Financial Management
	+ Adopt a consumption model
	+ Measure overall efficiency
	+ Stop spending money on undifferentiated heavy lifting
	+ Analyze and attribute expenditure

+ Design
	+ Practice Cloud Financial Management 
	+ Expenditure and usage awareness 
	+ Cost-effective resources 
	+ Manage demand and supply resources 
	+ Optimize over time 


### 6. Sustainability
+ Design Principles
	+ Understand your impact
	+ Establish sustainability goals
	+ Maximize utilization
	+ Anticipate and adopt new, more efficient hardware and software offerings
	+ Use managed services
	+ Reduce the downstream impact of your cloud workloads

+ Design
	+ Region selection
	+ User behavior patterns
	+ Software and architecture patterns
	+ Data patterns
	+ Hardware patterns
	+ Development and deployment process 
