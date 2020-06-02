> # **Microsoft Azure**


- Microsoft Azure is Microsoft's public cloud computing platform. 
- It provides a range of cloud services, including computing, analytics, storage and networking. 
- Users can pick and choose from these services to develop and scale new applications, or run existing applications in the public cloud.
- It offers tools that support all industries while aiming to help businesses manage challenges and meet their organizational goals. 
- Azure also charges you on a pay-as-you-go basis, meaning subscribers receive a bill each month that only charges them for the specific resources they have used.

## Working:

- Azure offers 4 different forms of cloud computing services:
  - infrastructure as a service (IaaS)
  - platform as a service (PaaS)
  - software as a service (SaaS) and 
  - serverless.
- Users can use these services to create cloud-based resources, such as virtual machines (VM) and databases.  
- A number of third-party sellers also make multiple softwares directly available through Azure.
  
  
## Microsoft provides five different customer support options for Azure:

- Basic
- Developer
- Standard
- Professional Direct
- Premier 
- These plans vary in terms of scope and price.


> ## Azure products and services:
- Microsoft sorts Azure cloud services into nearly two dozen categories, including:

### Compute.
- These services enable a user to deploy and manage VMs, as well as support remote application access. 

### Mobile.
- These products help developers build cloud applications for mobile devices, providing notification services, support for back-end tasks, tools for building application program interfaces (APIs). 

### Web. 
- These services support the development and deployment of web applications. They also offer features many exciting features for notification and reporting, etc.

### Storage. 
- This category of services provides scalable cloud storage for structured and unstructured data. It also supports big data projects, persistent storage and archival storage.

### Analytics.
- These services provide distributed analytics and storage, as well as features for real-time analytics, big data analytics, machine learning (ML), internet of things (IoT) etc.

### Media and content delivery network (CDN).
- These CDN services include on-demand streaming, digital rights protection, encoding and media playback and indexing. Ex. Netflix.

### Internet of things.
- These services help users capture, monitor and analyze IoT data from sensors and other devices. 
- Services include notifications, analytics, monitoring and support for coding and execution, etc.

### Development. 
- These services help application developers share code, test applications and track potential issues.
- Azure supports a range of application programming languages, including JavaScript, Python, .NET and Node.js. 

### Security. 
- These products provide capabilities to identify and respond to cloud security threats etc.

### Artificial intelligence (AI) and machine learning.
- This is a wide range of services that a developer can use to infuse artificial intelligence, machine learning and cognitive computing capabilities into applications and data sets.

### Management 
- These services provide a range of backup, recovery, compliance, automation, scheduling and monitoring tools that can help a cloud administrator manage an Azure deployment.

### Blockchain.
- The Azure Blockchain Service allows you to join a blockchain consortium or to create your own and many more functionalties.

### What do most people use Azure for:

- The platform is frequently used for backup and disaster recovery.
- Its use cases are extremely diverse.
- Running virtual machines or containers in the cloud is one of the most popular uses for Microsoft Azure
- Azure is also commonly used as a platform for hosting databases in the cloud.
- Azure supports open source technologies, so you can use the tools and technologies you prefer. 
- Run virtually any application using your data source, with your operating system, on your device. 
- Azure is the only consistent hybrid cloud, has more regions than any cloud provider, delivers.


> # **Virtual Network(VNet):**

1. An virtual network(VNet) is a representation of your own network in Cloud.
2. It is similar to our own on-premise network which we use at home.
3. It is an isolation of Azure cloud Network dedicated to your own subscription.
4. If you have your own **Subscripton** in Azure, this VNet is completely dedicated to you/your organisation. 
5. They are completely isolated from other virtual networks, unless you establish a connection between two virtual networks.

## On-premise Network and Vnet:

