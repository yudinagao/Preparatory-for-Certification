# Design an Azure Compute Soltion

## Considerations

-Architecture and infrastructure requirements
    - Microservice
    - Full-fledged orchestration
    - Serverless
-Support for new workload scenarios, like HPC applications
    - Control
    - Workloads
-Required hosting options, including platform, infrastructure, and functions
    - IaaS
    - PaaS
    - FaaS
-Support for migrations, such as cloud-optimized or lift and shift
    - Cloud optimized
    - Lift and Shift
    - Containerized

## Azure Virtual Machine

- IaaS
- Build new Workloads
- Lift and Shift Migrations

### Considerations

- Network
- VM name
- Size
- Pricing Model
- OS

## Azure Batch

- Parallel Workloads
- Coupled Workloads
    - Starts a pool of compute VM
    - Install applications
    - Runs jobs
    - Identifies failure, requeues work and scales down the pool

### Considerations

- Pools
- Nodes
- Jobs

## Azure App Service

- Build and host web apps, background jobs, mobile backend, Resful API
- PaaS
- Support Multiple Languages and Frameworks
- Load Balancing
- Authentication and Authorization
- CD

## Azure Functions

- Scalability
- language of your choice
- Compute on demand
- Ideal solution for triggered

### Considerations 

- Long running functions
- Durable Functions
- Performance and Scaling
- Defensive Functions
- Not sharing storage accounts

## Azure Logic Apps

- Connect across cloud, on-premises and hybrid
- schedle and send email
- rout and process customer orders
- SFTP or FTP to Azure Storage
- Monitor tweets, create alerts and tasks

### Cosniderations

- Integration
- Performance
- Conditional expressions
- Connectors
- Mixing compute solutions
-

## Azure Container Instances

- Fast Startup
- Per Second Billing
- Hypervisor-level Security
- Custom Size
- Persistent Storage
- Linux and Windows

### Considerations

- Use a private registry
- Ensure image integrity throughout the life cycle
- Monitor container resource activity

## Azure Container Instances X Azure Virtual Machines

| Compare 	|Azure Container Instances 	|Azure Virtual Machines|
| ----      | -----                     | ---                   |
|Isolation 	|Container Instances typically provide lightweight isolation from the host and other containers, but doesn't provide as strong a security boundary as a virtual machine. 	|A virtual machine provides complete isolation from the host operating system and other virtual machines. Isolation is useful when a strong security boundary is critical, such as hosting apps from competing companies on the same server or cluster.|
|Operating system 	|Container Instances runs the user mode portion of an operating system and can be tailored to contain just the needed services for your application. This configuration results in fewer system resources being utilized. 	|Each virtual machine runs a complete operating system. Azure Virtual Machines typically requires more system resources than Container Instances, such as CPU, memory, and storage.|
|Deployment 	|Container Instances deploy individual containers by using Docker via the command line. Multiple containers are deployed by using an orchestrator such as Azure Kubernetes Service. 	|You can deploy individual virtual machines by using Windows Admin Center or Hyper-V Manager. Multiple virtual machines can be deployed by using PowerShell or System Center Virtual Machine Manager.|
|ersistent storage 	|Container Instances use Azure Disks for local storage for a single node, or Azure Files (SMB shares) for storage shared by multiple nodes or servers. 	|With Azure Virtual Machines, you can use a virtual hard disk (VHD) for local storage for a single virtual machine, or an SMB file share for storage shared by multiple servers.|
|Fault tolerance 	|If a cluster node fails in Azure Container Instances, any containers running on it are rapidly recreated by the orchestrator on another cluster node. 	|A virtual machine can fail over to another server in a cluster with the operating system of the virtual machine restarting on the new server.|

## Azure Kuerbernetes Services (AKS)

- Managed by Azure and its Free
- Open source Kubernetes

### Consideration

- Identity and security management
- Integrated logging and monitoring
- Automatic cluster node and pod scaling
- Cluster node upgrades
- Storage volume support
- Virtual network support
- Ingress with HTTP application routing support
- Docker image support
- Private container registry
