Notes for Kubernetes Components | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/02/2021 06:38 PM
Highlights URL: https://readwise.io/bookreview/8071229
SourceUrl: https://kubernetes.io/docs/concepts/overview/components/

%%8071229topstart%%
#### Extras:

%%8071229topend%%
 
-----
 ## Highlights:

### In production environments, the control plane usually runs a...
>In production environments, the control plane usually runs across multiple computers and a cluster usually runs multiple nodes, providing fault-tolerance and high availability ^rw152789784hl


Highlighted: 03/02/2021 06:35 PM
Updated: 03/02/2021 06:35 PM

%%152789784start%%
#### Extras:

%%152789784end%%

------

### The API server is a component of the Kubernetes control plan...
>The API server is a component of the Kubernetes control plane that exposes the Kubernetes API. The API server is the front end for the Kubernetes control plane ^rw152789929hl


Highlighted: 03/02/2021 06:35 PM
Updated: 03/02/2021 06:35 PM

%%152789929start%%
#### Extras:

%%152789929end%%

------

### kube-scheduler
Control plane component that watches for newl...
>kube-scheduler
Control plane component that watches for newly created Pods with no assigned node, and selects a node for them to run on. ^rw152789933hl


Highlighted: 03/02/2021 06:36 PM
Updated: 03/02/2021 06:36 PM

%%152789933start%%
#### Extras:

%%152789933end%%

------

### kube-controller-manager
Control Plane component that runs co...
>kube-controller-manager
Control Plane component that runs controller processes
&gt;Logically, each controller is a separate process, but to reduce complexity, they are all compiled into a single binary and run in a single process. ^rw152789938hl

Comment: the deployment controller is an example controller ^rw152789938comment

Highlighted: 03/02/2021 06:36 PM
Updated: 03/02/2021 06:36 PM

%%152789938start%%
#### Extras:

%%152789938end%%

------

### cloud-controller-manager
A Kubernetes control plane componen...
>cloud-controller-manager
A Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider&#39;s API, and separates out the components that interact with that cloud platform from components that just interact with your cluster. ^rw152789943hl


Highlighted: 03/02/2021 06:36 PM
Updated: 03/02/2021 06:36 PM

%%152789943start%%
#### Extras:

%%152789943end%%

------

### kubelet
An agent that runs on each node in the cluster. It m...
>kubelet
An agent that runs on each node in the cluster. It makes sure that containers are running in a Pod. ^rw152789956hl


Highlighted: 03/02/2021 06:37 PM
Updated: 03/02/2021 06:37 PM

%%152789956start%%
#### Extras:

%%152789956end%%

------

### The kubelet takes a set of PodSpecs that are provided throug...
>The kubelet takes a set of PodSpecs that are provided through various mechanisms and ensures that the containers described in those PodSpecs are running and healthy. The kubelet doesn&#39;t manage containers which were not created by Kubernetes ^rw152789982hl


Highlighted: 03/02/2021 06:37 PM
Updated: 03/02/2021 06:37 PM

%%152789982start%%
#### Extras:

%%152789982end%%

------

### kube-proxy maintains network rules on nodes. These network r...
>kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster. ^rw152789983hl


Highlighted: 03/02/2021 06:37 PM
Updated: 03/02/2021 06:37 PM

%%152789983start%%
#### Extras:

%%152789983end%%

------

### DNS
While the other addons are not strictly required, all Ku...
>DNS
While the other addons are not strictly required, all Kubernetes clusters should have cluster DNS, as many examples rely on it
&gt;Cluster DNS is a DNS server, in addition to the other DNS server(s) in your environment, which serves DNS records for Kubernetes services. ^rw152790005hl


Highlighted: 03/02/2021 06:38 PM
Updated: 03/02/2021 06:38 PM

%%152790005start%%
#### Extras:

%%152790005end%%

------

### Cluster-level Logging
A cluster-level logging mechanism is r...
>Cluster-level Logging
A cluster-level logging mechanism is responsible for saving container logs to a central log store with search&#x2F;browsing interface ^rw152790013hl


Highlighted: 03/02/2021 06:38 PM
Updated: 03/02/2021 06:38 PM

%%152790013start%%
#### Extras:

%%152790013end%%

------

