SNI is a "newer" protocol the requires the client to indicate the hostname of the target server in the SSL handshake. This makes it possible for one web server to house multiple SSL certificates to server multiple websites.

SNI only works for [[Application Load Balancer]]s and [[Network Load Balancer]]s currently.