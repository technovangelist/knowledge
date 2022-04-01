Notes for Kubernetes Autoscaling in Production: Best Practices for Cluster Autoscaler, HPA and VPA

## Source:
Author: replex.io
Category: articles
Updated: 03/04/2021 06:44 PM
Highlights URL: https://readwise.io/bookreview/8094661
SourceUrl: https://www.replex.io/blog/kubernetes-in-production-best-practices-for-cluster-autoscaler-hpa-and-vpa


#### Extras:


 
-----
 ## Highlights:

### The cluster autoscaler is a Kubernetes tool that increases o...
>The cluster autoscaler is a Kubernetes tool that increases or decreases the size of a Kubernetes cluster (by adding or removing nodes), based on the presence of pending pods and node utilization metrics. ^rw153387904hl


Highlighted: 03/04/2021 06:39 PM
Updated: 03/04/2021 06:39 PM


#### Extras:



------

### In addition to specifying a pod disruption budget for system...
>In addition to specifying a pod disruption budget for system pods, another best practice is to also specify a pod disruption budget for application pods. This will ensure that the cluster autoscaler does not scale down pod replicas beyond a certain minimum number and will protect critical applications from disruptions and ensure high availability. ^rw153387935hl


Highlighted: 03/04/2021 06:40 PM
Updated: 03/04/2021 06:40 PM


#### Extras:



------

### For the cluster autoscaler to remain responsive it is import...
>For the cluster autoscaler to remain responsive it is important to ensure that the cluster does not exceed a certain size. The official scalability and responsiveness service level for the cluster autoscaler is set at 1000 nodes with each node running 30 pods. ^rw153388001hl


Highlighted: 03/04/2021 06:41 PM
Updated: 03/04/2021 06:41 PM


#### Extras:



------

### Ensure Resource Requests are Close to Actual Usage
>Ensure Resource Requests are Close to Actual Usage ^rw153388092hl


Highlighted: 03/04/2021 06:41 PM
Updated: 03/04/2021 06:41 PM


#### Extras:



------

### Over-provision Cluster to Ensure head room for Critical pods...
>Over-provision Cluster to Ensure head room for Critical pods ^rw153388099hl


Highlighted: 03/04/2021 06:41 PM
Updated: 03/04/2021 06:41 PM


#### Extras:



------

### The cluster autoscaler has a service level objective (SLO) o...
>The cluster autoscaler has a service level objective (SLO) of 30 seconds latency between the time a pod is marked as unschedulable to the time that it requests a scale-up to the cloud provider ^rw153388112hl


Highlighted: 03/04/2021 06:42 PM
Updated: 03/04/2021 06:42 PM


#### Extras:



------

### For larger clusters of up to a 1000 nodes this latency is ex...
>For larger clusters of up to a 1000 nodes this latency is expected to be around the 60 second mark. ^rw153388114hl


Highlighted: 03/04/2021 06:42 PM
Updated: 03/04/2021 06:42 PM


#### Extras:



------

### A best practice therefore is to ensure that resource request...
>A best practice therefore is to ensure that resource request values are configured for all containers of each individual pod, that is a part of the Kubernetes controller being scaled using HPA ^rw153388156hl


Highlighted: 03/04/2021 06:43 PM
Updated: 03/04/2021 06:43 PM


#### Extras:



------

### Configure Cooldown Period
>Configure Cooldown Period ^rw153388219hl


Highlighted: 03/04/2021 06:43 PM
Updated: 03/04/2021 06:43 PM


#### Extras:



------

### Avoid using HPA and VPA in tandem
>Avoid using HPA and VPA in tandem ^rw153388233hl


Highlighted: 03/04/2021 06:43 PM
Updated: 03/04/2021 06:43 PM


#### Extras:



------

### Use VPA together with Cluster autoscaler
>Use VPA together with Cluster autoscaler ^rw153388255hl


Highlighted: 03/04/2021 06:44 PM
Updated: 03/04/2021 06:44 PM


#### Extras:



------

