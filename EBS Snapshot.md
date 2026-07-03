Makes a copy of your [[EBS Volume]] at a certain point, which you can then move into a different AZ and attach to an EC2

EBS Snapshots can be stored in an EBS Archive to save on cost, but if you want to restore from an EBS Snapshot it takes 24-72 hours for the restore to run.

A recycle bin can also be configured for EBS Snapshots that would help prevent accidental deletion. The retention rate for the recycle bin can be set from 1 day to 1 year.

Finally, there is a Fast Snapshot Restore (FSR) that forces a full initialization to have no latency on first use. This is quick, but also expensive.