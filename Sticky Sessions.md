Stick Sessions can be enabled for the Classic Load Balancer, [[Application Load Balancer]], and [[Network Load Balancer]].

"Stickiness" refers to when client traffic is received by the [[Elastic Load Balancer]], the load balancer remembers that client via a [[Cookie|cookie]] and makes sure to route that users traffic through the same EC2 Instance

The use case for this is to make sure that the user doesn't lose their session data. There is potential downside, however. A user who is very active (very sticky) can bring imbalance to the load over the backend EC2 instances