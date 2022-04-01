Notes for Key Kubernetes Audit Logs for Monitoring Cluster Security | Datadog

## Source:
Author: datadoghq.com
Category: articles
Updated: 02/04/2021 09:36 AM
Highlights URL: https://readwise.io/bookreview/7542680
SourceUrl: https://www.datadoghq.com/blog/key-kubernetes-audit-logs-for-monitoring-cluster-security/

%%7542680topstart%%
#### Extras:
in case you haven’t seen any great examples showing the use of the security signals feature of datadog, this article ([https://www.datadoghq.com/blog/key-kubernetes-audit-logs-for-monitoring-cluster-security/](https://www.datadoghq.com/blog/key-kubernetes-audit-logs-for-monitoring-cluster-security/)) does a great job of going through it. Explains the issues that can come up in k8s, why you should pay attention, how datadog points you to the issue. too many articles on the web just show what to do, but I really like how this one really covers the ‘why’.
%%7542680topend%%


 
-----
 ## Highlights:

### In the screenshot above, Datadog detected a user’s attempt t...
>In the screenshot above, Datadog detected a user’s attempt to launch an interactive shell in a running pod via the kubectl exec command. Most users should not need to run commands in a pod, so you should investigate further to ensure that the user’s account isn’t compromised ^rw141337182hl

Comment: ![](https://imgix.datadoghq.com/img/blog/key-kubernetes-audit-logs-for-monitoring-cluster-security/kubernetes_audit_logs_security_user_exec.png?auto=format&fit=max&w=698&dpr=2) ^rw141337182comment

Highlighted: 02/04/2021 09:36 AM
Updated: 02/04/2021 09:36 AM

%%141337182start%%
#### Extras:

%%141337182end%%



------

### Datadog offers a built-in Kubernetes audit log integration, ...
>Datadog offers a built-in Kubernetes audit log integration, so you can easily track environment activity in real time. To start collecting your audit logs, you will need to deploy the Datadog Agent to your Kubernetes environment, then enable log collection. ^rw141335434hl


Highlighted: 02/04/2021 09:34 AM
Updated: 02/04/2021 09:34 AM

%%141335434start%%
#### Extras:

%%141335434end%%



------

### You should also monitor for attempts to create a ClusterRole...
>You should also monitor for attempts to create a ClusterRoleBinding that attaches an account to the cluster-admin role. An account with this role binding has full control over every resource in the cluster and in all namespaces. If you see this activity in your audit logs, you should investigate further to ensure that the account isn’t compromised. You can find all of this information in your audit logs' authorization.k8s.io/reason attribute. ^rw141335425hl


Highlighted: 02/04/2021 09:34 AM
Updated: 02/04/2021 09:34 AM

%%141335425start%%
#### Extras:

%%141335425end%%



------

### The cluster-admin role in RBAC policies gives accounts super...
>The cluster-admin role in RBAC policies gives accounts super-user access to any resource ^rw141335408hl


Highlighted: 02/04/2021 09:34 AM
Updated: 02/04/2021 09:34 AM

%%141335408start%%
#### Extras:

%%141335408end%%



------

### Privileged containers are particularly valuable to attackers...
>Privileged containers are particularly valuable to attackers because they provide unfettered access to other malicious activity, such as privilege escalation ^rw141335355hl


Highlighted: 02/04/2021 09:33 AM
Updated: 02/04/2021 09:33 AM

%%141335355start%%
#### Extras:

What kind of container is particularly valuable to attackers since it provides unfettered access to other malicious activity, such as access escalation? #flashcard 
Privileged Containers
<!--ID: 1612592376132-->

%%141335355end%%




------

### If you notice the same service account or IP address creatin...
>If you notice the same service account or IP address creating new pods or host mounts on a node, you may need to scale back that account’s permissions or update your admission controllers ^rw141335352hl


Highlighted: 02/04/2021 09:33 AM
Updated: 02/04/2021 09:33 AM

%%141335352start%%
#### Extras:



%%141335352end%%



------

### Attackers will often look for a service account (or create a...
>Attackers will often look for a service account (or create a new account) that has the ability to attach pods to the host network or create new pods in a preconfigured namespace, such as kube-system or kube-public. This allows them to communicate with other pods in the namespace, create pods with privileged containers, mount hostPath volumes on a node for unrestricted access to the host’s file system, or deploy a DaemonSet to easily control every node in a cluster. ^rw141335348hl


Highlighted: 02/04/2021 09:33 AM
Updated: 02/04/2021 09:33 AM

%%141335348start%%
#### Extras:

%%141335348end%%



------

### It’s important to note that managed Kubernetes services (e.g...
>It’s important to note that managed Kubernetes services (e.g., Google Kubernetes Engine, Amazon Elastic Kubernetes Service) generally disable anonymous access, but it is still an important configuration to check ^rw141335299hl


Highlighted: 02/04/2021 09:32 AM
Updated: 02/04/2021 09:32 AM

%%141335299start%%
#### Extras:

%%141335299end%%



------

### With access to the API server, an attacker will attempt to f...
>With access to the API server, an attacker will attempt to find and control other resources in your environment, such as service accounts and pods ^rw141335107hl

Comment: and k8s allows anonymous requests to the api server by default. whoa ^rw141335107comment

Highlighted: 02/04/2021 09:31 AM
Updated: 02/04/2021 09:31 AM

%%141335107start%%
#### Extras:

%%141335107end%%



------

### On the other hand, policies that collect audit events from e...
>On the other hand, policies that collect audit events from endpoints not directly related to cluster activity, such as /healthz or /version, create noise. ^rw141334849hl


Highlighted: 02/04/2021 09:29 AM
Updated: 02/04/2021 09:29 AM

%%141334849start%%
#### Extras:

%%141334849end%%



------

### For instance, a policy that doesn’t collect data about pod a...
>For instance, a policy that doesn’t collect data about pod activity makes it more difficult to know when an unauthorized account creates new pods with privileged containers ^rw141334846hl


Highlighted: 02/04/2021 09:28 AM
Updated: 02/04/2021 09:28 AM

%%141334846start%%
#### Extras:

%%141334846end%%



------

### The server filters these events through an audit policy. An ...
>The server filters these events through an audit policy. An audit policy is a set of rules that specifies which audit events should be recorded and where they should be sent, for example to either a JSON log file or an external API backend for storage. ^rw141334675hl

Comment: ![](https://imgix.datadoghq.com/img/blog/key-kubernetes-audit-logs-for-monitoring-cluster-security/kubernetes_audit_logs_security_diagram.png?auto=format&fit=max&w=698&dpr=2) ^rw141334675comment

Highlighted: 02/04/2021 09:27 AM
Updated: 02/04/2021 09:28 AM

%%141334675start%%
#### Extras:

%%141334675end%%



------

### When a request comes in to the Kubernetes API server, it can...
>When a request comes in to the Kubernetes API server, it can create one of several different audit events such as creating a new pod or service account ^rw141334670hl


Highlighted: 02/04/2021 09:27 AM
Updated: 02/04/2021 09:27 AM

%%141334670start%%
#### Extras:

%%141334670end%%



------

### Kubernetes audit logs provide a complete record of activity ...
>Kubernetes audit logs provide a complete record of activity (e.g., the who, where, when, and how) in your Kubernetes control plane. Monitoring your audit logs can be invaluable in helping you detect and mitigate misconfigurations or abuse of Kubernetes resources before confidential data is compromised. However, Kubernetes components and services can generate millions of log events per day, so knowing which logs to focus on is difficult. ^rw141334580hl


Highlighted: 02/04/2021 09:26 AM
Updated: 02/04/2021 09:26 AM

%%141334580start%%
#### Extras:

%%141334580end%%



------

