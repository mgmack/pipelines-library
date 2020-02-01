Concepts
Overview
What is Kubernetes
Kubernetes Components
The Kubernetes API
Working with Kubernetes Objects
Understanding Kubernetes Objects
Kubernetes Object Management
Names
Namespaces
Labels and Selectors
Annotations
Field Selectors
Recommended Labels
Cluster Architecture
Nodes
Master-Node Communication
Controllers
Concepts Underlying the Cloud Controller Manager
Containers
Images
Container Environment Variables
Runtime Class
Container Lifecycle Hooks
Workloads
Pods
Pod Overview
Pods
Pod Lifecycle
Init Containers
Pod Preset
Pod Topology Spread Constraints
Disruptions
Ephemeral Containers
Controllers
ReplicaSet
ReplicationController
Deployments
StatefulSets
DaemonSet
Garbage Collection
TTL Controller for Finished Resources
Jobs - Run to Completion
CronJob
Services, Load Balancing, and Networking
EndpointSlices
Service
Service Topology
DNS for Services and Pods
Connecting Applications with Services
Ingress
Ingress Controllers
Network Policies
Adding entries to Pod /etc/hosts with HostAliases
IPv4/IPv6 dual-stack
Storage
Volumes
Persistent Volumes
Volume Snapshots
CSI Volume Cloning
Storage Classes
Volume Snapshot Classes
Dynamic Volume Provisioning
Node-specific Volume Limits
Configuration
Configuration Best Practices
Resource Bin Packing for Extended Resources
Managing Compute Resources for Containers
Pod Overhead
Assigning Pods to Nodes
Taints and Tolerations
Secrets
Organizing Cluster Access Using kubeconfig Files
Pod Priority and Preemption
Scheduling Framework
Security
Overview of Cloud Native Security
Policies
Limit Ranges
Resource Quotas
Pod Security Policies
Scheduling
Kubernetes Scheduler
Scheduler Performance Tuning
Cluster Administration
Cluster Administration Overview
Certificates
Cloud Providers
Managing Resources
Cluster Networking
Logging Architecture
Configuring kubelet Garbage Collection
Federation
Proxies in Kubernetes
Controller manager metrics
Installing Addons
Extending Kubernetes
Extending your Kubernetes Cluster
Extending the Kubernetes API
Extending the Kubernetes API with the aggregation layer
Custom Resources
Compute, Storage, and Networking Extensions
Network Plugins
Device Plugins
Operator pattern
Service Catalog
Poseidon-Firmament - An alternate scheduler
Edit This Page

What is Kubernetes
This page is an overview of Kubernetes.

Going back in time
Why you need Kubernetes and what can it do
What Kubernetes is not
What's next
Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

The name Kubernetes originates from Greek, meaning helmsman or pilot. Google open-sourced the Kubernetes project in 2014. Kubernetes builds upon a decade and a half of experience that Google has with running production workloads at scale, combined with best-of-breed ideas and practices from the community.

Going back in time
Let’s take a look at why Kubernetes is so useful by going back in time.

Deployment evolution

Traditional deployment era: Early on, organizations ran applications on physical servers. 
There was no way to define resource boundaries for applications in a physical server, and this caused resource allocation issues. For example, if multiple applications run on a physical server, there can be instances where one application would take up most of the resources, and as a result, the other applications would underperform. A solution for this would be to run each application on a different physical server. But this did not scale as resources were underutilized, and it was expensive for organizations to maintain many physical servers.
---------------------------------------------------
Virtualized deployment era: As a solution, virtualization was introduced. I
t allows you to run multiple Virtual Machines (VMs) on a single physical server’s CPU. Virtualization allows applications to be isolated between VMs and provides a level of security as the information of one application cannot be freely accessed by another application.

Virtualization allows better utilization of resources in a physical server and allows better scalability because an application can be added or updated easily, reduces hardware costs, and much more. With virtualization you can present a set of physical resources as a cluster of disposable virtual machines.

Each VM is a full machine running all the components, including its own operating system, on top of the virtualized hardware.
---------------------------------------------------
Container deployment era: Containers are similar to VMs, but they have relaxed isolation properties to share the Operating System (OS) among the applications. Therefore, containers are considered lightweight. Similar to a VM, a container has its own filesystem, CPU, memory, process space, and more. As they are decoupled from the underlying infrastructure, they are portable across clouds and OS distributions.

Containers have become popular because they provide extra benefits, such as:

Agile application creation and deployment: increased ease and efficiency of container image creation compared to VM image use.

Continuous development, integration, and deployment: provides for reliable and frequent container image build and deployment with quick and easy rollbacks (due to image immutability).

Dev and Ops separation of concerns: create application container images at build/release time rather than deployment time, thereby decoupling applications from infrastructure.

Observability not only surfaces OS-level information and metrics, but also application health and other signals.

Environmental consistency across development, testing, and production: Runs the same on a laptop as it does in the cloud.

Cloud and OS distribution portability: Runs on Ubuntu, RHEL, CoreOS, on-prem, Google Kubernetes Engine, and anywhere else.

Application-centric management: Raises the level of abstraction from running an OS on virtual hardware to running an application on an OS using logical resources.

Loosely coupled, distributed, elastic, liberated micro-services: applications are broken into smaller, independent pieces and can be deployed and managed dynamically – not a monolithic stack running on one big single-purpose machine.

Resource isolation: predictable application performance.

Resource utilization: high efficiency and density.
