Devin Iverson
02/14/22
What is a SMB port?

# What is an SMB Port?

The Server Message Block Protocol (SMB Protocol) is a client-server communication protocol used for sharing access to files, printers, serial ports, and data on a network. It can also carry transaction protocols for authenticated inter-process communication. In short, the SMB protocol is a way for computers to talk to each other.

SMB works through a client-server approach, where a client makes specific requests, and the server responds accordingly. This is known as a response-request protocol. This protocol facilitates file shares between networked computers. It enables users or applications to make requests to a file server and access resources like printer sharing, mail slots, and named pipes on the remote server.

## What are Ports 139 and 445?

SMB is a network file sharing protocol that requires an open port on a computer or server to communicate with other systems. SMB ports are generally port numbers 139 and 445.

## Are Open Ports Dangerous?

While port 139 and 445 aren’t inherently dangerous, there are known issues with exposing these ports to the internet. You can check if a port is open by using the ‘netstat’ command. Open ports are necessary to communicate across the internet. However, an open port can become a security risk when the service listening to the port is misconfigured, unpatched, vulnerable to exploits, or has poor network security rules. The most dangerous open ports are wormable ports, like the one that the SMB protocol uses, which are open by default in some operating systems.

Early versions of the SMB protocol were exploited during the **WannaCry ransomware attack** through a **zero-day exploit called EternalBlue**. WannaCry exploited legacy versions of Windows computers that used outdated versions of the SMB protocol. WannaCry is a network **worm** with a transport mechanism designed to automatically spread itself. The transport code scans for systems vulnerable to the EternalBlue exploit and then installs **DoublePulsar**, a backdoor tool, and executes a copy of itself. An infected computer will search its Windows network for devices accepting traffic on TCP ports 135-139 or 445 indicating the system is configured to run SMB. It will then initiate an SMBv1 connection to the device and use **buffer overflow** to take control of the system and install ransomware component of the attack. This means WannaCry can spread automatically without victim participation.

## How to keep Ports 139 and 445 Secure

1. **Avoid exposing SMB ports**; ports 135-139 and 445 are not safe to publicly expose and have not been for a decade.

2. **Patch Everything**; keep your systems up-to-date to avoid exploits of known vulnerabilities.

3. **No single point of failure**; If your data is important, then it should be backed up, at least one other secure location.

4. **Use a Firewall or Endpoint Protection**; Most solutions will include a blacklist of known attacker IP addresses.

5. **Use a Virtual Private Network (VPN)**; VPNs encrypt and protect network traffic.

6. **Implement Virtual Local Area Networks(VLANs)**; VLANs can be used to isolate internal network traffic

7. **Use MAC address filtering**; this can prevent unknown systems form accessing you network.