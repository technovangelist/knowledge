Notes for Datadog on Kubernetes Monitoring

## About
Author: Datadog
Title: Datadog on Kubernetes Monitoring
Category: YouTube
Published: 11/18/2020 09:21 AM
 ^ytPlypVevZfW8about

## Highlights:

Timecode: [8:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=482) ^ytPlypVevZfW8482t

Comment: ==What data do we have
Metrics server
kube-state-metrics
Deployment metadata to enable
integrations: autodiscovery== ^ytPlypVevZfW8482c

-----
Timecode: [15:27](https://www.youtube.com/watch?v=PlypVevZfW8&t=927) ^ytPlypVevZfW8927t

Comment: ==the problems with rolling out via daemonset was that you could not control the speed of rollout and it would overload the controller== ^ytPlypVevZfW8927c

-----
Timecode: [16:21](https://www.youtube.com/watch?v=PlypVevZfW8&t=981) ^ytPlypVevZfW8981t

Comment: ==extended daemonset
oss controller
Open Source
Custom Rolling Update
Canary Deployment
ExtendedDaemonsetSetting== ^ytPlypVevZfW8981c

-----
Timecode: [31:34](https://www.youtube.com/watch?v=PlypVevZfW8&t=1894) ^ytPlypVevZfW81894t

Comment: ==Liveness/readiness probes
Used to restart containers
direct traffic
command, HTTP, TCP
Defined by the workload owners== ^ytPlypVevZfW81894c

-----
Timecode: [31:43](https://www.youtube.com/watch?v=PlypVevZfW8&t=1903) ^ytPlypVevZfW81903t

Comment: ==first thing to check for monitoring the workloads: are the nodes running== ^ytPlypVevZfW81903c

-----
Timecode: [32:45](https://www.youtube.com/watch?v=PlypVevZfW8&t=1965) ^ytPlypVevZfW81965t

Comment: ==example of liveness proble config
livenessProbe:
initialDelaySeconds: 20
failure Threshold: 6
httpGet:
path: /live
port: 5555
scheme: HTTP
periodSeconds: 15
successThreshold: 1
timeoutSeconds: 5
[. . . ]== ^ytPlypVevZfW81965c

-----
Timecode: [35:00](https://www.youtube.com/watch?v=PlypVevZfW8&t=2100) ^ytPlypVevZfW82100t

Comment: ==as the number of apps, nodes, services, etc go up, tagging becomes very important== ^ytPlypVevZfW82100c

-----
Timecode: [36:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=2162) ^ytPlypVevZfW82162t

Comment: ==default tags: 
Metadata (auto)
image_name,
image_tag,
chart_name,
pod_name,
kube_cluster_name,
kube_namespace
Custom tagging
Kubernetes labels
Environment variables
Agent configuration== ^ytPlypVevZfW82162c

-----
Timecode: [36:29](https://www.youtube.com/watch?v=PlypVevZfW8&t=2189) ^ytPlypVevZfW82189t

Comment: ==unified tagging: env, service, version== ^ytPlypVevZfW82189c

-----
Timecode: [40:12](https://www.youtube.com/watch?v=PlypVevZfW8&t=2412) ^ytPlypVevZfW82412t

Comment: ==the four golden signals
latency
errors
traffic
saturation== ^ytPlypVevZfW82412c

-----
Timecode: [8:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=482) ^ytPlypVevZfW8482t

Comment: ==What data do we have
Metrics server
kube-state-metrics
Deployment metadata to enable
integrations: autodiscovery== ^ytPlypVevZfW8482c

-----
Timecode: [15:27](https://www.youtube.com/watch?v=PlypVevZfW8&t=927) ^ytPlypVevZfW8927t

Comment: ==the problems with rolling out via daemonset was that you could not control the speed of rollout and it would overload the controller== ^ytPlypVevZfW8927c

-----
Timecode: [16:21](https://www.youtube.com/watch?v=PlypVevZfW8&t=981) ^ytPlypVevZfW8981t

Comment: ==extended daemonset
oss controller
Open Source
Custom Rolling Update
Canary Deployment
ExtendedDaemonsetSetting== ^ytPlypVevZfW8981c

-----
Timecode: [31:34](https://www.youtube.com/watch?v=PlypVevZfW8&t=1894) ^ytPlypVevZfW81894t

Comment: ==Liveness/readiness probes
Used to restart containers
direct traffic
command, HTTP, TCP
Defined by the workload owners== ^ytPlypVevZfW81894c

-----
Timecode: [31:43](https://www.youtube.com/watch?v=PlypVevZfW8&t=1903) ^ytPlypVevZfW81903t

Comment: ==first thing to check for monitoring the workloads: are the nodes running== ^ytPlypVevZfW81903c

-----
Timecode: [32:45](https://www.youtube.com/watch?v=PlypVevZfW8&t=1965) ^ytPlypVevZfW81965t

Comment: ==example of liveness proble config
livenessProbe:
initialDelaySeconds: 20
failure Threshold: 6
httpGet:
path: /live
port: 5555
scheme: HTTP
periodSeconds: 15
successThreshold: 1
timeoutSeconds: 5
[. . . ]== ^ytPlypVevZfW81965c

-----
Timecode: [35:00](https://www.youtube.com/watch?v=PlypVevZfW8&t=2100) ^ytPlypVevZfW82100t

Comment: ==as the number of apps, nodes, services, etc go up, tagging becomes very important== ^ytPlypVevZfW82100c

-----
Timecode: [36:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=2162) ^ytPlypVevZfW82162t

Comment: ==default tags: 
Metadata (auto)
image_name,
image_tag,
chart_name,
pod_name,
kube_cluster_name,
kube_namespace
Custom tagging
Kubernetes labels
Environment variables
Agent configuration== ^ytPlypVevZfW82162c

-----
Timecode: [36:29](https://www.youtube.com/watch?v=PlypVevZfW8&t=2189) ^ytPlypVevZfW82189t

Comment: ==unified tagging: env, service, version== ^ytPlypVevZfW82189c

-----
Timecode: [40:12](https://www.youtube.com/watch?v=PlypVevZfW8&t=2412) ^ytPlypVevZfW82412t

Comment: ==the four golden signals
latency
errors
traffic
saturation== ^ytPlypVevZfW82412c

-----
Timecode: [8:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=482) ^ytPlypVevZfW8482t

Comment: ==What data do we have
Metrics server
kube-state-metrics
Deployment metadata to enable
integrations: autodiscovery== ^ytPlypVevZfW8482c

-----
Timecode: [15:27](https://www.youtube.com/watch?v=PlypVevZfW8&t=927) ^ytPlypVevZfW8927t

Comment: ==the problems with rolling out via daemonset was that you could not control the speed of rollout and it would overload the controller== ^ytPlypVevZfW8927c

-----
Timecode: [16:21](https://www.youtube.com/watch?v=PlypVevZfW8&t=981) ^ytPlypVevZfW8981t

Comment: ==extended daemonset
oss controller
Open Source
Custom Rolling Update
Canary Deployment
ExtendedDaemonsetSetting== ^ytPlypVevZfW8981c

-----
Timecode: [31:34](https://www.youtube.com/watch?v=PlypVevZfW8&t=1894) ^ytPlypVevZfW81894t

Comment: ==Liveness/readiness probes
Used to restart containers
direct traffic
command, HTTP, TCP
Defined by the workload owners== ^ytPlypVevZfW81894c

-----
Timecode: [31:43](https://www.youtube.com/watch?v=PlypVevZfW8&t=1903) ^ytPlypVevZfW81903t

Comment: ==first thing to check for monitoring the workloads: are the nodes running== ^ytPlypVevZfW81903c

-----
Timecode: [32:45](https://www.youtube.com/watch?v=PlypVevZfW8&t=1965) ^ytPlypVevZfW81965t

Comment: ==example of liveness proble config
livenessProbe:
initialDelaySeconds: 20
failure Threshold: 6
httpGet:
path: /live
port: 5555
scheme: HTTP
periodSeconds: 15
successThreshold: 1
timeoutSeconds: 5
[. . . ]== ^ytPlypVevZfW81965c

-----
Timecode: [35:00](https://www.youtube.com/watch?v=PlypVevZfW8&t=2100) ^ytPlypVevZfW82100t

Comment: ==as the number of apps, nodes, services, etc go up, tagging becomes very important== ^ytPlypVevZfW82100c

-----
Timecode: [36:02](https://www.youtube.com/watch?v=PlypVevZfW8&t=2162) ^ytPlypVevZfW82162t

Comment: ==default tags: 
Metadata (auto)
image_name,
image_tag,
chart_name,
pod_name,
kube_cluster_name,
kube_namespace
Custom tagging
Kubernetes labels
Environment variables
Agent configuration== ^ytPlypVevZfW82162c

-----
Timecode: [36:29](https://www.youtube.com/watch?v=PlypVevZfW8&t=2189) ^ytPlypVevZfW82189t

Comment: ==unified tagging: env, service, version== ^ytPlypVevZfW82189c

-----
Timecode: [40:12](https://www.youtube.com/watch?v=PlypVevZfW8&t=2412) ^ytPlypVevZfW82412t

Comment: ==the four golden signals
latency
errors
traffic
saturation== ^ytPlypVevZfW82412c

## Video Description on YouTube:
With many blog posts published and talks given on the topic, it’s no secret that Datadog is running Kubernetes at scale. We currently run dozens of clusters, some of them with thousands of nodes. Additionally, we have clusters running in multiple clouds. How are we monitoring all of that, ensuring we can scale up quickly and safely?

In this session Ara Pulido, Technical Evangelist, will chat with Celene Chang and Charly Fontaine - both software engineers on the Container Integrations team at Datadog. This team is responsible for deploying and running the Datadog Agent in our Kubernetes clusters. We’ll cover how we are running the Datadog Agent in our clusters, which metrics we care about, and the monitors we have set up. By the end of the session you will have new ideas and best practices on monitoring Kubernetes with Datadog that you can apply in your own environment.

Links mentioned in the talk
ExtendedDaemonset Github: https://github.com/DataDog/extendeddaemonset
Watermark Pod Autoscaler Github: https://github.com/DataDog/watermarkpodautoscaler
How to monitor Kubernetes audit logs: https://www.datadoghq.com/blog/monitor-kubernetes-audit-logs/
Explore Kubernetes resources with Datadog Live Containers: https://www.datadoghq.com/blog/explore-kubernetes-resources-with-datadog/

00:00 - Intro
02:01 - Main discussion
06:19 - Kubernetes Monitoring 101
14:36 - Best practices: Agent deployment
18:28 - Best practices: Platform monitoring
29:23 - Best practices: Audit logs
31:08 - Best practices: Workload monitoring
34:36 - Best practices: Tagging
38:45 - Autoscaling
48:48 - KubeCon discussion
53:29 - Q&A