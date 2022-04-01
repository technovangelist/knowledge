Notes for Share a Cluster With Namespaces | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/05/2021 09:03 AM
Highlights URL: https://readwise.io/bookreview/8100303
SourceUrl: https://kubernetes.io/docs/tasks/administer-cluster/namespaces/

%%8100303topstart%%
#### Extras:
**Kubernetes Namespaces**
%%8100303topend%%
 
-----
 ## Highlights:

### A mechanism to attach authorization and policy to a subsecti...
>A mechanism to attach authorization and policy to a subsection of the cluster ^rw153517148hl

Comment: is attaching authorization policy to a namespace common? do you attach direct to the namespace? ^rw153517148comment

Highlighted: 03/05/2021 08:19 AM
Updated: 03/05/2021 08:43 AM

%%153517148start%%
#### Extras:
#todo 
- [ ] research attaching authorization policy to a namespace
- [ ] 
%%153517148end%%

------

### Use cases include:
>Use cases include: ^rw153517279hl

Comment: use cases for namespaces:

1. As a cluster operator, I want to support multiple user communities on a single cluster.
2. As a cluster operator, I want to delegate authority to partitions of the cluster to trusted users in those communities.
3. As a cluster operator, I want to limit the amount of resources each community can consume in order to limit the impact to other communities using the cluster.
As a cluster user, I want to interact with resources that are pertinent to my user community in isolation of what other user communities are doing on the cluster. ^rw153517279comment

Highlighted: 03/05/2021 08:22 AM
Updated: 03/05/2021 08:23 AM

%%153517279start%%
#### Extras:

%%153517279end%%

------

### When you create a Service, it creates a corresponding DNS en...
>When you create a Service, it creates a corresponding DNS entry. This entry is of the form &lt;service-name&gt;.&lt;namespace-name&gt;.svc.cluster.local, which means that if a container just uses &lt;service-name&gt; it will resolve to the service which is local to a namespace. This is useful for using the same configuration across multiple namespaces such as Development, Staging and Production. If you want to reach across namespaces, you need to use the fully qualified domain name (FQDN) ^rw153517291hl

Comment: test ^rw153517291comment

Highlighted: 03/05/2021 08:23 AM
Updated: 03/05/2021 09:03 AM

%%153517291start%%
#### Extras:

When you create a service, it creates a corresponding DNS entry of {[service-name]}.{[namespace-name].svc.cluster.local #cloze
<!--ID: 1614965751910-->

  
%%153517291end%%

------

