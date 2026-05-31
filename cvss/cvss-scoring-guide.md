# CVSS v3.1 Scoring Reference

**Reference:** NIST NVD CVSS v3.1 Calculator, FIRST CVSS v3.1 Specification

---

## Overview

CVSS (Common Vulnerability Scoring System) v3.1 is a standardized method for assessing the severity of security vulnerabilities. This guide provides a quick reference for scoring, metric definitions, and common vulnerability examples.

> **Always use the official calculator for final scores.**
> https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator

---

## Severity Ratings & Remediation Timeframes

| Score Range | Rating | Action |
|-------------|--------|--------|
| 9.0 - 10.0 | Critical | Immediate remediation required |
| 7.0 - 8.9 | High | Remediate within 2 weeks |
| 4.0 - 6.9 | Medium | Remediate within 30 days |
| 0.1 - 3.9 | Low | Remediate within 90 days |
| 0.0 | None | Informational only |

---

## Base Score Metrics

### Attack Vector (AV)

| Value | Description | Weight |
|-------|-------------|--------|
| N | Network - Exploitable remotely over the internet | Highest |
| A | Adjacent - Requires access to the local network | High |
| L | Local - Requires local system access | Medium |
| P | Physical - Requires physical device access | Lowest |

### Attack Complexity (AC)

| Value | Description |
|-------|-------------|
| L | Low - No special conditions, attack can be repeated reliably |
| H | High - Specific conditions must exist, not reliably repeatable |

### Privileges Required (PR)

| Value | Description |
|-------|-------------|
| N | None - No authentication required |
| L | Low - Basic authenticated user |
| H | High - Admin or privileged user |

### User Interaction (UI)

| Value | Description |
|-------|-------------|
| N | None - No user action required |
| R | Required - User must take an action (click link, open file) |

### Scope (S)

| Value | Description |
|-------|-------------|
| U | Unchanged - Impact limited to the vulnerable component |
| C | Changed - Impact extends to other components or systems |

### Confidentiality / Integrity / Availability Impact (CIA)

| Value | Description |
|-------|-------------|
| N | None - No impact |
| L | Low - Some impact, attacker has limited control |
| H | High - Total or significant impact |

---

## Common Vulnerability Vector Examples

| Scenario | Vector | Score |
|----------|--------|-------|
| Unauthenticated remote code execution | AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H | 10.0 |
| Auth bypass via network | AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H | 9.8 |
| SQL injection (no auth required) | AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:N | 9.1 |
| Stored XSS (user interaction) | AV:N/AC:L/PR:L/UI:R/S:C/C:L/I:L/A:N | 5.4 |
| IDOR (read other user data) | AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:N/A:N | 6.5 |
| Hardcoded API key in source | AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:L/A:N | 8.2 |
| Missing HTTPS on login page | AV:N/AC:H/PR:N/UI:R/S:U/C:H/I:N/A:N | 5.3 |
| Local privilege escalation | AV:L/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H | 7.8 |
| Reflected XSS | AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N | 6.1 |
| Directory traversal (read-only) | AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:N/A:N | 6.5 |

---

## Temporal & Environmental Modifiers

These are optional metrics that adjust the base score for context.

### Exploit Code Maturity (E)

| Value | Meaning |
|-------|---------|
| X | Not Defined (Default) |
| U | Unproven - Theoretical, no known exploit |
| P | Proof-of-Concept - PoC exists but not weaponised |
| F | Functional - Functional exploit available |
| H | High - Weaponised, widely deployed exploit |

### Remediation Level (RL)

| Value | Meaning |
|-------|---------|
| X | Not Defined (Default) |
| O | Official Fix - Vendor patch available |
| T | Temporary Fix - Workaround available |
| W | Workaround - Informal mitigation |
| U | Unavailable - No fix exists |

---

## Severity by CWE Type

| CWE | Vulnerability Type | Severity | Notes |
|-----|--------------------|-----------|-------|
| CWE-89 | SQL Injection | High / Critical | Depends on auth requirement |
| CWE-79 | XSS | Medium / High | Stored XSS is higher than reflected |
| CWE-287 | Improper Authentication | High / Critical | Context-dependent |
| CWE-306 | Missing Authentication | High / Critical | Usually NNN vector |
| CWE-200 | Information Exposure | Low / Medium | Depends on data sensitivity |
| CWE-798 | Hardcoded Credentials | High / Critical | Usually network-accessible |
| CWE-22 | Path Traversal | Medium / High | Depends on file sensitivity |
| CWE-352 | CSRF | Medium | Requires user interaction |
| CWE-611 | XXE | High | Can lead to SSRF/RCE |
| CWE-502 | Unsafe Deserialisation | High / Critical | Often leads to RCE |

---

## How to Use in Security Audits

1. **Identify the vulnerability** and map it to a CWE where applicable.
2. **Determine base metrics** (AV, AC, PR, UI, S, CIA) based on attack characteristics.
3. **Calculate base score** using the NIST calculator.
4. **Apply temporal modifiers** if exploit or remediation status is known.
5. **Apply environmental modifiers** to reflect the specific organisational context.
6. **Document the vector string** and score in findings.
7. **Prioritise remediation** based on the final score and severity rating.

---

## Quick Reference Card

**Network-accessible + Low complexity + No auth + No interaction + Changed scope + High CIA = 10.0 (Critical)**

**Key risk multipliers:**
- AV:N > AV:A > AV:L > AV:P
- PR:N > PR:L > PR:H
- S:C increases score significantly over S:U
- UI:N > UI:R

**Temporal priority boosters:**
- E:H (exploit in the wild) + RL:U (no fix) = escalate response urgency
- E:U (no exploit) + RL:O (patch available) = standard patch cycle

---

*Reference: FIRST CVSS v3.1 Specification | NIST NVD CVSS v3.1 Calculator*
