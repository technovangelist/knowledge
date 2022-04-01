Notes for Rancher Docs: Kubernetes Workloads and Pods

## Source:
Author: rancher.com
Category: articles
Updated: 02/02/2021 12:52 PM
Highlights URL: https://readwise.io/bookreview/7505024
SourceUrl: https://rancher.com/docs/rancher/v2.x/en/k8s-in-rancher/workloads/


#### Extras:
**kubernetes**



 
-----
 ## Highlights:

### CronJobs are similar to jobs. CronJobs, however, runs to com...
>CronJobs are similar to jobs. CronJobs, however, runs to completion on a cron-based schedule. ^rw140460503hl


Highlighted: 02/02/2021 12:52 PM
Updated: 02/02/2021 12:52 PM


#### Extras:





------

### Jobs launch one or more pods and ensure that a specified num...
>Jobs launch one or more pods and ensure that a specified number of them successfully terminate. Jobs are best used to run a finite task to completion as opposed to managing an ongoing desired application state. ^rw140460502hl


Highlighted: 02/02/2021 12:52 PM
Updated: 02/02/2021 12:52 PM


#### Extras:
[desired state](/knowledge/desired state)




------

### Daemonsets ensures that every node in the cluster runs a cop...
>Daemonsets ensures that every node in the cluster runs a copy of pod. For use cases where you’re collecting logs or monitoring node performance, this daemon-like workload works best. ^rw140460500hl


Highlighted: 02/02/2021 12:52 PM
Updated: 02/02/2021 12:52 PM


#### Extras:
**daemonset**




------

### StatefulSets, in contrast to deployments, are best used when...
>StatefulSets, in contrast to deployments, are best used when your application needs to maintain its identity and store data. An application would be something like Zookeeper—an application that requires a database for storage. ^rw140460499hl


Highlighted: 02/02/2021 12:52 PM
Updated: 02/02/2021 12:52 PM


#### Extras:
**statefulsets**




------

### Deployments are best used for stateless applications (i.e., ...
>Deployments are best used for stateless applications (i.e., when you don’t have to maintain the workload’s state). Pods managed by deployment workloads are treated as independent and disposable. If a pod encounters disruption, Kubernetes removes it and then recreates it. An example application would be an Nginx web server. ^rw140460497hl


Highlighted: 02/02/2021 12:51 PM
Updated: 02/02/2021 12:52 PM


#### Extras:
**deployments**




------

