---
title: 1.Network Attacks
---

---
# 1. Network Attacks

1. Types of Attacks
1. Sources of Attacks

## What is an attack & Why do we do it ?

## Types of Attacks

- Denial of service
- Back door
- Spoofing
- Mathematical
- Brute force
- Software exploitation Attack

# Denial of service Attack

# Back door Attack

# Spoofing Attack

# Brute force Attack

# Software exploitation Attack

# 2 Types of Software

1. Good Software
1. Bad Software / Malicious Software

## MALWARE = **MAL**icious Soft**WARE**

# MALWARE
Any kind of intrusive software that is installed without consent can be classified malware. It can be it code, scripts or active content.

# Malware Attacks
- Viruses
- Worms
- Trojans
- Spyware
- Adware
- Rootkits

## Viruses

spreads via deliberate user action such as downloading a file or running a program

A computer virus is a type of malware that propagates by inserting a copy of itself into and becoming part of another program. It spreads from one computer to another, leaving infections as it travels. Viruses can range in severity from causing mildly annoying effects to damaging data or software and causing denial-of-service (DoS) conditions. Almost all viruses are attached to an executable file, which means the virus may exist on a system but will not be active or able to spread until a user runs or opens the malicious host file or program. When the host code is executed, the viral code is executed as well. Normally, the host program keeps functioning after it is infected by the virus. However, some viruses overwrite other programs with copies of themselves, which destroys the host program altogether. Viruses spread when the software or document they are attached to is transferred from one computer to another using the network, a disk, file sharing, or infected e-mail attachments.

## Worms

spreads automatically by replicating itself across computers or networks

Computer worms are similar to viruses in that they replicate functional copies of themselves and can cause the same type of damage. In contrast to viruses, which require the spreading of an infected host file, worms are standalone software and do not require a host program or human help to propagate. To spread, worms either exploit a vulnerability on the target system or use some kind of social engineering to trick users into executing them. A worm enters a computer through a vulnerability in the system and takes advantage of file-transport or information-transport features on the system, allowing it to travel unaided.

## Trojans

spreads by appearing safe or desirable but disguising its true intent (e.g., backdoors)

A Trojan is another type of malware named after the wooden horse the Greeks used to infiltrate Troy. It is a harmful piece of software that looks legitimate. Users are typically tricked into loading and executing it on their systems. After it is activated, it can achieve any number of attacks on the host, from irritating the user (popping up windows or changing desktops) to damaging the host (deleting files, stealing data, or activating and spreading other malware, such as viruses). Trojans are also known to create back doors to give malicious users access to the system.
Unlike viruses and worms, Trojans do not reproduce by infecting other files nor do they self-replicate. Trojans must spread through user interaction such as opening an e-mail attachment or downloading and running a file from the Internet.

## Bots

runs in the background while hijacking computing resources (e.g., bot networks)

## Spyware

monitors user activities for marketing purposes or keylogs user credentials

## Adware

serves unwanted ads or redirects user’s browser traffic

## Spyware

## Adware

## Rootkits

Stuxnet - the first known rootkit for industrial control systems

A rootkit is a clandestine computer program designed to provide continued privileged access to a computer while actively hiding its presence. The term rootkit is a connection of the two words "root" and "kit." Originally, a rootkit was a collection of tools that enabled administrator-level access to a computer or network. Root refers to the Admin account on Unix and Linux systems, and kit refers to the software components that implement the tool. Today rootkits are generally associated with malware – such as Trojans, worms, viruses – that conceal their existence and actions from users and other system processes.

## What Can a Rootkit Do?

A rootkit allows someone to maintain command and control over a computer without the computer user/owner knowing about it. Once a rootkit has been installed, the controller of the rootkit has the ability to remotely execute files and change system configurations on the host machine. A rootkit on an infected computer can also access log files and spy on the legitimate computer owner’s usage.

## Rootkit Detection

It is difficult to detect rootkits. There are no commercial products available that can find and remove all known and unknown rootkits. There are various ways to look for a rootkit on an infected machine. Detection methods include behavioral-based methods (e.g., looking for strange behavior on a computer system), signature scanning and memory dump analysis. Often, the only option to remove a rootkit is to completely rebuild the compromised system.

## Rootkit Protection

Many rootkits penetrate computer systems by piggybacking with software you trust or with a virus. You can safeguard your system from rootkits by ensuring it is kept patched against known vulnerabilities. This includes patches of your OS, applications and up-to-date virus definitions. Don't accept files or open email file attachments from unknown sources. Be careful when installing software and carefully read the end-user license agreements.

Static analysis can detect backdoors and other malicious insertions such as rootkits. Enterprise developers as well as IT departments buying ready-made software can scan their applications to detect threats including "special" and "hidden-credential" backdoors. 

## OWASP 🐝

> Open Web Application Security Project

## OWASP Top 10

1. Injection
1. Weak Authentication and session management
1. XSS (Cross site scripting)
1. Insecure Direct Object References
1. Security Misconfiguration
1. Sensitive Data Exposure
1. Missing Function Level Access Control
1. Cross Site Request Forgery
1. Using Components with Known Vulnerabilities
1. Unvalidated Redirects and Forwards


## Sources of attacks

- Internal
	- Disaffected staff

- External
	- Via internet connections
	- Through unsecured wireless access point
	- Viruses introduced by email

---
## External Links

[Ransomware - Anatomy of an Attack](https://www.youtube.com/watch?v=4gR562GW7TI)

[Anatomy of an IoT Attack](https://www.youtube.com/watch?v=GvLnb4YQHh0)

[The Attack](https://www.youtube.com/watch?v=CMsp8WiBxzM)

[STUXNET: The Virus that Almost Started WW3](https://www.youtube.com/watch?v=7g0pi4J8auQ)

[Stuxnet Malware Analysis Paper](https://www.codeproject.com/Articles/246545/Stuxnet-Malware-Analysis-Paper)

[Stuxnet on Wikipedia](https://en.wikipedia.org/wiki/Stuxnet)

[Classes of Malicious Software](https://www.cisco.com/c/en/us/about/security-center/virus-differences.html)

[Backdoors](https://www.youtube.com/watch?v=7ZwGvFu9WhY)

[Veracode](https://www.veracode.com/security/rootkit)
