# Finding Report Template

| Field | Value |
|-------|-------|
| Finding ID |  |
| Title |  |
| Category |  |
| Component |  |
| Severity |  |
| CVSS Base Score |  |
| CVSS Vector |  |
| Status | Open |
| Date Identified |  |
| Date Remediated |  |
| Remediating Team |  |
| Description |  |
| Technical Details |  |
| Evidence / Proof of Concept |  |
| Impact |  |
| Risk Rating |  |
| Recommended Remediation |  |
| Remediation Steps |  |
| Verification Steps |  |
| References |  |
| Framework Mappings |  OWASP ASVS: <br> OWASP Top 10: <br> CWE: <br> Essential Eight: <br> ISO 27001:  |
| Notes |  |
| Assessor |  |

---

## Fields Explanation

### Identification

- **Finding ID**: Use convention `CATEGORY-COMPONENT-NN` (e.g., `AUTH-EF-01`)
- **Title**: A short descriptive title for the finding
- **Category**: The security category (e.g., Authentication, Authorisation, Injection)
- **Component**: Where the issue was found (e.g., API, Web, Database)
- **Severity**: Low / Medium / High / Critical
- **CVSS Base Score**: Score from 0.0–10.0 using CVSS v3.1
- **CVSS Vector**: Full vector string for reproducibility
- **Status**: Open / In Progress / Resolved / Reduced / Out of Scope

### Context

- **Date Identified**: The date the finding was discovered
- **Date Remediated**: The date remediation was confirmed (leave blank if open)
- **Remediating Team**: The team or individual responsible for the fix

### Technical Content

- **Description**: A clear one-paragraph summary of the issue
- **Technical Details**:Detailed technical explanation including affected code or configuration
- **Evidence / Proof of Concept**: Supporting evidence such as code snippets, API calls, or request/response examples

### Risk

- **Impact**: What could happen if this issue is exploited
- **Risk Rating**: Your internal risk classification

### Remediation

- **Recommended Remediation**: The high-level fix to resolve the issue
- **Remediation Steps**: Step-by-step instructions for the development or security team
- **Verification Steps**: How to confirm the fix is effective after remediation

### Reference

- **References**: Relevant external links to vendor guidance, standards, or advisories
- **Framework Mappings**: How the finding maps to OWASP ASVS, OWASP Top 10, CWE, ND Essential Eight, and ISO 27001

### Record

- **Notes**: Any additional notes or contextual information
- **Assessor Name of the person who identified and documented the finding
