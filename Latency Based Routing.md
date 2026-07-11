Latency Based Routing means that routing by [[Route 53]] will be executed with the latency of the client in mind. The client will be given whatever resource has the least amount of latency for them.

For example, if a user in Germany has the least amount of latency in the US, then they will be directed to a resource in the US. Latency is based on traffic between users and AWS regions.