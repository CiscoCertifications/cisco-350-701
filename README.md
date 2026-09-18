# Cisco 350-701 SCOR Exam: Implementing and Operating Cisco Security Core Technologies

[![Cisco Certified](https://img.shields.io/badge/Cisco_Certified-CCNP_Security_Core_|_CCIE_Qualifier-049fd9?style=for-the-badge&logo=cisco&logoColor=white)](https://www.cisco.com/)
[![Track](https://img.shields.io/badge/Track-Security_Core-049fd9?style=for-the-badge&logo=cisco)](https://www.cisco.com/)
[![Level](https://img.shields.io/badge/Level-Professional_Core_|_Expert_Qualifier-1BA0D7?style=for-the-badge)](https://www.cisco.com/)
[![Duration](https://img.shields.io/badge/Duration-120_Minutes-orange?style=for-the-badge)](https://www.cisco.com/)
[![Score](https://img.shields.io/badge/Passing_Score-~825%20%2F%201000-blue?style=for-the-badge)](https://www.cisco.com/)
[![Practice Partner](https://img.shields.io/badge/Practice_Partner-CertsClub_(20%25_Off_Code:_club20)-28a745?style=for-the-badge&logo=shield)](https://www.certsclub.com/cisco/)

---

## 1. Exam Overview & Candidate Profile

The **Cisco 350-701 SCOR (Implementing and Operating Cisco Security Core Technologies)** exam is the flagship security examination that qualifies candidates for both the **CCNP Security** certification and serves as the written prerequisite for the **CCIE Security** 8-hour practical lab exam.

The examination tests a candidate's advanced security skills across core cybersecurity domains: foundational security concepts (Zero Trust, PKI, cryptography), network security (Next-Generation Firewalls, NGIPS, VPNs, routing security), cloud security (Cisco Umbrella, CASB, Cloud Mailbox Defense), content security (Cisco Secure Email and Web Appliances), endpoint security (Cisco Secure Endpoint / AMP), and secure network visibility and enforcement (Cisco ISE, 802.1X, TrustSec, and Secure Network Analytics / Stealthwatch).

### Target Candidate Profile & Roles
* **Senior Network Security Engineer / Security Infrastructure Architect**
* **Security Operations Center (SOC) Escalation Lead**
* **Zero Trust & Cloud Security Solutions Consultant**
* **Candidate for CCIE Security Lab Exam**
* **Prerequisites:** Strong operational understanding of IP networking, network defense appliances, and security architecture (3–5 years practical experience recommended).

---

## 2. Key Exam Specifications

| Parameter | Official Specification |
| :--- | :--- |
| **Exam Code** | 350-701 |
| **Exam Name** | Implementing and Operating Cisco Security Core Technologies (SCOR) |
| **Associated Credentials** | CCNP Security Core / CCIE Security Qualifier / Specialist |
| **Duration** | 120 Minutes |
| **Passing Score** | ~825 / 1000 (Dynamic scaled calibration) |
| **Question Count** | 90–105 questions |
| **Question Formats** | Multiple Choice (single/multiple select), Drag-and-Drop, Simlets, Security Topology Scenarios |
| **Delivery Vendor** | Pearson VUE Authorized Test Centers & OnVUE Online Remote Proctored |
| **Practice Test Partner** | **[350-701 Practice Test](https://www.certsclub.com/cisco/)** (Coupon: `club20` for 20% off) |

---

## 3. Skills Measured & Blueprint Domain Weighting

| Domain Code | Domain Title | Exam Weight | Key Technical Objectives Covered |
| :--- | :--- | :---: | :--- |
| **1.0** | **Security Concepts** | **25%** | Zero Trust architecture (NIST SP 800-207); Common vulnerabilities and attacks (SQLi, XSS, CSRF, DDoS, MITM); Cryptographic algorithms (NGE, AES-GCM, SHA-2, Elliptic Curve, RSA); Public Key Infrastructure (PKI, CRL, OCSP, SCEP); Threat intelligence and MITRE ATT&CK mapping. |
| **2.0** | **Network Security** | **20%** | Cisco Firepower Threat Defense (FTD) and FMC management; Next-Generation IPS (Snort 3); Site-to-site and remote access VPNs (IKEv2, FlexVPN, AnyConnect SSL/DTLS); Layer 2 security (DHCP Snooping, DAI, Port Security, Private VLANs); Control Plane Policing (CoPP). |
| **3.0** | **Securing the Cloud** | **15%** | Cisco Umbrella (DNS-layer security, Cloud-Delivered Firewall, Secure Web Gateway, Cloud Access Security Broker - CASB); Cloud Mailbox Defense; Securing cloud workloads in AWS, Azure, and Google Cloud; API security. |
| **4.0** | **Content Security** | **15%** | Cisco Secure Email (ESA) features: Sender Policy Framework (SPF), DKIM, DMARC, Outbreak Filters, Email Encryption, DLP; Cisco Secure Web Appliance (WSA) features: WCCP, explicit proxy, SSL Decryption, authentication policies. |
| **5.0** | **Endpoint Protection and Detection** | **10%** | Cisco Secure Endpoint (AMP for Endpoints): File Trajectory, Device Trajectory, engines (Spero, Ethos, Tetra, Orbital); Endpoint Posture assessment; Cloud and on-premises threat analysis. |
| **6.0** | **Secure Network Access, Visibility, and Enforcement** | **15%** | Cisco Identity Services Engine (ISE): 802.1X, MAB, Central Web Auth (CWA), RADIUS CoA; Cisco TrustSec (SGTs, SGACLs); Cisco Secure Network Analytics (Stealthwatch): NetFlow analysis, behavioral anomaly detection, Encrypted Traffic Analytics (ETA). |

---

## 4. Scenario-Based Technical Practice Questions

### Scenario 1: Zero Trust Architecture - NIST SP 800-207 Core Logical Components
**Topology Background:**  
An enterprise adopts a Zero Trust Architecture (ZTA) aligned with NIST SP 800-207 across its hybrid cloud environments. An employee requests access to an internal accounting application from a home laptop. In the NIST ZTA reference model, which logical component is responsible for evaluating user credentials, device posture, and enterprise security policies to make the definitive decision whether to grant or deny access?

* A. Policy Enforcement Point (PEP)
* B. Policy Decision Point (PDP) / Policy Engine (PE)
* C. Data Plane Gateway
* D. Static Network Firewall

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* Under NIST SP 800-207, the Zero Trust architecture splits control into two core logical planes:
  1. **Policy Decision Point (PDP):** Composed of the **Policy Engine (PE)** (which evaluates enterprise policy, threat intelligence, and behavioral analytics to make the actual grant/deny decision) and the **Policy Administrator (PA)** (which issues credentials or commands to establish the session).
  2. **Policy Enforcement Point (PEP):** The component (such as an edge gateway, proxy, or agent) that intercepts, terminates, and enables connections between the client and enterprise resource upon instruction from the PDP.
* Distractor analysis: Option A (PEP) enforces the decision but does not evaluate policy to decide. Options C and D are data forwarding mechanisms.

---

### Scenario 2: Public Key Infrastructure - OCSP vs. CRL Validation
**Topology Background:**  
A security administrator configures mutual TLS (mTLS) certificate authentication for corporate web gateways. Under high-throughput conditions, downloading the complete Certificate Revocation List (CRL) introduces significant network latency and memory overhead on the security appliances. Which protocol should the administrator configure to enable real-time, per-certificate revocation checks without downloading large multi-megabyte revocation lists?

* A. Simple Network Management Protocol (SNMP)
* B. Online Certificate Status Protocol (OCSP)
* C. Simple Certificate Enrollment Protocol (SCEP)
* D. Directory Access Protocol (LDAP) bulk query

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* **Online Certificate Status Protocol (OCSP) (RFC 6960):** Provides a lightweight, real-time query mechanism to verify the revocation status of a specific X.509 digital certificate.
* Instead of periodically downloading large, static **Certificate Revocation Lists (CRLs)**, the validating appliance sends an OCSP request containing the serial number of the single certificate in question to an **OCSP Responder**. The responder replies immediately with `Good`, `Revoked`, or `Unknown`.
* Distractor analysis: Option A is a management protocol. Option C (SCEP) is used to enroll and obtain certificates, not verify revocation. Option D (LDAP) is used to retrieve static CRL distribution points.

---

### Scenario 3: Cloud Security - Cisco Umbrella DNS-Layer Protection & Intelligent Proxy
**Topology Background:**  
An enterprise implements Cisco Umbrella to protect off-network remote laptops from phishing domains. When a user requests a domain that Cisco Talos categorizes as "Suspicious / Gray" (neither definitively malicious nor definitively benign), how does Cisco Umbrella handle the DNS resolution and subsequent HTTP request?

* A. It returns `127.0.0.1` to drop the packet locally.
* B. It resolves the query to the Cisco Umbrella Intelligent Proxy IP address, redirecting the client's subsequent HTTP/HTTPS traffic to Umbrella for deep URL and file inspection (including AV and Cisco Threat Grid sandbox scanning).
* C. It ignores the request and allows direct connection without logging.
* D. It resets the client's network adapter.

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* Cisco Umbrella DNS-layer security handles traffic based on domain classification:
  * **Known Good:** Resolves to the legitimate external destination IP directly.
  * **Known Bad:** Resolves to a block page IP address (`hit-block.opendns.com`).
  * **Gray / Suspicious:** Resolves to the **Cisco Umbrella Intelligent Proxy**. The client browser connects to the Intelligent Proxy, which inspects the specific URL path, performs SSL decryption, and scans file downloads using multi-engine antivirus and Cisco Threat Grid sandboxing before permitting delivery.
* Distractor analysis: Option A drops loopback traffic. Option C bypasses inspection. Option D is an invalid client action.

---

### Scenario 4: Content Security - Email Authentication Mechanisms (SPF, DKIM, DMARC)
**Topology Background:**  
An enterprise detects that external adversaries are spoofing corporate email addresses (`ceo@corp.com`) to conduct Business Email Compromise (BEC) wire transfer scams against customers. The organization configures SPF, but attackers bypass it by spoofing the visible `From:` header. Which email security standard must be implemented to cryptographically sign outgoing messages and enforce domain alignment between the visible `From:` header and the cryptographic signature?

* A. Transport Layer Security (STARTTLS)
* B. DomainKeys Identified Mail (DKIM) combined with Domain-based Message Authentication, Reporting, and Conformance (DMARC)
* C. Simple Mail Transfer Protocol over SSL (SMTPS)
* D. DNSSEC record pinning

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* Email spoofing defense relies on a three-tiered framework:
  1. **SPF (Sender Policy Framework):** Validates the sender's mail server IP against published DNS records, but only checks the envelope `Return-Path` (RFC 5321), not the visible `From:` header (RFC 5322).
  2. **DKIM (DomainKeys Identified Mail):** Uses public-key cryptography to append a digital signature (`DKIM-Signature`) to the email header, guaranteeing payload integrity.
  3. **DMARC:** Enforces **Identifier Alignment** between the visible `From:` header and the SPF/DKIM domains. A DMARC policy (`p=reject`) instructs recipient mail servers to reject messages that fail alignment and sends diagnostic reporting back to the enterprise.
* Distractor analysis: Options A and C provide transport encryption in transit, but do not authenticate sender identity or prevent header spoofing. Option D authenticates DNS zone data.

---

### Scenario 5: Web Security - Cisco Secure Web Appliance WCCP Redirection
**Topology Background:**  
A network engineer deploys a Cisco Secure Web Appliance (WSA) in transparent mode alongside a Cisco Catalyst 9500 core switch. The switch must intercept outgoing HTTP (port 80) and HTTPS (port 443) traffic and redirect it to the WSA without configuring proxy settings on client web browsers. Which Cisco protocol dynamically redirects web traffic from the switch to the proxy?

* A. Web Cache Communication Protocol (WCCP v2)
* B. Virtual Router Redundancy Protocol (VRRP)
* C. Network Address Translation (NAT)
* D. Border Gateway Protocol (BGP)

**Correct Answer:** **A**

**Detailed Technical Explanation:**  
* **WCCP (Web Cache Communication Protocol) v2:** A Cisco-developed protocol that allows switches and routers to transparently intercept web traffic and redirect it to one or more content caching engines or web proxies (like Cisco WSA).
* The switch intercepts TCP ports 80 and 443 on specified ingress interfaces and encapsulates the packets (using GRE or Layer 2 rewrite) to the WSA. If the WSA fails, WCCP automatically stops redirection, ensuring high-availability network bypass.
* Distractor analysis: Option B (VRRP) provides default gateway redundancy. Option C modifies IP headers without proxy cache coordination. Option D is a WAN routing protocol.

---

### Scenario 6: Endpoint Security - Cisco Secure Endpoint (AMP) Behavioral Engines
**Topology Background:**  
A targeted malware attack executes a zero-day payload on an executive workstation. The file has never been seen globally and has an "Unknown" SHA-256 disposition in the Cisco AMP cloud. Which on-box detection engine in Cisco Secure Endpoint analyzes runtime process behaviors (e.g., process injection, credential dumping, API hooking) in memory to terminate the attack before encryption occurs?

* A. Spero Machine Learning Engine
* B. Malicious Activity Protection (MAP) engine
* C. ClamAV static signature engine
* D. Simple File Fetcher

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* Cisco Secure Endpoint (formerly AMP for Endpoints) employs multiple specialized detection engines:
  * **Tetra:** Traditional signature-based on-disk antivirus.
  * **Spero:** Machine learning engine that inspects static structural properties of PE files.
  * **Ethos:** File grouping and fuzzy hash heuristics.
  * **Malicious Activity Protection (MAP):** A behavioral analysis engine that continuously monitors runtime process activities on the endpoint in real time. When it detects suspicious behaviors (such as ransomware attempting rapid file encryption or Mimikatz dumping LSASS memory), MAP terminates the offending process tree immediately, even if the file hash is completely unknown.
* Distractor analysis: Option A (Spero) is a static pre-execution analyzer. Option C uses static definitions. Option D is fictional.

---

### Scenario 7: Network Access Control - MAB vs. 802.1X Fallback
**Topology Background:**  
An engineer configures an enterprise access switch for IEEE 802.1X port security. Legacy environmental temperature sensors and IP cameras lacking 802.1X supplicants cannot authenticate, resulting in closed switchports. How should the switchport be configured to allow non-802.1X endpoints to access the network while enforcing 802.1X for corporate laptops?

* A. Set the port to unmanaged hub mode.
* B. Configure 802.1X with MAC Authentication Bypass (MAB) fallback, where the switch queries Cisco ISE using the device's MAC address after 802.1X timeouts expire.
* C. Hardcode all sensor MAC addresses into Spanning Tree BPDU Guard.
* D. Disable AAA globally on the switch.

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* **MAC Authentication Bypass (MAB):** Enables network access for devices (like printers, cameras, and IoT sensors) that lack an 802.1X software supplicant.
* By configuring authentication order and priority (`authentication order dot1x mab` and `authentication priority dot1x mab`), the switch first attempts 802.1X EAP authentication. If the endpoint does not respond to EAPoL identity requests within the configured timeout, the switch falls back to MAB, sending the device's MAC address as a RADIUS Access-Request to Cisco ISE for profiling and authorization.
* Distractor analysis: Option A creates bridging loops and destroys access control. Option C disables ports. Option D removes security entirely.

---

### Scenario 8: Network Visibility - Cisco Secure Network Analytics (Stealthwatch)
**Topology Background:**  
A SOC analyst detects that an adversary has established an encrypted TLS 1.3 Command and Control (C2) channel from an internal database server. Because the session is encrypted with forward-secret cipher suites, payload inspection cannot decrypt the traffic. How does **Cisco Secure Network Analytics (Stealthwatch)** identify that this encrypted session is malicious without decrypting the payload?

* A. By injecting synthetic plaintext bytes into the active session.
* B. Using Encrypted Traffic Analytics (ETA) to analyze Initial Data Packet (IDP) characteristics, sequence of packet lengths and times (SPLT), and TLS fingerprinting.
* C. By brute-forcing the server's private key in real time.
* D. By disabling TCP window scaling across all core switches.

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* **Encrypted Traffic Analytics (ETA):** A Cisco technological innovation that detects malware within encrypted traffic without breaking privacy or requiring decryption:
  1. **Initial Data Packet (IDP):** Extracts unencrypted metadata from the TLS Client Hello and Server Hello (supported cipher suites, TLS version, extensions).
  2. **Sequence of Packet Lengths and Times (SPLT):** Analyzes the rhythm, inter-arrival time, and packet sizes of the flow. Machine learning models distinguish legitimate browsing patterns from malicious botnet beaconing or data exfiltration.
  3. These metrics are exported via enhanced NetFlow/IPFIX to Cisco Secure Network Analytics for automated threat scoring.
* Distractor analysis: Option A corrupts sessions. Option C is cryptographically impossible with modern ciphers. Option D degrades network performance.

---

### Scenario 9: Infrastructure Hardening - Control Plane Policing (CoPP) Syntax
**Topology Background:**  
An engineer hardens a core enterprise router against Denial-of-Service attacks targeting the BGP routing protocol. What Modular QoS CLI (MQC) configuration model must be implemented to police control plane traffic destined for the router's local CPU?

* A. `access-list 100 deny tcp any any eq 179` applied outbound on physical interfaces
* B. A `class-map` matching routing protocols, bound to a `policy-map` enforcing rate limits, applied under `control-plane` via `service-policy input`
* C. `ip verify unicast source reachable-via rx` applied to all loopback interfaces
* D. `switchport port-security violation shutdown`

**Correct Answer:** **B**

**Detailed Technical Explanation:**  
* **Control Plane Policing (CoPP):** Implemented using Cisco Modular QoS CLI (MQC):
  1. Define traffic matching classes: `class-map match-all BGP_CLASS` matching ACLs for TCP port 179.
  2. Create policy actions: `policy-map COPP_POLICY` configuring police rate limits (e.g., `police 8000 conform-action transmit exceed-action drop`).
  3. Attach to the control plane:
     ```ios
     control-plane
      service-policy input COPP_POLICY
     ```
* This ensures that transit data plane packets forward at hardware line rate while the route processor is shielded from packet floods.
* Distractor analysis: Option A blocks all BGP sessions globally. Option C is uRPF for spoofing. Option D is Layer 2 switchport security.

---

### Scenario 10: Endpoint Compliance - Cisco ISE Adaptive Network Control (ANC)
**Topology Background:**  
A security analyst reviewing SIEM alerts confirms that an employee workstation (`192.168.10.75`) has been compromised by a trojan actively scanning internal subnets. The analyst uses Cisco ISE Adaptive Network Control (ANC) to immediately isolate the workstation. What action does ISE perform against the access switch to enforce this quarantine?

* A. ISE issues a RADIUS Change of Authorization (CoA) RFC 5176 message instructing the switch to apply a restrictive Quarantine Authorization Profile (e.g., assigning a Quarantine DACL or VLAN).
* B. ISE shuts down the building's core fiber uplinks.
* C. ISE wipes the local hard drive of the endpoint over SNMP.
* D. ISE revokes the Active Directory domain controller's Kerberos master key.

**Correct Answer:** **A**

**Detailed Technical Explanation:**  
* **Cisco ISE Adaptive Network Control (ANC):** Provides automated and manual incident mitigation:
  * When the analyst (or an integrated platform like Cisco Secure Network Analytics or FMC) triggers an **ANC Quarantine**, ISE looks up the active session for the target IP/MAC.
  * ISE immediately issues a **RADIUS CoA (RFC 5176)** to the access switchport.
  * The switch re-evaluates the session and applies the Quarantine Authorization Profile (enforcing a restrictive Quarantine DACL that blocks all traffic except DNS/remediation or shifting the port to an isolated remediation VLAN).
* Distractor analysis: Options B, C, and D are destructive, non-existent, or unrelated administrative actions.

---

## 5. Recommended Study Resources & Official Documentation

* [Cisco 350-701 SCOR Official Exam Blueprint](https://learningnetwork.cisco.com/s/scor-exam-topics)
* [Cisco Press: CCNP and CCIE Security Core SCOR 350-701 Official Cert Guide](https://www.ciscopress.com/)
* [350-701 Practice Test - CertsClub](https://www.certsclub.com/cisco/) (Use coupon `club20` for 20% off)
* [NIST SP 800-207: Zero Trust Architecture](https://csrc.nist.gov/publications/detail/sp/800-207/final)
* [Cisco Umbrella Technical Documentation & Configuration Guides](https://docs.umbrella.com/)
* [Cisco Secure Endpoint (AMP) User Guide](https://www.cisco.com/c/en/us/support/security/fireamp-endpoints/series.html)

---

## 6. SEO Keywords & Search Index Topics

```
350-701, 350-701 exam, 350-701 practice test, 350-701 study guide, cisco 350-701,
scor, cisco scor, ccnp security core, ccie security qualifier,
certsclub 350-701, zero trust nist sp 800-207 policy engine, ocsp vs crl revocation,
umbrella intelligent proxy gray domains, spf dkim dmarc email alignment,
cisco wsa wccp transparent redirection, amp for endpoints malicious activity protection,
802.1x mab fallback authentication order, encrypted traffic analytics eta stealthwatch,
control plane policing copp mqc, ise adaptive network control anc quarantine coa
```

---

## 7. Community Discussions & Contributions

* **Architecture Discussions & Policy Reviews:** Share Zero Trust designs, Cisco Umbrella configurations, and FTD/ISE policy templates in [GitHub Discussions](../../discussions).
* **Issue Submissions:** To report an errata or suggest new technical questions, open a ticket in [GitHub Issues](../../issues).
* **Security Contributions:** Community security playbooks and CML lab topologies are welcomed via Pull Requests.

---
*Maintained by the Cisco Certified Curriculum Community. Contributions and pull requests are welcomed.*
