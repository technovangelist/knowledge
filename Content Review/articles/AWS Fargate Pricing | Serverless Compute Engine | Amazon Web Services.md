Notes for AWS Fargate Pricing | Serverless Compute Engine | Amazon Web Services

## Source:
Author: aws.amazon.com
Category: articles
Updated: 03/01/2021 07:36 PM
Highlights URL: https://readwise.io/bookreview/8059282
SourceUrl: https://aws.amazon.com/fargate/pricing/#Supported_Configurations


#### Extras:


 
-----
 ## Highlights:

### Supported Configurations
CPU
Memory Values
0.25 vCPU	0.5GB, ...
>Supported Configurations
CPU
Memory Values
0.25 vCPU	0.5GB, 1GB, and 2GB
0.5 vCPU	Min. 1GB and Max. 4GB, in 1GB increments
1 vCPU	Min. 2GB and Max. 8GB, in 1GB increments
2 vCPU	Min. 4GB and Max. 16GB, in 1GB increments
4 vCPU	Min. 8GB and Max. 30GB, in 1GB increments ^rw152484737hl


Highlighted: 03/01/2021 07:30 PM
Updated: 03/01/2021 07:30 PM


#### Extras:
### Supported Configurations

| CPU       | Memory Values                             |
| --------- | ----------------------------------------- |
| 0.25 vCPU | 0.5GB, 1GB, and 2GB                       |
| 0.5 vCPU  | Min. 1GB and Max. 4GB, in 1GB increments  |
| 1 vCPU    | Min. 2GB and Max. 8GB, in 1GB increments  |
| 2 vCPU    | Min. 4GB and Max. 16GB, in 1GB increments |
|  4 vCPU    |    Min. 8GB and Max. 30GB, in 1GB increments |







------

### Take advantage of Savings Plans if you have steady state Far...
>Take advantage of Savings Plans if you have steady state Fargate usage. Savings Plans offers savings of up to 50% on your AWS Fargate usage in exchange for a commitment to use a specific amount of compute usage (measure in dollars per hour) for a one or three year term. ^rw152485381hl


Highlighted: 03/01/2021 07:36 PM
Updated: 03/01/2021 07:36 PM


#### Extras:

Is there a way to save money on Fargate? #flashcard 
the Savings Plans offer up to 50% saving in exchange for commitment for 1 to 3 year term.
<!--ID: 1614656366189-->





------

### Duration
Pricing is per second with a 1-minute minimum. Dura...
>Duration
Pricing is per second with a 1-minute minimum. Duration is calculated from the time you start to download your container image (docker pull) until the Task terminates, rounded up to the nearest second. ^rw152485383hl


Highlighted: 03/01/2021 07:36 PM
Updated: 03/01/2021 07:36 PM


#### Extras:

When does the duration for Fargate billing start? #flashcard 
it starts when you start the download of your container image and stops when the task terminates
<!--ID: 1614656366178-->




------

