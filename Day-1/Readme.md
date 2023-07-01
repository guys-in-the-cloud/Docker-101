# Docker Day-1
---
## Introduction of Containers
### 1. Traditional Deployment 
Traditional deployment refers to the conventional method of deploying software applications where the application is installed and executed directly on physical servers. It involves manually setting up hardware, installing the OS, dependencies, and the application on servers without isolation.

<p align="center">
<img width="280" alt="Screenshot 2023-07-01 at 8 04 36 PM" src="https://github.com/guys-in-the-cloud/Docker-101/assets/100664099/814fc0e9-5a51-482e-be15-de359cc7c270">

</p>

#### Disadvantages of Traditional Deployment
(i) Dependency Conflicts: Different applications may require different versions of dependencies, causing conflicts and making it hard to manage software dependencies effectively.

(ii) Resource Inefficiency: Lack of isolation may result in inefficient resource utilization as applications compete for resources on the same server, leading to potential performance issues.

(iii) Limited Scalability: Traditional deployment may not scale as easily as containerized deployments, making it more challenging to accommodate increasing workloads and traffic.

### 2. Virtualized Deployment
Virtualization was introduced to solve the problems of traditional deployment. Virtual machines (VMs) are indeed a significant advancement in the realm of software deployment and infrastructure management. VMs offer a way to create isolated and independent environments on a single physical server. With the help of Hypervisor we create multiple VMs on a single physical machine, each with its own dedicated operating system and isolated environment.

<p align="center">
<img width="261" alt="Screenshot 2023-07-01 at 8 07 11 PM" src="https://github.com/guys-in-the-cloud/Docker-101/assets/100664099/25d06c7a-ab07-40ef-a94a-44c1f71264bb">
</p>


#### Disadvantages of Virtual Machines

(i) Resource Overhead: VMs require a hypervisor layer to manage and run multiple virtual instances, which adds some resource overhead. This means that VMs may not be as lightweight as other deployment options, like containers.

(ii) Boot Time: VMs generally have longer boot times compared to containers. Starting up a VM involves loading the entire operating system, which can be slower than the near-instant startup times of containers.

(iii) Resource Allocation Complexity: Configuring resource allocation for VMs can be more complex, as you need to determine the appropriate amount of CPU, memory, and storage for each VM. This can lead to over-provisioning or under-utilization of resources.

### 3. Container Deployment
Containers are similar to VMs, but they have better isolation which allows the operating system to be shared among applications. Having similarities to a VM, a container has its own filesystem, share of CPU, memory, process space, and more. As they are decoupled from the underlying infrastructure, they are portable across clouds and OS distributions. Containers are lightweight.  
<p align="center">
  <img width="256" alt="Screenshot 2023-07-01 at 8 19 33 PM" src="https://github.com/guys-in-the-cloud/Docker-101/assets/100664099/98393555-0a2c-45b8-8603-a059637d9b5c">
</p>

 ### Namespace and Control Group (cgroup)
The kernel's Namespace and Control Group (cgroup) features play a crucial role in achieving isolation and resource control for containers.

1. Namespaces: Namespaces allow the kernel to create separate and isolated environments for various aspects of a container, such as its process space, network, filesystem, and more. Each container operates within its own namespace, which gives the illusion that it has its private resources, even though it's sharing the underlying host resources.

For example:

(i) PID Namespace: Ensures each container sees only its processes and can't access processes from other containers.<br />
(ii) Network Namespace: Provides each container with its own network stack, IP addresses, ports, etc. <br />
(iii) Mount Namespace: Gives each container its isolated filesystem view, so they can have their own root file system. <br />

2. Control Groups (cgroups): Cgroups allow the kernel to limit and manage resource usage for containers. They enable controlling CPU, memory, disk I/O, and other resources on a per-container basis. This prevents any single container from consuming excessive resources and ensures fair resource allocation among all containers on the system.

By leveraging these kernel features, containers achieve strong isolation while sharing the host OS efficiently. This efficient utilization of resources, combined with portability and fast start-up times, makes containers a unique and powerful technology for modern application deployment and management.

