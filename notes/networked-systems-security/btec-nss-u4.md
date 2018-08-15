---
title: # 4.Apply System Security
---
footer: *Networked Systems Security*
slidenumbers: true
autoscale: true
build-lists: true

# 4.Apply System Security

### Table of Content

- Administration
  - Procedures
    - Implementing password policy,
    - Locking down user accounts,
    - Securing administrator’s permissions,
    - Protecting against viruses,
    - Restricting access to critical services,
    - Installing or updating security software
- Algorithms
  - Types
    - Private Key (Symmetric) Encryption
    - Private/Public key (Asymmetric) encryption
  - Examples
    - DES
    - 3DES
    - RSA
    - Hashing
- Transport methods
  - IPSEC
  - GRE
  - VPN
- Application
  - Certificates (SSL)
  - Trust memberships
- Filtering
  - Firewalls
  - Access control lists ()
- Test
  - Test for functionality
  - Test for performance
    - Does security measure slow down system functions



## Administration:
  - Procedures
    - Implementing password policy
    - Locking down user accounts
    - Securing administrator’s permissions
    - Protecting against viruses
    - Restricting access to critical services
    - Installing or updating security software
## Algorithms
  
  There are two types of cryptosystem based on the nature of key generation and usage.
  - Symmetric CryptoSystem / Private Key Encryption / Private Key Cryptography
  - Asymmetric CryptoSystem / Private/Public Key Encryption / Private/Public Key Cryptography

### 1. Private Key Encryption


### 2. Private/Public key encryption

  - Examples
    - DES
    - 3DES
    - RSA
    - Hashing
## Transport methods
  
1. IPSEC
1. GRE
1. VPN

### 1. IPSEC

#### Application of IPsec

* Secure branch office connectivity over the Internet
* Secure remote access over the Internet
* Establishing extranet and intranet connectivity with partners
* Enhancing electronic commerce security

#### Benefits of IPsec

* When IPsec is implemented in a firewall or router, it provides strong security that can be applied to all traffic crossing the perimeter.Traffic within a company or workgroup does not incur the overhead of security-related processing.

* IPsec in a firewall is resistant to bypass if all traffic from the outside must use IP and the firewall is the only means of entrance from the Internet into the organization.

* IPsec is below the transport layer (TCP, UDP) and so is transparent to applications. There is no need to change software on a user or server system when IPsec is implemented in the firewall or router. Even if IPsec is implemented in end systems, upper-layer software, including applications, is not affected.

* IPsec can be transparent to end users.There is no need to train users on security mechanisms, issue keying material on a per-user basis, or revoke keying material when users leave the organization.

* IPsec can provide security for individual users if needed.This is useful for offsite workers and for setting up a secure virtual subnetwork within an organization for sensitive applications.

### 2. GRE (Generic Routing Encapsulation)
<!-- https://www.juniper.net/documentation/en_US/junos/topics/concept/gre-tunnel-services.html -->
Generic Routing Encapsulation (GRE) is a tunneling protocol developed by Cisco Systems that can encapsulate a wide variety of network layer protocols inside virtual point-to-point links over an Internet Protocol network.
Generic routing encapsulation (GRE) provides a private, secure path for transporting packets through an otherwise public network by encapsulating (or tunneling) the packets.

GRE encapsulates data packets and redirects them to a device that de-encapsulates them and routes them to their final destination. This allows the source and destination switches to operate as if they have a virtual point-to-point connection with each other (because the outer header applied by GRE is transparent to the encapsulated payload packet). For example, GRE tunnels allow routing protocols such as RIP and OSPF to forward data packets from one switch to another switch across the Internet. In addition, GRE tunnels can encapsulate multicast data streams for transmission over the Internet.

Data is routed by the system to the GRE endpoint over routes established in the route table. (These routes can be statically configured or dynamically learned by routing protocols such as RIP or OSPF.) When a data packet is received by the GRE endpoint, it is de-encapsulated and routed again to its destination address.

GRE tunnels are stateless-–that is, the endpoint of the tunnel contains no information about the state or availability of the remote tunnel endpoint. Therefore, the switch operating as a tunnel source router cannot change the state of the GRE tunnel interface to down if the remote endpoint is unreachable.

- Encapsulation and De-Encapsulation on the Switch
Encapsulation—A switch operating as a tunnel source router encapsulates and forwards GRE packets as follows:

