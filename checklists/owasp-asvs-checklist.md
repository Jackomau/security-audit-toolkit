# OWASP ASVS v4.0 Checklist

> A condensed, practical checklist based on OWASP ASVS v4.0 for web application security reviews.
> This is a working reference, not a replacement for the full ASVS standard.
> Full standard: https://owasp.org/www-project-application-security-verification-standard/

## How to Use This Checklist

- Go through each item and mark **P** (Pass), **F** (Fail), or **N/A** (Not Applicable).
- Record findings using the `findings-template/finding-template.md` when an item fails.
- Document evidence and screenshots to support each pass/fail decision.

---

## V1 - Architecture, Design and Threat Modelling

- [ ] **V1.1** A threat model or similar exercise is defined and maintained.
- [ ] **V1.2** Compliance with applicable privacy and security regulations is ensured.
- [ ] **V1.3** All security controls are documented and justified.
- [ ] **V1.4** The application architecture clearly separates trusted and untrusted components.

## V2 - Authentication

- [ ] **V2.1** All user accounts are protected by strong authentication.
- [ ] **V2.2** Passwords are stored using secure, salted, and adaptive hashing.
- [ ] **V2.3** Default credentials are changed or removed before deployment.
- [ ] **V2.4** Multi-factor authentication is available for sensitive operations.
- [ ] **V2.5** Authentication requests are rate-limited to prevent brute force attacks.
- [ ] **V2.6** Session tokens are regenerated on authentication state changes.

## V3 - Session Management

- [ ] **V3.1** Session tokens are unique, random, and of sufficient length.
- [ ] **V3.2** Session tokens are invalidated on logout and after a timeout.
- [ ] **V3.3** Session tokens are protected from interception and cross-site exposure.
- [ ] **V3.4** Session tokens are not exposed in URLs or error messages.
- [ ] **V3.5** Cookies use `Secure`, `HttpOnly`, and `SameSite` flags where appropriate.

## V4 - Input Validation and Output Encoding

- [ ] **V4.1** All input is validated, sanitised, and normalised before processing.
- [ ] **V4.2** Output is encoded appropriately for the target context (HTML, JS, URL, SQL).
- [ ] **V4.3** Parameterised queries or prepared statements are used for all database access.
- [ ] **V4.4** Server-side validation is always used; client-side validation is supplementary.

## V5 - Access Control

- [ ] **V5.1** Access control is enforced server-side for all requests.
- [ ] **V5.2** Vertical and horizontal access control is tested for all resources.
- [ ] **V5.3** Default deny is enforced; access is granted only explicitly.
- [ ] **V5.4** Privilege separation is enforced; users cannot escalate their own privileges.
- [ ] **V5.5** All paths to protected resources enforce access control checks.

## V6 - Cryptography

- [ ] **V6.1** Strong cryptographic algorithms and key lengths are used.
- [ ] **V6.2** Random number generation is secure and non-predictable.
- [ ] **V6.3** TLS 1.2 or higher is enforced for all communication.
- [ ] **V6.4** Cryptographic keys are stored securely and not hard-coded.

## V7 - Error Handling and Logging

- [ ] **V7.1** Error messages do not leak sensitive information.
- [ ] **V7.2** Security-relevant events are logged with sufficient context.
- [ ] **V7.3** Logs are protected from unauthorised access and tampering.
- [ ] **V7.4** Log entries include timestamps, source, and event context.

## V8 - Data Protection

- [ ] **V8.1** Sensitive data is classified and handled according to its sensitivity.
- [ ] **V8.2** Sensitive data is encrypted at rest and in transit.
- [ ] **V8.3** Data retention and deletion policies are defined and enforced.
- [ ] **V8.4** Personal data handling complies with applicable regulations.

## V9 - Communications

- [ ] **V9.1** All communication channels use secure protocols.
- [ ] **V9.2** Certificate validation is enforced on all outbound connections.
- [ ] **V9.3** Web application headers are set correctly (e.g., CSP, X-Frame-Options).
- [ ] **V9.4** Cross-origin resource sharing (CORS) is properly configured.

## V10 - Malicious Code

- [ ] **V10.1** Dependencies are scanned for known vulnerabilities.
- [ ] **V10.2** Unused or unnecessary components are removed.
- [ ] **V10.3** Software and libraries are updated on a defined schedule.
- [ ] **V10.4** Source code is reviewed for backdoors and malicious logic.

## V11 - Business Logic

- [ ] **V11.1** Business logic flows are mapped and documented.
- [ ] **V11.2** Time-based and state-based controls are validated.
- [ ] **V11.3** Automated anti-automation controls are in place for sensitive actions.
- [ ] **V11.4** Financial, data, or action integrity checks are validated.

## V12 - Files and Resources

- [ ] **V12.1** File uploads are validated for type, size, and content.
- [ ] **V12.2** Uploaded files are stored outside the web root with safe access.
- [ ] **V12.3** File paths and names are not user-controllable without sanitisation.
- [ ] **V12.4** Dangerous functions are restricted or removed.

## V13 - API Security

- [ ] **V13.1** All API endpoints enforce authentication and authorisation.
- [ ] **V13.2** API requests are rate-limited and throttled appropriately.
- [ ] **V13.3** API schemas are validated and documented.
- [ ] **V13.4** API responses do not expose internal structure or excessive data.

## Notes

Record any skipped or N/A items with justification.
Report all failed items as structured findings using the finding template.
