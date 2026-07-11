All Amazon [[S3]] objects have what's called a **key**. The key is essentially the full path to the object.

![[Pasted image 20260711005848.png]]

Even though this looks like a directory path, there is no concept of "directories" within buckets.

Object values have a max size of 50TB, and if you upload anything that is more than 5GB you'll need to use a "multi-part upload" which will upload your file in increments of 5GB.