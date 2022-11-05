## Why SQL Injection Matters
Standardized query language (SQL) is, in one form or another, still the dominant method of inserting, filtering and retrieving information from a database. Loads of SQL queries will be coursing through your web applications on almost every page load - regardless if it's a tiny toy website with a tiny SQLite file, or a popular ecommerce site with millions of visits per hour.
An attacker who is armed with literally nothing but a web browser, some basic SQL knowledge and an internet connection, can exploit flaws in your web application - extracting user data, discovering or resetting credentials and using it as a launch point for deeper assaults on your network.

### How do Web Frameworks Prevent SQL Injection?
In general, web frameworks prevent SQL injection attacks by providing easy methods of data querying so that developers aren't seduced into writing hideously vulnerable SQL string concatenation statements.
They perform two important tasks:
1. They offer specific user input sanitization countermeasures to defend common SQL Injection patterns: the framework will strip NULL characters, line breaks, single quotes, etc. that are often used to piggyback additional SQL commands into an intended query.
2. They provide a syntax for declaring what a SQL statement is supposed to look like before actually trying to execute it.

### What's vulnerable to SQL injection attacks?
Everything having a web configuration interface backed by a database is responsible for everything being susceptible to SQL injection attacks.
Example include:
* Smart Home Hubs - Smart home hubs can be compromised, their credentials overridden, people can spy on you with your own security system.
* Network Equipment - Once cracked, network devices like routers and switches offer a tremendous foothold for launching more in depth attacks deeper into a network
* Fancy Electric Sport Cars - Can be remotely hacked, have their accounts compromised and the possibility of remotely disabling the car
* Android Apps - Once compromised your private pictures and contacts are vulnerable