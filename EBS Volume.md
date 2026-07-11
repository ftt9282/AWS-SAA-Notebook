Elastic Block Store Volume

Think of this as a "network USB stick". It is a network drive that can be quickly attached/dethatched from an [[EC2]]. 

EBS Volumes are locked to an AZ. For example, if you create an EBS volume in us-east-1 you can only attach it to EC2 instances inside of us-east-1, and not us-east-2. 

EBS Volumes have a setting called "Delete on Termination" which makes it so that if an EC2 instance is terminated, the EBS Volume is also deleted. By default, the 'root' volume will be deleted from the EBS Volume, but you can change this in the settings.

If you need to move an EBS Volume to another AZ it can be done through an [[EBS Snapshot]].

![[Pasted image 20260704234103.png]]

Only gp3 / gp3 ([[General Purpose SSD]]) and io1 / io2 ([[Block Express SSD]]) can be used as boot volumes
