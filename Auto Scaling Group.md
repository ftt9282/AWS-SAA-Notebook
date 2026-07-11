An ASG allows you to scale in/out EC2 instances based on current load. It ensures that you have the necessary amount of EC2s running. The ASG is a free service, you only pay for the underlying EC2 instances.

With the ASG you set 3 parameters:
- Minimum Capacity
- Desired Capacity
- Maximum Capacity

The ASG is a smart service as it integrates with an [[Elastic Load Balancer]]. 

- When the ELB runs health checks and determines an EC2 within the ASG to be unhealthy, the ASG will automatically recreate that EC2
- Whenever the number of the EC2s changes within the ASG, the ELB will automatically distribute traffic based on the current count

ASGs are setup by creating what is called a **Launch Template**.

![[Pasted image 20260707114258.png]]

