In another video on this channel we looked at RBAC, what it means and how to create and use roles. In that video we saw that the actual roles and bindings are pretty trivial to create. But Users are much more difficult. And creating the certificates for users and updating them often is critical if you want to successfully implement RBAC. If you want to know about the details of RBAC and how it works, you might want to watch that other video. But at a high level, you create a user and role. And then you can create a role binding that binds the role to the user. a role defines one or more permissions in the form of what you can do to any resource in kubernetes. its important to remember that RBAC in kubernetes is additive. A user can have many roles, and all the permissions in all the roles add up to access level a user has. There is no way for a role to remove permission to any resource.

So users are critical to RBAC. How do you create them? Well, one of the issues with creating users in Kubernetes is that there aren't really any users in kubernetes. There are certificates. Certificates are bound to roles. A user name is just the common name for the certificates. Creating those certificates isn't really hard, but there is a series of steps you must follow. First you need to generate a key that represents the user. You will probably use a command like openssl or cfssl to do that. Then create what is called a certificate signing request or csr. You need to come up with the manifest for that CSR and then use kubectl to approve it.  To actually sign in to the cluster you need to come up with the kubeconfig file which you can generate based on the information in the new certificate. The next challenge is distributing that kubeconfig to the actual user. 

This may not sound like a lot of effort. But now replicate that for each user in the organization and then repeat it every so often to ensure you have short-lived certificates for security purposes. Oh, and then distribute the new kubeconfig. There are scripts out there to automate a lot of this, such as Brendan Burns' kubernetes-adduser, but even that doesn't tackle the kubeconfig update and distribution problems. 

With Infra, everything around user certificates is automated. The kubeconfig is automatically generated and kept up to date as long as you are using Infra. 

And that’s a little bit about creating users for RBAC manually vs using Infra. On this channel we look at a lot of the tools and technologies used in Infra as well as tangential technologies in similar areas. If you found the video useful, please like and subscribe to see more. Thanks so much for watching. Goodbye. 


----


There are a lot of parts about Kubernetes that are hard. Once everything is configured, compute resources are easier to scale in interesting ways, but getting there can be complicated. One of the more challenging aspects of Kubernetes is the idea of Roles and Role Based Access Control, or RBAC. When you first set up a kubernetes cluster, you will probably see a kubeconfig file that gives you the full Cluster Admin role. And while it is easy to share that kubeconfig with others, you really shouldn't. 

If everyone is a cluster admin, then anyone can do things they shouldn't. What can a cluster admin do? Well, everything from delete existing services and pods, or running processes that might be against company policy, all the way up to deleting nodes. Some of these actions could be intentional while others, perhaps most, are probably accidental. Once you are a cluster admin, its too easy to copy and paste a command that destroys your environment. And if your machine is compromised, the attacker can also do anything they like. 

The principle of least privilege says that a subject should be given only those privileges needed for it to complete its task. This applies to kubernetes just as much as it does to the operating system on your computer. But how do you give a user access to just the things they need in the cluster. Or how about giving an application just the rights it needs? Well, it turns out it is pretty simple

All you need is to define the user and the role and then bind the role to the user. The only problem is that there aren't really users in kubernetes... a user name is actually the common name of a certificate. So defining a user is as simple as generating a new certificate. But to generate that cert, you need to use the certificate and key of the certificate authority in the kubernetes cluster. So you will probably need a tool like openssl, because you aren't actually going to be able to do that with kubectl. And its not actually one command you need to run, because you actually need to start with a private key and then a certificate signing request, and then use that in conjunction with the CA to actually generate the certificate for the user. 

Then you need to build the kube config file so that starts by defining a cluster which includes  the public key of the certificate authority as well as the address of the api server. Then you need to add the credentials for the user which is really the certificate you generated. Then you need to add the context which links the cluster to the user. OK, so that’s not too hard, right? Oh, and you really should update the cert and thus the kubeconfig fairly often... 5 minutes is a good interval. Oh, and you are going to need to do this for all your users...every 5 minutes

And despite all those steps we have done, we have only created a user. Remember, we need to define the user and a role, and then bind the role to the user. If that user tries to do anything right now they will get an error since they aren't allowed to do anything yet. 

