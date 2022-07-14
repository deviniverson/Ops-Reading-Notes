Microsoft's directory and identity management service for Windows domain networks.

## Active Directory is made up of a number of different directory services, including:
* Active Directory Domain Services (AD DS): the core Active Directory service used to manage users and resources.
* Active Directory Lightweight Directory Services (AD LDS): a low-overhead version of AD DS for directory-enabled applications.
* Active Directory Certificate Services (AD CS): for issuing and managing digital security certificates.
* Active Directory Federation Services (AD FS): for sharing identity and access management information across organizations and enterprises.
* Active Directory Rights Management Services (AD RMS): for information rights management (controlling access permissions to documents, workbooks, presentations, etc.)

## Fundamental AD features and capabilities includes:
* **A schema** that defines the classes of objects and attributes contained in the directory.
* **A global catalog** that contains detailed information about every object in the directory
* **A query and index mechanism** that allows users, administrators, and applications to efficiently find directory information
* **A replication service** that disseminates directory data across the network
The Active Directory schema supports various types of objects like User, Group, Contact, Computer, Shared Folder, Printer, and Organizational Unit, along with a set of descriptive attributes for each object. For example, User Object attributes include information like the user's name, address, and telephone number.
Active Directory makes user of other security and network protocols including LDAP, DNS, and Microsoft's version of the Kerberos authentication protocol.

## Active Directory Data Structures
* **A domain** is a collection of objects (e.g. users, devices) that share the same Active Directory database. A domain is identified by a DNS name like company.com
* **A tree** is a collection of one or more domains with a contiguous namespace (they have a common DNS root name like marketing.company.com, engineering.company.com)
* **A forest** is a collection of one or more trees that share a common shema, global catalog, and directory configuration - but aren't part of a contiguous namespace.

## Active Directory Benefits
* **Security** - Active Directory helps businesses improve security by controlling access to network resources.
* **Extensibility** - companies can easily organize Active Directory data to align with their organizational structure and business needs.
* **Simplicity** - administrators can centrally manage user identities and access privileges across the enterprise, helping businesses simplify management and reduce operations expenses.
* **Resiliency** - Active Directory supports redundant components and data replication to enable high availability and business continuity.
