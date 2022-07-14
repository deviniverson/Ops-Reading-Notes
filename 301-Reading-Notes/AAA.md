# Computer Network | AAA (Authentication, Authorization and Accounting)
 
## AAA (Authentication, Authorization, Accounting)
 
AAA is the standard-based framework used to control who is permitted to use network resources (through authentication), what they are authorized to do (through authorization), and capture the actions performed while accessing the network (through accounting).
 
## AAA implementation: AAA can be implemented by using the local database of the device or by using an external ACS server.
 
* Local database – if we want to use the local running configuration of the router or switch to implement AAA, we should create users first for authentication and provide privilege levels to users for Authorization.
* ACS server – This is the common method used. An external ACS server is used for AAA on which configuration on both router and ACS is required. The configuration includes creating a user, separate customized method list for authentication, Authorization, and Accounting. The client or Network Access Server (NAS) sends authentication requests to the ACS server and the server takes the decision to allow the user to access the network resource or not according to the credentials provided by the user.
 
## Resource: 
https://www.geeksforgeeks.org/computer-network-aaa-authentication-authorization-and-accounting/
