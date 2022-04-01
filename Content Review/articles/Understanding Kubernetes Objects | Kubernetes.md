Notes for Understanding Kubernetes Objects | Kubernetes

## Source:
Author: kubernetes.io
Category: articles
Updated: 03/02/2021 06:43 PM
Highlights URL: https://readwise.io/bookreview/8071240
SourceUrl: https://kubernetes.io/docs/concepts/overview/working-with-objects/kubernetes-objects/

%%8071240topstart%%
#### Extras:

%%8071240topend%%
 
-----
 ## Highlights:

### Almost every Kubernetes object includes two nested object fi...
>Almost every Kubernetes object includes two nested object fields that govern the object&#39;s configuration: the object spec and the object status. ^rw152790050hl

Comment: the object spec is the desired state. the status is the current state.

is the status determined on request or updated every interval and then on request that collected state is reported? I think it is the latter ^rw152790050comment

Highlighted: 03/02/2021 06:39 PM
Updated: 03/02/2021 06:41 PM

%%152790050start%%
#### Extras:

%%152790050end%%

------

### For example: in Kubernetes, a Deployment is an object that c...
>For example: in Kubernetes, a Deployment is an object that can represent an application running on your cluster. When you create the Deployment, you might set the Deployment spec to specify that you want three replicas of the application to be running. The Kubernetes system reads the Deployment spec and starts three instances of your desired application--updating the status to match your spec. If any of those instances should fail (a status change), the Kubernetes system responds to the difference between spec and status by making a correction--in this case, starting a replacement instance ^rw152790153hl


Highlighted: 03/02/2021 06:42 PM
Updated: 03/02/2021 06:42 PM

%%152790153start%%
#### Extras:

%%152790153end%%

------

### When you use the Kubernetes API to create the object (either...
>When you use the Kubernetes API to create the object (either directly or via kubectl), that API request must include that information as JSON in the request body. Most often, you provide the information to kubectl in a .yaml file. kubectl converts the information to JSON when making the API request. ^rw152790193hl


Highlighted: 03/02/2021 06:42 PM
Updated: 03/02/2021 06:42 PM

%%152790193start%%
#### Extras:

%%152790193end%%

------

### Required Fields
In the .yaml file for the Kubernetes object ...
>Required Fields
In the .yaml file for the Kubernetes object you want to create, you&#39;ll need to set values for the following fields
&gt;apiVersion - Which version of the Kubernetes API you&#39;re using to create this object
kind - What kind of object you want to create
metadata - Data that helps uniquely identify the object, including a name string, UID, and optional namespace
spec - What state you desire for the object ^rw152790264hl


Highlighted: 03/02/2021 06:43 PM
Updated: 03/02/2021 06:43 PM

%%152790264start%%
#### Extras:

%%152790264end%%

------

