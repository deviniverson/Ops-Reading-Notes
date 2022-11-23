# Sniffing and Evasion
From an information security perspective, sniffing refers to tapping the traffic or routing the traffic to a target where it can be captured, analyzed and monitored. Sniffing is usually performed to analyze the network usage, troubleshooting network issues, monitoring the session for development and testing purposes.

## Define a Sniffing Attack
One example to keep in mind, bugging a telephone line in order to hear the calls that a person receives in order to get some information. Any network packet having information in plain text can be intercepted and read by the attackers. This information can be usernames, passwords, secret codes, banking details or any information which is of value to the attacker. This attack is just the technical equivalent of a physical spy.
### Sniffing Motives:
* Getting usernames or passwords
* Stealing bank related/ transaction related information
* Spying on email and chat messages
* Identity theft

## Types of Sniffing
* Passive Sniffing: Occurs at the hub. The sniffer device is placed at the hub then all the network traffic can be directly captured by the sniffer. The sniffer can sit there undetected for a long time and spy on the network.
* Active Sniffing: The sniffer will flood the switch with bogus requests so that the CAM table gets full. Once full, the switch will act as a switch and send the network traffic to all ports. This way the attacker can sniff the traffic from the switch.

## Some other attack implementations in the network
* MAC flooding: Flooding the switch with MAC addresses so that the CAM table is overflowing and sniffing can be done.
* DNS cache poisoning: Altering the DNS cache records so that it redirects the requests to a malicious website where the attacker can capture the traffic.
* Evil Twin Attack: The attacker uses malicious software to change the DNS of the victim. The attacker has a twin DNS set up already, which will respond to the requests.
* MAC spoofing: The attacker can gather the MAC address(s) that are being connected to the switch. The sniffing device is set with the same MAC address so that the messages that are intended for the original machine are delivered to the sniffer machine since it has the same MAC address set.

## Top Sniffing Tools
* Wireshark
* dSniff
* Debookee

## Precautionary measures against Sniffing attacks
1. Connect to trusted networks.
2. Encrypt! Encrypt! Encrypt!: Encrypt all traffic that leaves your system.
3. Network scanning and monitoring: Networks must be scanned for any kind of intrusion attempt or rogue devices that may be setup in span mode to capture traffic.
