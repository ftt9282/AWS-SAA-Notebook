Allows for async replication for an [[S3]] bucket to either a different region (Cross-Region Replication) or the same region (Same-Region Replication). [[Versioning]] must be enabled in order for replication to work, and proper [[IAM]] permissions also need to be set.

If you enabled replication only new objects are replicated, and there is a setting called `Delete marker replication` which makes it so that objects deleted in the source bucket are also deleted in the replicated bucket. The deletion is done through the use of delete tags that are set when an object is delete. Please note that deleting only a version of an object is a 'permanent delete' and will not set a delete tag, therefore the version will not also automatically be deleted in the replica.



