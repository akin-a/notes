Amazon VPC
==========

- one of the foundational services offered by AWS.
- It allows you to launch AWS resources in a **logically isolated network** which **you can define and control**.

![alt text](https://github.com/akin-a/notes/blob/main/images/VPC1.PNG)

Components of VPC
-----------------

![alt text](https://github.com/akin-a/notes/blob/main/images/vpc2.PNG)

- VPC’s are associated with a Private CIDR range of either an IPv4 address or IPv6.
- VPC’s are divided into sub-networks or subnets, which spans across an Availability Zone in the region.
- Each subnet has its own CIDR IP range which is a **subset of the VPC** CIDR range.
- Instances are launched into any one of the subnets and are allocated a Private within the IP range of the subnet.
- VPC’s have a **router** and a **route table** attached to the subnets, which allows to control the** flow of traffic** based on the **routing rules** defined.
- Since VPC’s are private networks, to enable access to the Internet, an Internet Gateway is attached to the VPC.
- VPC’s have Network Access Control Lists or NACLs at the subnet level to control the Inbound and Outbound traffic to them.

VPC and Subnets
---------------
![alt text](https://github.com/akin-a/notes/blob/main/images/vpc3.PNG)
![alt text](https://github.com/akin-a/notes/blob/main/images/vpc4.PNG)
![alt text](https://github.com/akin-a/notes/blob/main/images/vpc5.PNG)
![alt text](https://github.com/akin-a/notes/blob/main/images/VPC6.PNG)
![alt text](https://github.com/akin-a/notes/blob/main/images/vpc7.PNG)



