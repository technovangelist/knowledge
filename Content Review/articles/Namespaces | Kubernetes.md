Notes for Namespaces | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/03/2021 03:36 PM
Highlights URL: https://readwise.io/bookreview/8080564
SourceUrl: https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/

%%8080564topstart%%
#### Extras:
**kubernetes**
%%8080564topend%%
 
-----
 ## Highlights:

### Kubernetes supports multiple virtual clusters backed by the ...
>Kubernetes supports multiple virtual clusters backed by the same physical cluster. These virtual clusters are called namespaces. ^rw153045482hl


Highlighted: 03/03/2021 03:34 PM
Updated: 03/03/2021 03:34 PM

%%153045482start%%
#### Extras:

%%153045482end%%

------

### For clusters with a few to tens of users, you should not nee...
>For clusters with a few to tens of users, you should not need to create or think about namespaces at all ^rw153045618hl


Highlighted: 03/03/2021 03:34 PM
Updated: 03/03/2021 03:34 PM

%%153045618start%%
#### Extras:

%%153045618end%%

------

### Names of resources need to be unique within a namespace, but...
>Names of resources need to be unique within a namespace, but not across namespaces ^rw153045942hl


Highlighted: 03/03/2021 03:34 PM
Updated: 03/03/2021 03:34 PM

%%153045942start%%
#### Extras:

%%153045942end%%

------

### Avoid creating namespace with prefix kube-, since it is rese...
>Avoid creating namespace with prefix kube-, since it is reserved for Kubernetes system namespaces ^rw153046070hl


Highlighted: 03/03/2021 03:35 PM
Updated: 03/03/2021 03:35 PM

%%153046070start%%
#### Extras:

%%153046070end%%

------

### When you create a Service, it creates a corresponding DNS en...
>When you create a Service, it creates a corresponding DNS entry. This entry is of the form &lt;service-name&gt;.&lt;namespace-name&gt;.svc.cluster.local, which means that if a container just uses &lt;service-name&gt;, it will resolve to the service which is local to a namespace. ^rw153046117hl


Highlighted: 03/03/2021 03:35 PM
Updated: 03/03/2021 03:35 PM

%%153046117start%%
#### Extras:

%%153046117end%%

------

### namespace resources are not themselves in a namespace. And l...
>namespace resources are not themselves in a namespace. And low-level resources, such as nodes and persistentVolumes, are not in any namespace ^rw153046119hl


Highlighted: 03/03/2021 03:36 PM
Updated: 03/03/2021 03:36 PM

%%153046119start%%
#### Extras:

%%153046119end%%

------

### To see which Kubernetes resources are and aren't in a namesp...
>To see which Kubernetes resources are and aren&#39;t in a namespace
&gt;In a namespace
kubectl api-resources --namespaced=true
&gt;Not in a namespace
kubectl api-resources --namespaced=false ^rw153046122hl


Highlighted: 03/03/2021 03:36 PM
Updated: 03/03/2021 03:36 PM

%%153046122start%%
#### Extras:

%%153046122end%%

------

