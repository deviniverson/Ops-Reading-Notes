# CIDR Block Notation & Network Segmentation

## CIDR Block Notation Explained
CIDR notation is a way of representing a CIDR block, which is simply a range of IP addresses. When you create a network, the aim is to make sure there are enough available IP addresses for your use case, without making the CIDR block too large and wasteful.
An IPv4 address is usually represented as four 8-bit decimal numbers or octets separated by dots, for example 127.0.0.1 (localhost on most systems). An 8-bit number when represented in the decimal system as opposed to binary has a range of 0-255.
So all four octets together add up to 32 bits, for a range of 0.0.0.0-255.255.255.255

In CIDR notation, this full range would be represented as 0.0.0.0/0. The final digit after the "/" represents how many bits make up the mask.
Say we have the CIDR block 10.0.0.0/16. What this effectively means is that half of the available bits for the mask are being used (32 x .5 = 16). Since masking is left-aligned, this gives us the range 10.0.0.0 - 10.0.255.255. As you can see, the first two octets (adding up to 16 bits) are masked and therefore do not change. So this particular CIDR block gives us a range of 65,536 (or 2^16) IP addresses.

## Network Segmentation and Why it Matters?

Network Segmentation is when different parts of a computer network, or network zones, are separated by devices like bridges, switches and routers. Network segmentation is a discipline and a framework that can be applied in the data center and on premises at your facilities.
Few key benefits:
* Limiting access privileges to those who truly need it
* Protecting the network from widespread cyberattacks
* Boosting network performance by reducing the number of users in specific zones

Types of network zones you may want to establish:
* Users
* Screened Subnet
* Guest Network
* IT Workstations
* Servers by Department
* VoIP/Communications
* Traditional Physical Security
* Industrial Control Systems
* Customer Databases

Benefits of Network Segmentation:
* Damage control and limitation in case of an incident via the smaller attack surface
* Improved access control for external and internal network security
* Reducing the attack plane and scope of compliance requirements related auditing
* Improving performance with less congestion on network traffic
* Better analytics around network monitoring, network access and network devices
* Endpoint device protection, especially important as IoT devices become more common

Network segmentation can boost your overall security policy by limiting access privileges to those who need it, protecting the network from widespread cyberattacks and enabling better network performance by reducing the number of users in specific zones.
