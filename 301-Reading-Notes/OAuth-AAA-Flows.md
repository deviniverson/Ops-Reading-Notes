## What is OAuth?
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.

### Give an example of what using OAuth would look like.
The simplest example of OAuth is when you go to log into a website, and it offers one or more opportunities to log on using another website’s/ service’s logon. You then click on the button linked to the other website, the other website authenticates you and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.

### How does OAuth work? What are the steps that it takes to authenticate the user?
1. OAuth only works using HTTPS, the user initiates a feature/transaction that needs to access another unrelated site or service.
2. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
3. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
4. The first site gives this token and secret to the initiating user’s client software.
5. The client’s software presents the request token and secret to their authorization provider (which my or may not be the second site)
6. If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
7. The user approves (or their software silently approves) a particular transaction type at the first website.
8. The user is given an approved access token (notice it’s no longer a request token)
9. The user gives the approved access token to the first website.
10. The first website gives the access token to the second website as proof of authentication on behalf of the user.
11. The second website lets the first website access their site on behalf of the user.
12. The user sees a successfully completed transaction occurring.

OAuth is not the first authentication/ authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly.
 
## Authorization and Authentication flows

### What is the difference between authorization and authentication?
* Authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.
* Real-world Example: When you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.

### What is Authorization Code Flow?
* Server-side apps where the source code is not publicly exposed, can use the Authorization Code Flow, which exchanges an Authorization Code for a token.

### What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
* Mobile and native applications can use the Authorization Code Flow, but require additional security. OAuth 2.0 provides a version of the Authorization Code Flow which use of a Proof Key for Code Exchange (PKCE)

### What is Implicit Flow with Form Post?
* Intended for public clients, or applications which are unable to securely store Client Secrets. Is no longer considered a best practice for requesting Access Tokens.

### What is Client Credentials Flow?
* Machine-to-machine system authenticates and authorizes the app rather than a user.

### What is Device Authorization Flow?
* Uses the an internet link on their computer or smartphone and authorize the device.

### What is Resource Owner Password Flow?
* Requests that users provide credentials (username and password), typically using an interactive form. 