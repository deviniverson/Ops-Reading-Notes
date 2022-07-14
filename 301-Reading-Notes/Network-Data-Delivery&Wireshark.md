Network Data Delivery: Layers 2 and 3 of the OSI Model

Open Systems Interconnection (OSI) model is a series of layers through which computer systems use to communicate. There are seven layers, and the networking layer would be layer 3. The network layer is responsible for packet forwarding, including routing through intermediate routers.
 
The data link layer, or layer 2, is the protocol layer that transfers data between nodes on a network segment across the physical layer, or what is commonly known as a host's physical address.
 
## The Seven Layers of the OSI Model:
1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

## Layer 2

Layer 2 is split in two parts:
1. the media access control(MAC) sub layer
* MAC (or physical) address provides an effective method of moving data across a small community of computing devices where routing traffic between multiple communities is not required.
* MAC address consists of a series of 12 hexadecimal numbers.
2. data link sublayer
* Establish protocols that relate to the structure of data frames that are placed on the network for data transmission. Uniformity is an important characteristic and includes placing both addresses for the data sender as well as the data recipient.

## Layer 3

Commonly referred to as the networking layer of the OSI model, layer 3 provides the structure relating to how data can be efficiently transferred from one network to another.
What is important is that you understand that a portion of an IP address is allocated for both network and host identification. Devices that are located on the same network will be able to communicate effectively at layer 2. Devices that are on different networks will communicate by directing their output data to routers that will be charged with the responsibility of delivery.

# WireShark and how is it used?

This is the go-to network packet capture tool for IT professionals. Wireshark will help you capture network packets and display them at a granular level. This tool lets you put your network traffic under a microscope, and then filter and drill down into it, zooming in on the root cause of problems, assisting with network analysis and ultimately network security.
 
## WireShark
 
Network protocol analyzer, or an application that captures packets from a network connection, such as from your computer to your home office or the internet. Packet is the name given to a discrete unit of data in a typical Ethernet network.
Wireshark is the most often-used packet sniffer in the world. Like any other packet sniffer, Wireshark does three things:
1. Packet Capture: Wireshark listens to a network connection in real time and then grabs entire streams of traffic  - quite possibly tens of thousands of packets at a time.
2. Filtering: Capable of slicing and dicing all of this random live data using filters. By applying a filter, you can obtain just the information you need to see.
3. Visualization: Wireshark allows you to dive right into the very middle of a network packet. It also allows you to visualize entire conversations and network streams.

## Color Coding means in Wireshark

Color : Packet Type
Light Blue : UDP
Black : Packets with errors
Light Green : HTTP traffic
Light Yellow : Windows-specific traffic, including Server Message Blocks(SMB) and NetBIOS
Dark Yellow : Router
Dark Grey : TCP SYN, FIN and ACK traffic

Not limited to just interpreting by color. It is possible to view the input/output (I/O) statistics of an entire packet capture. In Wireshark, just go to Statistics >> I/O Graph, and you'll see a graph. 
