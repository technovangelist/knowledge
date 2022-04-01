Notes for Troubleshoot Applications | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/03/2021 07:01 PM
Highlights URL: https://readwise.io/bookreview/8081002
SourceUrl: https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application/


#### Extras:
**troubleshooting** **debug**  **kubernetes** 

 
-----
 ## Highlights:

### If a Pod is stuck in Pending it means that it can not be sch...
>If a Pod is stuck in Pending it means that it can not be scheduled onto a node. Generally this is because there are insufficient resources of one type or another that prevent scheduling. Look at the output of the kubectl describe ... command above. There should be messages from the scheduler about why it can not schedule your pod. ^rw153050354hl


Highlighted: 03/03/2021 03:56 PM
Updated: 03/03/2021 03:56 PM


#### Extras:



------

### You are using hostPort: When you bind a Pod to a hostPort th...
>You are using hostPort: When you bind a Pod to a hostPort there are a limited number of places that pod can be scheduled. In most cases, hostPort is unnecessary, try using a Service object to expose your Pod. If you do require hostPort then you can only schedule as many Pods as there are nodes in your Kubernetes cluster ^rw153050537hl


Highlighted: 03/03/2021 03:57 PM
Updated: 03/03/2021 03:57 PM


#### Extras:



------

### The most common cause of Waiting pods is a failure to pull t...
>The most common cause of Waiting pods is a failure to pull the image. There are three things to check
&gt;Make sure that you have the name of the image correct.
Have you pushed the image to the repository?
Run a manual docker pull &lt;image&gt; on your machine to see if the image can be pulled. ^rw153050822hl

Comment: &lt;&#x2F;image&gt; ^rw153050822comment

Highlighted: 03/03/2021 03:57 PM
Updated: 03/03/2021 07:01 PM


#### Extras:


  
  


------

### If your pod is not behaving as you expected, it may be that ...
>If your pod is not behaving as you expected, it may be that there was an error in your pod description (e.g. mypod.yaml file on your local machine), and that the error was silently ignored when you created the pod. Often a section of the pod description is nested incorrectly, or a key name is typed incorrectly, and so the key is ignored. For example, if you misspelled command as commnd then the pod will be created but will not use the command line you intended it to use. ^rw153052433hl


Highlighted: 03/03/2021 03:58 PM
Updated: 03/03/2021 03:58 PM


#### Extras:



------

### The first thing to do is to delete your pod and try creating...
>The first thing to do is to delete your pod and try creating it again with the --validate option. For example, run kubectl apply --validate -f mypod.yaml. If you misspelled command as commnd then will give an error ^rw153052878hl


Highlighted: 03/03/2021 03:58 PM
Updated: 03/03/2021 03:58 PM


#### Extras:





------

### The next thing to check is whether the pod on the apiserver ...
>The next thing to check is whether the pod on the apiserver matches the pod you meant to create (e.g. in a yaml file on your local machine). For example, run kubectl get pods&#x2F;mypod -o yaml &gt; mypod-on-apiserver.yaml and then manually compare the original pod description, mypod.yaml with the one you got back from apiserver, mypod-on-apiserver.yaml. There will typically be some lines on the &quot;apiserver&quot; version that are not on the original version. This is expected. However, if there are lines on the original that are not on the apiserver version, then this may indicate a problem with your pod spec. ^rw153054038hl


Highlighted: 03/03/2021 03:59 PM
Updated: 03/03/2021 03:59 PM


#### Extras:



------

### Services provide load balancing across a set of pods. There ...
>Services provide load balancing across a set of pods. There are several common problems that can make Services not work properly. ^rw153054934hl


Highlighted: 03/03/2021 04:00 PM
Updated: 03/03/2021 04:00 PM


#### Extras:



------

### First, verify that there are endpoints for the service. For ...
>First, verify that there are endpoints for the service. For every Service object, the apiserver makes an endpoints resource available
&gt;You can view this resource with
&gt;kubectl get endpoints ${SERVICE_NAME} ^rw153055019hl


Highlighted: 03/03/2021 04:00 PM
Updated: 03/03/2021 04:00 PM


#### Extras:



------

### if your Service is for an nginx container with 3 replicas, y...
>if your Service is for an nginx container with 3 replicas, you would expect to see three different IP addresses in the Service&#39;s endpoints. ^rw153055099hl


Highlighted: 03/03/2021 04:00 PM
Updated: 03/03/2021 04:00 PM


#### Extras:



------

### If you are missing endpoints, try listing pods using the lab...
>If you are missing endpoints, try listing pods using the labels that Service uses. Imagine that you have a Service where the labels are
&gt;spec
&gt;selector
&gt;name: nginx
&gt;type: frontend
You can use
&gt;kubectl get pods --selector=name=nginx,type=frontend
to list pods that match this selector. Verify that the list matches the Pods that you expect to provide your Service. ^rw153055326hl


Highlighted: 03/03/2021 04:01 PM
Updated: 03/03/2021 04:01 PM


#### Extras:



------

### If the list of pods matches expectations, but your endpoints...
>If the list of pods matches expectations, but your endpoints are still empty, it&#39;s possible that you don&#39;t have the right ports exposed. If your service has a containerPort specified, but the Pods that are selected don&#39;t have that port listed, then they won&#39;t be added to the endpoints list
&gt;Verify that the pod&#39;s containerPort matches up with the Service&#39;s targetPort ^rw153055796hl


Highlighted: 03/03/2021 04:02 PM
Updated: 03/03/2021 04:02 PM


#### Extras:






------

### If you can connect to the service, but the connection is imm...
>If you can connect to the service, but the connection is immediately dropped, and there are endpoints in the endpoints list, it&#39;s likely that the proxy can&#39;t contact your pods
&gt;There are three things to check
&gt;Are your pods working correctly? Look for restart count, and debug pods.
Can you connect to your pods directly? Get the IP address for the Pod, and try to connect directly to that IP.
Is your application serving on the port that you configured? Kubernetes doesn&#39;t do port remapping, so if your application serves on 8080, the containerPort field needs to be 8080.
What&#39;s ^rw153056026hl


Highlighted: 03/03/2021 04:02 PM
Updated: 03/03/2021 04:02 PM


#### Extras:





------

