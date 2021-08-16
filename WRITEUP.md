# Write-up

### Analyze, choose, and justify the appropriate resource option for deploying the app.


VMs
---

    * Cost more than App Services : VM are more expensive and can be more time consuming for developers.
    * Are more orientated to IaaS because give full control and access to the VM. You :
        * Can choose : CPU type,RAM quatity, Storage and SO used
        * Can control instalation, configuration and maintenance of the all necesary software.
    * Multiple VMs can be grouped to provide high availability, scalability using Virtual Machine Scale Sets and Load Balancers.

App Services
------------
    * Cheaper to run comparing to VMs. Developers focus on the application. 
    * Are orientated to PaaS. Azure controls the infrastructure (hardware,OS and install software on the server) with high availability and auto-scaling

My choice and my justification
------------------------------

1. My choice is **App Service**

2. Justification
    * The application is light at this moment so it not need a lot of hardware resources. And it's not necesary to take a control about the software.
    * less cost than VM's
 

### Assess app changes that would change your decision.

* When the application need more hardware reources or more control. ( App Service is limited to a maximum of 14GB of memory and 4 vCPU cores per instance)
* When need more control over the software: special configutarion , some concrete software version
* When the App deployed begins to require a higher storage capacity, the storage capacity would need to be extended beyond what was initially set.

