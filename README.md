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



# AWS Placement Groups (हिंदी + English)

## 🔸 What is a Placement Group? (Placement Group क्या है?)

**English:**  
A Placement Group in AWS is used to place EC2 instances in a specific way for better performance or high availability.

**Hindi:**  
AWS में Placement Group का उपयोग EC2 instances को एक खास तरीके से रखने के लिए किया जाता है ताकि performance बेहतर हो या system ज़्यादा सुरक्षित रहे।

---

## 🔹 Types of Placement Groups (Placement Group के प्रकार)

### 1. ✅ Cluster Placement Group

**English:**  
- All EC2 instances are placed very close to each other.
- Best for fast communication, low latency, high speed.
- Used for Big Data, gaming, HPC.
- **Limitation:** All are in one zone — if it fails, all are affected.

**Hindi:**  
- सभी instances को बहुत पास-पास रखा जाता है।
- तेज़ स्पीड और कम देरी (low latency) मिलती है।
- उपयोग: Big Data, Gaming, HPC जैसे कामों में।
- **कमज़ोरी:** एक ही ज़ोन में होते हैं — एक ज़ोन डाउन हुआ तो सब बंद हो सकते हैं।

---

### 2. ✅ Spread Placement Group

**English:**  
- Each EC2 instance is placed on different hardware.
- Best for critical applications — more protection.
- **Limit:** Max 7 instances per AZ.

**Hindi:**  
- हर instance को अलग-अलग server पर रखा जाता है।
- ज़्यादा सुरक्षा मिलती है — एक failure का असर बाकी पर नहीं पड़ता।
- **सीमा:** एक Availability Zone में केवल 7 instances रख सकते हैं।

---

### 3. ✅ Partition Placement Group

**English:**  
- Instances are divided into groups (called partitions), each placed on separate racks.
- Best for big data systems like Hadoop, Kafka.
- Helps in fault isolation.

**Hindi:**  
- Instances को group (partition) में बांटा जाता है, हर group अलग hardware (rack) पर होता है।
- बड़े systems (Hadoop, Kafka) के लिए बेहतर।
- Fault isolate करने में मदद मिलती है।

---

## 🔸 Easy Summary Table (सरल सारांश तालिका)

| Type       | Placement Style (कैसे रखे जाते हैं) | Use Case (उपयोग)            |
|------------|-------------------------------------|------------------------------|
| Cluster    | Close together (पास-पास)            | High speed, low latency work |
| Spread     | Far apart (दूर-दूर)                 | High availability, safety    |
| Partition  | Grouped (ग्रुप में, अलग-अलग)        | Big data, fault isolation    |

---

Let me know if you want me to save and download this `.md` file for you!
