# Virtual Machine-VM
### Creating VM from portal

1. Subscription: (freeTrial, pay-as-you-go, students)
2. Resource group: 
3. VM Name:
4. Region:
5. Availability Zone:
6. Security type:
7. Image: Depending on the requirements
8. Size:
9. Authentication type: password/SSH

---
## Defination:
- **Resource group:** A **Resource Group** in Azure is a logical container for resources that share the same lifecycle, permissions, and policies. It helps you organize and manage related Azure resources efficiently. Resources within a group can be deployed, updated, and deleted together as a single management unit.

- **Types of sizes:** 
    1. B-series: Burstable virtual machines
    Examples: development and test servers, low-traffic web servers, small databases, micro services, servers for proof-of-concepts, and build servers.
    2. D-series: General purpose virtual machines
    Example: many enterprise-grade applications, e-commerce systems, web front ends, desktop virtualization solutions, customer relationship management applications, entry-level and mid-range databases, application servers, gaming servers, and media servers.
    3. E-series: Memory optimized virtual machines
    Example: SAP HANA, SAP S/4 HANA application layer, SAP NetWeaver application layer, and more broadly, memory-intensive enterprise applications, large relational database servers, data warehousing workloads, business intelligence applications, in-memory analytics workloads, and additional business-critical applications, including systems that process transactions of a financial nature.
    4. F-series: Compute optimized virtual machines
    Example: batch processing, web servers, analytics, and gaming for the Fa series VMs, and Electronic Design Automation (EDA) and SQL workloads for the FX series VMs.
    5. H-series: High Performance Computing virtual machines
    Example: fluid dynamics, finite element analysis, seismic processing, reservoir simulation, risk analysis, electronic design automation, rendering, Spark, weather modeling, quantum simulation, computational chemistry, and heat transfer simulation.
    6. L-series: Storage optimized virtual machines
    Example: NoSQL databases such as Cassandra, MongoDB, Cloudera, and Redis. Data warehousing applications and large transactional databases are great use cases as well.
    7. M-series: Ultra memory optimized virtual machines
    Example: large in-memory databases such as SAP HANA, SAP S/4 HANA, and SQL Hekaton, and data warehousing and high-performance computing (HPC).
    8. N-series: GPU accelerated virtual machines
    Example: large-scale AI model training, fine-tuning and distillation, agentic AI systems, digital twins and metaverse simulations, physical AI for robotics and IoT, generative AI inference, immersive visualization, and collaborative 3D design.

- Authentication Types:
    1. Password: While creating VM we should provide username and password.
    Connecting in gitBash
    ```bash
    # Password login
    ssh username@PUBLIC_IP
    ```
    2. SSH: Secure Shell
    ```bash
    chmod 400 demo.pem
    ssh -i demo.pem username@PUBLIC_IP
    ```
---
Reference link:  
- Image Types: [https://azure.microsoft.com/en-in/pricing/details/virtual-machines/series/](https://azure.microsoft.com/en-in/pricing/details/virtual-machines/series/)

- SSH: [https://www.cloudflare.com/en-gb/learning/access-management/what-is-ssh/](https://www.cloudflare.com/en-gb/learning/access-management/what-is-ssh/)