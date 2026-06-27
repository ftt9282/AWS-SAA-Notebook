Identity and Access Management

A service in AWS that allows you to create [[Groups]] and [[Users]].
Groups and users can be assigned permissions via something called a [[Policy]].

IAM users are assigned passwords, and there a couple different options
- A regular password that can be changed directly by IAM user themselves, or managed by an administrator to be changed after a set amount of time
- [[Multi Factor Authentication]]

IAM can also assign [[Roles]] to services, as if the services were a user so that they can perform actions on your behalf.

IAM has a couple options for security tools:
- IAM Credentials Report
	- Gives a list of all your account's users and the status of their credentials
- IAM Access Advisor
	- Shows permissions granted to a user and when those services were last accessed