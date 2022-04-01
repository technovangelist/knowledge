Notes for AWS Lambda Execution Environment - AWS Lambda

## Source:
Author: docs.aws.amazon.com
Category: articles
Updated: 01/25/2021 10:20 PM
Highlights URL: https://readwise.io/bookreview/7341329
SourceUrl: https://docs.aws.amazon.com/lambda/latest/dg/runtimes-context.html#runtimes-lifecycle

%%7341329topstart%%
#### Extras:
[AWS Lambda](/knowledge/Tools I Use/AWS Lambda)
%%7341329topend%%


 
-----
 ## Highlights:

### Shutdown: This phase is triggered if the Lambda function doe...
>Shutdown: This phase is triggered if the Lambda function does not receive any invocations for a period of time. In the Shutdown phase, Lambda terminates the runtime, alerts the extensions to let them stop cleanly, and then removes the environment. Lambda sends a Shutdown event to each extension, which tells the extension that the environment is about to be shut down. ^rw136367530hl


Highlighted: 01/25/2021 10:20 PM
Updated: 01/25/2021 10:20 PM

%%136367530start%%
#### Extras:
**shutdown phase**
%%136367530end%%



------

### Invoke: In this phase, Lambda invokes the function handler. ...
>Invoke: In this phase, Lambda invokes the function handler. After the function runs to completion, Lambda prepares to handle another function invocation. ^rw136367529hl


Highlighted: 01/25/2021 10:20 PM
Updated: 01/25/2021 10:20 PM

%%136367529start%%
#### Extras:
**invoke phase**
%%136367529end%%



------

### The Init phase is split into three sub-phases: Extension ini...
>The Init phase is split into three sub-phases: Extension init, Runtime init, and Function init ^rw136367493hl


Highlighted: 01/25/2021 10:19 PM
Updated: 01/25/2021 10:19 PM

%%136367493start%%
#### Extras:
**init phase**
%%136367493end%%



------

### Init: In this phase, Lambda creates or unfreezes an executio...
>Init: In this phase, Lambda creates or unfreezes an execution environment with the configured resources, downloads the code for the function and all layers, initializes any extensions, initializes the runtime, and then runs the function’s initialization code (the code outside the main handler). The Init phase happens either during the first invocation, or in advance of function invocations if you have enabled provisioned concurrency. ^rw136367490hl


Highlighted: 01/25/2021 10:19 PM
Updated: 01/25/2021 10:19 PM

%%136367490start%%
#### Extras:

%%136367490end%%



------

### The function's runtime communicates with Lambda using the Ru...
>The function's runtime communicates with Lambda using the Runtime API ^rw136367464hl


Highlighted: 01/25/2021 10:18 PM
Updated: 01/25/2021 10:18 PM

%%136367464start%%
#### Extras:

%%136367464end%%



------

