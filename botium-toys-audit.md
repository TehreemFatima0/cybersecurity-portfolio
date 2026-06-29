# GRC Case Study: Botium Toys Security Risk & Compliance Audit

### Frameworks Evaluated
* NIST Cybersecurity Framework (CSF)
* PCI DSS
* GDPR
* SOC2

---

## Scope & Objectives
* **Goal:** Establish a secure baseline for a growing retail business by identifying vulnerable infrastructure touchpoints.
* **Current State:** The organization possesses basic technical perimeter defenses (firewall, antivirus) but completely lacks administrative policies, data encryption, and access controls.

---

## Controls Assessment Checklist

| Control Category | Control Name | In Place? | Operational Context |
| :--- | :--- | :---: | :--- |
| **Administrative** | Least Privilege | **No** | Excessive access privileges across vendors and internal users. |
| **Administrative** | Disaster Recovery Plans | **No** | No business continuity strategy exists for operational downtime. |
| **Administrative** | Password Policies | **No** | Lack of mandatory complexity rules or rotation cycles. |
| **Administrative** | Separation of Duties | **No** | Critical responsibilities overlap without peer validation. |
| **Technical** | Firewall | **Yes** | Basic packet filtering perimeter firewall is deployed. |
| **Technical** | Intrusion Detection System (IDS) | **No** | No active automated network traffic anomaly monitoring. |
| **Technical** | Backups | **Yes** | Routine database and configuration backups are maintained. |
| **Technical** | Antivirus Software | **Yes** | Standard endpoint protection active on workplace systems. |
| **Technical** | Encryption | **No** | Customer payment data and PII are transmitted in clear text. |
| **Technical** | Password Management System | **No** | No corporate tool used; passwords managed manually by staff. |
| **Physical** | Physical Security Locks | **Yes** | Access to offices and warehouse requires physical keys. |
| **Physical** | CCTV Surveillance | **Yes** | Cameras actively monitor building entry and exit points. |
| **Physical** | Fire Detection & Prevention | **Yes** | Functioning smoke detectors and sprinkler systems installed. |

---

## Regulatory Compliance Checklist

### Payment Card Industry Data Security Standard (PCI DSS)
* [ ] **No** - Only authorized users have access to customers’ credit card information.
* [ ] **No** - Credit card information is stored, accepted, processed, and transmitted securely.
* [ ] **No** - Data encryption procedures secure transaction touchpoints.
* [ ] **No** - Secure password management policies are adopted.

### General Data Protection Regulation (GDPR)
* [ ] **No** - E.U. customers’ data is actively kept private and classified.
* [ ] **No** - A 72-hour data breach notification protocol is established.
* [ ] **No** - Data is properly inventoried and monitored for privacy compliance.

### System and Organizations Controls (SOC Type 1 & 2)
* [ ] **No** - User access control policies are formally established.
* [ ] **No** - PII/SPII data maintains strict confidentiality baselines.
* [ ] **No** - Data integrity verification mechanisms are operational.

---

## Strategic Recommendations
1. **Access Governance:** Implement the Principle of Least Privilege and deploy a centralized Password Management tool.
2. **Data Protection:** Transition payment workflows to encrypted protocols (AES-256 for data-at-rest, TLS for data-in-transit) to satisfy basic PCI DSS and GDPR requirements.
3. **Monitoring & Response:** Deploy an open-source Intrusion Detection System (IDS) and draft a 72-hour incident notification playbook for compliance readiness.
