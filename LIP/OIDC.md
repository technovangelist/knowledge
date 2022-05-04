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

OIDC. Open ID Connect. You might have seen those letters as you navigate the web, but what does it mean. Well the first three letters are for OpenID. You may remember this as an early way to login to some of the web apps you used. But versions 1 and 2 of OpenID didn't get a lot of adoption. Version 3, or OpenID Connect, has gotten rid of the XML and custom message signature schema used and instead leverages OAuth 2 which uses TLS, and that is already in use on every client and server platform today. So what is Oauth 2?? Well OAuth is an authorization framework. Version 2 of OAuth came out around 2013 and simplified the flows quite a bit while causing a little bit of Internet drama. 