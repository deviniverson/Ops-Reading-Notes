# What is a Reverse Proxy?
A reverse proxy is a server that sits in front of web servers and forwards client (web browser) requests to those web servers. Reverse proxies are typically implemented to help increase security, performance, and reliability.

## Proxy Server
A forward proxy server or proxy, web proxy, is a server that sits in front of a group of clients' machines. When those computers make requests to sites and services on the internet, the proxy server intercepts those requests and then communicates with web servers on behalf of those clients, like a middleman.
## 3 computers involved in a typical forward proxy communication.
1. User's home computer
2. A forward proxy server
3. A website's origin server (where the website data is stored)
## A few reasons one might want to use a forward proxy:
* To avoid state or institutional browsing restrictions
* To block access to certain content
* To protect their identity online

## The difference between forward and reverse proxy:
The difference is subtle but important. A simplified way to sum it up would be to sya that a forward proxy sits in front of a client and ensures that no origin server ever communicates directly with that specific client. On the other hand, a reverse proxy sits in front of an origin server and ensures that no client ever communicates directly with that origin server.

## Some benefits of a reverse proxy:
* Load Balancing
* Protection from attacks
* Global Server Load Balancing (GSLB)
* Caching
* SSL encryption