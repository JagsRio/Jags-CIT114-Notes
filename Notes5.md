# Networking and Content Delivery

### Topics in networking & content delivery
1. Networking basics
2. Amazon VPC (Virtual Private Cloud)
3. VPC networking
4. VPC security
5. Amazon Route 53
6. Amazon CloudFront

## Networking
### Basic Networking
+ A computer network is two or more machines that are connected together in order to communicate.
+ Networking can be logically divided into subnets.
+ Networking requires a networking device like a router or switch

### IP (Internet Protocal) Address
+ It is unique
+ Expressed as four decimal numbers separated by dots
+ Each number has 8 bits (0 to 255)
+ Combined total of the four numbers is 32 bits in binary format
+ 32 bit address is called IPv4 
+ IPv6 addresses also exist and use 128 bits.
+ IPv6 address is composed of eight groups of 4 letters and numbers separated by colons.
+ Each group has 16 bits (o to ffff)

### Classless Inter-Domain Routing (CIDR)
192.0.2.0/24
24 represents how many bits are fixed
192.0.0.[0 to 255]
CIDR is a way to express a group of IP addresses that consecutive to each other.

## OSI Model (7 layers)
| Layer | Number | Function | Protocol/Address |
| --------- | ----------- | ------------------ | ---------------------------|
Application | 7 | Means for an application to access a netwrk | HTTP(S), FTP,DHCP, LDAP |
Presentaion | 6 | Ensures that the application layer can read & encryption | ASCI, ICA |
Session | 5 | Enables orderly exchange of data | NetBIOS, RPC
Transport | 4 | Provides protocols to support host-to-host communication | TCP, UDP
Network | 3 | Routing and packet forwarding (routers) | IP
Data Link | 2 | Transfer data in the same LAN network (hubs and switches) | MAC
Physical | 1 | Transmission and reception of raw bitstreams over a physical medium | Signals (1s and 0s)

## Amazon VPC
+ Logically isolates section of the AWS Cloud where you can launch AWS resources in a virtual network defined by you.
+ Provides control over your virtual networking resources including:
	+ Selection of IP Address range
	+ Creation of subnets
	+ Configure route tables and network gateways.
+ Allows you to customize the network configuration for your VPC
+ Allows you to use multiple layers of security

### VPCs and Subnets
**VPCs:**
+ Logically isolated from other VPCs
+ Dedicated to your AWS account
+ Belong to single AWS region but can span multiple AZs

**Subnets:**
+ Range of IP Addresses that divide an VPC
+ Belong to a single AZ
+ Classified as public or private

**IP Addressing:**
1. When you create a VPC, you assign it to an IPv4 CIDR block (Private IP Addresses)
2. You cannot change the address range after you create the VPC
3. The **LARGEST** IPv4 CIDR block size is /16  (65,536 addresses)
4. The **SMALLEST** IPv4 CIDR block size is /28 (16 addresses)
5. IPv6 is also supported
6. CIDR blocks of subnets cannot overlap

**Reserved IP Addresses**
> AWS reserves 5 IP addresses in each subnet

CIDR Block 10.0.0.0/24 | Reserved for |
---------------------- | ------------- |
10.0.0.0 | Network address |
10.0.0.1 | Internal communication |
10.0.0.2 | DNS resolution |
10.0.0.3 | Future use |
10.0.0.255 | Network broadcast |

**Public IP Addresses**
+ Manually assigned through an Elastic IP Address
+ Automatically assigned through auto-assign at the subnet level

**Elastic IP Addresses**
+ Associated with an AWS Account
+ Can be allocated and remapped anytime
+ Additional costs may apply
> [!Note]
> With an elastic IP Address, you can mask the failure of an instance by rapidly remapping the address to another instance in your VPC

> [!Tip]
> Associating the Elastic IP Address with the network interface has an advantage over associating directly with an instance.

> **Each instance in your VPS has a default network interface that is assigned a private IPv4 address from the IPv4 address range of your VPC. You cannot detach a primary network interface of an instance but can add other network interface to an instant.**

**Route tables and routes**
+ A route table contains a set of rules that you can configure to direct network traffic from your subnet.
+ Each route specifies a destination and a target
+ By default, every route table contains a local route for communcation wihin the VPC
+ Each subnet must be associated with a route table.

> [!Tip]
> A subnet can be associated with only one route table at a time, but you can associate multiple subnets to the same route table. Subnets and route table have a one-to-one mapping even though you can map one route table to multiple subnets.

## VPC Security
**Security Groups**
+ A security group acts as a virtual firewall that controls inbound and outbound traffic, to and from your instance.
+ Security groups acts at the instance level, at the network interface card.
+ Assign each instance in your VPC to a different set of security groups.

**__Security groups have rules to manage instance traffic__**

**__By default, security groups are sealed shut to inbound traffic.__**

**__Security groups are stateful__**

**__The outbound traffic is always allowed__**

**Network Access Control lists (Network ACLs)**
+ Network ACLs act at the subnet level
+ Setup ACLs with rules that allow or deny
+ Additionally you can specify ports and protocols

Each subnet in your VPC must be associated with a network ACL
ACL has separae inbound and outbound rules. 
Each rule can either allow or deny traffic
Default ACLs allow all inbound and outbound IPv4 traffic
Network ACLs are stateless.

Security Groups versus Network ACLs
Attribute | Security Groups | Network ACLs |
-------------- | ----------- | ------------------------ | 
Scope  | Instance level | Subnet level | 
Supported rules | Allow rules only | Allow and deny rules | 
State | Stateful (return traffic is automatically allowed) | Stateless (return traffic must be explicitly allowed by rules) | 
Order of Rules | All rules are evaluated before decision to allow traffic | Rules are evaluated in number order before decision to allow traffic

Amazon Route 53
Domain Name System
DNS resolution is the process of translating an internal name to the corresponding IP address

Route 53:
+ Highly available and scalable DNS web service
+ Fully compliant with IPv4 and IPv6
+ Connects user requests to infrastructure running in AWS and also outside of AWS
+ Can be used to check the health of your resources
+ Features traffic flow
+ Allows you to register domain names

Route 53 supported routing
Simple routing - single-server environment
Weighted routing - Assign weights to resource record sets to specify frequency
Latency routing - Improve your global applications
Geolocation routing - Route traffic based on location of your users
Geoproximity routing - Route traffic based on location of your resources
Failover routing - Fail over to a backup site if your primary site becomes unreachable.
Multivalue answer routing - Respond to DNS queries with up to eight healthy records selected at random.

Amazon CloudFront
Fast, global and secure CDN service
Global network of edge locations and Regional edge caches
Self-service model
Pay-as-you-go pricing
