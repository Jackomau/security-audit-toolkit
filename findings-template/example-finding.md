# Example Finding Report

> This is an anonymised example to demonstrate how to use the finding template.
> No real client data, code, or system names are included.

| Field | Value |
|-------|-------|
| Finding ID | AUTHZ-API-01 |
| Title | Missing Authorisation Check on User Profile API Endpoint |
| Category | Authorisation |
| Component | API |
| Severity | High |
| CVSS Base Score | 7.5 |
| CVSS Vector | AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N |
| Status | Open |
| Date Identified | 2026-05-31 |
| Date Remediated |  |
| Remediating Team |  |
| Description | The user profile API endpoint does not verify that the requesting user is authorised to access the requested profile. An authenticated attacker can enumerate and retrieve profile data for any user by manipulating the user ID parameter. |
| Technical Details | The API endpoint `GET /api/v1/users/{userId}` returns user profile information without validating whether the requesting user ID matches the `userId` path parameter. No role-based or ownership-based checks are performed. |
| Evidence / Proof of Concept | 1. Log in as User A.<br>2. Capture the request to `GET /api/v1/users/123`.<br>3. Change the userId to `124` (User B).<br>4. The response returns User B's profile data, including email and name, without any authorisation error. |
| Impact | Any authenticated user can access other users' profile information, violating data confidentiality and potentially violating privacy regulations. |
| Risk Rating | High |
| Recommended Remediation | Implement an authorisation check that verifies the requesting user is authorised to access the requested profile. |
| Remediation Steps | 1. Add an ownership or role-based check before returning profile data.<br>2. For standard users, verify that `requestingUserId == userId`.<br>3. For admin users, ensure a valid admin role is present and log the access.<br>4. Return `403 Forbidden` instead of user data when authorisation fails. |
| Verification Steps | 1. Log in as User A.<br>2. Attempt to retrieve User B's profile via the API.<br>3. Confirm that the response returns `403 Forbidden` instead of profile data. |
| References | - [OWASP - Broken Object Level Authorisation](https://owasp.org/www-project-api-security/latest/4-enforced-authorization/)<br> - [CWE-284 Improper Access Control](https://cwe.mitre.org/data/definitions/284.html) |
| Framework Mappings |  OWASP ASVS: 5.1, 5.2 <br> OWASP Top 10: A01:2021 Broken Object Level Authorisation <br> CWE: CWE-284 <br> Essential Eight: N/A <br> ISO 27001: A.9.4.2 Secure log-on, A.9.4.5 Use of privileged utility programmes |  |
| Notes | This finding was identified during automated API testing with manual verification. |
| Assessor |  |

---

## How to Use This Example

1. Copy this file as a starting point for a new finding.
2. Replace all placeholder values with real data from your assessment.
3. Remove this section before sharing or submitting the finding.
