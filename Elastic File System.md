The Elastic File System is a network file system that can be attached to multiple EC2s, and the EC2s can be in multiple AZ.

The EFS solution is highly available, scalable, and *expensive*. It's about 3 times as expensive as a gp2, and it's pay per use.

Access control of the EFS is done via a [[Security Groups|security group]].