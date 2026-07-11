The Elastic Load Balancer (EBS) in AWS is a managed load balancer that is considered a "no brainer" when it comes to whether or not you should use it.

- AWS guarantees that it will be working
- AWS takes care of upgrades, maintenance, etc.
- Only a few configuration knobs are provided for EBS

It is more cost efficient and much easier to use EBS rather than setup your own load balancer, and it is integrated within many other AWS offerings.

Load balancing with EBS is maintained through various Health Checks that are sent out by EBS. A message is sent via a port/endpoint, and if the [[EC2]] does not respond with `200 OK` then that instance is considered "unhealthy" and stops being used for load balancing.

There are currently 4 main types of load balancers:
- Classic Load balancer (CLB)
	- Depreciated, used back in 2009
- [[Application Load Balancer]] (v2 - new gen - 2016)
	- Uses HTTP, HTTPS, WebSocket
- [[Network Load Balancer]] (v2 - new gen - 2017)
	- Uses TCP, TLS, UDP
- [[Gateway Load Balancer]] (2020)
	- Operates at Layer 3 (network protocol)

![[Pasted image 20260706141514.png]]

Above is an example of the [[Security Groups|security group]] setup for a load balancer. Traffic is allowed from anywhere into the load balancer, but for the EC2s traffic is limited to just the load balancer itself.