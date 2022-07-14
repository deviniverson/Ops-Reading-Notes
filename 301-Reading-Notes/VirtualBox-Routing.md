# VirtualBox Network Settings
Networking is a critical component of interactive computer operations. It is difficult to imagine how to exchange data between computers without networks in a world where everything is changing at ever growing speed.
VirtualBox network modes to be discussed:
* Not Attached
* NAT
* NAT Network
* Bridged Adapter
* Internal Network
* Host-Only Adapter
* Generic Driver

Each VirtualBox VM can use up to eight virtual network adapters, each of which in turn is referred to as a network interface controller (NIC).

## Types of Virtual Network Adapters in VirtualBox
Virtual Network adapter is a software-emulated physical device. There are six virtual adapter types that can be virtualized by VirtualBox:
* AMD PCnet-PCI II (Am79C970A) - This network adapter is based on an AMD chip and can be used in many situations. As for Windows guests, this network adapter can be used for older Windows versions
* AMD PCnet-FAST III (Am79C973) - virtualized network adapter is supported by almost all guest operating systems that can run on VirtualBox. GRUB (the boot loader) can use this adapter for network boot.
* Intel PRO/1000 MT Desktop (82540EM) - adapter works perfectly with WIndows Vista and newer Windows versions. Most Linux distributions support this adapter as well.
* Intel PRO/1000 T Server (82543GC) - WIndows XP recognizes this adapter without installing additional drivers.
* Intel PRO/1000 MT Server (82545EM) - Adapter model is useful to import OVF templates from other platforms and can facilitate import process.
* Paravirtualized Network Adapter (virtio net) - is used only in special cases

## Not Attached
Virtual network adapter is installed in a VM, but the network connection is missing, much like when you unplug the Ethernet network cable when using a physical network adapter. This mode can be helpful for testing.
Instead of using the Not Attached mode, you can use any other network mode without ticking the Cable Connected checkbox.

## NAT
Network mode is enabled for a virtual network adapter by default. A guest operating system on a VM can access hosts in a physical local-area network (LAN) by using a virtual NAT (Network Address Translation) device. External networks, including the internet, are accessible from a guest OS. Default address for NAT is 10.0.2.2 (this is also the IP address of the default gateway for a VM). The network mask is 255.255.255.0

## NAT Network
Similar to NAT mode that you use for configuring a router. If you use the NAT Network mode for multiple virtual machines, they can communicate with each other via the network. Default address for NATNetwork is 10.0.2.0/24

## Bridged Adapter
Used for connecting the virtual network adapter of a VM to a physical network to which a physical network adapter of the VirtualBox host machine is connected.

## Internal Network
VM whose adapters are configured to work in the VirtualBox Internal Network mode are connected to an isolated virtual network. VMs connected to the internal network cannot be accessed from a host or any other devices.

## Host-only Adapter
Network mode is used for communicating between a host and guests. A VM can communicate with other VMs connected to the host-only network, and with the host machine.

## Generic Driver
This network mode allows you to share the generic network interface. A user can select the appropriate driver to be distributed in an extension pack or be included with VirtualBox.
Two sub-modes are available for VirtualBox Generic Driver mode - UDP Tunnel and VDE (Virtual Distributed Ethernet) Networking:
* UDP Tunnel - Virtual machines that run on different hosts can communicate transparently by using an existing network infrastructure.
* VDE Networking - Virtual machines can connect to a virtual distributed switch on Linux or FreeBSD hosts. You need to compile VirtualBox from sources to use VDE networking since standard VirtualBox packages don't include this feature.

## Port Forwarding
A process of intercepting traffic addressed to the appropriate IP address and port in addition to redirecting that traffic to a different IP address and/or port. 
