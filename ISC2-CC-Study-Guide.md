# ISC2 CC Last-Minute Study Guide

## Domain 1: Security Principles

### CIA Triad
- **Confidentiality**: Preventing unauthorized disclosure of information. Associated with PII, PHI.
- **Integrity**: Data remains accurate, complete, and unaltered. Baselines verify integrity.
- **Availability**: Authorized users can access systems/data when needed.

### AAA + Non-Repudiation
- **Identification**: Claiming an identity (username).
- **Authentication**: Proving identity with factors (something you know, have, or are).
- **Authorization**: What the authenticated user is allowed to do.
- **Accounting**: Logging and tracking actions.
- **Non-repudiation**: User cannot deny performing an action.
- **MFA** requires at least two *different* factor types. Username + password = SFA (both knowledge).

### Risk Management
- **Asset**: Anything of value requiring protection.
- **Vulnerability**: Weakness that can be exploited.
- **Threat**: Person/event trying to exploit a vulnerability.
- **Likelihood**: Probability of exploitation.
- **Impact**: Magnitude of harm if realized.
- **Risk**: Function of likelihood and impact.

### Risk Treatment Options
| Option | Meaning |
|---|---|
| Avoid | Stop the risky activity entirely |
| Accept | Do nothing; live with the risk |
| Mitigate | Add controls to reduce likelihood/impact (most common) |
| Transfer | Shift financial impact to third party (insurance) |

### Security Control Types
- **Physical**: Locks, guards, fences, CCTV, mantraps, turnstiles, badge readers.
- **Technical/Logical**: Firewalls, ACLs, IDS/IPS, encryption, authentication.
- **Administrative**: Policies, procedures, standards, training.

### Governance Hierarchy
Regulations/Laws > Standards > Policies > Procedures
- **GDPR**: EU privacy law, applies to anyone handling EU persons data.
- **HIPAA**: US health information protection.

### Access Control Models
| Model | Description |
|---|---|
| DAC | Discretionary - owner decides permissions |
| MAC | Mandatory - system enforces centrally |
| RBAC | Role-based - permissions tied to roles |

### Key Principles
- **Least Privilege**: Give minimum access needed to do the job.
- **Defense in Depth**: Multiple layered controls (people, process, technology).
- **Segregation of Duties**: Split critical tasks among multiple people.
- **Two-Person Integrity**: Two authorized people required for sensitive activity.

### ISC2 Code of Ethics
- Protect society, the common good, public trust, and infrastructure.
- Act honorably, honestly, justly, responsibly, and legally.
- Provide diligent and competent service.

## Domain 2: Incident Response, Business Continuity, Disaster Recovery

### Key Terms
- **Event**: Any observable occurrence in a system/network.
- **Incident**: Event that actually or potentially jeopardizes CIA.
- **Breach**: Loss of control/unauthorized disclosure of sensitive information.
- **Exploit**: Specific attack using a vulnerability.
- **Intrusion**: Deliberate unauthorized access attempt or success.
- **Zero-day**: Previously unknown vulnerability with no existing signature/detection.

### Incident Response (IR) - 4 Phases (MEMORIZE ORDER)
1. **Preparation** - Policies, tools, IR plan, training.
2. **Detection and Analysis** - Identify/confirm incidents.
3. **Containment, Eradication, Recovery** - Stop spread, remove cause, restore systems.
4. **Post-Incident Activity** - Lessons learned and improvements.

### Business Continuity (BC)
- **Purpose**: Keep critical business functions running *during* disruption.
- Contains: BC team contacts, immediate response procedures, call trees, authority lines, vendor/emergency contacts.

### Disaster Recovery (DR)
- **Purpose**: Restore IT and operations *after* major outage.
- Contains: Executive summary, department plans, technical guides, team copies, checklists.

### BC vs DR Quick Compare
| | Business Continuity | Disaster Recovery |
|---|---|---|
| Focus | Keep running *during* disruption | Restore *after* outage |
| Scope | Business operations | IT systems |

## Domain 3: Access Control Concepts

### Access Control Basics
- **Subject**: Who is requesting access.
- **Object**: What is being accessed.
- **Rule**: How/when access is granted.

