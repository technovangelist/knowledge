Notes for A Nice Way to Share Code Between Lambda Functions | by Alejandro Pinola | Jan, 2021 | Medium

## Source:
Author: Alejandro Pinola
Category: articles
Updated: 02/05/2021 08:07 AM
Highlights URL: https://readwise.io/bookreview/7558279
SourceUrl: https://medium.com/@alepinola/a-nice-way-to-share-code-between-lambda-functions-76104fe29730


#### Extras:
**Alejandro Pinola**[AWS Lambda](/knowledge/Tools I Use/AWS Lambda)



 
-----
 ## Highlights:

### The way to tackle this problem is just to add an environment...
>The way to tackle this problem is just to add an environment variable NODE_PATH with the value shared/nodejs/node_modules. ^rw141645636hl

Comment: Interesting ^rw141645636comment

Highlighted: 02/05/2021 06:22 AM
Updated: 02/05/2021 08:07 AM


#### Extras:





------

### It’s quite simple, you just need to declare a shared layer i...
>It’s quite simple, you just need to declare a shared layer in your CFN template, then associate the Lambda functions to this resource, and finally put all the packages (npm modules or your own) in place during the build process. ^rw141645635hl

Comment: How to do it with serverless framework? ^rw141645635comment

Highlighted: 02/05/2021 06:19 AM
Updated: 02/05/2021 08:07 AM


#### Extras:
**Cloudformation**




------

### If the size of the code you upload to a Lambda function is b...
>If the size of the code you upload to a Lambda function is bigger than 3MB you will not be able to debug your lambda in the AWS console, nor make changes on the fly, and not even see the code you wrote. ^rw141645634hl

Comment: This is the big reason this idea is interesting ^rw141645634comment

Highlighted: 02/05/2021 06:18 AM
Updated: 02/05/2021 08:07 AM


#### Extras:





------

