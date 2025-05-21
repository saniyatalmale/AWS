# AWS
AWS Cloud:
what is cloud computing ?
explain cloud service models ?
explain deployment models in cloud ?
explain IAM servise ?
explain policies in IAM ?
explain roles in IAM ?
diff roles and policies ?
explain ec2 service ?
explain instance types and perchasing options?
diff ami and snapshot ?
explain ebs volume types ?
explain concept of loadbalancing ?
diff ALB and NLB ?
explain autoscaling ?
explain s3 service and its advantages ?
diff s3 efs and ebs ?
explain s3 storage classes ?
what is lifecycle policy in s3 ?
explain vpc service ?
diff public and private subnet ?
explain nat ?
explain peering connection ?
diff nacl and sg ?
what is domain name ?
what is hosted zone ?
explain records in rt53 ?
explain routing policies ?
explain concept of ssl ?
explain CDN ?
what is edge location ?
explain OAC/OAI in cloudfront ?
what is latency?





# AWS Cloud Interview Questions & Answers

## 1. What is Cloud Computing?
Cloud computing means using services like servers, storage, and databases over the internet. You don't need to buy hardware – just use what you need and pay for it.

## 2. Cloud Service Models
- **IaaS**: You get virtual machines and storage (Example: EC2).
- **PaaS**: Platform to build and deploy apps (Example: Elastic Beanstalk).
- **SaaS**: Ready-to-use software over the internet (Example: Gmail).

## 3. Cloud Deployment Models
- **Public Cloud**: Services shared on the internet (Example: AWS).
- **Private Cloud**: Used by only one company.
- **Hybrid Cloud**: Mix of public and private.
- **Community Cloud**: Shared by similar organizations.

## 4. IAM (Identity and Access Management)
IAM helps control who can access your AWS resources. You can create users, groups, roles, and give them permissions.

## 5. IAM Policies
Policies are rules (written in JSON) that give or deny permissions. There are two types:
- **Managed Policies**: Created by AWS or you.
- **Inline Policies**: Directly attached to users, groups, or roles.

## 6. IAM Roles
Roles give temporary access to AWS resources. Common for EC2, Lambda, and cross-account access.

## 7. Difference: Roles vs Policies
- **Role**: Grants temporary access.
- **Policy**: Describes what actions are allowed.

## 8. EC2 (Elastic Compute Cloud)
EC2 lets you run virtual servers in AWS. You choose OS, instance type, and storage.

## 9. Instance Types & Purchasing Options
- **Types**: General (t2), Compute (c5), Memory (r5), Storage (i3)
- **Purchase**: On-demand, Reserved, Spot, Savings Plan

## 10. AMI vs Snapshot
- **AMI**: Used to launch EC2 (includes OS, apps)
- **Snapshot**: Backup of EBS volume

## 11. EBS Volume Types
- gp3/gp2: General SSD
- io1/io2: High-performance SSD
- st1: Big data HDD
- sc1: Cold storage HDD

## 12. Load Balancing
Distributes traffic across servers to keep apps available and reliable.

## 13. ALB vs NLB
- **ALB**: Works at HTTP level (Layer 7)
- **NLB**: Works at network level (Layer 4), faster

## 14. Auto Scaling
Automatically adds/removes EC2 based on traffic/load.

## 15. S3 (Simple Storage Service)
Stores files like images, videos, backups. Highly durable and scalable.

## 16. S3 vs EBS vs EFS
| Feature | S3 | EBS | EFS |
|--------|----|-----|-----|
| Type   | Object | Block | File |
| Use    | Backup | Attached to EC2 | Shared file system |
| Access | API/web | EC2 only | Multiple EC2s |

## 17. S3 Storage Classes
- Standard
- Infrequent Access (IA)
- Glacier
- Deep Archive
- Intelligent-Tiering

## 18. S3 Lifecycle Policy
Moves files to cheaper storage or deletes them after a set time.

## 19. VPC (Virtual Private Cloud)
Your private network in AWS. You control IPs, subnets, routes, and firewalls.

## 20. Public vs Private Subnet
- **Public**: Has internet access
- **Private**: No direct internet

## 21. NAT (Network Address Translation)
Lets private subnet instances access the internet securely.

## 22. VPC Peering
Connects two VPCs so they can talk to each other.

## 23. NACL vs Security Group
| Feature | NACL | Security Group |
|--------|------|----------------|
| Level  | Subnet | EC2 instance |
| Rules  | Allow/Deny | Only Allow |
| Type   | Stateless | Stateful |

## 24. Domain Name
Easy-to-remember website address like google.com.

## 25. Hosted Zone
A container in Route 53 for your domain’s DNS records.

## 26. Route 53 Records
- **A**: Domain to IP
- **CNAME**: One domain to another
- **MX**: Email server
- **TXT**: Text data

## 27. Routing Policies
- Simple
- Weighted
- Latency-based
- Failover
- Geolocation

## 28. SSL (Secure Socket Layer)
Encrypts data between browser and server (used in HTTPS).

## 29. CDN (Content Delivery Network)
Speeds up content delivery by caching data near users.

## 30. Edge Location
CDN server location closer to users to reduce delay.

## 31. OAI vs OAC
- **OAI**: Older method to secure S3 with CloudFront
- **OAC**: New IAM-based way to do the same with more features

## 32. Latency
Delay in data transfer. Lower latency = faster response.
