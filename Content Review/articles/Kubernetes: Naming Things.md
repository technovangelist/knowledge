Notes for Kubernetes: Naming Things

## Source:
Author: Michael Hausenblas
Category: articles
Updated: 01/25/2021 10:05 PM
Highlights URL: https://readwise.io/bookreview/7341239
SourceUrl: https://www.openshift.com/blog/kubernetes-naming-things

%%7341239topstart%%
#### Extras:
**kubernetes**
%%7341239topend%%


 
-----
 ## Highlights:

### Kubernetes: Naming Things
>Kubernetes: Naming Things ^rw136365751hl

Comment: Some interesting examples of commands to find things that are run in k8s ^rw136365751comment

Highlighted: 01/25/2021 10:04 PM
Updated: 01/25/2021 10:05 PM

%%136365751start%%
#### Extras:

%%136365751end%%



------

### kubectl run webserver --image=nginx deployment.apps/webserv...
>kubectl run webserver --image=nginx
>deployment.apps/webserver created
>kubectl get pods
>selector=run=webserver
>output=jsonpath={.items[*].metadata.name
>webserver-5748cdbbfc-7vn5j ^rw136365427hl

Comment: when you run something, it will give it a label of run=that something. and then output=jsonpath={xxx} says look for that jsonpath and output that ^rw136365427comment



Highlighted: 01/25/2021 10:00 PM
Updated: 01/25/2021 10:02 PM

%%136365427start%%
#### Extras:

%%136365427end%%



------

### there are only two hard problems in computer science, namely...
>there are only two hard problems in computer science, namely cache invalidation, naming things, and off-by-one errors ^rw136365198hl


Highlighted: 01/25/2021 09:58 PM
Updated: 01/25/2021 09:58 PM

%%136365198start%%
#### Extras:

%%136365198end%%



------

