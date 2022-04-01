Notes for AWS Lambda Best Practices. Here I Would Like to Discuss About The… | by Praveen Sambu | Jan, 2021 | Medium

## Source:
Author: Praveen Sambu
Category: articles
Updated: 02/05/2021 08:07 AM
Highlights URL: https://readwise.io/bookreview/7558280
SourceUrl: https://sambupraveen.medium.com/aws-lambda-best-practices-71ebc79c47f1

%%7558280topstart%%
#### Extras:
[AWS Lambda](Tools I Use/AWS Lambda.md)**Praveen Sambu**
%%7558280topend%%


 
-----
 ## Highlights:

### Keep Containers warm.
>Keep Containers warm. ^rw141645641hl

Comment: Depends. Often this is just stupid ^rw141645641comment

Highlighted: 02/05/2021 06:26 AM
Updated: 02/05/2021 08:07 AM

%%141645641start%%
#### Extras:
**Keep Lambdas Warm**
%%141645641end%%



------

### This is kind of micro service approach and it is recommended...
>This is kind of micro service approach and it is recommended to write lambda as small as possible and have it do one task. So that cost can be saved as it consumes less memory ^rw141645640hl

Comment: It depends. If two tasks combined takes 20ms then splitting up can add time for cold start ^rw141645640comment

Highlighted: 02/05/2021 06:24 AM
Updated: 02/05/2021 08:07 AM

%%141645640start%%
#### Extras:

%%141645640end%%



------

### Instead of hardcoding, use Environment variables. If you are...
>Instead of hardcoding, use Environment variables. If you are writing to s3 bucket. instead of giving bucket name in handler, configure that in env variable and use it from there so that we can change it in run time ^rw141645639hl

Comment: Great idea ^rw141645639comment

Highlighted: 02/05/2021 06:23 AM
Updated: 02/05/2021 08:07 AM

%%141645639start%%
#### Extras:
**S3** #activetodos 
%%141645639end%%



------

### Keep declarations/Instantons outside the lambda handlerThis ...
>Keep declarations/Instantons outside the lambda handlerThis allows the lambda handler to reuse the objects when container get reused. Incase with your database connections this would be even matter more. ^rw141645637hl


Highlighted: 02/05/2021 06:23 AM
Updated: 02/05/2021 08:07 AM

%%141645637start%%
#### Extras:

%%141645637end%%



------