When a switch receives a data packet (payload) to be tunneled, it sends the packet to the tunnel interface.
The tunnel interface encapsulates the data in a GRE packet and adds an outer IP header.
The IP packet is forwarded on the basis of the destination address in the outer IP header.
De-encapsulation—A switch operating as a tunnel remote router handles GRE packets as follows:

When the destination switch receives the IP packet from the tunnel interface, the outer IP header and GRE header are removed.
The packet is routed based on the inner IP header.

### 3. VPN (Virtual Private Network)

A VPN, or Virtual Private Network, is a secure tunnel between two or more devices. VPNs are used to protect private web traffic from snooping, interference, and censorship.
ExpressVPN can also act as a proxy, allowing you to surf the web anonymously from wherever you want.

- Hide your IP address and location
- Encrypt your communications
- Access blocked-content based on geo-location
 
## Application
  - SSL Certificates
  - Trust memberships

### SSL Certificates

SSL Certificates are small data files that digitally bind a cryptographic key to an organization’s details. When installed on a web server, it activates the padlock and the https protocol and allows secure connections from a web server to a browser. Typically, SSL is used to secure credit card transactions, data transfer and logins, and more recently is becoming the norm when securing browsing of social media sites.

SSL Certificates bind together:
- A domain name, server name or hostname.
- An organizational identity (i.e. company name) and location.

What is an SSL Certificate?
SSL Certificates are small data files that digitally bind a cryptographic key to an organization’s details. When installed on a web server, it activates the padlock and the https protocol and allows secure connections from a web server to a browser. Typically, SSL is used to secure credit card transactions, data transfer and logins, and more recently is becoming the norm when securing browsing of social media sites.

SSL Certificates bind together:

A domain name, server name or hostname.
An organizational identity (i.e. company name) and location.


An organization needs to install the SSL Certificate onto its web server to initiate a secure session with browsers. Once a secure connection is established, all web traffic between the web server and the web browser will be secure.

When a certificate is successfully installed on your server, the application protocol (also known as HTTP) will change to HTTPs, where the ‘S’ stands for ‘secure’. Depending on the type of certificate you purchase and what browser you are surfing the internet on, a browser will show a padlock or green bar in the browser when you visit a website that has an SSL Certificate installed.

- How Does an SSL Certificate Work?
SSL Certificates use something called public key cryptography.

This particular kind of cryptography harnesses the power of two keys which are long strings of randomly generated numbers. One is called a private key and one is called a public key.A public key is known to your server and available in the public domain. It can be used to encrypt any message. If Alice is sending a message to Bob she will lock it with Bob’s public key but the only way it can be decrypted is to unlock it with Bob’s private key. Bob is the only one who has his private key so Bob is the only one who can use this to unlock Alice’s message. If a hacker intercepts the message before Bob unlocks it, all they will get is a cryptographic code that they cannot break, even with the power of a computer.

If we look at this in terms of a website, the communication is happening between a website and a server. Your website and server are Alice and Bob.

- Why Do I Need An SSL Certificate?
SSL Certificates protect your sensitive information such as credit card information, usernames, passwords etc. It also:

  - Keeps data secure between servers
  - Increases your Google Rankings
  - Builds/Enhances customer trust 
  - Improves conversion rates

- Where Do I Buy An SSL Certificate?
SSL Certificates need to be issued from a trusted Certificate Authority. Browsers, operating systems, and mobile devices maintain list of trusted CA root certificates.

The Root Certificate must be present on the end user's machine in order for the Certificate to be trusted. If it is not trusted the browser will present untrusted error messages to the end user. In the case of e-commerce, such error messages result in immediate lack of confidence in the website and organizations risk losing confidence and business from the majority of consumers.

Companies like GlobalSign are known as trusted Certificate Authorities. This is because browser and operating system vendors such as Microsoft, Mozilla, Opera, Blackberry, Java, etc., trust that GlobalSign is a legitimate Certificate Authority and that it can be relied on to issue trustworthy SSL Certificates. The more applications, devices and browsers the Certificate Authority embeds its Root into, the better "recognition" the SSL Certificate can provide.

GlobalSign was founded in 1996 in Europe and remains one of the longest running Certificate Authorities in the region.

### Trust memberships

## Filtering
  - Firewalls
  - Access control lists

## Test
  - Test for functionality
  - Test for performance
    - Does security measure slow down system functions