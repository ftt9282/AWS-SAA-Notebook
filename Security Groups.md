Security Groups are foundational to the network security in AWS. For simplicity, each security group only gives the capability to *allow* traffic rather than *deny*.

![[Pasted image 20260627174032.png]]

Some good things to know about Security Groups:
- They can be attached to multiple instances
- They are locked down to a region/VPC combination
- Since they live outside of the EC2, blocked traffic will never reach the EC2
- It's usually easier to maintain one separate security group for SSH access since SSH access can get confusing
- All inbound traffic is BLOCKED by default
- All outbound traffic is ALLOWED by default

Below are some ports we'll need to know for the exam:
[[Classic Ports To Know]]