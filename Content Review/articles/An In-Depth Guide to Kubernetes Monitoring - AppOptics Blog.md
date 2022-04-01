Notes for An In-Depth Guide to Kubernetes Monitoring - AppOptics Blog

## Source:
Author: blog.appoptics.com
Category: articles
Updated: 03/03/2021 12:54 PM
Highlights URL: https://readwise.io/bookreview/8078263
SourceUrl: https://blog.appoptics.com/an-in-depth-guide-to-kubernetes-monitoring/


#### Extras:


 
-----
 ## Highlights:

### When deploying a pod to a Kubernetes cluster, the Kubernetes...
>When deploying a pod to a Kubernetes cluster, the Kubernetes scheduler selects a node for it to run on. Kubernetes will report metrics on pods as soon as they’re defined, which means you can track the state of a pod before it’s deployed to a node. Pods that are scheduled but not running are recorded in the kubernetes.pod.status.condition.scheduled metric, while running pods are recorded in the kubernetes.pod.status.condition.ready. A pod is only considered successfully deployed once all of its containers have been created and at least one container is running or starting. ^rw152991367hl


Highlighted: 03/03/2021 10:49 AM
Updated: 03/03/2021 10:49 AM


#### Extras:



------

### To differentiate between multiple instances of the same pod,...
>To differentiate between multiple instances of the same pod, Kubernetes assigns each pod a unique identifier (ID). ^rw152991384hl


Highlighted: 03/03/2021 10:49 AM
Updated: 03/03/2021 10:49 AM


#### Extras:



------

### Pod states include Pending – the pod is waiting to be sche...
>Pod states include
&gt;Pending – the pod is waiting to be scheduled
Running – the pod is scheduled, and its containers are running
Succeeded – the pod completed its task and its containers were terminated
Failed – the pod is stopped, and at least one of its containers stopped with a failure
Unknown – the pod’s state can’t be determined ^rw153000690hl


Highlighted: 03/03/2021 11:25 AM
Updated: 03/03/2021 11:25 AM


#### Extras:



------

### For example, in the AppOptics dashboard shown above, the “pe...
>For example, in the AppOptics dashboard shown above, the “pending pods (by node)” chart shows the number of pods waiting to be scheduled according to thekubernetes.pod.status.phase.Pending metric. A short increase is typical when creating a new deployment as pods are created and scheduled. However, a sustained increase could mean a scheduling failure due to low cluster resources or a problem with the scheduler itself ^rw153000718hl

Comment: One way to  identify a problem with the scheduler ^rw153000718comment

Highlighted: 03/03/2021 11:25 AM
Updated: 03/03/2021 11:26 AM


#### Extras:



------

### Like with pods, Kubernetes assigns each deployment a unique ...
>Like with pods, Kubernetes assigns each deployment a unique identifier. You can use this identifier to filter deployment metrics to a specific instance instead of viewing metrics across all deployments ^rw153000770hl


Highlighted: 03/03/2021 11:26 AM
Updated: 03/03/2021 11:26 AM


#### Extras:



------

### Deployments don’t create pods themselves, but delegate the t...
>Deployments don’t create pods themselves, but delegate the task to ReplicaSets ^rw153000774hl


Highlighted: 03/03/2021 11:26 AM
Updated: 03/03/2021 11:26 AM


#### Extras:



------

### ReplicaSets report aggregate pod metrics, including Target...
>ReplicaSets report aggregate pod metrics, including
&gt;Targeted – the total number of non-terminated pods managed by this ReplicaSet
Unavailable – the number of pods in an unavailable state
Available – the total number of pods currently deployed
Desired – the number of desired pods according to the deployment
Updated – the number of non-terminated pods matching the latest deployment specification ^rw153000785hl


Highlighted: 03/03/2021 11:27 AM
Updated: 03/03/2021 11:27 AM


#### Extras:



------

### For example, if the number of available pods is less than th...
>For example, if the number of available pods is less than the number of desired pods, you can assume the deployment is either in the process of creating new pods or failed to meet specifications. AppOptics records these metrics as
kubernetes.deployment.status.[State]Replicas, e.g. kubernetes.deployment.status.TargetedReplicas and kubernetes.deployment.status.UnavailableReplicas. ^rw153001047hl

Comment: Pods failing to meet spec ^rw153001047comment

Highlighted: 03/03/2021 11:32 AM
Updated: 03/03/2021 11:33 AM


#### Extras:



------

### A Deployment is considered unfinished if its current state d...
>A Deployment is considered unfinished if its current state does not equal the desired state. This could indicate an ongoing deployment or a failed deployment. If a deployment remains in the unfinished state for too long, there could be underlying problems with its configuration or the Kubernetes cluster. AppOptics records unfinished deployments in the kubernetes.deployment.status.deploynotfinished metric. ^rw153001214hl


Highlighted: 03/03/2021 11:33 AM
Updated: 03/03/2021 11:33 AM


#### Extras:



------

### In this example, we want to deploy a website. We have a simp...
>In this example, we want to deploy a website. We have a simple deployment running a Nginx pod with multiple replicas for load balancing. However, we’ve noticed our website appears to be running slower than expected, and after reviewing host metrics, all of our network traffic appears to be going to a single node. To troubleshoot this issue, we need to find out what exactly is happening and why our deployment isn’t scaling properly ^rw153022097hl

Comment: 1. Check resources
  `kubectl top node` gets capacity available
2. kubernetes.pod.status.phase.Pending stuck at 1
3. `kubectl get pods` shows one pod pending
4. `kubectl describe pod:&lt;pod name&gt;` shows an error about ports not available
5. the deployment spec states a specific port, but two replicas can&#39;t use the same port, assuming its on the same node. so need to replace hostPort with a service and ingress ^rw153022097comment

Highlighted: 03/03/2021 12:50 PM
Updated: 03/03/2021 12:54 PM


#### Extras:



------

