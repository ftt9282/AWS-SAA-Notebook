A Multi AZ setup is typically used for disaster recovery with [[Relational Database Service|RDS]]

It uses SYNC replication, so all changes to the main RDS DB are immediately sent over to the standby RDS DB which is housed in a different AZ.

One DNS name is used, which means the application that is connecting to the main DB will automatically failover to the standby DB if connection to the main is lost.

It should be noted that Multi AZ is used for maximizing availably, and not used for scaling.

Technically if you wanted to you could setup a [[RDS Read Replicas|Read Replica]] and then use that as a form of Multi AZ for disaster recovery.

Bringing an RDS instance from a Single-AZ to a Multi-AZ is a very simple process that requires **zero** downtime operation. It's just a matter of going into the RDS settings and clicking "modify" to enable Multi AZ.