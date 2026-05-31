# Security Audit Toolkit

A practical security audit toolkit for structured web application code reviews, finding documentation, and framework-aligned reporting. This repository is designed to demonstrate a repeatable assessment workflow using recognised security standards and documentation practices.

## Overview

This toolkit supports a consistent approach to source code security reviews for web applications. It focuses on documenting findings clearly, mapping issues to recognised frameworks, and applying severity scoring in a way that is useful for audit, consulting, and portfolio demonstration purposes.

## What\'s Included

```text
security-audit-toolkit/
├── findings-template/
│   ├── finding-template.md       ← Structured finding report template (23 fields)
│   └── example-finding.md        ← Anonymised example finding
├── checklists/
│   ├── owasp-asvs-checklist.md   ← OWASP ASVS v4.0 checklist
│   └── essential-eight.md        ← ASD Essential Eight maturity assessment
└── cvss/
    └── cvss-scoring-guide.md     ← CVSS v3.1 scoring reference
```

## Use Cases

This repository is suitable for:

- Structured web application code review exercises.
- Security consulting and internal audit documentation workflows.
- Cybersecurity portfolio projects that demonstrate secure review methodology.
- Student or junior analyst practice in writing professional findings and mapping controls.

## Assessment Workflow

1. Start with the checklist to review the application systematically.
2. Record each issue using the finding template so the write-up remains clear and consistent.
3. Score severity using the CVSS guide and verify the result with the official calculator where needed.
4. Map each finding to relevant frameworks such as OWASP ASVS, OWASP Top 10, Essential Eight, ISO 27001, and CWE.

## Quick Example

A simple review flow might look like this:

- Review authentication and session handling controls against the ASVS checklist.
- Identify a missing authorisation check in an API endpoint.
- Document the issue using the finding template with impact, evidence, and remediation notes.
- Assign a CVSS base score and map the issue to ASVS, OWASP Top 10, and a relevant CWE.

## Frameworks Referenced

| Framework | Purpose |
|-----------|--------|
| [OWASP ASVS v4.0](https://owasp.org/www-project-application-security-verification-standard/) | Application security verification requirements |
| [CVSS v3.1](https://www.first.org/cvss/v3.1/specification-document) | Vulnerability severity scoring |
| [ASD Essential Eight](https://www.cyber.gov.au/resources-business-and-government/essential-cyber-security/essential-eight) | Australian cyber security baseline |
| [ISO 27001:2022](https://www.iso.org/standard/27001) | Information security management reference |
| [OWASP Top 10](https://owasp.org/www-project-top-ten/) | Common web application risk categories |

## Finding ID Convention

```text
CATEGORY-COMPONENT-NN

Examples:
  AUTH-EF-01
  AUTHZ-API-02
  CRYPTO-DB-01
  SESS-WEB-03
  INJECT-API-01
```

This naming format helps keep findings organised and easier to track across review notes and final reporting.

## Scope and Ethics

- This toolkit is intended for authorised security assessments only.
- All included examples should remain anonymised and non-client specific.
- No client data, proprietary code, or sensitive system details should be stored in this repository.
- All testing and review activities should be performed within a defined and approved engagement scope.

## Why This Repo Matters

Security reviews often fail because findings are inconsistent, weakly documented, or disconnected from recognised frameworks. This repository aims to solve that by providing a simple structure for repeatable review work that is easier to communicate to technical and non-technical stakeholders.

For portfolio purposes, it also shows practical capability in secure code review, framework mapping, reporting discipline, and security assessment methodology.
