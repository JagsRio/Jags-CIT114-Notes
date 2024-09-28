# Storage

## Amazon Elastic Block Store
> [!Note]
> Persistent storage is any data storage device that retains data after power to that device is shut off and also called non-volatile storage

+ Each EBS volume is automatically replicated within its availablity zone to protect you from component failure.
+ Designed for high availability and durability
+ EBS is also high scalable so you can scale up or down within minutes while paying a low price for only what you provision.

| Block storage | object storage |
| ---------------- | -------------- |
Change one block (piece of file) | Entire file must be updated |

Amazon EBS allows you to __create individual storage volumes__ and attach them to EC2 instances.
+ Offers block-level storage
+ Volumes are automatically replicated within its AZ
+ It can be backed up automatically to Amazon S3 by way of snapshots
+ Offers low latency
+ Uses include:
	+ Boot volumes and storage for EC2 instances
	+ Data storage with a file system
	+ Database hosts
	+ Enterprise applications

### Volume types
**Solid State Drives (SSD)**
| x/y | General Purpose | Provisioned IOPS |
| -------------------- | --------------- | ----------------- |
| Max Volume Size | 16 TiB | 16 TiB |
| Max IOPS/Volume | 16,000 | 64,000 |
| Max throughput/Vol | 250 MiB/s | 1000 MiB/s |

**Hard Disk Drives (HDD)**
| x/y | General Purpose | Provisioned IOPS |
| -------------------- | --------------- | ----------------- |
| Max Volume Size | 16 TiB | 16 TiB |
| Max IOPS/Volume | 500 | 250 |
| Max throughput/Vol | 500 MiB/s | 250 MiB/s |

### Snapshots:
+ Point-in-time snapshots
+ Recreate a new volume at any time

### Encryption:
+ Encrypted EBS volumes
+ No additional cost

### Elasticity:
+ Increase capacity
+ Change to different types

## Amazon Simple Storage Service (S3)
+ Object level storage
+ Data is stored as objects in buckets
+ Virtually unlimited storage
+ Single object is limited to 5 TB
+ Designed for 11 9s of durability
+ Granular access to buckets and objects
+ By default data is always private
+ Server-side encryption allows you to encrypt data at rest and in transit
+ Notifications on modification or deletion and linking to Lamda functions

### Amazon S3 storage classes
**Storage classes designed for different use cases**
1. **Amazon S3 standard**
	+ Designed for high availability, high durability and performance for frequently accessed data
	+ Low latency and high throughput
2. **Amazon S3 Intelligent-Tiering**
	+ Designed for data that is accessed less frequently but provides rapid access when needed
3. **Amazon S3 Standard-Infrequent Access**
	+ Designed for high durability, high throughut and low latency of S3 standard with a low per gigabyte storage and retrieval fee
	+ Useful for long-term storage and backups and datastore for disaster recovery files.
4. **Amazon S3 One Zone-Infrequent Access**
	+ Designed for data that is accessed less frequently but provides rapid access when needed
	+ Stored in a single AZ
	+ Good choice for storing secondary backup copies
5. **Amazon S3 Glacier**
	+ Secure and durable low cost storage class for data archiving
	+ 3 options to retrieve objects from minutes to hours
6. **Amazon S3 Glacier Deep Archive**
	+ Lowest cost storage class
	+ Long-term retention and digital preservation for data accessed once or twice a year
	+ Good for regulated industries like financial, healthcare and public sectors

## Amazon Elastic File System (Amazon EFS)
> [!Note]
> EFS implements storage for multiple EC2 instances that can access the storage at the same time.

### EFS Features
+ File storage in the AWS Cloud
+ Works well for big data and analytics, media and content management, web serving
+ Petabyte-scale, low latency system
+ Shared storage
+ Elastic capacity
+ Supports Network File System (NFS) 
+ Compatible with all linux-based AMIs for EC2

### EFS implementation steps
1. Create your EC2 resources and launch your EC2 instance
2. Create your EFS file system
3. Create your mount targets in the appropriae subnets
4. Connect your EC2 instances to the mount targets
5. Verify the resources and protection of your AWS account


## Amazon S3 Glacier
### S3 Glacier is a secure, durable and extremely low-cost service for data archiving and long-term backup.
+ S3 Glacier is designed to provide 11 9s of durability for objects
+ Supports encryption of data in transit and at rest through Secure Socket Layer (SSL) or Transport Layer Security (TLS)
+ Vault locak feature enforces compliance through a policy
+ Extremely low-cost design works well for long-term archiving

### Retrivel options:
+ Expedited : 1-5 minutes (Most expensive)
+ Standard : 3-5 hours (Less expensive)
+ Bulk : 5-12 hours (Least expensive)



