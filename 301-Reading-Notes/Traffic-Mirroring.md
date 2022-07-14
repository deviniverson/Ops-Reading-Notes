# Capture Network Traffic with SPAN vs TAP

There are two mechanisms to capture network traffic:
* port mirroring (commonly called SPAN)
* TAP (Terminal Access Point)

## Port Mirroring
Port mirroring, also known as SPAN or roving analysis, is a method of monitoring network traffic which forwards a copy of each incoming and/or outgoing packet from one(or several) port(s) (or VLAN) of a switch to another port where the analysis device is connected. Port mirroring can be managed locally or remotely.
To configure port mirroring, an administrator selects one or several ports from which all packets will be copied (source ports) and another port or ports where the copies of the packets will be sent (destination port).
Port mirroring is the most commonly used solution for capturing traffic because it is inexpensive, flexible in terms of how much traffic can be captured at once, and remotely configurable.

Port mirroring drawbacks:
* Can consume significant CPU resources while active.
* There is a risk of not receiving some packets (media errors)
* In the case of traffic congestion at the switch level, port mirroring is likely to drop some traffic (because the SPAN process does not have priority)
* In some cases, a better solution for long-term monitoring may be a passive TAP or an Ethernet repeater ("hub")

Port mirroring Advantages:
* Low cost
* Can be configured remotely through IP or Console port
* The only way to capture intra-switch traffic
* A good way to capture traffic on several ports at once.

## Network TAP
A network TAP (Terminal Access Point) is a hardware device which can passively capture traffic on a network. It is commonly used to monitor the traffic between two points in the network. If the network between these two points consists of a physical cable, a network TAP may be the best way to capture traffic.
Network TAPs are commonly used by monitoring and collection devices such as APS. TAPs can also be used in security applications because they are non-obtrusive, are not detectable on the network, can deal with full-duplex and non-shared networks, and will usually pass-through traffic even if the tap stops working or loses power.

Advantages of TAP:
* No risk of dropped packets
* Monitoring of all packets (including hardware errors(MAC & media))
* Provides full visibility, including congestion situations

Drawbacks of TAP:
* The device may require two listening interfaces on the analysis device
* Costly
* No visibility on intra-switch traffic
* Not appropriate for the observation of a narrow traffic range