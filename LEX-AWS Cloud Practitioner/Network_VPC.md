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

Route Table
-----------

![alt text](https://github.com/akin-a/notes/blob/main/images/vpc8.PNG)

- When a VPC is created, a Route Table called as the Main Route Table gets created along with it.
- All the Subnets in a VPC are implicitly associated with this Main Route Table.
- The Route table comprises of a set of rules, called as routes that determine the flow of network traffic from your subnet. 
- Custom Route Tables can also be created. One Subnet can be associated with only a single Route Table.

![alt text](https://github.com/akin-a/notes/blob/main/images/vpc9.PNG)

- Every Route in the table has a destination and a target.
- The **Destination** is a CIDR range of IP address, which specifies where you want the traffic to go.
- Target specifies, either a gateway, a network interface, or connection through which to send the destination traffic, example an 
  Internet Gateway.
- For **communication within the VPC** a Local Route is added in the table by default as shown.
  Destination for this local route is the CIDR range of the VPC. Target is local.
  This route ensures that traffic which wants to reach a destination within the
- Subnets associated with this Route Table, will allow EC2 instances launched within them to communicate with each other because of this 
  local route.


