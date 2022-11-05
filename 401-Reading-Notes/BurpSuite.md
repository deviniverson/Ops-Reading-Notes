## What is Burp Suite?
Burp Suite is a suite of tools from PortSwigger designed to aid in the penetration testing of web applications over both HTTP and HTTPS. The primary tool is a proxy designed to allow the analysis and editing of web traffic. The proxy can intercept web requests and responses and read and edit them in real-time before they reach their respective destinations.

Many of the tools included in Burp Suite are designed to integrate with the main proxy and can have requests imported to them.
* Intruder allows you to import a request and attempt and can then run through them automatically.
* Repeater allows you to import a web request and then make manual modifications to it and see the response side by side allowing you to make minor adjustments to attempted exploits and easily see if it's working.
* A dashboard feature shows a list of identified issues, although these need to be manually checked for false positives.
* Sequencer is designed to analyze the randomness of data such as session IDs, CSRF tokens, and password reset tokens.
* The decoder allows you to decode strings from a range of encoding standards as well as allowing you to encode data again.
* Comparer allows you to compare two strings to check for minor differences.
