---
description: >-
  A set of commands that will make you more efficient at working with
  Kubernetes.
---

# 🎮 Useful kubectl commands

There are a set of `bash` aliases that help to provide with some quick `kubectl` commands:

```bash
alias kubecontext='kubectl config get-contexts'
alias kubepods='kubectl get pods'
alias kubelogs='kubectl logs -f'
alias kubesvcs='kubectl get svc'
alias kubedpls='kubectl get deployments'
alias kube-set-context='kubectl config use-context'
alias kube-clear-context='kubectl config unset current-context'
```

We recommend adding those to your source. We will be using these aliases in the remaining of this section.

1. If you are accessing multiple Kubernetes clusters (like our staging and production) you need to repeat [Getting access section](https://www.notion.so/Kubernetes-specification-9a011d93bf4a4655af8416acf5edeccf?pvs=21) for each cluster to configure your `kubectl` to access both clusters - but to switch between both while they are already configured you should use these commands:

```bash
# this will show you your currently configured clusters and the one with a start (*) next to it is the one that is currently active and used by kubectl
kubecontext

# output should be similar to this:
CURRENT   NAME                                                                CLUSTER                                                             AUTHINFO                                                           NAMESPACE
*         arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-staging    arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-staging    arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-staging   
          arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-production arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-production arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-production

# to switch between contexts use this command: (this one will switch to crowd-kube-staging cluster)
kube-set-context arn:aws:eks:eu-central-1:359905442998:cluster/crowd-kube-staging

# from this point on all kubectl command will be accessing this cluster
```

2. Instead of doing `kubectl get pods` just do `kubepods` and it will print the same thing - a list of service instances running inside Kubernetes
3. To get logs from a pod you first should get a name of the pod with `kubepods` or if you have `kubectl` autocomplete setup you can also just do `kubelogs job-generator` and press tab for autocomplete to fill you in with the rest of the pod name - the final command should look like: `kubelogs job-generator-dpl-64df888968-z4klr`
4. To get a shell access to within a running pod you can execute this: `kubectl exec --stdin --tty job-generator-dpl-64df888968-z4klr -- /bin/sh` replacing the pod name with the one you want (in this case it was `job-generator-dpl-64df888968-z4klr` , also depending on the docker image that was used to start the pod you will have to use `/bin/sh` instead of `/bin/bash` for a shell since `alpine` images don’t have `bash` shell included. `/bin/sh` works just as well although it doesn’t have all the tools that `bash` offers you plus some commands are different - for example sourcing a file with bash is just `source file` with sh you have to do `. file`
