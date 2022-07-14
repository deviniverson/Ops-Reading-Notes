A port scanner is a computer program that checks network ports for one of three possible statuses - open, closed, or filtered.
Port scanners are valuable tools in diagnosing network and connectivity issues. Attackers use port scanners to detect possible access points for infiltration and to identify what kinds of devices you are running on the network, like firewalls, proxy servers or VPN servers.

## How does a port scanner operate?
A port scanner sends a network request to connect to a specific TCP or UDP port on a computer and records the response.
Three translated responses:
1. Open, Accepted (What can I do for you?)
2. Closed, Not Listening (The port is currently in use at this time.)
3. Filtered, Dropped, Blocked (Silence, (no response).)

So what a port scanner does is send a packet of network data to a port to check the current status. If you wanted to check to see if your web server was operating correctly, you would check the status of port 80 on that server to make sure it was open and listening.
The status helps network engineers diagnose network issues or application connectivity issues, or help attackers find possible ports to use for infiltration into your network.

## What is a Port?
A port is a virtual location where networking communication starts and ends.
There are two kinds of network ports on each computer (65,536 of each for a total of 131,082): * TCP
* UDP
The first 1023 TCP ports are well-known ports reserved for applications like FTP(21), HTTP(80), or SSH(22) and the Internet Assigned Numbers Authority (IANA) reserves these points to keep them standardized.
TCP ports 1024 - 49151 are available for use by services or applications, and you can register them with IANA, so they are considered semi-reserved. Port 49152 and higher are free to use.

## Port Scanning Basics
Port scans generally occur early in the cyber kill chain, during reconnaissance and intrusion. Attackers use port scans to detect targets with open and unused ports that they can repurpose for infiltration, command and control, and data exfiltration or discover what applications run on that computer to exploit a vulnerability in that application.

## Port Scanning Techniques
* Ping Scan - The simplest scan, a ping scan looks for any ICMP replies indicating if a target is alive.
* TCP Half Open - A fast and common scan that requests an ACK packet from a computer. Also called a SYN scan.
* TCP Connect - Similar to the TCP Half Open scan, but the TCP Connect scan completes the TCP connection.
* UDP - Slower than a TCP scan, a UDP scan works best when you send a specific payload to a target, such as a DNS request.
* Stealth Scanning - Quiet and unobvious, stealth scanning is commonly used by hackers for this reason.
Nmap is one of the most popular open-source port scanning tools available. Nmap provides a number of different port scanning techniques for different scenarios. TCP half-open scans are the default scan in Nmap

## Additional Scanning Techniques
More scans and the reasons to run them:
* TCP ACK scan - to map firewall rulesets
* TCP Window scan - can differentiate open ports from closed ports but only works on a minority of systems
* -scanflags - for the advanced user that wants to send their custom TCP flags in a scan, you can do that in Nmap

## Port Scanning Tools
* Nmap
* Solarwinds Port Scanner
* Netcat
* Advanced Port Scanner
* NetScanTools

## How to Detect a Port Scan?
There are a few different techniques to detect port scans, which could be attempts to scan your network for vulnerabilities.
One is a dedicated port scan detector software application, like PortSentry or Scanlogd.
Netcat includes port scanning functionality as well as the ability to create a simple chat server or program different packets for testing purposes.
Intrusion detection systems (IDS) are another way to detect port scans. Look for an IDS that uses a wide variety of rules to detect the various kinds of port scans that aren't merely threshold-based.

## Why should you run a port scan?
You should run port scans proactively to detect and close all possible vulnerabilities that attackers might exploit. Proactive port scanning is a good habit that you should repeat on a regular schedule.

## Implications of running a port scan
Some caveats to running port scans:
* Some services or computers might fail from a port scan. This is for internal systems more than internet-facing systems, but can happen.
* Running port scans without authorization can be considered an aggressive action, and if you are on a shared network, you might scan a system that isn't under your control, which isn't good.
* Port scans are a critical part of building a good defense from cyberattacks. Attackers are using port scans, as well. You need to beat them to the punch and close down possible attack vectors and make their lives as difficult as possible.
Protecting the perimeter is only part of the battle, however. You need to protect and monitor your data with the same vigilance you protect and monitor your ports.
