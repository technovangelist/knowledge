Notes for Key Metrics for Monitoring AWS Fargate | Datadog

## Source:
Author: David M. Lentz
Category: articles
Updated: 03/01/2021 09:00 PM
Highlights URL: https://readwise.io/bookreview/8055079
SourceUrl: https://www.datadoghq.com/blog/aws-fargate-metrics/


#### Extras:
**Elastic Container Service** **EKS** **Fargate** **serverless**  **scheduler**

 
-----
 ## Highlights:

### Fargate is similar to serverless container platforms from Go...
>Fargate is similar to serverless container platforms from Google (Cloud Run) and Microsoft (AKS virtual nodes). ^rw152371079hl

Comment: aws fargate vs the others ^rw152371079comment

Highlighted: 03/01/2021 11:37 AM
Updated: 03/01/2021 11:37 AM


#### Extras:

What is the Google equivalent of AWS Fargate? #flashcard 
Google Cloud Run
<!--ID: 1614629174787-->


What is the Microsoft equivalent of AWS Fargate? #flashcard 
AKS virtual nodes
<!--ID: 1614629174792-->




------

### Fargate’s serverless infrastructure
>Fargate’s serverless infrastructure ^rw152371212hl

Comment: is serverless the right term here? ^rw152371212comment

Highlighted: 03/01/2021 11:38 AM
Updated: 03/01/2021 11:38 AM


#### Extras:



------

### When you use Fargate, you don’t need to create and manage th...
>When you use Fargate, you don’t need to create and manage the EC2 instances that host your containers. Instead, Fargate automatically launches compute resources, which are instances provisioned from a Fargate-specific fleet. These compute resources are owned and managed by AWS; they’re not created within your account and do not run in your VPC. ^rw152371345hl

Comment: so can you use your own vpc with fargate? ^rw152371345comment

Highlighted: 03/01/2021 11:41 AM
Updated: 03/01/2021 11:41 AM


#### Extras:



------

### Fargate schedules a single workload on each compute resource...
>Fargate schedules a single workload on each compute resource it creates, which is sized specifically for that workload ^rw152371429hl

Comment: when using ec2 backed ecs or eks, you specify the size of the ec2 instances and workloads are added to them. multiple workloads are added till all resources on the instance are used up. with fargate, the compute resource is created based on the resource needs of the workload so each workload gets its own compute resource created. ^rw152371429comment

Highlighted: 03/01/2021 11:42 AM
Updated: 03/01/2021 11:51 AM


#### Extras:



------

### If the orchestrator cannot locate an EC2 instance that has r...
>If the orchestrator cannot locate an EC2 instance that has resources available to accommodate the new workload, it will not be able to schedule the workload (unless you have configured the cluster to use autoscaling). ^rw152371495hl

Comment: when your ec2 instances have an amount of resources even slightly below what is required of the workload, the workload will not be scheduled. (assuming autoscaling not being used.). Fargate will schedule no matter what.  though there are probably some limits? ^rw152371495comment

Highlighted: 03/01/2021 11:45 AM
Updated: 03/01/2021 11:46 AM


#### Extras:



------

### Each EC2 instance costs a flat hourly rate regardless of the...
>Each EC2 instance costs a flat hourly rate regardless of the number of containers the scheduler has placed there ^rw152371548hl

Comment: with fargate you pay for the resources used by the compute resources for the active workloads. with ecs or eks you pay for the compute resources available from your ec2&#39;s no matter whether you are actively using them or not ^rw152371548comment

Highlighted: 03/01/2021 11:47 AM
Updated: 03/01/2021 11:48 AM


#### Extras:
 


------

### The general differences we’ve discussed in this section betw...
>The general differences we’ve discussed in this section between EC2-backed containers and Fargate-backed containers apply to both ECS and EKS ^rw152372696hl

Comment: ecs and eks can be backed by fargate or by ec2 ^rw152372696comment

Highlighted: 03/01/2021 11:51 AM
Updated: 03/01/2021 11:51 AM


#### Extras:
I think this is something I didn't quite get before

AWS ECS and EKS compute resources can be provided by what two services? #flashcard 
EC2 and Fargate
<!--ID: 1614628784794-->




------

### If you’re running Linux containers, you have the option to l...
>If you’re running Linux containers, you have the option to launch ECS workloads onto Fargate compute resources, your own EC2 instances, or both—but you can only run Windows containers on EC2 instances ^rw152443780hl

Comment: ecs with windows can only use ec2. no fargate for windows ^rw152443780comment

Highlighted: 03/01/2021 04:31 PM
Updated: 03/01/2021 04:32 PM


#### Extras:



------

### ECS allows you to group your containers into logical units c...
>ECS allows you to group your containers into logical units called tasks. You can launch multiple copies of a task as a service, and ECS will automatically ensure that your desired number of copies is running. Your task definition specifies the details of your task, including the task size—the amount of memory and CPU that your task requires. You must specify these values in the cpu and memory keys of your task definition file, and they must align with one of the combinations listed in the Fargate supported configurations table—otherwise, AWS will return an error. ^rw152484536hl

Comment: so fargate defines a list of acceptable cpu and memory sizes. you must choose a valid size else it fails to schedule ^rw152484536comment

