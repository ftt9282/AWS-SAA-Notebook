Aurora is a proprietary technology from AWS, and it supports both Postgres and MySQL as an Aurora DB.

Aurora is AWS cloud optimized, and boasts as 5x performance improvement over MySQL on [[Relational Database Service|RDS]], and a 3x improvement over Postgres on RDS.

It scales automatically in increments of 10GN up to 256TB, and it can have up to 15 replicas. The replication process is also faster than MySQL.

All of this improvement comes at a cost, as Aurora is ~20% more expensive than RDS, but it is so much more efficient at scale that it is well worth it.

#### High Availability and Read Scaling

Anytime you write anything, Aurora stores 6 copies of your data across 3 AZs. Of that...
- 4 copies out of 6 are needed for writes
- 3 copies out of 6 are needed for reads
So you can still read/write even if one AZ goes down. There is also a cool self healing feature with peer-to-peer replication if Aurora senses that its data is corrupt. 

Aurora is similar to [[RDS Multi AZ]] since it has one main database that takes writes. If that main DB fails, the failover only takes 30 seconds. It can also have 15 read replicas serving reads. Finally, it has support for Cross Region Replication.

#### DB Cluster

The Aurora DB cluster is maintained by utilizing a **Writer Endpoint** and **Reader Endpoint**.

A Writer Endpoint is always pointing to the main DB, which in turn is pointed to the storage volume. If the main DB changes due a failover, the Write Endpoint changes with it.

One cool feature with read replicas associated with Aurora DB is that they're autoscaling, and can add/remove read replicas as needed. The client needs a way to keep up with the ever-changing read replicas, which is where the Reader Endpoint comes in. The Reader Endpoint connects to all of the current read replicas, and the client connects to the Reader Endpoint.

#### Backups

Backups for Aurora DB are automated, and on the same 1 to 35 day schedule as RDS. However, backups for Aurora cannot be disabled like they can with RDS. You can also trigger manual backups as well.

#### Cloning

In cases where you want to setup a staging (validation) environment of an Aurora DB, it is much easier to clone the DB rather than create a snapshot and restore a new DB from that snapshot. 

Aurora DB lets you clone a production DB using the *copy-on-write* protocol, which initially uses the same data volume as the original DB cluster