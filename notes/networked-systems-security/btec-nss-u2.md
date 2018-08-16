---
title: # 2.Security Systems
---

footer: *Networked Systems Security*
slidenumbers: true
autoscale: true
build-lists: true

# 2. Security Systems

> Know about security related hardware and software
1. Email systems
- Security features eg secure MIME, spam, hoaxing, relay agents
1. Wireless systems: security features eg site surveys, MAC association, WEP/WPA keys,TKIP
1. Networked devices: security features eg router, switch, wireless access point
1. Transmission media: issues eg use of shielding
1. Personal access control: devices eg biometrics, passwords, usernames, permissions, digital signatures
1. Security control at device level: access control eg protocols, log in, certificates
1. Encryption: eg encrypting files for confidentiality, encryption with application-specific tools, recovering encrypted data
1. Intrusion detection systems: devices eg firewalls, virus protection, spyware protection, file monitoring, folder monitoring, use of honeypots, alarms

---
 
# Email Systems

- S/MIME (Secure/Multipurpose Internet Mail Extensions)
- SPAM (stupid pointless annoying messages)

<!-- - HOAXING -->
<!-- - Relay Agents -->

---

# Wireless Systems

<!-- - Site Surveys -->
<!-- - MAC Assocications -->
- WEP/WPA Keys
- TKIP

<!-- --- -->

<!-- # 1. Site Surveys -->

<!-- A wireless site survey, sometimes called an RF site survey or wireless survey, is the process of planning and designing a wireless network, to provide a wireless solution that will deliver: -->

<!-- - the required wireless coverage,
- data rates,
- network capacity,
- roaming capability and
- Quality of Service (QoS) -->

<!-- The survey usually involves a site visit to test for RF interference, and to identify optimum installation locations for access points. This requires analysis of building floor plans, inspection of the facility, and use of site survey tools. Interviews with IT management and the end users of the wireless network are also important to determine the design parameters for the wireless network. As part of the wireless site survey, the effective range boundary is set, which defines the area over which signal levels needed support the intended application. This involves determining the minimum signal to noise ratio (SNR) needed to support performance requirements. Wireless site survey can also mean the walk-testing, auditing, analysis or diagnosis of an existing wireless network, particularly one which is not providing the level of service required. -->

<!-- ---

# 2. MAC Associations

- MAC Address Filtering
- Whitelisting
- Blacklisting -->

---

# 3. WEP/WPA Keys

- WEP - Wired Equivalent Privacy
- WPA - Wireless Protected Access
- WPA2 Keys
- WPA2 Enterprise

<!-- # Radio Analogy -->

---

### WEP - Wired Equivalent Privacy

- 64bit / 128bit Key Size

### WPA - Wireless Protected Access

- Encryption Algorithm
	- RC4
- Protocol
	- TKIP (Temporal Key Integrity Protocol)
- Every Packet gets a unique encryption key

### WPA2
- Encryption Algorithm
	- AES (Advanced Encryption Standard)
- Protocol
	- CCMP (Counter Mode Cipher Block Chaining) Message Authentication Code Protocol

### WPA2 Enterprise
- Supports user grouping

<!-- # IDS -->





---

| ENCRYPTION STANDARD | Protocol | Algorithm | Should you use it? |
| :---: | :---: | :---: | :---: |
| WEP | TKIP | RC4 | No |
| WPA | TKIP | RC4 | Only if WPA2 is not available |
| WPA2 | CCMP | AES | Yes |



---

# External Links

[Host Based IDS](https://www.alienvault.com/blogs/security-essentials/open-source-intrusion-detection-tools-a-quick-overview)