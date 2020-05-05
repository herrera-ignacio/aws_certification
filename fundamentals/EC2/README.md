# EC2 - Elastic Cloud Computing

![ec2](./ec2.png)

#### Must know

* Security Groups & Best practices
* Private vs Public IP (IPv4)
* Static vs Elastic IP
* EC2 User Data
* AMIs
* Launch types
* Pricing
* Instances overview
* Basic How To Do(s)

#### Basic Cloud Architecture Overview

* __EC2__: Renting virtual machines
* __EBS__: Storing data on virtual drives
* __ELB__: Distributing load across machines
* __ASG__: Scaling the services

## Security Groups

![security groups](./ec2-sg.png)

Control how traffic is allowed into or out our EC2 Machines. It's a fundamental skill to troubleshoot networking issues.

* Access to ports
* Authorised IP ranges - IPv4 and IPv6
* Control of Inbound network (other to instance)
* Control of Outbound network (instance to other)

![sg in-depth](./ec2-sg-2.png)

#### Example configuration

![sg example](./sg-example.png)

## Security Groups - Best Practices

* Can be attached to multiple instances
* Locked down to region / VPC
* Lives “_outside_” EC2 - instance won’t see blocked traffic
* It’s good to maintain one separate security group for SSH
* Application not accessible (timeout) means security group issue
* Application “connection refused” means application error or not launched
* All inbound traffic is blocked by default
* All outbound traffic is authorized by default
* Can reference to other security groups

![sg best practices](./sg-best-practices.png)
