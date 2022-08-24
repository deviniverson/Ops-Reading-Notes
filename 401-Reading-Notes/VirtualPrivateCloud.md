# What is a Virtual Private Cloud (VPC)?

A VPC is a public cloud offering that lets an enterprise establish its own private cloud-like computing environment on shared public cloud infrastructure. A VPC gives an enterprise the ability to define and control a virtual network that is logically isolated from all other public cloud tenants, creating a private, secure place on the public cloud.
For an example: Imagine that a cloud provider's infrastructure is a residential apartment building with multiple families living inside. Being a public cloud tenant is akin to sharing an apartment with a few roommates. In contrast, having a VPC is like having your own private condominium, no one else has the key, and no one can enter the space without your permission.

## VPC Features
VPCs are a "best of both worlds" approach to cloud computing. They give customers many of the advantages of private clouds, while leveraging public cloud resources and savings.
### Some key features include:
* Agility: Control the size of your virtual network and deploy cloud resources whenever your business needs them.
* Availability: Redundant resources and highly fault-tolerant availability zone architectures mean your applications and workloads are highly available.
* Security: Because the VPC is a logically isolated network, your data and applications won't share space or mix with those of the cloud provider's other customers.
* Affordability: VPC customers can take advantage of the public cloud's cost-effectiveness, such as saving on hardware costs, labor times, and other resources.

## VPC Benefits
* Flexible business growth
* Satisfied customers
* Reduced risk across the entire data lifecycle
* More resources to channel toward business innovation

## VPC Architecture
### In a VPC, you can deploy cloud resources into your own isolated virtual network. These cloud resources - also known as logical instances - fall into three categories
1. Compute: Virtual server instances are present to the user as virtual CPUs with a predetermined amount of computing power, memory, etc.
2. Storage: VPC customers are typically allocated a certain block storage quota per account, with the ability to purchase more.
3. Networking: You can deploy virtual versions of various networking functions into your virtual private cloud account to enable or restrict access to its resources. These include public gateways, load balancers, and routers

### Three-tier architecture in a VPC
1. The ** web or presentation tier **, which takes requests from web browsers and presents information created by or stored within the layers to end users.
2. The ** application tier**, which houses the business logic and is where most processing takes place.
3. The ** database tier **, consists of database servers that store the data processed in the application tier.
To create a three-tier application architecture on a VPC, you assign each tier its own subnet, which will give it its own IP address range. Each layer is automatically assigned its own unique ACL.

## VPC Security
### Two types of network access controls comprise the layers of VPC security:
1. Access control list (ACLs): A list of rules that limit who can access a particular subnet within your VPC
2. Security group: You can create groups of resources and assign uniform access rules to them. Security groups act like virtual firewalls, controlling the flow of traffic to your virtual servers, no matter which subnet they are in.
