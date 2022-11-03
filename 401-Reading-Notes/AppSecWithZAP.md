## Security Testing Basics
Software security testing is the process of assessing and testing a system to discover security risks and vulnerabilities of the system and its data.
* Assessing is defined as the analysis and discovery of vulnerabilities without the attempting to actually exploit them.
* Testing is defined as the discovery and attempted exploitation of vulnerabilities.

A common breakout of Security Testing is:
* Vulnerability Assessment - The system is scanned and analyzed for security issues.
* Penetration Testing - The system undergoes analysis and attack from simulated malicious attackers.
* Runtime Testing - The system undergoes analysis and security testing from an end user.
* Code Review - The system code undergoes a detailed review and analysis looking specifically for security vulnerabilities.

### Penetration Testing
Carried out as if the tester was a malicious external attacker with a goal of breaking into the system and either stealing data or carrying out some sort of denial-of-service attack.

### The Pentesting Process
* Explore - Tester attempts to learn about the system being tested.
* Attack - The tester attempts to exploit the known or suspected vulnerabilities to prove they exist.
* Report - The tester reports back the results of their testing, including the vulnerabilities, how they exploited them and how difficult the exploits were, and the severity of the exploitation.

## ZAP (Zed Attack Proxy)
Free, open-source penetration testing tool being maintained under the umbrella of the Open Web Application Security Project (OWASP).

ZAP is what is known as a "man-in-the-middle-proxy". It stands between the tester's browser and the web application so that it can intercept and inspect messages sent between browser and web application, modify the contents if needed, and then forward these packets on to the destination. It can be used as a stand-alone application, and as a daemon process. 
