Notes for “Let’s Use Kubernetes!” Now You Have 8 Problems

## Source:
Author: Itamar Turner-Trauring
Category: articles
Updated: 02/05/2021 03:46 PM
Highlights URL: https://readwise.io/bookreview/1548108
SourceUrl: https://pythonspeed.com/articles/dont-need-kubernetes/


#### Extras:
**Itamar Turner-Trauring**

 
-----
 ## Highlights:

### So already you’re talking about two machines or virtual mach...
>So already you’re talking about two machines or virtual machines just to get anything at all done. And that just gives you … one machine ^rw141751601hl


Highlighted: 02/05/2021 03:46 PM
Updated: 02/05/2021 03:46 PM
https://instapaper.com/read/1284918897/15419661


#### Extras:



------

### Kubernetes is a distributed system: there’s a main machine t...
>Kubernetes is a distributed system: there’s a main machine that controls worker machines. Work is scheduled across different worker machines. Each machine then runs the work in containers ^rw141751599hl


Highlighted: 02/05/2021 03:44 PM
Updated: 02/05/2021 03:46 PM
https://instapaper.com/read/1284918897/15419655


#### Extras:
**kubernetes**


------

### Kubernetes has plenty of moving parts—concepts, subsystems, ...
>Kubernetes has plenty of moving parts—concepts, subsystems, processes, machines, code—and that means plenty of problems ^rw141751240hl


Highlighted: 02/05/2021 03:42 PM
Updated: 02/05/2021 03:46 PM
https://instapaper.com/read/1284918897/15419650


#### Extras:
this is a test


------

### And if what you care about is downtime, your first thought s...
>And if what you care about is downtime, your first thought shouldn’t be “how do I reduce deployment downtime from 1 second to 1ms”, it should be “how can I ensure database schema changes don’t prevent rollback if I screw something up.” ^rw43203487hl


Highlighted: 03/12/2020 10:00 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### The features Kubernetes provides for reliability (health che...
>The features Kubernetes provides for reliability (health checks, rolling deploys), can be implemented much more simply, or already built-in in many cases. For example, nginx can do health checks on worker processes, and you can use docker-autoheal or something similar to automatically restart those processes. ^rw43203486hl


Highlighted: 03/12/2020 09:59 AM
Updated: 02/05/2021 03:46 PM


#### Extras:
**Docker**


------

### Distributed applications are hard to debug. You need whole n...
>Distributed applications are hard to debug. You need whole new categories of instrumentation and logging to getting understanding that isn’t quite as good as what you’d get from the logs of a monolithic application. ^rw43203485hl


Highlighted: 03/12/2020 09:58 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### Distributed applications are really hard to write correctly....
>Distributed applications are really hard to write correctly. Really. The more moving parts, the more these problems come in to play. ^rw43203484hl


Highlighted: 03/12/2020 09:58 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### There are plenty of imperfect solutions to choose; the simpl...
>There are plenty of imperfect solutions to choose; the simplest and best solution is to not use Kubernetes. ^rw43203483hl


Highlighted: 03/12/2020 09:58 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### The more you buy in to Kubernetes, the harder it is to do no...
>The more you buy in to Kubernetes, the harder it is to do normal development: you need all the different concepts (Pod, Deployment, Service, etc.) to run your code. So you need to spin up a complete K8s system just to test anything, via a VM or nested Docker containers ^rw43203482hl


Highlighted: 03/12/2020 09:57 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### Kubernetes is a large system with significant operational co...
>Kubernetes is a large system with significant operational complexity. The assessment team found configuration and deployment of Kubernetes to be non-trivial, with certain components having confusing default settings, missing operational controls, and implicitly defined security controls. ^rw43203481hl


Highlighted: 03/12/2020 09:57 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### In Kubernetes, an EndpointSlice contains references to a set...
>In Kubernetes, an EndpointSlice contains references to a set of network endpoints. The EndpointSlice controller automatically creates EndpointSlices for a Kubernetes Service when a selector is specified. These EndpointSlices will include references to any Pods that match the Service selector. EndpointSlices group network endpoints together by unique Service and Port combinations
>By default, EndpointSlices managed by the EndpointSlice controller will have no more than 100 endpoints each. Below this scale, EndpointSlices should map 1:1 with Endpoints and Services and have similar performance
>I actually understand that, somewhat, but notice how many concepts are needed: EndpointSlice, Service, selector, Pod, Endpoint. ^rw43203480hl


Highlighted: 03/12/2020 09:55 AM
Updated: 02/05/2021 03:46 PM


#### Extras:
**EndpointSlice****selector****pod****endpoint**


------

### And yes, much of the time you won’t need most of these featu...
>And yes, much of the time you won’t need most of these features, but then much of the time you don’t need Kubernetes at all. ^rw43203479hl


Highlighted: 03/12/2020 09:55 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### Before you can run a single application, you need the follow...
>Before you can run a single application, you need the following highly-simplified architecture (original source in Kubernetes documentation
>The ^rw43203478hl


Highlighted: 03/12/2020 09:54 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### A security review from 2019 described the code base as follo...
>A security review from 2019 described the code base as follows
>the Kubernetes codebase has significant room for improvement. The codebase is large and complex, with large sections of code containing minimal documentation and numerous dependencies, including systems external to Kubernetes. There are many cases of logic re-implementation within the codebase which could be centralized into supporting libraries to reduce complexity, facilitate easier patching, and reduce the burden of documentation across disparate areas of the codebase.” ^rw43203477hl


Highlighted: 03/12/2020 09:54 AM
Updated: 02/05/2021 03:46 PM


#### Extras:
**code review**


------

### If you’re part of a small team, Kubernetes probably isn’t fo...
>If you’re part of a small team, Kubernetes probably isn’t for you: it’s a lot of pain with very little benefits. ^rw43203476hl


Highlighted: 03/12/2020 09:52 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

### Solutions designed for 500 software engineers working on the...
>Solutions designed for 500 software engineers working on the same application are quite different than solutions for 50 software engineers. And both will be different from solutions designed for a team of 5. ^rw43203475hl


Highlighted: 03/12/2020 09:52 AM
Updated: 02/05/2021 03:46 PM


#### Extras:



------

