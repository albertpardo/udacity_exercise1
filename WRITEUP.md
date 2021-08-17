# Write-up

### Analyze, choose, and justify the appropriate resource option for deploying the app.


#### Cost

I have estimated the cost using [Azure Calculator](https://azure.microsoft.com/en-in/pricing/calculator/).

| Service type | Region  | Description   | Estimated monthly cost |
| ------------ | ------  | ------------  | ---------------------- |
|    VM        | Westus2 | Instance A0   | $13.19 |
|    VM        | Westus2 | Instance A1   | $16.84 |
| ------------ | ------  | ------------  | ---------------------- |
|  App Service | Westus2 | Basic Tier B1 | $12.41 |


Note : 
    - Instance A0 : 1 Core, 0.75Gb RAM, 20 GB Temporary storage , $0.018/hour

    - Instance A1 : 1 Core, 1.75Gb RAM, 40 GB Temporary storage , $0.023/hour

    - Basic Tier B1 : 1 Core, 1.75Gb RAM, 10 GB Storage , $0.018/hour

I have choose *Instance A1* and *Basic Tier B1* for comparation because both use 1.75Gb RAM.

#### VMs

    * Cost more than App Services : VM are more expensive and can be more time consuming for developers (this time must be added to de VM cost).
    * Are more orientated to IaaS because give full control and access to the VM. You :
        * Can choose : CPU type,RAM quatity, Storage and SO used
        * Can control instalation, configuration and maintenance of the all necesary software.
    * Multiple VMs can be grouped to provide high availability, scalability using Virtual Machine Scale Sets and Load Balancers.

#### App Services

    * Cheaper to run comparing to VMs. Developers focus on the application (No extra time means no more cost). 
    * Are orientated to PaaS. Azure controls the infrastructure (hardware,OS and install software on the server) with high availability and auto-scaling.


#### VMs vs App Services

(See this [scalability link](https://docs.microsoft.com/en-us/azure/architecture/guide/technology-choices/compute-decision-tree#scalability)

|                        | VM      | App Service |
| ---------------------- | ------- | ----------- |     
| Estimated monthly cost | $16.84  | $12.41 |
| Scalability Autoscaling | use Virtual machine scale sets | Built-in service|    
| Scalability Load balancer | use Azure Load Balancer | Integrated |

#### My choice and my justification

1. My choice is **App Service**

2. Justification

    * The application is light at this moment so it not need a lot of hardware resources. And it's not necesary to take a control about the software.
    * less cost than VM's
    * Developers can focus on the application because don't need to spend time wiht the VM and don't worry about managing Autoscaling and Load balancer because are included.
 

### Assess app changes that would change your decision.

* When the application need more hardware resources , more control or more scalability. ( App Service is limited to a maximum of 14GB of memory and 4 vCPU  cores per instance)
* When need more control over the software: special configutarion , some concrete software version
* When the App deployed begins to require a higher storage capacity, the storage capacity would need to be extended beyond what was initially set.