### Physical Access Controls (prevent tailgating/piggybacking)
- Mantraps, turnstiles, guards, fences, lights, CCTV, alarms.
- Locked doors, gates, sealed windows, cable protection, laptop locks, badges/swipe cards.

### Logical Access Controls
- Passwords, biometrics, token readers, permissions, ACLs.

### Provisioning Lifecycle
1. New hire - Create/onboard account.
2. Role change - Modify permissions.
3. Leave - Temporary disable account.
4. Termination - Delete/offboard account.

## Domain 4: Network Security

### Network Basics
- Common types: LAN, WAN, WLAN, VPN.
- Devices: Hubs, switches, routers, firewalls, servers, access points, endpoints.

### OSI Model (7 Layers)
Physical > Data Link > Network > Transport > Session > Presentation > Application

### TCP/IP Model (4 Layers)
Network Interface > Internet > Transport > Application

### IP Addressing
- **IPv4**: 32-bit addresses. Private ranges: 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16. Loopback: 127.0.0.1.
- **IPv6**: 128-bit hex addresses. Supports far more addresses. Improved security.

### Secure Ports Table (MEMORIZE)
| Function | Insecure | Secure |
|---|---|---|
| File Transfer | 21 FTP | 22 SFTP |
| Remote Terminal | 23 Telnet | 22 SSH |
| Email Sending | 25 SMTP | 587 SMTP+TLS |
| Time Sync | 37 Time | 123 NTP |
| Web | 80 HTTP | 443 HTTPS |
| DNS | 53 DNS | 853 DNS-over-TLS |
| Email Retrieval | 143 IMAP | 993 IMAP+TLS |
| Directory | 389 LDAP | 636 LDAPS |
| Management | 161/162 SNMPv1/2 | 161/162 SNMPv3 |

### Network Threats
- **DoS/DDoS**: Overwhelm resources to block legitimate use.
- **Spoofing**: Faking identity (IP, MAC, email, SSID, username).
- **On-Path/MITM**: Attacker intercepts/modifies traffic between parties.
- **Side-Channel**: Observing power, timing, emissions to infer secrets.
- **Phishing/Whaling**: Social engineering via email (whaling targets high-value individuals).

### Malware Types
- **Virus**: Attaches to legitimate files.
- **Worm**: Self-replicating, spreads across networks.
- **Trojan**: Hides inside legitimate software.
- **Ransomware**: Encrypts data demanding payment.
- **Spyware**: Secretly monitors activity.
- **Rootkit**: Grants privileged hidden access.
- **Adware**: Displays unwanted advertisements.

### Detection vs Prevention Tools
| Tool | Detects | Prevents |
|---|---|---|
| IDS | Yes | No |
| IPS | Yes | Yes (inline blocking) |
| SIEM | Yes (log correlation) | No |
| Firewall | Partially | Yes |
| Anti-Malware | Yes | Yes |

- **HIDS**: Monitors a single host.
- **NIDS**: Monitors network traffic patterns.
- **SIEM**: Aggregates and correlates logs from many sources.

### Network Infrastructure
- **Data Center Security**: Power (UPS, generators), HVAC, fire suppression (gas/water), physical access control, redundancy.
- **Defense in Depth**: Segmentation, DMZs, VLANs, NAC, zero trust, microsegmentation.

### Cloud Models
| Model | What Provider Manages | What You Manage |
|---|---|---|
| SaaS | Everything | Configuration/data |
| PaaS | Platform + runtime | Applications + data |
| IaaS | Compute/storage/network | OS + apps + data |

### Deployment Models
- **Public**: Shared infrastructure.
- **Private**: Dedicated to one org.
- **Community**: Shared among similar orgs.
- **Hybrid**: Mix of public and private.

- **SLA**: Contract specifying availability, performance, security, DR, data ownership.
- **MOU/MOA**: Memorandum of understanding/agreement for site sharing.

## Domain 5: Security Operations

### Data Security Lifecycle (MEMORIZE ORDER)
**Create > Store > Use > Share > Archive > Destroy**

