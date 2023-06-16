---
description: A quick explanation of the most common used Kubernetes keywords in this section.
---

# 💬 Kubernetes terminology

### `Deployment` 

An instruction to Kubernetes on how it should start a service - this includes which Docker image to use, which environment variables to pass, which command to run inside a Docker container... It is very similar to what we do with `docker-compose.yaml` files. 
    
It’s up to Kubernetes to start a service (a pod) on a node (in our case EC2 instance available to Kubernetes to deploy services to) that has enough RAM and CPU left. If a pod dies because of deployment Kubernetes will see that a Deployment does not have any pods running and will start it up again. A deployment can also specify how many instances would we like to run (for example we can say that we want 5 `nodejs-workers` to be up and running all the time and Kubernetes will start 5 pods of `nodejs-worker` for us and we don’t need to care about where and how (like on which EC2 instance will they be running etc.)
    
### Pod

A pod is an instance of the service running - most of the time a pod is started by a Deployment so we don’t usually manually create pods. A pod is analog to a running docker container on your local machine.

### Service

A Kubernetes service is a definition of how a pod is accessible. This is usually only done for services that have some sort of ports exposed, like a REST API.Our `worker` services don’t need a Kubernetes service definition since they don’t have any ports. Don’t let the word service fool you - it doesn’t have anything to do with our normal meaning of a service (like a `job-generator` or `nodejs-worker`) but it’s a special Kubernetes definition to configure networking between services and ingress.

### Ingress
A Kubernetes ingress acts as a load balancer between outside world and the inside of Kubernetes cluster (in fact we use an `[nginx` as a Kubernetes ingress provider](https://kubernetes.github.io/ingress-nginx/deploy/) in our clusters). An ingress configuration tells Kubernetes which services through which ports are accessible to the outside world and how (through which routes, ports…). With ingress configuration we told kubernetes that our `frontend` is accessible through `[app.crowd.dev](http://app.crowd.dev)` and our `api` is accessible through `app.crowd.dev/api`. In the background ingress configuration gets transformed to an `nginx` configuration file and passed to an `nginx` instance running in the cluster that is acting as an `ingress` provider.

### ConfigMap
A `ConfigMap` is a resource inside Kubernetes that we can create manually. It acts as a store for configuration as a key-value pair storage. We are using this to store our environment variables inside Kubernetes and then providing those values from the `ConfigMap` to each of our services as environment variables. It’s a pretty powerful tool to abstract configuration away.

### Secret
A secret is similar to a `ConfigMap`, but it should store sensitive information. We are currently not using secrets for our configuration just because it’s harder to set up. We are using secrets for `letsencrypt` certificate auto renewal which we are doing with Kubernetes [certificate manager](https://cert-manager.io/docs/).

### Node
A node is an actual server instance (in our case AWS EC2 instance) that is available to Kubernetes and it will be used to start pods on them. Kubernetes is aware of the CPU/RAM/DISK usage on the nodes and will try to evenly distribute pods across all nodes so that they are evenly loaded