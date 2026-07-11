Cross-Zone Load Balancing is a load balancing feature that will distribute traffic evenly across your EC2, regardless of how many EC2s are in each AZ.

For example, if `AZ_1` has 2 EC2 instances and `AZ_2` has 8 EC2 instances, the load balancers will still make it so that each EC2 will take on 10% of the traffic... rather than the 2 EC2s in `AZ_1` each getting 25% and the EC2s in `AZ_2` getting 6.25% each.

Cross-Zone Load Balancing is enabled by default for [[Application Load Balancer]]s and no additional charges are given for traffic that spans multiple AZs. Cross-Zone Load Balancing **IS NOT** enabled by default for [[Network Load Balancer]]s and [[Gateway Load Balancer]]s and you will be charged for traffic that spans multiple AZs.