All S3 classes have a standard rate a high durability of 99.999999999% (11 9s). If you store 10,000,000 objects with Amazon S3, you can on average expect to incur a loss of a single object once every 10,000 years.

The Standard tier has the following storage option:

![[Pasted image 20260717141652.png]]

For data that is not frequently accessed, but requires rapid access when needed, there are the following options:

![[Pasted image 20260717141827.png]]

If you want to house data for archiving/backup purposes then a Glacier Storage class makes sense. There are different options depending on how quickly you want that data returned to you upon request.

![[Pasted image 20260717141940.png]]

If you want to have your objects automatically moved between various Access Tiers based on usage then you can use S3 Intelligent Tiering

![[Pasted image 20260717142123.png]]
