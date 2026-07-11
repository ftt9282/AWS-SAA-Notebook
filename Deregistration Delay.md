This is the delay that the [[Elastic Load Balancer]] gives to an EC2 instance that has been deemed "unhealthy". 

Existing connections will remain for a specified amount of time, and new requests will cease. The default delay time is 300 seconds, but this can be anywhere from 1 to 3600 seconds.

If your requests are short it's better to also set the delay time to be short. However, if your users are needing to do something like upload large files, it's best to have the delay time be longer so as to not interrupt them.