# BreachForge Labs — Day 11

# OWASP Top 10 Practical Task

## Lab / Target

**Lab:** Damn Vulnerable Web Application (DVWA)

**Target:** Local DVWA installation

**Address:** http://localhost/DVWA/

## Authorized Scope

Testing was limited to my locally installed DVWA training environment.

No random websites, public systems, real users, or unauthorized
applications were tested.

## Testing Performed

The following activities were performed:

* Reviewed the OWASP Top 10 categories.
* Created security scenario mappings.
* Identified authentication and authorization concepts.
* Browsed DVWA normally to understand its attack surface.
* Identified forms, inputs, pages and security-related functionality.
* Observed normal HTTP requests using browser Developer Tools.
* Classified observations using the OWASP Top 10.
* Collected screenshots as permitted evidence.
* Documented security observations and remediation ideas.

## Observations

### 1. Authentication

DVWA provides a login mechanism that authenticates users.

OWASP Category:
A07 — Identification and Authentication Failures

### 2. User Input

DVWA contains multiple areas where users can provide input.

OWASP Category:
A03 — Injection

User input should be validated and safely processed.

### 3. Authorization

Security-sensitive functionality requires appropriate authorization
controls.

OWASP Category:
A01 — Broken Access Control

Authorization should be enforced by the server for protected actions
and resources.

## Evidence

Evidence is stored in the `screenshots` directory.

* `Day11_01.png`
* `Day11_02.png`

Sensitive information such as passwords, tokens, cookies and private
user information was excluded.

## Impact

Security weaknesses in authentication, authorization, and input
handling can potentially affect account security, data confidentiality,
or application integrity.

The observations in this report should not be considered confirmed
vulnerabilities unless they were safely verified through an authorized
DVWA exercise.

## Remediation

### Authentication

Use secure authentication and session-management practices, including
strong password protection and appropriate account security controls.

### Authorization

Enforce authorization checks on the server for every protected resource
and action.

### Input Handling

Validate user input according to expected formats and safely handle
untrusted input.

### HTTPS / Data Protection

Use HTTPS to protect sensitive information during transmission.

## Security Mindset

When assessing a new web application, I would first understand the
application's purpose, users, authentication flow, authorization model,
and attack surface. I would identify important pages, forms, parameters,
APIs, file features, and other user-controlled areas before performing
any security testing. This helps me understand how the application works
and allows security testing to be performed in a controlled and
authorized way.

## Conclusion

This exercise helped me understand how the OWASP Top 10 categories can
be connected to real web application features. I also practiced
identifying the attack surface, observing normal HTTP behavior,
documenting evidence, and thinking about appropriate remediation.
