Notes for Operating Etcd Clusters for Kubernetes

## Source:
Category: articles
Updated: 04/03/2020 05:57 PM
Highlights URL: https://readwise.io/bookreview/1577859
SourceUrl: https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/

%%1577859topstart%%
#### Extras:
**etcd****kubernetes**
%%1577859topend%%


 
-----
 ## Highlights:

### If the majority of etcd members have permanently failed, the...
>If the majority of etcd members have permanently failed, the etcd cluster is considered failed ^rw43947504hl


Highlighted: 03/23/2020 11:55 AM
Updated: 03/23/2020 05:14 PM

%%43947504start%%
#### Extras:

%%43947504end%%



------

### Scaling up etcd clusters increases availability by trading o...
>Scaling up etcd clusters increases availability by trading off performance. Scaling does not increase cluster performance nor capability ^rw43947503hl


Highlighted: 03/23/2020 11:54 AM
Updated: 03/23/2020 05:14 PM

%%43947503start%%
#### Extras:

%%43947503end%%



------

### All Kubernetes objects are stored on etcd.
>All Kubernetes objects are stored on etcd. ^rw43947502hl


Highlighted: 03/23/2020 11:51 AM
Updated: 03/23/2020 05:14 PM

%%43947502start%%
#### Extras:

%%43947502end%%



------

### etcd cluster achieves high availability by tolerating minor ...
>etcd cluster achieves high availability by tolerating minor member failures. However, to improve the overall health of the cluster, replace failed members immediately. ^rw43947501hl


Highlighted: 03/23/2020 11:47 AM
Updated: 03/23/2020 05:14 PM

%%43947501start%%
#### Extras:

%%43947501end%%



------

### Access to etcd is equivalent to root permission in the clust...
>Access to etcd is equivalent to root permission in the cluster so ideally only the API server should have access to it. ^rw43947500hl


Highlighted: 03/23/2020 11:47 AM
Updated: 03/23/2020 05:14 PM

%%43947500start%%
#### Extras:

%%43947500end%%



------

### An unstable etcd indicates that no leader is elected.
>An unstable etcd indicates that no leader is elected. ^rw43947499hl


Highlighted: 03/23/2020 11:45 AM
Updated: 03/23/2020 05:14 PM

%%43947499start%%
#### Extras:

%%43947499end%%



------

### Performance and stability of the cluster is sensitive to net...
>Performance and stability of the cluster is sensitive to network and disk IO. ^rw43947498hl


Highlighted: 03/23/2020 11:44 AM
Updated: 03/23/2020 05:14 PM

%%43947498start%%
#### Extras:

%%43947498end%%



------

### Prerequisites
Run etcd as a cluster of odd members etcd is...
>Prerequisites
Run etcd as a cluster of odd members
>etcd is a leader-based distributed system. Ensure that the leader periodically send heartbeats on time to all followers to keep the cluster stable
>Ensure that no resource starvation occurs. ^rw43947497hl


Highlighted: 03/23/2020 11:43 AM
Updated: 03/23/2020 05:14 PM

%%43947497start%%
#### Extras:

%%43947497end%%



------

