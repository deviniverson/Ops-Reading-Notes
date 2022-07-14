CIA Triad is one of the basic building blocks of information security and a vital piece in establishing secure enterprise file transfers.

## CIA Triad refers to:
* Confidentiality
* Integrity
* Availability

**To establish a secure system, you must achieve all three objectives.**

## Confidentiality:
Refers to the principle of restricting access to or knowledge of certain pieces of information to certain individuals.
There are several reasons for doing so.
* A company might not want competitors to know its trade secrets, key personnel salaries, list of customers, products in development, or sales and marketing plans
* A law firm might want to preserve attorney-client privilege
* A healthcare organization may want to secure ePHI and comply with HIPAA/HITECH requirements

Unfortunately, when two parties exchange information over a network, especially one as vulnerable as the internet, the confidentiality of that information will always be at risk.
Attackers can steal secret information by either carrying out a main-in-the-middle attack to eavesdrop on a transmission or hack directly into a server.

## Integrity:
Pertains to the principle of preventing data from being tampered. Data integrity is particularly crucial in business transactions where unauthorized alteration to data can lead to disputes, report misstatements, and financial losses.

Integrity can likewise be compromised during data transfers through either man-in-the-middle attacks (where attackers can intercept the data, make changes, and then forward the altered data to the intended recipient) or through a direct hack on the server.

## Availability:
In the case of file transfers, data access problems can be due to a variety of reasons.
* Power interruptions
* Network disruptions
* Server failures
* Missing files
* DDoS attacks
* Natural disasters

Availability issues can be a serious problem, especially if they involve business-critical data. More so if the data is part of a supply chain, where several organizations or business units can suffer.

## Technical solutions for achieving confidentiality in enterprise file transfers
Encryption solutions are usually grouped into two categories: those that encrypt data-at-rest and those that decrypt data-in-transit. File transfers require both.
**Data-in-transit encryption:** achieved through solutions like SSL or SSH
**Data-at-rest encryption:** achieved through OpenPGP or other disk-level or file-level encryption solutions.

**End-to-end encryption** is when you encrypt data before (while in the sender's server), during (while traversing the network) and after (upon arrival at the recipient's server) a file transfer.

## Integrity in enterprise file transfers
Hash functions and digital signatures are security elements that are readily available in secure file transfer protocols like FTPS, HTTPS, SFTP, and WebDAVs.

## Availability in enterprise file transfers
The best way to ensure service availability is to set up a high availability (HA) cluster. There are two ways to do this.
1. **Active-passive high availability configuration:** Entail setting up one or more failover server(s) that can immediately take over should the primary server go down.
2. **Active-active high availability configuration:** Set up two or more server(s) in such a way that they are both active servers. The main purpose of an active-active HA configuration is to distribute the workload and reduce the chance of a server from going down due to overload.
