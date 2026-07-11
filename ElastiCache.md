![[Pasted image 20260708153457.png]]

The same concept with ElastiCache is applied to user session logins as well.

There are 3 patterns that can be used for ElastiCache:
- Lazy Loading
	- This is what is pictured above
- Write Through
	- Adds or update data in the cache when written to a DB so that there is no stale data
- Session Store
	- Store temporary session data in a cache (using TTL features)