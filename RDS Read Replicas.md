[[Relational Database Service|RDS]] can take advantage of what are called Read Replicas. Read Replicas are ASYNC replications of your RDS database that an application can read from if your application is running into issues with the number of reads being sent to RDS. Currently, you can have up to 15 Read Replicas at a time.

Since the replications are ASYNC, that means that writes to the main RDS database might not have time to replicate before another read is sent. That is why these replicas are described as "eventually consistent".

Replicas also have the neat ability to be promoted to their own full-fledged database if the administrator chooses to do so.

In order to get these replicas to work, the application that is reading from them must update their connection string to read from the replicas.

Normally there is a network cost fee when data goes from one AZ to another, but with Read Replicas, as long as RDS DB instance and the Read Replica are in the same region (with/without different AZs) then there will be no fee.