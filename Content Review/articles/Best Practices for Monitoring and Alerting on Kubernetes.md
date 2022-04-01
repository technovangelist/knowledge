Notes for Best Practices for Monitoring and Alerting on Kubernetes

## Source:
Author: rancher.com
Category: articles
Updated: 03/03/2021 11:12 AM
Highlights URL: https://readwise.io/bookreview/8078434
SourceUrl: https://rancher.com/learning-paths/best-practices-for-monitoring-and-alerting-on-kubernetes/


#### Extras:


 
-----
 ## Highlights:

### A proper monitoring strategy for containerized applications ...
>A proper monitoring strategy for containerized applications needs to provide visibility into the additional infrastructure layers introduced by Kubernetes orchestration and the container runtime ^rw152994464hl

Comment: https:&#x2F;&#x2F;rancher.com&#x2F;img&#x2F;learning-paths&#x2F;03-best-practices-for-monitoring-and-alerting-on-kubernetes&#x2F;media&#x2F;traditional-vs-container-monitoring-layers-orig.png ^rw152994464comment

Highlighted: 03/03/2021 11:09 AM
Updated: 03/03/2021 11:10 AM


#### Extras:
![](https://rancher.com/img/learning-paths/03-best-practices-for-monitoring-and-alerting-on-kubernetes/media/traditional-vs-container-monitoring-layers-orig.png)


------

### The Kubernetes control plane constitutes the brain of the cl...
>The Kubernetes control plane constitutes the brain of the cluster. ^rw152994862hl


Highlighted: 03/03/2021 11:11 AM
Updated: 03/03/2021 11:11 AM


#### Extras:



------

### Basic monitoring of these components would involve an HTTP c...
>Basic monitoring of these components would involve an HTTP check that queries the health check endpoint (&#x2F;healthz) exposed by instances of these services or by scraping the componentstatus endpoint in the Kubernetes API (try kubectl get componentstatus). ^rw152994871hl


Highlighted: 03/03/2021 11:12 AM
Updated: 03/03/2021 11:12 AM


#### Extras:



------

### control plane components expose internal metrics via a Prome...
>control plane components expose internal metrics via a Prometheus HTTP endpoint (&#x2F;metrics) that can be ingested into a time-series database ^rw152994874hl


Highlighted: 03/03/2021 11:12 AM
Updated: 03/03/2021 11:12 AM


#### Extras:



------

