# Docker Day-1
---
## Introduction of Containers
### 1. First We Understand Traditional Deployment of Applications/Software in IT Industry
Traditional deployment refers to the conventional method of deploying software applications where the application is installed and executed directly on physical servers. It involves manually setting up hardware, installing the OS, dependencies, and the application on servers without isolation.
#### Disadvantages of Traditional Deployment
(i) Dependency Conflicts: Different applications may require different versions of dependencies, causing conflicts and making it hard to manage software dependencies effectively.

(ii) Resource Inefficiency: Lack of isolation may result in inefficient resource utilization as applications compete for resources on the same server, leading to potential performance issues.

(iii) Limited Scalability: Traditional deployment may not scale as easily as containerized deployments, making it more challenging to accommodate increasing workloads and traffic.

### 2. Virtual Machines
Virtual machines (VMs) are indeed a significant advancement in the realm of software deployment and infrastructure management. VMs offer a way to create isolated and independent environments on a single physical server. With the help of Hypervisor we create multiple VMs on a single physical machine, each with its own dedicated operating system and isolated environment.

#### Disadvantages of Virtual Machines

(i) Resource Overhead: VMs require a hypervisor layer to manage and run multiple virtual instances, which adds some resource overhead. This means that VMs may not be as lightweight as other deployment options, like containers.

(ii) Boot Time: VMs generally have longer boot times compared to containers. Starting up a VM involves loading the entire operating system, which can be slower than the near-instant startup times of containers.

(iii) Resource Allocation Complexity: Configuring resource allocation for VMs can be more complex, as you need to determine the appropriate amount of CPU, memory, and storage for each VM. This can lead to over-provisioning or under-utilization of resources.
