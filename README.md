ZAP Security Scan Report

Overview

This repository contains the security scan results generated using OWASP ZAP (Zed Attack Proxy). The scan was performed on http://testphp.vulnweb.com to identify security vulnerabilities, categorize them based on risk levels, and suggest possible remediations.

Scan Details

Date: February 10, 2025

Tool: OWASP ZAP

Scope: Full site scan

Included Risk Levels: High, Medium, Low, Informational

Excluded Risk Levels: None

Confidence Levels: User Confirmed, High, Medium, Low

Summary of Findings

Alert Counts by Risk Level

Risk Level

Count

High

0

Medium

3

Low

3

Informational

5

Total

11

Key Vulnerabilities Identified

Absence of Anti-CSRF Tokens (Medium Risk)

Content Security Policy (CSP) Header Not Set (Medium Risk)

Missing Anti-clickjacking Header (Medium Risk)

Server Leaks Information via "X-Powered-By" Header (Low Risk)

Server Leaks Version Information via "Server" Header (Low Risk)

X-Content-Type-Options Header Missing (Low Risk)

Authentication Request Identified (Informational)

Charset Mismatch (Header vs Meta Content-Type Charset) (Informational)

Information Disclosure - Suspicious Comments (Informational)

Modern Web Application Indicators (Informational)

User Controllable HTML Element Attribute (Potential XSS) (Informational)

Recommendations

To improve security, consider implementing the following measures:

Implement CSRF protection mechanisms such as CSRF tokens.

Configure a Content Security Policy (CSP) header to prevent cross-site scripting (XSS) attacks.

Set X-Frame-Options to mitigate clickjacking risks.

Hide version information in HTTP response headers to reduce fingerprinting attacks.

Enforce X-Content-Type-Options: nosniff to prevent MIME-type sniffing.

Conduct regular security scans and penetration testing to detect new vulnerabilities.

References

OWASP CSRF Prevention Guide

Mozilla CSP Documentation

OWASP Security Headers Guide

License

This project is open-source and available under the MIT License.
