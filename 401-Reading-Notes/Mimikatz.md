# Pass the Hash with Mimikatz

## What is Mimikatz?
Mimikatz is an open-source application that allows users to view and save authentication credentials such as Kerberos tickets. The toolset works with the current release of Windows and includes a collection of different network attacks to help assess vulnerabilities. Attackers commonly use Mimikatz to seal credentials and escalate privileges because in most cases, endpoint protection software and antivirus systems will not detect or delete the attack.

## What can Mimikatz do?
* Pass-the-hash: Attackers use Mimikatz to pass an exact hash string to log in to the target computer.
* Pass-the-ticket: Mimikatz provides functionality for a user to pass a Kerberos ticket to another computer and log in with that user's ticket.
* Overpass-the-hash: This technique passes a unique key obtained from a domain controller to impersonate a user.
* Kerberoast golden tickets: A golden ticket gives you non-expiring domain admin credentials to any computer on the network.
* Kerberoast silver tickets: Kerberos grants a user a TGS ticket that's used to log into any services on the network.
* Pass-the-cache: Generally the same as a pass-the-ticket, but uses the saved and encrypted login data on a Mac/UNIX/Linux system.

## How do you use Mimikatz?
1. Run Mimikatz as an administrator. (Run as admin even if you're already using an administrator account)
2. Check your version of Mimikatz - 32bit or 64bit.
3. Extract "Clear text passwords" from memory - The module "sekurlsa" lets you dump passwords from memory.
The output will show if you have appropriate permissions to continue.
a. mimkatz # privilege::debug
start the logging functions so you can refer back to your work
b. mimkatz # log nameoflog.log
output all of the clear text passwords stored on this computer
c. mimkatz # sekurlsa::logonpasswords

## How do you defend against Mimikatz?
1. Restrict admin privileges
2. Change caching policy (Disable password-caching)
3. Turn off debugging privileges.
4. Increase local security authority (Configure additional local security authority (LSA) protection.)