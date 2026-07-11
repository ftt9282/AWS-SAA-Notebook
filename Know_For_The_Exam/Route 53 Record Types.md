![[Pasted image 20260708201404.png]]

#### CNAME vs Alias

The Alias and CNAME record are fairly similar, but there is one major difference.

Both Alias and CNAME records point a hostname to any other hostname. For example, `app.mydomain.com => blabla.anything.com`. However, ONLY the Alias works for both ROOT domain and NON-ROOT domain. By that I mean, Alias works for both `app.mydomain.com` as well as `mydomain.com`.

An Alias can also have many different targets, but one thing that it can't target is an EC2 DNS name.