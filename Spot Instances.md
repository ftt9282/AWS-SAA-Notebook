Spot Instances differ compared to other instances because new spot instances are handled via a Spot Request. A Spot Request will always try and generate a number of instances specified by the user, and if a Spot Instance is stopped it will automatically create a new one.

Cancelling a Spot Request DOES NOT terminate a Spot Instance. The Spot Instance still needs to be manually terminated, and in order to terminate a Spot Instance you have to first cancel the Spot Request.

Spot Instances can be group together in what is called a [[Spot Fleet]].