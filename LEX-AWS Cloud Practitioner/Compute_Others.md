AWS LAMBDA
==========
- Serverless Computing Platform
- **Event-Driven Execution:** Lambda functions can be triggered by various events such as HTTP requests, changes in AWS services (like S3, DynamoDB), and custom events.
- Auto-Scaling
- Multi-Language Support: Lambda supports multiple programming languages including Node.js, Python, Java, Go, and more.
- Fully Managed Service: AWS manages the underlying infrastructure, including server provisioning, scaling, and maintenance.

AWS BATCH
=========
- Service to run batch computing workloads of any scale.
- It has all underlying infra.
- _Job_ : A unit of work submitted to batch
- _Job Definition_ : defines how job should run
- _Job Queue_ : where the job resides until it gets scheduled.

AWS LIGHTSAIL
==============
- More easier / lighter service to host apps
- Pre packaged hosting  offering **common launch configuration**
- We dont need to configure anything
- Easier than EC2, EBS etc
- Ideal for simple workloads, quick deployments and to start with AWS

AWS Outposts
=============
- An **on-premises** IT as a **service** (ITaaS) platform.
- Outposts, which acts as a **hybrid cloud**, allows users to host an environment similar to a public cloud on premise.
- To run Outposts, users will require **physical space,** power and a network to deploy Outpost **hardware on premise**. Users then can securely connect to an AWS Availability Zone over a VPN or AWS Direct Connect. Once everything is set up, users can log into the AWS Management Console, and configure and order their Outposts service. AWS will ship Outposts to the user, where they can then hook the service up, and view Outposts in the AWS Management Console.
- When used?
  During very specific use cases like,
  - you need super-low latency between AWS infra and prem equipment
  - you have very high data security or sovereignty requirements
