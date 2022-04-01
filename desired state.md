A **kubernetes** **deployment** defines a desired state. That desired state is achieved using a process that has been built by the kubernetes development team. You could achieve the same thing using a script, but chances are any script that you write will not go through the same level of debugging and/or revisions that the kubernetes process has gone through. In the case of the deployment, this is the **deployment controller**

from https://kubernetes.io/docs/concepts/workloads/controllers/deployment/: You describe a desired state in a Deployment, and the Deployment Controller changes the actual state to the desired state at a controlled rate. You can define Deployments to create new **ReplicaSets**, or to remove existing Deployments and adopt all their resources with new Deployments.


#todo
- [ ] looks like the kubernetes documentation has improved a lot. need to read it: https://kubernetes.io/docs/concepts/overview/
