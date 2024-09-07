# Cloud Economics and Billing

### The topics covered in this module: ###
+ Fundamentals of pricing
+ Total Cost of Ownership (TCO)
+ AWS organizations
+ AWS Billing and Cost Mgmt
+ Technical Support

*After completing the module you should be able to explain and recognize AWS pricing philosophy, indicate elements of total cost of ownership, know how to set up organizational structure and permissions and be able to explain the AWS billing dashboard Anf also explain the Technical Support and levels of suuport available for the customers*

## The top 3 main services driving the cost for AWS billing: ##
+ ### Compute ###
+ ### Storage ###
+ ### Data transfer outbound - no cost for inbound data transfer ###


### _AWS had maintained the same philosophy : Pay as you go, Pay less when you reserve, Pay even less when AWS grows. Pay only for services that you consume with no large upfront expenses and all services are available on demand_ ###

### Benefits of AWS ###
+ AWS Storage Services offers pricing depending on the frequency of the data access.
+ AWS focuses on lowering costs and improving operational efficiencies
+ Future high performing resources replace current slower resources for no extra charge

## Free Tier ##
### Amazon offers some services free for 1 year ###
+ 750 hours of Amazon EC2 Linux or RHEL or SLES t2.micro instance usage (1 GiB of memory and 32-bit and 64-bit platform support) – enough hours to run continuously each month
+ 750 hours of an Elastic Load Balancer plus 15 GB data processing
+ 750 hours of Amazon RDS Single-AZ Micro DB Instances, running MySQL, PostgreSQL, Oracle BYOL or SQL Server Express Edition – enough hours to run a DB Instance continuously each month. You also get 20 GB of database storage, 10 million I/Os and 20 GB of backup storage
+ 750 hours of Amazon ElastiCache Micro Cache Node usage – enough hours to run continuously each month
+ 30 GB of Amazon Elastic Block Storage in any combination of General Purpose (SSD) or Magnetic, plus 2 million I/Os (with EBS Magnetic) and 1 GB of snapshot storage
+ 5 GB of Amazon S3 standard storage, 20,000 Get Requests, and 2,000 Put Requests
+ 25 GB of Storage, 25 Units of Read Capacity and 25 Units of Write Capacity, enough to handle up to 200M requests per month with Amazon DynamoDB
+ 25 Amazon SimpleDB Machine Hours and 1 GB of Storage
+ 1,000 Amazon SWF workflow executions can be initiated for free. A total of 10,000 activity tasks, signals, timers and markers, and 30,000 workflow-days can also be used for free
+ 100,000 Requests of Amazon Simple Queue Service
+ 100,000 Requests, 100,000 HTTP notifications and 1,000 email notifications for Amazon Simple Notification Service
+ 10 Amazon Cloudwatch metrics, 10 alarms, and 1,000,000 API requests
+ 50 GB Data Transfer Out, 2,000,000 HTTP and HTTPS Requests for Amazon CloudFront

### Always Free Services
1. Virtual Private Cloud (VPC)
2. Auto-Scaling
3. Elastic Beanstalk
4. CloudFormation
5. Identity and Access Management (IAM)

## Total Cost of Ownership
### _Comparing on-premises and cloud computing_

| On-premises | Cloud |
|-------------|-------|
| Facilities  | Infrastructure is purchased from service provider |
| Hardware Equipment | No upfront costs |
| Licenses | Pay for what you use |
| Maintenance | Improves agility and faster time to market
| Scaling up takes time and is expensive | Scaling down saves resources |
| Scaling down does not reduce costs | scaling up is on demand |


> "By leveraging the security best practices of AWS, we’ve been able to eliminate a lot of compliance tasks that in the past took up valuable time and money.”
Brian Mercer, Senior Software Architect, Deleware North

## AWS Organizations
AWS Organizations is an account management service that enables you to consolidate multiple AWS accounts into an organization that you create and centrally manage. AWS Organizations includes account management and consolidated billing capabilities that enable you to better meet the budgetary, security, and compliance needs of your business. As an administrator of an organization, you can create accounts in your organization and invite existing accounts to join the organization.

### Steps to Create an Organization
1. Create your organizationLinks to an external site.: In this step, you create an organization with your current AWS account as the master account. You also invite one AWS account to join your organization, and you create a second account as a member account.
2. Create the organizational unitsLinks to an external site. Next, you create two organizational units (OUs) in your new organization and place the member accounts in those OUs.
3. Create the service control policies Links to an external site.You can apply restrictions to what actions can be delegated to users and roles in the member accounts by using service control policies (SCPs)Links to an external site.. In this step, you create two SCPs and attach them to the OUs in your organization.
4. Testing your organization's policiesLinks to an external site. You can sign in as users from each of the test accounts and see the effects that the SCPs have on the accounts.


## Billing and Cost Management
### The Billing and Cost Management service provides features that you can use to do the following:
+ Estimate and plan your AWS costs
+ Receive alerts if your costs exceed a threshold that you set
+ Assess your biggest investments in AWS resources
+ Simplify your accounting if you work with multiple AWS accounts
+ Important tools built into the Billing and Cost Management include:

### Most important parts of Billing and Cost Management in AWS
1. AWS Cost Explorer
2. AWS Budgets
3. AWS Cost and Usage Reports

## Technical Support
### -At AWS following support levels are available:_
+ Basic
+ Developer
+ Business
+ Enterprise support plans

### Save when you reserve - _this is a question in knowledge check_
For certain services like Amazon EC2 and Amazon RDS, you can invest in reserved capacity. With Reserved Instances, you can save up to 75% over equivalent on-demand capacity. When you buy Reserved Instances, the larger the upfront payment, the greater the discount. Reserved Instances are available in 3 options:
1. All Upfront Reserved Instance (AURI)
2. Partial Upfront Reserved Instance (PURI)
3. No Upfront Reserved Instance (NURI)
