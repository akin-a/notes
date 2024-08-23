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