Now you need to create the roles and bind the roles to the user certificate. Defining roles is a bit easier. Your roles are going to be a collection of verbs and the resources those verbs apply to. The verbs you can include can be found in the chart on this page (https://kubernetes.io/docs/reference/access-authn-authz/authorization/#determine-the-request-verb). The resources can include any of the resources available in your cluster. 

So creating roles is relatively easy but users is a bit of a challenge. If however, you are using Infra, the user part and linking the user to the role is just as easy. 

Lets take a look at the roles that are defined on this cluster. There are actually two types of roles in Kubernetes: Roles and ClusterRoles. Roles are defined per namespace and clusterroles are defined for the cluster. You can see that there are a lot of cluster roles defined for the system to function. You probably won't ever touch those. The roles that you probably will use include view, edit, admin, and cluster-admin. We will look at these in more detail as well as create new roles in a future video. 

Let's close out this video by using one of these roles for a new user. The command to create a new user is ... . That command includes the role. And a user can have many roles. One very important thing to remember is that roles and permissions in kubernetes are additive. If any role that a user has defines access to a resource, then the user has access no matter what the other roles define. 


that was a bit too user focused. lets just look at rbac and roles in the first one.

RBAC. Role Based Access Control. You will see that term used in lots of different tools. Essentially it comes down to a simple concept. Chances are each user doesn't have a unique level of access to most of an application. So we create roles that users can share. All the users who are editors have the editor role. And all the admins have the level of access an admin should have. So you define the role and what access that role should have, and then bind those roles to users. 

In kubernetes, you can have many roles bound to any one user, but its important to remember that access in kubernetes is additive. If a user has been assigned a role that is minimal in the level of access it provides but they have also been assigned a role with more access they have all the access defined in all the roles combined. There is no way to remove access without removing the role that provided that access. Also there are two general types of roles: Roles which apply to a namespace, and ClusterRoles that apply to the whole cluster. In a simple test environment, this is easy to deal with, but in a larger environment where a user may have hundreds of roles of both types, navigating through permissions can be a challenge. There are tools to help navigate those permissions and in a future video we will take a look at some of them.

Creating roles in Kubernetes is somewhat easy. You define which resource you want the subject to have access to. We switched over to the word 'subject' because that can refer to both a human user as well as a process running an application automatically. Then you list out the verbs that subject should be able to apply to that resource. There are a number of verbs that work. This chart in the kubernetes documentation lists them out. Get will get an individual resource, list with get collections. and watch will watch an individual or collection of resources. And then there is create, update, patch, delete, and deletecollection. The resources are that we can work with can be seen when we run `kubectl api-resources`. So i could create a role that allows someone to get, list, update, and create Pods. In most cases, a role will be a collection of these verb resource pairings. You can see this if you run the command `kubectl get clusterrole edit`. This shows us all the permissions in the edit cluster-role. Lets take a look at a very simple role that just allows a subject get, watch, and list of a pod. You can see that it is called pod-reader and applies only to the default namespace.  

xxxxx
using this
```yaml
apiVersion: rbac.authorization.k8s.io/v1
kind: Role
metadata:
  namespace: default
  name: pod-reader
rules:
- apiGroups: [""] # "" indicates the core API group
  resources: ["pods"]
  verbs: ["get", "watch", "list"]
```
xxxx

Creating roles is pretty easy. Creating users and groups is not easy, so we will take a look at that in a future video. But once you have a user and role, then you bind the two together. Here we can see an example of this, binding the pod-reader role from a few seconds ago.

xxxx
using this
```yaml
apiVersion: rbac.authorization.k8s.io/v1
# This role binding allows "jane" to read pods in the "default" namespace.
# You need to already have a Role named "pod-reader" in that namespace.
kind: RoleBinding
metadata:
  name: read-pods
  namespace: default
subjects:
# You can specify more than one "subject"
- kind: User
  name: jane # "name" is case sensitive
  apiGroup: rbac.authorization.k8s.io
roleRef:
  # "roleRef" specifies the binding to a Role / ClusterRole
  kind: Role #this must be Role or ClusterRole
  name: pod-reader # this must match the name of the Role or ClusterRole you wish to bind to
  apiGroup: rbac.authorization.k8s.io
```
xxxx

So you can see that binding is actually pretty easy as well. But setting up the binding for lots of users is where this part gets challenging and that’s why using groups and OIDC providers in Infra becomes a huge timesaver. Let's go through those steps again right now. I have already installed Infra on a cluster and setup the integration with Okta. I have this set of groups defined in Okta and I have already defined these roles in the cluster. So now i just have to run this command to bind the two together. And now every user who is a member of  that group has the access defined in that role. This is all achievable without Infra but everything gets so much easier when you use it. 

And that’s a little bit about RBAC, Kubernetes, and Infra. On this channel we look at a lot of the tools and technologies used in Infra as well as tangential technologies in similar areas. If you found the video useful, please like and subscribe to see more. Thanks so much for watching. Goodbye. 
 `