Highlighted: 03/01/2021 07:28 PM
Updated: 03/01/2021 07:29 PM


#### Extras:



------

### You can optionally specify container-level resources in the ...
>You can optionally specify container-level resources in the containerDefinitions object within the task definition ^rw152516686hl


Highlighted: 03/01/2021 08:16 PM
Updated: 03/01/2021 08:16 PM


#### Extras:

What object defines container level resources within the task definition for ECS? #flashcard 
containerDefinitions
<!--ID: 1614658797744-->




------

### When you create an ECS cluster, you can designate a capacity...
>When you create an ECS cluster, you can designate a capacity provider to specify the type of infrastructure on which your tasks will run: your own EC2 instances, Fargate, or Fargate Spot, which makes Fargate infrastructure available at a reduced (but variable) price determined by market demand. You can combine multiple capacity providers in a capacity provider strategy and assign a weight to each capacity provider to determine the mix of infrastructure that will support your cluster ^rw152523492hl

Comment: capacity provider strategy looks very interesting. can set a weight per provider to use more or less fargate vs ec2 ^rw152523492comment

Highlighted: 03/01/2021 08:48 PM
Updated: 03/01/2021 08:49 PM


#### Extras:



------

### Each Fargate compute resource runs a single pod
>Each Fargate compute resource runs a single pod ^rw152523589hl

Comment: with fargate and eks, each pod runs in a compute resource. (vs each task in ecs) ^rw152523589comment

Highlighted: 03/01/2021 08:50 PM
Updated: 03/01/2021 08:51 PM


#### Extras:



------

### A Deployment defines a logical collection of pods, and Kuber...
>A Deployment defines a logical collection of pods, and Kubernetes automatically replaces pods in a Deployment if they become unavailable ^rw152523618hl


Highlighted: 03/01/2021 08:51 PM
Updated: 03/01/2021 08:51 PM


#### Extras:



------

### You can use a Kubernetes Service to assign a stable IP addre...
>You can use a Kubernetes Service to assign a stable IP address for a group of pods that make up a single application, even as the addresses of pods themselves change as Kubernetes replaces failed pods. ^rw152523621hl


Highlighted: 03/01/2021 08:51 PM
Updated: 03/01/2021 08:51 PM


#### Extras:



------

### DaemonSets—which ensure that a replica of a designated pod i...
>DaemonSets—which ensure that a replica of a designated pod is running on all nodes in your cluster—are not supported by Fargate. ^rw152523664hl

Comment: since there is no notion of nodes in a fargate backed eks, there can be no daemonset which define a minimum number of replicas per node ^rw152523664comment

Highlighted: 03/01/2021 08:51 PM
Updated: 03/01/2021 08:52 PM


#### Extras:



------

### In EKS, you can create one or more Fargate profiles, which s...
>In EKS, you can create one or more Fargate profiles, which specify selectors—a namespace and zero or more labels—that determine which pods in your cluster will run on Fargate. ^rw152523701hl

Comment: instead of the capacity provider strategy in ecs, you can define multiple fargate profiles with different selectors determine with pods run on fargate ^rw152523701comment

Highlighted: 03/01/2021 08:53 PM
Updated: 03/01/2021 08:55 PM


#### Extras:



------

### Once you’ve associated a Fargate profile with your EKS clust...
>Once you’ve associated a Fargate profile with your EKS cluster, AWS automatically detects which pods match the ones you’ve specified in your profile, and launches them on Fargate ^rw152523802hl


Highlighted: 03/01/2021 08:55 PM
Updated: 03/01/2021 08:57 PM


#### Extras:



------

### For example, consider a pod comprised of an init container w...
>For example, consider a pod comprised of an init container whose memory request value is 2 GB, and two application containers: an NGINX container with a memory request of 1 GB and a Redis container with a memory request of 3 GB. Fargate would select a resource combination whose memory value is nearest to (but not lower than) 4.25 GB—the sum of the application containers&#39; memory requests plus 256 MB. Fargate would launch a compute resource with 5 GB of memory to run this pod. ^rw152523970hl

Comment: hmm, so is it possible that a fargate resource will consume more resources from eks than from ecs because of the k8s overhead? ^rw152523970comment

Highlighted: 03/01/2021 08:57 PM
Updated: 03/01/2021 08:58 PM


#### Extras:



------

### Monitoring Fargate will also help you understand costs, whic...
>Monitoring Fargate will also help you understand costs, which are determined by the number of tasks or pods you run, the amount of time you run them, and the memory and CPU allocated to each compute resource. ^rw152524110hl

Comment: its potentially easy for costs to run away from you if you aren&#39;t monitoring them ^rw152524110comment

Highlighted: 03/01/2021 08:58 PM
Updated: 03/01/2021 08:59 PM


#### Extras:



------

### If you’ve underprovisioned resources, your cluster may not p...
>If you’ve underprovisioned resources, your cluster may not perform well due to resource constraints. On the other hand, if you’ve overprovisioned resources, you could end up paying more for Fargate than necessary ^rw152524139hl


Highlighted: 03/01/2021 09:00 PM
Updated: 03/01/2021 09:00 PM


#### Extras:
Tags: ecs eks fargate


------

