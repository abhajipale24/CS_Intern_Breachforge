# Day 11 — DVWA Security Observations

## Lab Information

Lab: Damn Vulnerable Web Application (DVWA)

Target: Local DVWA installation

Authorized Scope: Only my locally installed DVWA application.

## Observation 01 — Login

I observed the DVWA login functionality.

The login page contains fields for user credentials and is responsible
for authenticating users.

OWASP Category:
A07 — Identification and Authentication Failures

Note:
The presence of a login page alone is not considered a vulnerability.
It is a security-sensitive feature that should be assessed carefully.

## Observation 02 — User Input

I observed user-controlled input fields in the DVWA modules.

User input should be validated and handled safely before being processed
by the application.

OWASP Category:
A03 — Injection

Note:
This is an observation of an input area and does not by itself prove
that the application contains an injection vulnerability.

## Observation 03 — Access-Controlled Functionality

I observed that the application contains different security-related
modules and settings that are available through the authenticated
application.

OWASP Category:
A01 — Broken Access Control

Security Purpose:
Authorization controls should ensure that users can only access
functionality they are permitted to use.

Note:
This observation alone does not prove an authorization vulnerability.

## Browser Network Observation

I used browser Developer Tools and the Network tab to observe normal
requests made by the DVWA application.

I recorded the request method, URL/resource, status code and resource
type without modifying or replaying the request.

## Evidence

Screenshot 01:
DVWA application/module showing a security-related feature.

Screenshot 02:
Browser Developer Tools Network tab showing a normal DVWA request.

## Safety

All observations were performed against my locally installed DVWA
training environment. No random or unauthorized websites were tested.
No passwords, tokens, cookies, or private information are included.