- In a On-premise network, to have accesibilty to public internet, it has to have a firewall, it has to send requests and receive requests throught a router.
- Hence a organisation will have to set up a router and a firewall/Multiple firewalls and the physical computer machines in the organisation.
- These physical computers would have their own unique ip addresses.
- Whenever a request is initiated for a pericular virtual machine, it comes from a IP address.
- It gets divided between the different web servers which are also VM’s, and the program will get executed.
- In AZURE, the equivalent of this whole network setup, is called as VNet.
- VNet is a service from Azure similar to the infrastructure. It is entirely a virtual setup.
- Azure infrastructure takes the role of the router. 
- It allows the access from the vnet to the public internet without any need of any type of configuration.

## Pricing in VNet:
- There is no extra cost for using VNet in Azure.
- The Computing usage of internet within the vnet will be charged as per the standard rates decribed in the Azure VM pricing.
- The VPN Gateways and Public IP Addresses used in the VNet will aslo be charged.

## **VNet benefits:**

### Isolation-
- VNets are completely isolated from one another.
- Nobody can access that Network unless the permission is granted.
- Also gives you the ability to create multiple environments for your Organisation.
- These environments are created for multiple reasons.
- You can create one environment which is purely for development, other purely for testing or production etc.
- They also can be entirely replica of each other for consistency.
- The possibilities are basically endless.

### Access to Public Internet-
- Every VM created will have by default access to  public internet.
- You can also control the access	by using **Network Security Grougs(NSG) and Firewalls**. 

### Security-
- Internet Traffic entering and exiting i.e. requests sent and received, on the VM, in the VNet can be controlled using Network Security Groups.

### Connectivity-
- If you want to connect a Secured Connection to VNet from your laptop, you can establish a VPN tunnel between your own PC to VNet, this is also possible.
- It is called as Point to Site Network.
- You can also connect multiple On-site PC’s to your VNet. 
- It is referred as Site to Site Network.
- Hybrid connectivity is possible.

### You can fully control the IP addresses, DNS servers, security policies.

### Vnet is further broken down into subnets. 
#### These are the Advantages VNet offers.

> VNet Overview:
In the following figure, VMs are represented as web servers and database servers. Each set of VMs are assigned to separate subnets in the VNet.
<img width="343" alt="vnetoverview" src="https://user-images.githubusercontent.com/65165798/83379660-b6f64b00-a3f9-11ea-8add-665d3f21c07d.png">

You can create a VNet before or as you create a VM. You create these resources to support communication with a VM:

- Network interfaces
- IP addresses
- Virtual network and subnets

In addition to those basic resources, you should also consider these optional resources:

- Network security groups
- Load balancers 


## Network Interface(NIC):
A [network interface (NIC)](../articles/virtual-network/virtual-network-network-interface.md) is the interconnection between a VM and a virtual network (VNet). A VM must have at least one NIC, but can have more than one, depending on the size of the VM you create.
- Network interface is the point of interconnection between a computer and a private or public network.
- A Network interface is generally a network interface card (NIC), but does not have to have a physical form. 
- Instead, the network interface can be implemented in software.

You can create a VM with multiple NICs, and add or remove NICs through the lifecycle of a VM. Multiple NICs allow a VM to connect to different subnets and send or receive traffic over the most appropriate interface. VMs with any number of network interfaces can exist in the same availability set, up to the number supported by the VM size. 


## Subnets
**subnets:**

1. A subnet is a range of IP addresses in the VNet. 
2. You can divide a VNet into multiple subnets for organization and security.  
3. Each NIC in a VM is connected to one subnet in one VNet.
4. NICs connected to subnets (same or different) within a VNet can communicate with each other without any extra configuration.

When you set up a VNet, you specify the topology, including the available address spaces and subnets. 

If the VNet is to be connected to other VNets or on-premises networks, you must select address ranges that don't overlap. The IP addresses are private and can't be accessed from the Internet.
 

By default, there is no security boundary between subnets, so VMs in each of these subnets can talk to one another. However, you can set up Network Security Groups (NSGs), which allow you to control the traffic flow to and from subnets and to and from VMs.
