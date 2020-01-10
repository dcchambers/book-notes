# Chapter 01

In a nutshell, Kubernetes should allow developers to deploy complex applications without needing to involve an Ops team. K8s itself will monitor and manage the application and can restart apps to recover from errors. The Ops team benefits because they now only have to focus on the health of the K8s cluster - not the apps that are running inside of it.

- *Linux Namespace* - Makes sure each process sees its own personal view of the system (files, processes, network interfaces, etc). Types of namespaces:
  - Mount (mnt)
  - Process ID (pod)
  - Network (net)
  - Inter-process communication (ipc)
  - UTS
    - Determines the hostname and domain name for that namespace
  - User ID (user)
- *Linux Control Group (cgroups)* - Limit the resources that a process can consume (CPU, memory, network bandwidth, etc).

## Kubernetes Architecture
- *master node* - hosts the Kubernetes control plane
  - Control plane
    - etcd
    - API server
    - Scheduler
    - Controller Manager
- *worker node* - runs the deployed applications
  - Kubelet
  - kube-proxy
  - Container Runtime (`docker`, `rkt`, etc)
