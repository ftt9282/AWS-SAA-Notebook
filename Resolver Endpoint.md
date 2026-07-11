In [[Route 53]] the default behavior for the Resolver Endpoint is to answer DNS queries for:
- Local domain names for EC2 instances
- Records in Private Hosted Zones
- Records in public Name Servers

However, it's possible to have a hybrid setup where the Resolver Endpoint resolves DNS queries from other DNS resolvers.

![[Pasted image 20260710140307.png]]

The diagram above shows the process for an *inbound* resolver, but the same concept applies for an *outbound* resolver as well, just reversed.