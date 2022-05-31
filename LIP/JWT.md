JSON Web Token
JWT
Pronounced JOT
jwt.io



Outline


Script
JWT. JSON Web Token. But it's usually pronounced as jot. if you hear someone talk about a jot, it might actually be a JSON Web Token. what is a json web token...i mean jot. It's simply a way to share some fact between services in a verifiable way. The actual RFC for jots says that it is a compact, url-safe means of representing claims to be transferred between two parties and that the claim can be digitally signed. A claim is any 'piece of information' about a subject.  And URL-Safe just means using any characters that are allowed in any URI. 

If you look around the web for information about JWT, you will find a lot of articles and videos that explain how to use them, along with a bunch like these that say they are terrible and no one should ever use them. The folks who say they are terrible, are mostly focused on one use-case, and two implementation details. The use case they are against is that of browser to service authentication, and mostly because, by default, the data in a jot in unencrypted and has no real expiration date. You can encrypt the data and set short expiration times, but that complicates things and by the time you do all that, there are other solutions such as session tokens that may be more appropriate. 

Infra uses jots for a different purpose and sets a short expiration time. In the video about OIDC, you saw that we use jots to record the claim of what this user's email address is and what groups they belong to. That on its own does not guarantee access to resources since the destination determines what access that user or group should have at run time. The digital signature on the claim allows the client and the destination to be confident that the user is who they claim to be and the groups are the groups they do in fact belong to. Let's take a look at one of these jots. First the raw jot looks like this. 
(((show on screen eyJhbGciOiJFZERTQSIsImtpZCI6InFBQ1NCdndib0Y1djU0S0RPRGlDY2xTMk0ybVRFeGNnTVl5VzBsZ2w3Zjg9IiwidHlwIjoiSldUIn0.eyJleHAiOjE2NTI5NjY2MzAsImdyb3VwcyI6bnVsbCwiaWF0IjoxNjUyOTY2MzMwLCJuYW1lIjoiYWRtaW4iLCJuYmYiOjE2NTI5NjYwMzAsIm5vbmNlIjoiQW1IVXBKOVc4NSJ9.66_ScBIIG5jmsAV_-b-NDb-fQF4VMYgLzdtt4nxD3P7jGw58kTO23vxHc0yOQsuGvXBtIs4-vLH_jDeUsmE3Dg)))

A jot is made of three components. First there is the header, then the payload, and finally the signature. And those three components are separated using dots or periods. So lets pull out the middle component. Each of these components is Base64 encoded. That’s what ensures the URL safe part that we mentioned before. Base64 encoding is not encryption, just a standard way of encoding the text. 

Now that that component is Base64 decoded, we see that the payload is this.

(((show on screen 
{
  "exp": 1652966630,
  "groups": null,
  "iat": 1652966330,
  "name": "admin",
  "nbf": 1652966030,
  "nonce": "AmHUpJ9W85"
}
)))

The iat value is the time this token was issued. nbf says that this token is not valid before this time. and exp is the time when this token expires. We can translate those Unix Timestamps to more common date and time formats and can see that this token has a lifetime of 5 minutes. 

The nonce is a required value for OpenIdConnect JWTs and ensures that this token hasn't been used before. 

So the last two values in the token are the actual claim. Groups and Name. The name is the user who is running the command and the groups lists out the groups this user is a member of. 

Now that information is used by the destination to determine what roles this user should be allowed to assume. 

And that is what a JWT is and how they are used in Infra. On this channel we look at a lot of the tools and technologies used in Infra as well as tangential technologies in similar areas. If you found the video useful, please like and subscribe to see more. Thanks so much for watching. Goodbye. 

## Tweets
Do you know what a JSON Web Token is? Find out here: 

JWTs can be awesome for some things and suck for others. We use them in the awesome way: 

See how we use JWTs here at Infra to enable single sign on to Kubernetes:

Is there a question you have about how we made Infra. Let me know and it may get turned into a video like this one about JWTs:

Why isn't token revokation a problem for us at Infra when using JWTs? Find out in this video:

Did you watch our video about OIDC? Well this here is the latest one about JWT: 