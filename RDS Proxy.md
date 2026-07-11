RDS Proxy is a fully managed proxy for [[Relational Database Service|RDS]]. It sits in front of an RDS database and acts as a connection pool. Rather than connecting directly to the RDS database, apps with instead connect to the RDS Proxy.

- Improves DB efficiency and minimizes open connections (and timeouts)
- Reduces RDS and [[Aurora]] failover time by up to 66%
- Can enforce IAM authentication for the DB
- RDS Proxy is never publicly accessible (can only go through VPC)