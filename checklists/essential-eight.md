# Essential Eight Maturity Assessment Checklist

**Framework:** ASD ACSC Essential Eight Mitigation Strategies
**Reference:** https://www.cyber.gov.au/business-government/asds-cyber-security-frameworks/essential-eight

---

## Maturity Levels

| Level | Description | Status |
|-------|-------------|--------|
| ML0 | Not implemented / Ad hoc | [ ] |
| ML1 | Partially aligned | [ ] |
| ML2 | Mostly aligned | [ ] |
| ML3 | Fully aligned | [ ] |

**Target Maturity Level:** ML2
**Assessor:** _________________
**Assessment Date:** _________________

---

## 1. Patch Applications

### ML1 - Partially Aligned
- [ ] 1.1 Internet-facing services patched within 2 weeks (or 48 hours if exploit exists)
- [ ] 1.2 Vulnerability scans of internet-facing services conducted daily
- [ ] 1.3 Commonly-targeted applications patched within 1 month
- [ ] 1.4 Fortnightly vulnerability scans of office productivity suites, web browsers, email clients, PDF software
- [ ] 1.5 Unsupported applications removed from internet-facing services and commonly-targeted software

### ML2 - Mostly Aligned
- [ ] 2.1 All application vulnerabilities patched within 1 month of release
- [ ] 2.2 Fortnightly vulnerability scans across ALL applications
- [ ] 2.3 Weekly vulnerability scans of office productivity suites, web browsers, email clients, PDF software
- [ ] 2.4 Unsupported applications removed across all assets

### ML3 - Fully Aligned
- [ ] 3.1 Vulnerabilities in office productivity suites, web browsers, email clients, PDF software mitigated within 2 weeks
- [ ] 3.2 Critical vulnerabilities with active exploits mitigated within 48 hours
- [ ] 3.3 Daily vulnerability scans of internet-facing services
- [ ] 3.4 Weekly vulnerability scans across all systems
- [ ] 3.5 Formal process for identifying and removing unsupported software
- [ ] 3.6 Automated patching mechanisms deployed where feasible

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 2. Patch Operating Systems

### ML1 - Partially Aligned
- [ ] 1.1 Internet-facing OS patched within 2 weeks (48 hours if exploit exists)
- [ ] 1.2 Daily vulnerability scans of internet-facing OS
- [ ] 1.3 Non-internet-facing OS patched within 1 month
- [ ] 1.4 Fortnightly vulnerability scans of non-internet-facing OS
- [ ] 1.5 Unsupported OS removed from internet-facing systems

### ML2 - Mostly Aligned
- [ ] 2.1 All OS vulnerabilities patched within 1 month
- [ ] 2.2 Fortnightly vulnerability scans of all operating systems
- [ ] 2.3 Unsupported OS removed from all devices

### ML3 - Fully Aligned
- [ ] 3.1 OS vulnerabilities mitigated within 2 weeks
- [ ] 3.2 Critical exploits addressed within 48 hours
- [ ] 3.3 Daily vulnerability scanning of all OS
- [ ] 3.4 Automated OS patch deployment in place
- [ ] 3.5 Formal process for OS lifecycle management

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 3. Multi-Factor Authentication (MFA)

### ML1 - Partially Aligned
- [ ] 1.1 MFA enabled for all remote access (VPN, RDP, webmail)
- [ ] 1.2 MFA enabled for all privileged accounts
- [ ] 1.3 MFA enforced for email access

### ML2 - Mostly Aligned
- [ ] 2.1 MFA enabled for all user accounts accessing important data repositories
- [ ] 2.2 MFA enforced for all cloud-based services (email, file storage, collaboration tools)
- [ ] 2.3 MFA required for administrative access to all systems
- [ ] 2.4 SMS-based MFA supplemented with app-based or hardware tokens for privileged users

### ML3 - Fully Aligned
- [ ] 3.1 Phishing-resistant MFA (FIDO2, hardware keys, certificate-based) for all privileged accounts
- [ ] 3.2 MFA enforced across all user accounts and all access types
- [ ] 3.3 MFA bypass/recovery procedures documented and secured
- [ ] 3.4 Regular review of MFA coverage and exceptions

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 4. Restrict Administrative Privileges

### ML1 - Partially Aligned
- [ ] 1.1 Administrative privileges assigned based on job requirements
- [ ] 1.2 Separate admin accounts used for privileged tasks (not daily use)
- [ ] 1.3 Admin privileges removed from standard users

### ML2 - Mostly Aligned
- [ ] 2.1 Privileged access managed via Just-In-Time (JIT) or similar approach
- [ ] 2.2 Admin accounts protected with MFA
- [ ] 2.3 Regular review of privileged account membership
- [ ] 2.4 Logging and monitoring of privileged account usage

### ML3 - Fully Aligned
- [ ] 3.1 Privileged Access Workstations (PAW) used for admin tasks
- [ ] 3.3 Automated provisioning/deprovisioning of admin rights
- [ ] 3.4 Detailed audit logs of all privileged actions
- [ ] 3.5 Regular attestation and recertification of admin access
- [ ] 3.6 No standing admin privileges on endpoints

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 5. Application Control

