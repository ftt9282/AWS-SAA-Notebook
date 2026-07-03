Amazon Machine Image

An AMI is essentially the entire blueprint for an EC2 instance. What some folks will do is setup and configure one EC2 instance, create a custom AMI from that EC2 instance, and then copy that AMI do a bunch of other instances so that the setup is exactly the same.

EC2 instances can be launched from:
- A public AMI (like the ones provided by AWS)
- Your own AMI
- An AMI from AWS Marketplace (some companies create AMIs and then sell them)