Provides control over where the EC2 instances are placed.

There are 3 main options:
- Cluster
	- Clusters EC2 into a single AZ which allows for the lowest latency
- Spread
	- Each EC2 instance is on a different hardware
	- Limited to 7 instances per AZ per placement group
- Partition
	- EC2s are placed inside of partitions, which can be represented by a "rack" in AWS
	- Up to 7 partitions per AZ
	- Partitions can span across multiple AZs