## What is Network Address Translation (NAT)

A process in which one or more local IP addresses are translated into one or more Global IP addresses and vice versa in order to provide Internet access to the local hosts. It does the translation of port numbers i.e. masks the port number of the host with another port number of the host with another port number, in the packet that will be routed to the destination. It then makes the corresponding entries of IP address and port number in the NAT table. NAT generally operates on a router or firewall.

Generally, the border router is configured for NAT i.e. the router which has one interface in the local(inside) network and one interface in the global(outside) network. When a packet traverses outside the local(inside) network, NAT converts that local(private) IP address to a global(public) IP address and is converted to a local(private) IP address.

If NAT runs out of addresses, i.e., no address is left in the pool configured then the packets will be dropped and an Internet Control Message Protocol(ICMP) host unreachable packet to the destination is sent.

## Network Address Translation (NAT) Types:
1. Static NAT- In this, a single unregistered(Private) IP address is mapped with a legally registered(Public) IP address i.e one-to-one mapping between local and global addresses. This is generally used for Web hosting. These are not used in organizations as there are many devices that will need Internet access and to provide Internet access, a public IP address is needed.  
* Example: If there are 3000 devices that need access to the internet, the organization has to buy 3000 public addresses that will be very costly.

2. Dynamic NAT- An unregistered IP address is translated into a registered(public) IP address from a pool of public IP addresses. If the IP address of the pool is not free, then the packet will be dropped as only a fixed number of private IP addresses can be translated to public addresses.
* Example: If there is a pool of 2 public IP addresses, then only 2 private IP addresses can be translated at a given time. If a 3rd private IP address wants to access the internet, then the packet will be dropped therefore many private IP addresses are mapped to a pool of public IP addresses. NAT is used when the number of users who want to access the internet is fixed. This is also very costly as the organization has to buy many global IP addresses to make a pool.

3. Port Address Translation (PAT)- Known as NAT overload, many local (private) IP addresses can be translated to a single registered IP address. Port numbers are used to distinguish the traffic i.e., which traffic belongs to which IP address. This is most frequently used as it is cost-effective as thousands of users can be connected to the Internet by using only one real global (public) IP address.


## Advantages of NAT:
* NAT conserves legally registered IP addresses.
* It provides privacy as the device's IP address, sending and receiving the traffic, will be hidden.
* Eliminates address renumbering when a network evolves.

## Disadvantages of NAT:
* Translation results in switching path delays.
* Certain applications will not function while NAT is enabled.
* Complicates tunneling protocols such as IPsec.
* The router being a network layer device, should not tamper with port numbers(transport layer) but it has to do so because of NAT.
