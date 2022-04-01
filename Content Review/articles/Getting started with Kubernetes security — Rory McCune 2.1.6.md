Notes for Getting started with Kubernetes security — Rory McCune 2.1.6

## Source:
Author: Kubernetes Community Days UK
Category: articles
Updated: 12/27/2021 10:42 PM
Highlights URL: https://readwise.io/bookreview/12486006
SourceUrl: https://youtu.be/W2q91qvr4gc

%%12486006topstart%%
#### Extras:
super interesting talk about quick wins on securing your **kubernetes** cluster. **rory mccune**  **security**
%%12486006topend%%


 
-----
 ## Highlights:

### mess up threshold. how many mess ups do you need to see a ma...
>mess up threshold. how many mess ups do you need to see a major security event. you don&amp;apos;t want it to be 1. many things should need to happen for there to be a security incident. or at least more than 1. ^rw263173469hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=571 ^rw263173469comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173469start%%
#### Extras:

%%263173469end%%



------

### an easy win is to make sure your cluster, or your api server...
>an easy win is to make sure your cluster, or your api server is never on the Internet directly. ^rw263173470hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=830 ^rw263173470comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173470start%%
#### Extras:

%%263173470end%%



------

### use managed kubernetes if you can. this means using the kube...
>use managed kubernetes if you can. this means using the kubernetes offered by google&#x2F;azure&#x2F;aws&#x2F;etc. they have the expertise to ensure the control plane is secure. ^rw263173471hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=881 ^rw263173471comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173471start%%
#### Extras:

%%263173471end%%



------

### dont mount service accountt tokens unless required.
>dont mount service accountt tokens unless required. ^rw263173472hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=949 ^rw263173472comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173472start%%
#### Extras:

%%263173472end%%



------

### default deny network policies. by default every container ca...
>default deny network policies. by default every container can reach out on the kubernetes network to any other container . ^rw263173473hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1044 ^rw263173473comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173473start%%
#### Extras:

%%263173473end%%



------

### set the security context on workloads.
>set the security context on workloads. ^rw263173474hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1163 ^rw263173474comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173474start%%
#### Extras:

%%263173474end%%



------

### securitycontext:privileged: false.  containers in most cases...
>securitycontext:privileged: false.  containers in most cases should not be privileged. ^rw263173475hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1184 ^rw263173475comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173475start%%
#### Extras:

%%263173475end%%



------

### securitycontext:allowPrivilegeEscalation: false. this is not...
>securitycontext:allowPrivilegeEscalation: false. this is not on by default. means a container could start without privilege and then request the higher access. ^rw263173476hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1224 ^rw263173476comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173476start%%
#### Extras:

%%263173476end%%



------

### dont ever run as root.
>dont ever run as root. ^rw263173477hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1288 ^rw263173477comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173477start%%
#### Extras:

%%263173477end%%



------

### securitycontextt:readOnlyRootFilesystem: true. when someone ...
>securitycontextt:readOnlyRootFilesystem: true. when someone gains access to your container they will look for a way to write tools to the machine. if they cannot they may move on to an easier machine and give up. ^rw263173478hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1369 ^rw263173478comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173478start%%
#### Extras:

%%263173478end%%



------

### securitycontext:capabilities:drop:all if your apps don&apos;...
>securitycontext:capabilities:drop:all if your apps don&amp;apos;t need the capabilities don&amp;apos;t take them. ^rw263173479hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1434 ^rw263173479comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173479start%%
#### Extras:

%%263173479end%%



------

### use an internal container registry that you control.
>use an internal container registry that you control. ^rw263173480hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1703 ^rw263173480comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173480start%%
#### Extras:

%%263173480end%%



------

### look into using kube-bench, trivy.
>look into using kube-bench, trivy. ^rw263173481hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1745 ^rw263173481comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173481start%%
#### Extras:

%%263173481end%%



------

### #timestamp
>#timestamp ^rw263173482hl

Comment: https:&#x2F;&#x2F;youtu.be&#x2F;W2q91qvr4gc?t=1809 ^rw263173482comment

Highlighted: 12/27/2021 10:42 PM
Updated: 12/27/2021 10:42 PM

%%263173482start%%
#### Extras:

%%263173482end%%



------

