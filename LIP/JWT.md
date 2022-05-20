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