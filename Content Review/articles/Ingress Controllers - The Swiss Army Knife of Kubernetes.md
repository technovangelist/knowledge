Notes for Ingress Controllers: The Swiss Army Knife of Kubernetes

## Source:
Author: Brian Ehlert
Category: articles
Updated: 01/04/2022 07:35 AM
Highlights URL: https://readwise.io/bookreview/12628652
SourceUrl: https://www.inoreader.com/article/3a9c6e7ae83dbb66-ingress-controllers-the-swiss-army-knife-of-kubernetes

%%12628652topstart%%
#### Extras:

%%12628652topend%%


 
-----
 ## Highlights:

### When deployed and configured properly, ingress controllers c...
>When deployed and configured properly, ingress controllers can radically simplify operation of Kubernetes clusters while enhancing security and improving performance and resilience ^rw266503767hl


Highlighted: 01/04/2022 06:59 AM
Updated: 01/04/2022 06:59 AM

%%266503767start%%
#### Extras:

%%266503767end%%



------

### Ingress controllers are essential for defining and managing ...
>Ingress controllers are essential for defining and managing ingress (north-south) traffic in Kubernetes, which is a more complex ingress environment than what you might find in non-Kubernetes apps. ^rw266503953hl


Highlighted: 01/04/2022 07:02 AM
Updated: 01/04/2022 07:02 AM

%%266503953start%%
#### Extras:
![north-south for IO to from cluster](/knowledge/Content Review/articles/north-south for IO to from cluster.md)
%%266503953end%%



------

### By default, apps running in Kubernetes pods (and containers)...
>By default, apps running in Kubernetes pods (and containers) are not accessible to external networks and traffic. Pods within Kubernetes can only communicate amongst themselves. Kubernetes does have a built-in configuration object for HTTP (Layer 7) load balancing, called ingress. This object defines how entities outside a Kubernetes cluster can connect to pods labeled with one or more Kubernetes services ^rw266503967hl


Highlighted: 01/04/2022 07:02 AM
Updated: 01/04/2022 07:02 AM

%%266503967start%%
#### Extras:

%%266503967end%%



------

### Reminder: The “LoadBalancer” service is not the same as a de...
>Reminder: The “LoadBalancer” service is not the same as a dedicated load balancer. ^rw266512626hl


Highlighted: 01/04/2022 07:15 AM
Updated: 01/04/2022 07:15 AM

%%266512626start%%
#### Extras:

%%266512626end%%



------

### Ingress controllers are sometimes described as a “specialize...
>Ingress controllers are sometimes described as a “specialized load balancer” for Kubernetes. So that begs the question: Do you need both a load balancer and an ingress controller? Well, the answer is: It depends. As was discussed in the previous post “Duplication, Not Consolidation: The Path Forward for Apps,” sometimes you need some functionality duplication based on who is using the tool and where it’s being deployed ^rw266513084hl


Highlighted: 01/04/2022 07:15 AM
Updated: 01/04/2022 07:15 AM

%%266513084start%%
#### Extras:

%%266513084end%%



------

### if you’re going to be scaling Kubernetes or in high-complian...
>if you’re going to be scaling Kubernetes or in high-compliance environments, organizations deploy both an ingress controller and load balancer. ^rw266513735hl


Highlighted: 01/04/2022 07:16 AM
Updated: 01/04/2022 07:16 AM

%%266513735start%%
#### Extras:

%%266513735end%%



------

### Load balancer (or ADC):     Managed by: A NetOps (or maybe S...
>Load balancer (or ADC):     Managed by: A NetOps (or maybe SecOps) team   Deployed: Outside Kubernetes as the only public-facing endpoint of services and apps delivered to users outside your cluster. Used as a more generic appliance designed to facilitate security and deliver higher-level network management.       Ingress controller:     Managed by: A platform ops or DevOps team   Deployed: Inside Kubernetes for fine-grain north-south load balancing capabilities (HTTP2, HTTP&#x2F;HTTPS, SSL&#x2F;TLS termination, TC ^rw266513911hl


Highlighted: 01/04/2022 07:16 AM
Updated: 01/04/2022 07:16 AM

%%266513911start%%
#### Extras:

%%266513911end%%



------

### Ingress controllers act as a second layer of access control ...
>Ingress controllers act as a second layer of access control just in case a global load balancer configuration drifts to an insecure setting. ^rw266514712hl


Highlighted: 01/04/2022 07:19 AM
Updated: 01/04/2022 07:19 AM

%%266514712start%%
#### Extras:

%%266514712end%%



------

### Because ingress controllers are designed to function at the ...
>Because ingress controllers are designed to function at the node and pod level, and are a control loop running on top of services, they’re the best location for enforcing encryption behaviors — the closest to the actual app ^rw266515719hl


Highlighted: 01/04/2022 07:27 AM
Updated: 01/04/2022 07:27 AM

%%266515719start%%
#### Extras:

%%266515719end%%



------

### For the most part, anyone deploying a production app in Kube...
>For the most part, anyone deploying a production app in Kubernetes needs to use a web application firewall (WAF) to protect the app and the cluster. WAFs can filter out bad traffic and protect exposed apps. That said, like anomaly detection, WAFs configured to protect at the global level of an enterprise environment are like blunt instruments that aren’t well-suited to implementing finer-grained security at the app layer. For this reason, many teams are now running their own WAFs inside Kubernetes at the ^rw266527960hl


Highlighted: 01/04/2022 07:35 AM
Updated: 01/04/2022 07:35 AM

%%266527960start%%
#### Extras:

%%266527960end%%



------

