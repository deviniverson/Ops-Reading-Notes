## What is cross-site scripting (XSS)?
A web security vulnerability that allows an attacker to compromise the interactions that users have with a vulnerable application. It allows an attacker to circumvent the same origin policy, which  is designed to segregate different websites from each other. Cross-site scripting vulnerabilities normally allow an attacker to masquerade as a victim user, to carry out any actions that the user is able to perform, and to access any of the user's data. 

### How does it work?
This works by manipulating a vulnerability web site so that it returns malicious JavaScript to users. When the malicious code executes inside the victim's browser, the attacker can fully compromise their interaction with the application.

### Types of XSS attacks:
* Reflected XSS, where the malicious script comes from the current HTTP request
* Stored XSS, where the malicious script comes from the website's database.
* DOM-based XSS, where the vulnerability exists in client-side code rather than server-side code.

### What can XSS be used for?
* Impersonate or masquerade as the victim user
* Carry out any action that the user is able to perform
* Read any data that the user is able to access.
* Capture the user's login credentials
* Perform virtual defacement of the web site
* Inject trojan functionality into the web site

### How to prevent XSS attacks:
* Filter input on arrival
* Encode data on output
* Use appropriate response headers
* Content Security Policy