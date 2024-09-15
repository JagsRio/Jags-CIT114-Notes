# AWS Security
### Cybersecurity best practices
- Keep software up to date
- Run up-to-date antivirus software
- enforce strong password
- Disable or remove default usernames & passwords
- Implement MFA authentication (MFA)
- Install and configure firewalls
- Be aware of phising emails

## AIC Triad
### Availability
- Always at your fingertips
- Redundancy
- Fault tolerance
- Patching

### Integrity
- Data is stored and transferred as intended
- Hashing
- Digital Signatures
- Certificates

### Confidentiality
- Encryption
- Access controls
- Steganography




> ## _Security should be the first and most important conversation regarding any IT implementation_

## Shared Responsibility Model
### Customer
+ Responsible for Security IN the cloud
	- Platform, Applications and IAM
	- OS, Networking and Firewall Configuration
	- Client-side data encryption & data integrity authentication
	- Server-side encryption
	- Network traffic protection


### AWS
+ Responsible for Security OF the cloud
	- Software : Compute, Storage, Database & Networking
	- Hardware : Regions, AZs and Edge locations


## AWS Best Practices for Security, Identity & Compliance
- IAM
- Data Protection & Privacy
- Infrastructure Protection
- Compliance
- Detection
Incident Investigating & Response


## Identity & Access Management (IAM)
***AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources for your users. You use IAM to control who can use your AWS resources (authentication) and what resources they can use and in what ways (authorization).***

1. A request is made to IAM to access a service.
2. IAM checks if permission to the service is explicitly denied.
	1. If yes, the request is denied and process ends
	2. If no, the request moves to the next check
3. IAM then checks if permission is explicitly allowed.
	1. If yes, the request is allowed and the request continues to the service
	2. If no, the request receives an implicit deny and the process ends

## Why should I use IAM
1. Granular permissions
2. Secure access to AWS resources for applications that run on Amazon EC2
3. Multi-factor authentication (MFA)
4. Identity federation
5. Identity information for assurance
6. PCI (Payment Card Industry) Compliance
7. DSS (Data Security Standard) Compliance
8. Eventually consistent
9. Free to use

## Elements of IAM
### IAM User
- An IAM user is a person or application that is defined in an AWS account, and that must make API calls to AWS products
- An IAM User can be assigned either
- Programmatic Access via CLI or SDK
- AWS Management Console

### IAM Group
- An IAM Group is a collection of IAM Users.
- A group can contain many users and a single user can belong to multiple groups
- Groups cannot be nested

### IAM Policy
- An IAM policy is a document that defines permissions to determine what users can do in the AWS account.
- There are 2 types of policies:
	- Identity-based policies
	- Resource-based policies

### IAM Role
- An IAM Role is a tool for granting temporary access to specific AWS resources in an AWS account. 

## Creating IAM User
Before you create an IAM user, you should secure your root account. It is a best practice to not use the root account unless absolutely necessary.

Only the root user can:
- Update the Account Root password
- Change AWS Support Plan
- Restore IAM user Permissions
- Change Account settings

## Steps to Secure a Root Account
1. As the account root user, secure your root account by doing the following:
2. Enable multi-factor authentication (MFA)
3. Enable a password policy for all users
4. Use CloudTrail to track user activity
5. Enable a billing report such as the AWS Cost and Usage Report
6. Store your account root credentials in a secure place
7. Create an administrator IAM Administrator User, see full steps below
8. Verify you can login as that IAM user in a separate browser
9. Disable and remove your account root access keys, if they exist
10. Sign out of your root account and use the IAM account, unless absolutely necessary

## Securing Data
- Data at Rest
- Data inTransit
- Securing S3 buckets
