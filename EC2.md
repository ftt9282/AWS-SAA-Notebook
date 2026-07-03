Elastic Compute Cloud = Infrastructure as a Service

Allows for the renting of virtual machines (EC2), storing data on virtual drives (EBS), distributing load across machines (ELB), and scaling the services using an auto-scaling group (ASG)

It's possible to automate the setup of EC2 instances using bootstrapping contained in the [[EC2 User Data]] file.

EC2 Instances come in different kinds of flavors, and each type is built for a different purpose in AWS.

- **General Purpose**
	- Great for a diversity of workloads like web servers or code repositories
		- Compute, Memory, Networking
		- t-series and m-series EC2 instances
- **Compute Optimized**
	- For intensive tasks that require high performance
	- C-series
- **Memory Optimized**
	- For workloads that process large amounts of datasets in memory
	- R, X, and z-series
- **Storage Optimized**
	- Great for storage intensive tasks
	- NoSQL and Relational Databases
	- I, D, or H1-series

EC2 Instance can have [[Security Groups]] attached to them which acts as a "firewall" for IPs / protocols wanting access to/from the EC2

EC2 Instances have the following purchasing options:
- **On-Demand Instances**
	- What we've seen so far in this course. You can spin up an instance with no upfront fee and then use it for as long as you want while paying by the second
- **Reserved (1 & 3 years)**
	- Used for longer workloads. The extended reservation provides a discount compared to things like the On-Demand instance pricing
- **Savings Plan**
	- Same savings as the Reserved instances, but with these you commit to a certain amount of usage and you're locked to a specific instance family / region
- **[[Spot Instances]]**
	- Provides the MOST discount (up to 90%) compared to the other plans, but at any moment you can lose your instance if your max price is less than the current spot price
	- Not recommended for critical jobs or databases
- **Dedicated Host**
	- A physical server with EC2 instance capacity fully dedicated to your use
- **Dedicated Instance**
	- Instances run on hardware dedicated to you, but you may share that hardware with other instances int he same account

[[Placement Groups]] provide additional control over the EC2 instances that you spin up

EC2s have the ability to go into Hibernation Mode, which utilizes the RAM on the EC2 to save the state before it goes into hibernation.