### ML1 - Partially Aligned
- [ ] 1.1 Approved application list defined
- [ ] 1.2 Unknown/malicious code prevented on internet-facing systems
- [ ] 1.3 Macro execution controlled on email clients

### ML2 - Mostly Aligned
- [ ] 2.1 Application control (whitelisting/deny-listing) on all workstations
- [ ] 2.2 Only approved applications can execute on endpoints
- [ ] 2.3 Process-level controls to prevent unauthorised execution

### ML3 - Fully Aligned
- [ ] 3.1 Application control enforced on all systems (servers, workstations, endpoints)
- [ ] 3.2 Real-time monitoring and alerting on application control violations
- [ ] 3.3 Cryptographic signing verification for approved applications
- [ ] 3.4 Automated alerting for unauthorised execution attempts
- [ ] 3.5 Regular review and update of approved application list

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 6. Restrict Microsoft Office Macros

### ML1 - Partially Aligned
- [ ] 1.1 Macros from internet blocked
- [ ] 1.2 Users notified when macros are blocked
- [ ] 1.3 Exceptions documented for business needs

### ML2 - Mostly Aligned
- [ ] 2.1 Macros from internet fully blocked by default
- [ ] 2.2 Only digitally signed macros from trusted sources allowed
- [ ] 2.3 Macro settings enforced via Group Policy/Intune
- [ ] 2.4 User awareness training on macro risks

### ML3 - Fully Aligned
- [ ] 3.1 All macros blocked organisation-wide
- [ ] 3.2 Digitally signed macros allowed only from verified publishers
- [ ] 3.3 Macro execution monitored and logged
- [ ] 3.4 Automated alerting for macro policy violations
- [ ] 3.5 Alternative solutions provided for legitimate macro-dependent workflows

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 7. User Application Hardening

### ML1 - Partially Aligned
- [ ] 1.1 Web browser extensions limited to essentials
- [ ] 1.2 Unnecessary web browser functionality disabled
- [ ] 1.3 Adobe Flash/Java removed or disabled

### ML2 - Mostly Aligned
- [ ] 2.1 Hardened configurations applied to all web browsers
- [ ] 2.2 Advertising blocked across all systems
- [ ] 2.3 Unnecessary file type associations disabled
- [ ] 2.4 Application hardening settings enforced via Group Policy/MDM

### ML3 - Fully Aligned
- [ ] 3.1 Hardening applied to ALL user applications (email, productivity, browsers)
- [ ] 3.2 Feature-level restrictions documented and maintained
- [ ] 3.3 Regular compliance scanning for hardening drift
- [ ] 3.4 Automated remediation of non-compliant configurations
- [ ] 3.5 Configuration baselines maintained and version-controlled

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## 8. Regular Backups

### ML1 - Partially Aligned
- [ ] 1.1 Backups of new/unmodified data performed regularly
- [ ] 1.2 Backups stored offline or on immutable media
- [ ] 1.3 At least annual backup restoration testing

### ML2 - Mostly Aligned
- [ ] 2.1 All critical data backed up at least daily
- [ ] 2.2 Backups retained for minimum 3 months
- [ ] 2.3 Backups encrypted in transit and at rest
- [ ] 2.4 Restoration testing performed at least every 3 months
- [ ] 2.5 Backup integrity verified regularly

### ML3 - Fully Aligned
- [ ] 3.1 Real-time or near-real-time backup of critical systems
- [ ] 3.2 Immutable/offline backup copies maintained (air-gapped where possible)
- [ ] 3.3 Full restoration testing performed monthly
- [ ] 3.4 Tested disaster recovery procedures documented
- [ ] 3.5 Backup coverage includes endpoints, servers, and cloud services
- [ ] 3.6 Recovery Time Objective (RTO) and Recovery Point Objective (RPO) defined and met

**Evidence:** _________________
**Assessed Level:** [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3

---

## Overall Assessment Summary

| Strategy | Current ML | Target ML | Gap | Priority |
|----------|------------|-----------|-----|----------|
| Patch Applications | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Patch Operating Systems | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Multi-Factor Auth | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Restrict Admin Privileges | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Application Control | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Restrict Office Macros | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| User App Hardening | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |
| Regular Backups | [ ] ML0 [ ] ML1 [ ] ML2 [ ] ML3 | ML2 | ___ | High/Med/Low |

### Findings

**Strengths:**


**Gaps Identified:**


**Recommendations:**


**Next Review Date:** _________________

---

## Notes

- Assessment based on ASD ACSC Essential Eight Framework
- Maturity levels: ML0 (Not Implemented), ML1 (Partially Aligned), ML2 (Mostly Aligned), ML3 (Fully Aligned)
- Organisations should aim for ML2 as minimum baseline; ML3 recommended for high-risk environments
- Reference: https://www.cyber.gov.au/resources-business-and-government/maintaining-devices-and-systems/cyber-security-guidelines-and-frameworks/essential-eight-controls
