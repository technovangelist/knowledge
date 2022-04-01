Notes for Blog: Monitoring Kubernetes Workloads: The Sidecar Pattern | Lightnetics

## Source:
Author: lightnetics.com
Category: articles
Updated: 03/04/2021 06:32 PM
Highlights URL: https://readwise.io/bookreview/8093255
SourceUrl: https://www.lightnetics.com/topic/25571/blog-monitoring-kubernetes-workloads-the-sidecar-pattern

%%8093255topstart%%
#### Extras:

%%8093255topend%%
 
-----
 ## Highlights:

### to gain visibility into the health and performance of the sy...
>to gain visibility into the health and performance of the system, you need access to monitoring data down the stack ^rw153357598hl


Highlighted: 03/04/2021 03:51 PM
Updated: 03/04/2021 03:51 PM

%%153357598start%%
#### Extras:

%%153357598end%%

------

### you need to be able to collect data from four primary source...
>you need to be able to collect data from four primary sources
&gt;The Kubernetes hosts running the Kubelet. The most common way to get data out of these hosts is to use the Prometheus node exporter, which scrapes data from the Kubernetes host and exposes system resource telemetry data on an HTTP endpoint.
The Kubernetes process, AKA Kubelet metrics. These provide details on Kubernetes nodes and the jobs they run.
The Kubelet’s built-in cAdvisor, which helps keep track of resource usage for running containers.
Kube-state-metrics for a big picture view at the Kubernetes cluster level. ^rw153357599hl


Highlighted: 03/04/2021 03:51 PM
Updated: 03/04/2021 03:51 PM

%%153357599start%%
#### Extras:

%%153357599end%%

------

### Examples of Kubernetes sidecars include Service mesh
Loggi...
>Examples of Kubernetes sidecars include
&gt;Service mesh
Logging platforms with agents that run as sidecars
Monitoring solutions like Sensu with an agent that runs as a sidecar, giving you a 1:1 pairing of a monitoring agent per collection of services. ^rw153387231hl


Highlighted: 03/04/2021 06:32 PM
Updated: 03/04/2021 06:32 PM

%%153387231start%%
#### Extras:

%%153387231end%%

------

