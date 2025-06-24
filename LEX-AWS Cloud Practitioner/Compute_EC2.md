EC2
===

What is EC2
-----------
- EC2 or Elastic Compute Cloud is a compute web service offered by AWS.
- It is an Infrastructure as a Service (IaaS) offered by AWS which provides secure, resizable compute capacity or server provisioning in the AWS cloud.
- Can be accessible via Web service console / CLI / programming language of choice using AWS SDKs.

Features:
---------
- Highly elastic
- 99.99% availability SLA
- Pay as you go pricing model

Capability of EC2 services
---------------------------
- The ability to launch EC2 instances or virtual machines with a customized operating environment known as **Amazon Machine Image** or AMI.
- Data in the EC2 instances are stored on virtual disks known as EBS volumes.
- EC2 allows to automatically scale our applications with the use of the **Autoscaling** feature.
- Traffic between multiple EC2 instances can be managed easily with the help of **Elastic load Balancer**.

Amazon Machine Image (AMI)
--------------------------
- Virtual machine (image)
- Read-only file system image that includes an operating system such as Linux or Windows and any additional software which is required
- AMI’s are region specific and every AMI has an AMI ID specific to that region.
- While selecting an AMI, the following considerations can be taken –
  - The Region where the EC2 instances will be launched.
  - The type of Operating system required.
  - The architecture, whether 32-bit or 64-bit is required.
  - The AMI provider.
  - and, any other additional software requirements.
- Ex. Amazon Linux 2, Amazon Linux AMI, Also Custom AMIs

EC2 instance types
------------------
- _General Purpose_ Instance : balance of compute, memory, networking.
  Ex: t2.micro, m5.large etc.,
- _Compute Optimized_ : For applications that require high performance processors, suited for workloads such as batch
  processing, scientific modeling and other compute intensive application.
  Ex: c6g.large, c5.large etc.,
- _Memory Optimized_ : memory intensive workloads such as real-time big data analytics, in-memory databases etc.
  Ex: r5.large, x1.16xlarge etc.,
- _Accelerated Computing_ Instance : These types of instances provide hardware acceleration with the use of GPUs and are suited for 
  workloads such as Machine or Deep learning, seismic analysis or workloads requiring high floating-point number calculations.
  Ex: p3.2xlarge, p2.xlarge, etc.,
- _Storage Optimized_ : suited for workloads such as NoSQL databases, data warehousing or workloads requiring high disk performance.
  Ex: i3.large, d2.xlarge etc.,
  
EC2 Instance Launch Types and Tenancy
-------------------------------------
### Launch Types ###

Based on how you want to pay for the EC2 Instances, there are different EC2 Instance Launch types
- _On-Demand Instance_  : Pay only for duration used, no long term commitment, suited for short term irregular work loads. 
- _Reserved Instance_  : For predictable long running workloads (like 1 or 3 years), upto 72% discount compared to on demand.
- _Spot Instance_       : Unused EC2 instances, purchased at very low cost, upto 09% discount compared to on demand.

### Tenancy ###

Based on the **tenancy of the underlying hardware** where the EC2 instances will be launched, there are 3 different launch types.
- _Shared_            : Default, underlying hardwares shared with other AWS customers, but EC2 instance is isolated.
- _Dedicated hosts_   : Entire physical server dedicated to an user, full visibility on sockets&physical cores, full control.
- _Dedicated Instance_: Entire physical server dedicated to an user but might be shared in same AWS account, no visibility on socket etc.

EC2 Instance storage
--------------------
### EBS Volumes ###

- Generally, this is the root device instance (except for some)
- Provides durable block level storage for EC2 instances.

### Instance storage Volumes ###

- Temporary block level storage
- Data is lost when the instance is stopped / restarted.

EC2 Placement Groups
--------------------
Default behaviour: Instance **spread across** the underlying **hardwares** in a single AZ. But there are other strategies also.
- _Cluster strategy_ : Hardwares tightly grouped in a single AZ, low latency issues._
- _Partition strategy_ : to spread instances across logical partitions such that groups of instances in one partition do not share the
underlying hardware with other groups
- _Spread strategy_ : strictly places a group of instances across distinct underlying hardware to reduce correlated failure.

EC2 Security Groups
--------------------
-  When an EC2 instance is launched, a **virtual firewall** called Security group envelopes the instance
-  This controls the _incoming and outgoing traffic_ using inbound and outbound rules.
-  It is **independent of the EC2** instance and part of **AWS VPC** infra.

EC2 Autoscaling
---------------
 Maintain high availability of app by Automatic scaling of the instances.
 
- Improves fault tolerance : Delete unhealthy instances
- lower cost : resources added only when its required

### Auto Scaling Groups (ASG) ###

- Logical collection of EC2 instance
- We can set _Minimum size_ (least number of EC2 instance), _Desired Capacity_ and _Maximum Size_ for a group.
- _Launch configuration_ : AMI ID, Instance type, key-pair, security group etc. (just like a ec2 instance configuration)
- **Launch Template** : Launch configuration  +  extra features   -> Launch template is the better one to create a ASG
- First we need to create a Launch Template, and with that we have to create an ASG.
- Types of scaling:
  - _Manual_ : Manual value for the size of auto scaling
  - _Dynamic_: Based on demand
  - _Scheduled_ : Scheduled for a particular day/time
    
Amazon Elastic Load Balancing (ELB)
------------------------------------
  A scalable solution from AWS which can automatically distribute traffic across multiple targets, such as EC2 Instances, containers, IP Addresses, and Lambda Function.
  - High Availability : Automatically distribute traffic across multiple targets.
  - E L B offers **health checks**, which can detect unhealthy targets, and stops sending traffic to them, for a consistent user experience.
  - Types of Load Balancer:
    - _Application Load Balancer_ : HTTP , HTTPs hosted web application
    - _Network Load Balancer_ : TCP and UDP traffic
    - _Gateway Load Balancer_ : Listens for all IP Packets.

Elastic Beanstalk (EBS)
=======================

Beanstalk make use of EC2 instances, Auto scaling, RDS, Load balancing etc, to _create an environment_ for the application to be deployed and run. Its a PaaS.

- Supports the apps developed on only JAVA, GoLang, Python, Node.js, Ruby, .NET, PHP
- Eg. Upload war file into EBS and configure everything to make it run.
- Features and Benefits:
  - Dev productivity
  - Complete Resource Control
  - Monitoring, Scaling, Deployment Options, Compliance.
- Concepts
  - Application
  - Application Version
  - Environment
  - Environment tier
  - Environment configuration
  - Saved configuration
    
