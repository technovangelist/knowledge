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

First you use the CLI to login. When you do that, it gives you a choice depending on how infra has been configured. You might login locally or with an OIDC provider such as Okta. Oh, by the way, providers such as Okta are often referred to as Identity Providers, or IdPs for short. So once you have verified your identity, the IdP sends a code back to the Infra CLI. That code, which is just a long string of alphanumeric characters, is then sent to the Infra server. The server then sends that to the IdP which says that that code was just generated for this specific user, lets say matt@example.com. And the IdP returns an access key which includes the user's ID and a secret. We store a hash of that secret in our database and then the key is sent to the CLI to use for the rest of the day. 