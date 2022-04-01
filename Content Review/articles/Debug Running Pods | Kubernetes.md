Notes for Debug Running Pods | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/03/2021 04:13 PM
Highlights URL: https://readwise.io/bookreview/8081556
SourceUrl: https://kubernetes.io/docs/tasks/debug-application-cluster/debug-running-pod/


#### Extras:
**kubernetes** **troubleshooting** **debug**

 
-----
 ## Highlights:

### If the container image includes debugging utilities, as is t...
>If the container image includes debugging utilities, as is the case with images built from Linux and Windows OS base images, you can run commands inside a specific container with kubectl exec
&gt;kubectl exec ${POD_NAME} -c ${CONTAINER_NAME} -- ${CMD} ${ARG1} ${ARG2} ... ${ARGN} ^rw153056096hl


Highlighted: 03/03/2021 04:03 PM
Updated: 03/03/2021 04:03 PM


#### Extras:






------

### Ephemeral containers are useful for interactive troubleshoot...
>Ephemeral containers are useful for interactive troubleshooting when kubectl exec is insufficient because a container has crashed or a container image doesn&#39;t include debugging utilities, such as with distroless images. kubectl has an alpha command that can create ephemeral containers for debugging beginning with version v1.18 ^rw153056150hl

Comment: this looks like a very cool feature ^rw153056150comment

Highlighted: 03/03/2021 04:04 PM
Updated: 03/03/2021 04:06 PM


#### Extras:






------

### Copying a Pod while adding a new container
Adding a new cont...
>Copying a Pod while adding a new container
Adding a new container can be useful when your application is running but not behaving as you expect and you&#39;d like to add additional troubleshooting utilities to the Pod
&gt;For example, maybe your application&#39;s container images are built on busybox but you need debugging utilities not included in busybox. You can simulate this scenario using kubectl run
&gt;kubectl run myapp --image=busybox --restart=Never -- sleep 1d
Run this command to create a copy of myapp named myapp-debug that adds a new Ubuntu container for debugging
&gt;kubectl debug myapp -it --image=ubuntu --share-processes --copy-to=myapp-debug ^rw153057016hl

Comment: that is super cool. you can make a copy of an existing pod changing the base image using the kubectl debug command. ^rw153057016comment

Highlighted: 03/03/2021 04:12 PM
Updated: 03/03/2021 04:13 PM


#### Extras:





------

