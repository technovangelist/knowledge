Notes for AWS Lambda Functions With a Static IP

## Source:
Category: articles
Updated: 03/18/2020 08:59 AM
Highlights URL: https://readwise.io/bookreview/1548109
SourceUrl: https://medium.com/@matthewleak/aws-lambda-functions-with-a-static-ip-89a3ada0b471

%%1548109topstart%%
#### Extras:
[AWS Lambda](/knowledge/Tools I Use/AWS Lambda)
%%1548109topend%%


 
-----
 ## Highlights:

### AWS Lambda supports executing your code from inside a VPC. W...
>AWS Lambda supports executing your code from inside a VPC. With this ability we’re able to create a NAT (Network Address Translator) Gateway so that all out-bound connections from our lambda functions will exit from the NAT which is assigned to a fixed IP address. This fixed IP adress can then be whitelisted by our third-parties
>Create a new VPC to run your code in (or use an existing VPC)
Create a new Internet Gateway to communicate with the Internet from inside your VPC
Create a Public Subnet and add a new route to the route table which routes to your Internet Gateway from 0.0.0.0/0
Create a new Elastic IP address.
Create a new NAT Gateway and assign it to the Public Subnet and Elastic IP address that you just created.
Create a Private Subnet and add a new route to the route table which routes to your NAT Gateway from 0.0.0.0/0 ^rw43203496hl

Comment: How to do a lambda from static ip ^rw43203496comment

Highlighted: 03/12/2020 08:57 AM
Updated: 03/12/2020 05:34 PM

%%43203496start%%
#### Extras:

%%43203496end%%



------

### solution
>solution ^rw43203494hl


Highlighted: 03/12/2020 08:55 AM
Updated: 03/12/2020 05:34 PM

%%43203494start%%
#### Extras:

%%43203494end%%



------

