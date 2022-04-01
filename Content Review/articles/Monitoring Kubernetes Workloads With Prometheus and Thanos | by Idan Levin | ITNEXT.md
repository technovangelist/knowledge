Notes for Monitoring Kubernetes Workloads With Prometheus and Thanos | by Idan Levin | ITNEXT

## Source:
Author: Idan Levin
Category: articles
Updated: 03/03/2021 12:59 PM
Highlights URL: https://readwise.io/bookreview/8079371
SourceUrl: https://itnext.io/monitoring-kubernetes-workloads-with-prometheus-and-thanos-4ddb394b32c


#### Extras:


 
-----
 ## Highlights:

### Monitoring Kubernetes should take into account all three lay...
>Monitoring Kubernetes should take into account all three layers mentioned above ^rw153022492hl

Comment: 1. underlying vm
2. k8s infra
3. applications ^rw153022492comment

Highlighted: 03/03/2021 12:56 PM
Updated: 03/03/2021 12:57 PM


#### Extras:



------

### Underlying VMs: to make sure the underlying virtual machines...
>Underlying VMs: to make sure the underlying virtual machines are healthy, the following metrics should be collected ^rw153022644hl

Comment: - Number of nodes
- Resource utilization per node (CPU, Memory, Disk, Network bandwidth)
- Node status (ready, not ready, etc.)
- Number of pods running per node ^rw153022644comment

Highlighted: 03/03/2021 12:57 PM
Updated: 03/03/2021 12:58 PM


#### Extras:



------

### Kubernetes Infrastructure: to make sure the Kubernetes infra...
>Kubernetes Infrastructure: to make sure the Kubernetes infrastructure is healthy, the following metrics should be collected ^rw153022685hl

Comment: - Pods health — instances ready, status, restarts, age
- Deployments status — desired, current, up-to-date, available, age
- StatefulSets status
- CronJobs execution stats
- Pod resource utilization (CPU and Memory)
- Health checks
- Kubernetes Events
- API Server requests
- Etcd stats
- Mounted volumes stats ^rw153022685comment

Highlighted: 03/03/2021 12:58 PM
Updated: 03/03/2021 12:59 PM


#### Extras:



------

### User Applications: each application should expose its own me...
>User Applications: each application should expose its own metrics, based on its core functionality, however, there are metrics which are common to most of the applications, such as: ^rw153022809hl

Comment: - HTTP requests (Total number, Latency, Response Code, etc.)
- Number of outgoing connections (e.g. database connections)
- Number of threads ^rw153022809comment

Highlighted: 03/03/2021 12:59 PM
Updated: 03/03/2021 12:59 PM


#### Extras:



------

