# Databases

### Databases offered by Amazon
1. Amazon Relational Database Service (RDS)
2. Amazon DynamoDB
3. Amazon Redshift
4. Amazon Aurora

> [!Note]
> Unmanaged - Scaling, fault tolerance and availability are managed by you

> [!Note]
> Managed - Scaling, fault tolerance and availability are typically built into the service

## Challenges of relational databases
+ Server maintenance and energy footprint
+ Software installation and patches
+ Database backups and high availability
+ Limits on scalability
+ Data Security
+ OS installation and patches

## Amazon RDS
1. Pick DB Instance Class
2. Pick DB Instance Storage
3. Pick Database Engine
4. Supported Engines:
	+ MySQL
	+ Amazon Aurora
	+ MS SQL Server
	+ PostgresSQL
	+ MariaDB
	+ Oracle

### Advantages of Amazon RDS
+ Amazon RDS can be deployed in a multi-AZs for high availability
+ It automatically generates a standby copy of the db instance in another availability zone within the same VPC
+ After initial seeding of the database copy, transactions are synchronously replicated to the standby copy
+ In event of failure of the primary AZ, Amazon automatically brings the standby DB instance online as the main instance.
+ Since applications reference the DB by name using the DNS domain endpoint, you dont need to change anything in your application code to use the standby copy.

### Amazon RDS also supports the creation of read replicas for MySQL, MariaDB, PostgresSQL and Amazon Aurora.
+ Offers asynchronous replication
+ Can be promoted to master if needed.
+ Use for read-heavy database workloads
+ Offload read queries


### When to use Amazon RDS
| Use Amazon RDS when you require | Do not use Amazon RDS when you require |
| -------------------------------- | -------------------------------------- |
| Complex transactions or complex queries | Massive read/write rates |
| Medium to high query or write rate - upto 30,000 IOPS | Sharding due to high data size or throughput demands |
| No more than a single worker node or shard | Simple GET or PUT requests and queries that a NoSQL Database can handle | 
| High Durability | RDBMS Customization |

Amazon DynamoDB
DynamoDB is a non-relational database

Relational DB versus Non-relational DB
| x/y | Relational (SQL) | Non-relational (NoSQL) |
| ---------------- | ------------------------ | ---------------- |
| Data Storage | Rows and Column | Key-value, document, graph |
| Schemas | Fixed | Dynamic |
| Querying | Uses SQL | Focuses on collection of documents |
| Scalanility | Vertical | Horizontal |

What is DynamoDB
+ Fast and flexible NoSQL database service
+ NoSQL database tables
+ Items can have differing attributes
+ Low-latency queries
+ Scalable read/write throughput
+ All data is stored in Solid State Drives (SSD)

Amazon Redshift
Redshift is a fast, fully managed data warehouse that makes it simple and cost-effective to analyze all your data by using standard SQL along with your existing business intelligence tools

Redshift use cases
+ Enterprise Data Warehouse (EDW)
	+ Migrate at a pace that customers are comfortable with
	+ Experiment without large upfront cost or commitment
	+ Respond faster to business needs
+ Big Data
	+ Low price point for small customers
	+ Managed service for ease of deployment and maintenance
	+ Focus more on data and less on database management
+ Software as a Service (SaaS)
	+ Scale the data warehouse capacity as demand grows
	+ Add analytic functionality to applications
	+ Reduce hardware and software costs

Amazon Aurora
+ Enterprise-class relational database
+ Compatible with MySQL or PostgreSQL
+ Automate time-consuming tasks

Aurora service benefits
+ Fast and available
+ Simple
+ Compatible
+ Pay-as-you-go
+ Managed service
+ Works seamlessly with AWS Database Migration Service
+ Works with AWS Schema Conversion Tool

Why use Aurora
+ High availability
+ Stores multiple copies of your data across different AZs
+ Data is backed up continuously to S3
+ You can use up to 15 read replicas with Aurora
+ Designed for instant crash recovery if your primary DB becomes unhealthy




