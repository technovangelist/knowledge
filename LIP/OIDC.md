# OIDC
OpenID Connect
https://openid.net/connect/
[OpenID Connect Whitepaper by PingIdentity](x-devonthink-item://A67FC39C-B1B4-49B4-A860-456A53F9CDBE)
- What is oidc?
	- Open ID Connect
	- open authentication protocol
	- simple layer ontop of oauth2.0
		- what is oauth2
			- provides authorization flows for web app, desktop and mobile
			- 
	- allows client to verify id of end user
- how is it relevant to us?

OIDC. Open ID Connect. You might have seen those letters as you navigate the web, but what does it mean. Well the first three letters are for OpenID. You may remember this as an early way to login to some of the web apps you used. But versions 1 and 2 of OpenID didn't get a lot of adoption. Version 3, or OpenID Connect, has gotten rid of the XML and custom message signature schema used and instead leverages OAuth 2 which uses TLS, and that is already in use on every client and server platform today. So what is Oauth 2?? Well OAuth is an authorization framework. Version 2 of OAuth came out around 2013 and simplified the flows quite a bit while also causing a little bit of Internet drama. OIDC wraps around that and provides authentication. OAuth on it's own doesn't really provide a standard method for a user to login and provide a password or other verification step. OIDC is what enables that authentication step. 

For Infra, we use OIDC providers to validate that you are who you say you are. There are quite a few steps involved with that and in the description below this video I will call out some great resources if you want to understand it in more detail. And we use OIDC and OAuth 2.0 throughout the solution to make sure you always have access. At a high level here is what happens:

Infra is made of a few key components. There is a CLI as well as a web UI. Then there is a server component that stores information in a database. You are going to have one server. Then for each cluster you want to connect to, there is a 'connector'.

First you use the CLI to login. When you do that, it gives you a choice depending on how infra has been configured. You might login locally or with an OIDC provider such as Okta. Oh, by the way, providers like Okta are often referred to as Identity Providers, or IdPs for short. So once you have verified your identity, the IdP sends a code back to the Infra CLI. That code, which is just a long string of alphanumeric characters, is then sent to the Infra server. The server then sends that to the IdP which says that that code was just generated for this specific user, lets say matt@example.com. And the IdP returns an access key which includes the user's ID and a secret. We store a hash of that secret in our database and then the key is sent to the CLI to use for the rest of the day. And since matt@example.com has been granted access to a number of clusters and we have just verified that you are matt@example.com, you now should see all the clusters you have access to in your kubeconfig files. When you use a tool such as kubectl to gain access to one of those clusters, it will check with the server to ensure you still have access. The server generates a JavaScript Web Token, or JWT, though its usually pronounced as JOT. That jot is sent over to the cluster and the connector on the cluster sees that the jot has been signed by the server so it can trust that you really have access. And now, assuming you have the access required to perform the action you ran, you will get the corresponding results. We will revalidate that you still have access every 5 minutes. That 5 minute interval is configurable, but if you increase the frequency, you may run into rate limits set by the IdP.