### Data Handling
- **Classification**: Assign sensitivity levels (highly restricted, moderately restricted, internal-only, public).
- **Labeling**: Apply handling markings based on classification.
- **Retention**: Keep data only as long as needed or legally required.
- **Destruction**: Methods depend on sensitivity:
  - Clearing: Overwriting data.
  - Purging/Sanitization: Removing data more thoroughly.
  - Degaussing: Magnetic erasure.
  - Physical destruction: Shredding/crushing media.

### Encryption
- **Symmetric**: Same key for encrypt/decrypt. Fast, used for bulk data.
- **Asymmetric**: Public/private key pair. Used for key exchange and digital signatures.

### Hashing
- **One-way function** producing a fixed-length digest.
- Properties: Easy to compute, hard to reverse, deterministic, collision-resistant, hard to modify unnoticed.
- Used for integrity verification, not confidentiality.

### Logging and Monitoring
- **Ingress monitoring**: Firewalls, gateways, IDS/IPS, auth systems, SIEM, anti-malware.
- **Egress monitoring / DLP**: Email, file transfers, portable media, web/API posts.
- Best practices: Centralize logs, protect integrity, set retention, review with SIEM.

### System Hardening
- Remove unnecessary apps/services (least functionality).
- Apply secure baselines and trusted OS configurations.
- Patch management: Plan > Test > Implement > Audit.

### Configuration Management
1. **Identification**: Document system, components, interfaces.
2. **Baseline**: Minimum acceptable secure configuration.
3. **Change Control**: RFC process with approval, testing, rollout, and **rollback** plan.
4. **Verification/Audit**: Confirm changes are correct and secure.

### Key Policies
| Policy | What It Covers |
|---|---|
| Data Handling | Classification, storage, encryption, backup, destruction |
| Password | Length, complexity, history, no sharing, compromise response |
| Acceptable Use (AUP) | Proper use of systems, networks, internet, devices |
| BYOD | Personal device rules, MDM, allowed apps, storage segmentation |
| Privacy | Handling of PII/PHI and compliance with privacy laws |
| Change Management | Documentation, approval, testing, rollback |

### Security Awareness Training
- **Education**: Broad security knowledge.
- **Training**: Role-specific skills and procedures.
- **Awareness**: Frequent reminders and campaigns.
- Focus areas: Social engineering, password hygiene, clean desk, data handling.

## ISC2 AI Exam Guidance

The ISC2 CC exam treats AI as a technology that can function as both a threat tool and a defensive tool. Questions mentioning AI should be answered using core security fundamentals.

### Key AI Points for CC Exam
- **AI as threat actor tool**: Can be used for automated reconnaissance, password spraying, malware propagation - similar to bots and automation.
- **AI in defensive products**: Anti-malware, IDS/IPS, SIEM, and anomaly detection may use ML/AI for threat identification.
- **Same core principles apply**: CIA triad, risk management, least privilege, segmentation, monitoring, logging, and ISC2 Code of Ethics all still govern AI systems.
- **Privacy and accountability**: Training data is an asset that needs protection; access to models must be controlled; logging provides non-repudiation for AI operations.

### Exam Strategy for AI Questions
1. Fall back to standard security fundamentals (CIA, AAA, risk management).
2. Apply least privilege and defense in depth to AI systems.
3. Remember AI raises the same ethical obligations under ISC2 Code of Ethics.
4. Treat AI-powered attacks with standard mitigations (strong auth, segmentation, monitoring, encryption).

## Rapid-Fire Self-Test (Answer out loud)

1. What are the three parts of the CIA triad?
2. Which risk treatment is most commonly used?
3. What is the difference between authentication and authorization?
4. What are the four Incident Response phases in order?
5. What is the difference between Business Continuity and Disaster Recovery?
6. Which access control model lets the owner decide permissions: DAC, MAC, or RBAC?
7. What secure protocol replaces Telnet?
8. What secure protocol replaces HTTP?
9. Which tool blocks attacks inline: IDS or IPS?
10. What is the difference between symmetric and asymmetric encryption?
11. What are the phases of the data lifecycle?
12. What is the difference between a hash and encryption?
13. What are the three control categories?
14. What does the principle of least privilege mean?
15. What does a zero-day vulnerability mean?
