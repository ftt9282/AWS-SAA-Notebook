Relational Database Service (RDS) is a managed DB service that uses SQL as a query language.

Since RDS is a managed service, AWS provides a ton of features:
- Provisioning and patching
- Continuous backups
- Monitoring dashboards
- Read replicas
- Multi AZ setup for disaster recovery
- Storage backed by [[Elastic Load Balancer|EBS]]
- etc...

RDS includes a feature called Storage Auto Scaling which will automatically detect when RDS is running out of free database storage. At that point it will scale your database storage up to whatever you've set for the maximum storage threshold.

#### Backups

Backups for RDS can either me automated or manual. For automated backups there is a full backup done every day during the backup window. Retention can be up to 35 days or you can disable backups by setting retention to 0.

Manual backups are DB snapshots that are manually triggered by the user. **Exam trick: To save cost with an RDS DB that you know won't be used for a while... just take a snapshot and remove the DB. Storage for a snapshot is a lot cheaper and when you're ready to use the DB again you can just restore**.