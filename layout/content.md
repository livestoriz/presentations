# Running Containers <br/>and Exposing Services

## Session 1

---

# Minikube

Minikube is a tool that makes it easy to run Kubernetes locally.

Minikube runs a single-node Kubernetes cluster inside a VM on your laptop

---

# Minikube - Current Features

- DNS
- NodePorts
- ConfigMaps and Secrets
- Dashboards
- Container Runtime: Docker and rkt
- Enabling CNI (Container Network Interface)

---

# Pods

- Smallest deployable units of computing
- Contain one or more containers
- Containers inside the pod
  - share namespaces
  - are scheduled together
- Emphemeral (won't be rescheduled)

---

# Labels & Selectors

- Labels
  - Key/value pairs that can be attached to objects
    - e.g. to pods, volumes, nodes, etc.
- Selectors
  - Select (group of) objects based on labels

---

# Deployments (& Replica Sets)

- Declarative way of deploying Pods
- Manages a Replica Set that in turn manages Pods
- Ensures that the desired number of Pods is running

---

# Services

- Abstraction layer on top of Pods
- Defines a logical set of Pods
- Defines a policy by which to access those
- Assigns them a single (virtual) service IP
- Takes care of simple load balancing
- Discovery via DNS

---

# Ingress

An Ingress is a collection of rules that allow inbound connections from outside the cluster to reach the cluster services.

Features
- Externally-reachable URLs
- Load balance traffic
- Terminate SSL
- Name based virtual hosting
