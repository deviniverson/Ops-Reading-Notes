# What is PKI (Public Key Infrastructure)?

Public Key Infrastructure is a technology for authenticating users and devices in the digital world. The basic idea is to have one or more trusted parties digitally sign documents certifying that a particular
cryptographic key belongs to a particular user or device. The key can then be used as an identity for the user in digital networks.

Users and devices that have keys are often just called entities. In general, anything can be associated with a key that it can use as its identity.
### Besides a user or device, it could be a:
* program
* process
* manufacturer
* component

## The purpose of a PKI is to securely associate a key with an entity.

The trusted party signing the document associating the key with the device is called a certificate authority (CA). The certificate authority also has a cryptographic key that it uses for signing these documents.
These documents are called certificates.

A public key infrastructure relies on digital signature technology, which uses public key cryptography. The basic idea is that entity and is used for signing. This key is called the private key.
There is another key derived from it, called the public key, which is used for verifying signatures but cannot be used to sign.

## X.509 Standard
Most public key infrastructures use a standardized machine-readable certificate format for the certificate documents. The standard is called X.509v3. Originally, it was an ISO standard, but these days it is maintained by the Internet Engineering Task Force as RFC 3280.

## Common Uses of Certificates
### Secure Websites - HTTPS
Most familiar use of PKI is in SSL certificates. SSL(Secure Sockets Layer) is the security protocol used on the web when you fetch a page whose address begins with https:. TLS (Transport Layer Security) is a newer version of the protocol.
Certificates and cryptographic authentication of the server prevent man-in-the-middle attacks.

### Authenticating Users and Computers - SSH
The Secure Shell protocol supports certificates for authenticating hosts and users. Tectia SSH uses standards-based X.509 certificates, whereas OpenSSH uses its own proprietary certificate formats.

### Email Signing and Encryption
Certificates are also used for secure email in corporations. The S/MIME standard specifies a message format for signed and encrypted messaging, using the X.509 certificate formats.

### Security Limitations of Public Key Infrastructure
The main weakness of public PKI is that any certificate authority can sign a certificate for any person or computer. Certificate authorities exist in many countries, some of which have rather authoritarian or even potentially hostile governments. 
Sometimes certificate authorities create or are coerced to create certificates for parties they have no business vouching for. Among other things, intelligence agencies can use fraudulent certificates for espionage, malware injection, and forging messages or evidence to disrupt or discredit adversaries. For this reason, only limited trust should be placed on certificates from public certificate authorities.