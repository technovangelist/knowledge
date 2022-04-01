Notes for Kubernetes Node Components: Service Proxy, Kubelet, and cAdvisor | by Jorge Acetozi | Jorgeacetozi | Medium

## Source:
Author: Jorge Acetozi
Category: articles
Updated: 05/25/2021 08:18 AM
Highlights URL: https://readwise.io/bookreview/7487991
SourceUrl: https://medium.com/jorgeacetozi/kubernetes-node-components-service-proxy-kubelet-and-cadvisor-dcc6928ef58c

%%7487991topstart%%
#### Extras:

%%7487991topend%%
 
-----
 ## Highlights:

### the Kubernetes node runs the Kubelet and Service Proxy compo...
>the Kubernetes node runs the Kubelet and Service Proxy components as well as a container engine such as Docker or Rocket ^rw140045437hl


Highlighted: 02/01/2021 03:59 PM
Updated: 02/01/2021 03:59 PM

%%140045437start%%
#### Extras:

%%140045437end%%

------

### The Service Proxy runs on each node and is responsible for w...
>The Service Proxy runs on each node and is responsible for watching the API Server for changes on services and pods definitions to maintain the entire network configuration up to date, ensuring that one pod can talk to another pod, one node can talk to another node, one container can talk to another container, and so on ^rw140045978hl


Highlighted: 02/01/2021 04:01 PM
Updated: 02/01/2021 04:01 PM

%%140045978start%%
#### Extras:
**kubernetes** **serviceproxy** **serviceproxy**
%%140045978end%%

------

### Kubelet is one of the most important components in Kubernete...
>Kubelet is one of the most important components in Kubernetes. Basically, it’s an agent that runs on each node and is responsible for watching the API Server for pods that are bound to its node and making sure those pods are running (it talks to the Docker daemon using the API over the Docker socket to manipulate containers lifecycle). It then reports back to the API Server the status of changes regarding those pods ^rw140166144hl


Highlighted: 02/01/2021 09:13 PM
Updated: 02/01/2021 09:13 PM

%%140166144start%%
#### Extras:
**kubernetes** **kubelet** 
%%140166144end%%

------

### Memex note from: 2021-2-1 21:14:2
>Memex note from: 2021-2-1 21:14:2 ^rw140166161hl

Comment: note this is a 2017 article ^rw140166161comment

Highlighted: 02/01/2021 09:14 PM
Updated: 02/01/2021 09:14 PM

%%140166161start%%
#### Extras:

%%140166161end%%

------

### Memex note from: 2021-5-25 8:18:5
>Memex note from: 2021-5-25 8:18:5 ^rw183454076hl

Comment: note this is a 2017 article ^rw183454076comment

Highlighted: 02/01/2021 09:14 PM
Updated: 05/25/2021 08:18 AM

%%183454076start%%
#### Extras:

%%183454076end%%



------

