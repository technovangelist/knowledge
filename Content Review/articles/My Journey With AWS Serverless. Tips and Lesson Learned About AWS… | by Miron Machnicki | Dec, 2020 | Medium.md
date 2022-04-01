Notes for My Journey With AWS Serverless. Tips and Lesson Learned About AWS… | by Miron Machnicki | Dec, 2020 | Medium

## Source:
Author: Miron Machnicki
Category: articles
Updated: 01/25/2021 10:23 PM
Highlights URL: https://readwise.io/bookreview/7188865
SourceUrl: https://machnicki.medium.com/my-journey-with-aws-serverless-7db5d91ecfc4

%%7188865topstart%%
#### Extras:
[AWS Lambda](/knowledge/Tools I Use/AWS Lambda)**Miron Machnicki**
%%7188865topend%%


 
-----
 ## Highlights:

### You should also consider Terraform, which is great framework...
>You should also consider Terraform, which is great framework for managing persistent shared infrastructure. It’s common practice to use Terraform for cloud infrastructure and SAM or Serverless for deploying applications ^rw136367585hl


Highlighted: 01/25/2021 10:23 PM
Updated: 01/25/2021 10:23 PM

%%136367585start%%
#### Extras:
**Terraform****SAM**
%%136367585end%%



------

### Your services can grow quickly. You might think to put all f...
>Your services can grow quickly. You might think to put all functions / resources definitions into one CloudFormation stack (eg. in single serverless.yaml /Serverless framework). As this sounds good for few functions (which together delivers single feature), in future it could make you some troubles ^rw136367575hl


Highlighted: 01/25/2021 10:23 PM
Updated: 01/25/2021 10:23 PM

%%136367575start%%
#### Extras:

%%136367575end%%



------

### max result size for Scan/Query operation is 1MB
>max result size for Scan/Query operation is 1MB ^rw136367565hl


Highlighted: 01/25/2021 10:22 PM
Updated: 01/25/2021 10:22 PM

%%136367565start%%
#### Extras:

%%136367565end%%



------

### DynamoDB should be reliable, especially if you’re using Glob...
>DynamoDB should be reliable, especially if you’re using Global Tables, but don’t forget about handling errors — log them, think about retry logic and set DLQ for your Lambda. ^rw136367558hl


Highlighted: 01/25/2021 10:22 PM
Updated: 01/25/2021 10:22 PM

%%136367558start%%
#### Extras:
**dynamodb**
%%136367558end%%



------

### be careful — it might be too much costly for some cases. If ...
>be careful — it might be too much costly for some cases. If your traffic is very dynamic, you can manage your provision concurrency within Application Auto Scaling ^rw136366925hl


Highlighted: 01/25/2021 10:14 PM
Updated: 01/25/2021 10:14 PM

%%136366925start%%
#### Extras:

%%136366925end%%



------

### SQS — queues (pull) are ideal solution when you expect throt...
>SQS — queues (pull) are ideal solution when you expect throttling problem — for example if your traffic is very dynamic and you would like to avoid to lose any messages, or if you want to optimize Lambda autoscaling (60 additional instances per minute to a maximum of 1,000 concurrent invocations); ^rw136361313hl


Highlighted: 01/25/2021 09:39 PM
Updated: 01/25/2021 09:39 PM

%%136361313start%%
#### Extras:

%%136361313end%%



------

### Think about access patterns
DynamoDB is fast, because you ac...
>Think about access patterns
DynamoDB is fast, because you access data directly from partition (you always need to know partition key and optionally sort key). When you query for more than one item, it’s important to have proper keys design. One key can be composition of different data. It’s common practice to give simple name to keys (as PK, SK) and keep different types of data in the same table (single table design). You can different that data types by adding prefix to your key followed by hash, such as TYPE#123. Because data in DynamoDB are organized in B-trees, you should also think about, how you would like to sort / filter it, and then design your sort key accordingly. If you would like to access your data in couple different ways, consider using GSI or LSI (global / local secondary index). ^rw132623629hl


Highlighted: 01/07/2021 03:58 PM
Updated: 01/15/2021 10:34 PM

%%132623629start%%
#### Extras:

%%132623629end%%



------

### you can set SQS queue or SNS topic as dead letter queue or a...
>you can set SQS queue or SNS topic as dead letter queue or as an on failure destination. In first case you will have access to all discarded events, in second case you will have access to events, but also to errors responses. ^rw132623628hl


Highlighted: 01/07/2021 03:54 PM
Updated: 01/15/2021 10:34 PM

%%132623628start%%
#### Extras:
**SQS****SNS**
%%132623628end%%



------

### For example Lambda calls via API Gateway or Elastic Load Bal...
>For example Lambda calls via API Gateway or Elastic Load Balancer are synchronous, as you expect response. ^rw132623627hl


Highlighted: 01/07/2021 03:51 PM
Updated: 01/15/2021 10:34 PM

%%132623627start%%
#### Extras:
**API Gateway****Elastic Load Balancer**
%%132623627end%%



------

### You can invoke Lambda synchronously or asynchronously
>You can invoke Lambda synchronously or asynchronously ^rw132623626hl

Comment: Need to check this

Ahh, I was thinking it meant execution, but think it means how it gets launched and not how it runs ^rw132623626comment

Highlighted: 01/07/2021 03:51 PM
Updated: 01/15/2021 10:34 PM

%%132623626start%%
#### Extras:

%%132623626end%%



------

### it might not be necessary to split logic into Lambdas, which...
>it might not be necessary to split logic into Lambdas, which computation time takes less < 1s ^rw132623625hl

Comment: Am I splitting up the lambdas in the right spots? ^rw132623625comment

Highlighted: 01/07/2021 03:50 PM
Updated: 01/15/2021 10:34 PM

%%132623625start%%
#### Extras:

%%132623625end%%



------

### provisioned concurrency
>provisioned concurrency ^rw132623624hl

Comment: hmm, I don't know if i know if this will benefit me. Should I always have 1? ^rw132623624comment

Highlighted: 01/07/2021 03:49 PM
Updated: 01/15/2021 10:34 PM

%%132623624start%%
#### Extras:

%%132623624end%%



------

