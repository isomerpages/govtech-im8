---
title: Application Security
permalink: /control-catalog/cybersecurity/as/
variant: markdown
description: ""
third_nav_title: Cybersecurity
---
Controls to prevent application vulnerabilities caused by insecure coding.

| Controls                                                                                     |
| -------------------------------------------------------------------------------------------- |
| [AS-1: Input Validation](#as-1-input-validation)                                             |
| [AS-2: Parameterised Interfaces](#as-2-parameterised-interfaces)                             |
| [AS-3: Output Sanitisation](#as-3-output-sanitisation)                                       |
| [AS-4: Authentication Mechanism Rate-Limiting](#as-4-authentication-mechanism-rate-limiting) |
| [AS-5: Password Requirements](#as-5-password-requirements)                                   |
| [AS-6: Password Salting and Hashing](#as-6-password-salting-and-hashing)                     |
| [AS-7: Access Control Check Enforcement](#as-7-access-control-check-enforcement)             |
| [AS-8: Secrets Management](#as-8-secrets-management)                                         |
| [AS-9: Content Security Policy (CSP)](#as-9-content-security-policy-csp)                     |
| [AS-10: HTTP Strict Transport Security (HSTS)](#as-10-http-strict-transport-security-hsts)   |
| [AS-11: Session Management](#as-11-session-management)                                       |
| [AS-12: Malware Scanning of Uploaded Files](#as-12-malware-scanning-of-uploaded-files)       |
| [AS-13: Exposure of Internal System Details](#as-13-exposure-of-internal-system-details)     |
| [AS-14: Secure Cryptographic Libraries](#as-14-secure-cryptographic-libraries)               |
| [AS-15: Password Change](#as-15-password-change)                                             |

## AS-1: Input Validation

**Group:** Application Security

### Control Statement

Validate all application inputs to ensure that they match the expected type, structure, or format.

### Control Recommendations

Strictly validating inputs against a comprehensive schema prevents injection attacks caused by inserting special characters or content that would cause the application to perform incorrect operations.

### Risk Statement

Without input validation, there&#39;s a heightened risk of injection attacks, data manipulation, or system crashes due to unexpected input, potentially leading to unauthorised access or disruption of services.

## AS-2: Parameterised Interfaces

**Group:** Application Security

### Control Statement

Use parameterised interfaces for database queries or system commands.

### Control Recommendations

Parameterised interfaces such Object-Relational Mapping (ORM) libraries ensure that parameters used in database queries or system commands are properly sanitised and prevent injection attacks.

### Risk Statement

Failure to use parameterised interfaces increases the vulnerability to SQL injection or command injection attacks, posing a significant risk of unauthorised access, data manipulation, or even potential system compromise.

## AS-3: Output Sanitisation

**Group:** Application Security

### Control Statement

Sanitise all application outputs that will be used to render a HTML document.

### Control Recommendations

Any application outputs that are returned to the requester and used to render a HTML document can lead to cross-site scripting (XSS) attacks if they contain special characters that change the rendering of the HTML document by the browser.

### Risk Statement

Lack of sanitisation for application outputs used in rendering HTML documents exposes the system to the risk of cross-site scripting (XSS) attacks, allowing malicious code execution in browsers.

## AS-4: Authentication Mechanism Rate-Limiting

**Group:** Application Security

### Control Statement

Apply rate-limiting on all authentication mechanisms to deter brute-force attacks.

### Control Recommendations

Consider rate-limiting to a maximum of 3 consecutive failed authentication attempts within 15 minutes or other reasonable rate limits. Time delays between log-on attempts reduce the risk of successful brute-forcing attacks. Bot mitigation tools such as CAPTCHA can further reduce this risk.

### Risk Statement

Without rate-limiting, there&#39;s an increased risk of unauthorised access as attackers may exploit weak credentials through repeated login attempts.

## AS-5: Password Requirements

**Group:** Application Security

### Control Statement

Where SSO or passwordless is not supported, verify that [ insert: param, as-5_prm_3 ] passwords are at least [ insert: param, as-5_prm_1 ] characters in length and [ insert: param, as-5_prm_2 ].

### Control Recommendations

Latest NIST [SP 800-63B](https://doi.org/10.6028/NIST.SP.800-63b) guidelines found that password length is a primary factor in determining the strength of a password while composition and complexity rules provide marginal security benefits.

### Risk Statement

Short or commonly used passwords increase the vulnerability to unauthorised access, potentially leading to compromised accounts and unauthorised activities on the system.

### Parameters

| ID         | Type                       | Description                       |
| ---------- | -------------------------- | --------------------------------- |
| as-5_prm_1 | number of characters (int) | The minimum length of a password. |
| as-5_prm_2 | policy (str)               | The password policy.              |
| as-5_prm_3 | type (str)                 | The type of password.             |

## AS-6: Password Salting and Hashing

**Group:** Application Security

### Control Statement

Store passwords as salted hashes using a password hashing scheme that is resistant to offline attacks such as those described in NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b). The salt should be:

- Generated using a cryptographically secure pseudo-random number generator in accordance with industry standards;
- At least 32 bits long; and
- Randomly generated for each account.

### Control Recommendations

Refer to NIST [SP 800-90Ar1](https://doi.org/10.6028/NIST.SP.800-90Ar1) for suitable pseudo-random number generators. Refer to NIST [SP 800-63b](https://doi.org/10.6028/NIST.SP.800-63b) Memorized Secret Verifiers section for suitable hashing schemes, including Argon2, scrypt, and PBKDF2. For application source code, use a cryptographically secure pseudo-random number generator function instead of an insecure one, such as crypto.randomBytes instead of Math.random in Node.js and java.security.SecureRandom.nextBytes instead of java.util.Random in Java.

### Risk Statement

Without salting and hashing, in case of a data breach, exposed passwords can be easily extracted, leading to potential compromise of accounts and sensitive information.

## AS-7: Access Control Check Enforcement

**Group:** Application Security

### Control Statement

Perform access control checks on all authenticated requests.

### Control Recommendations

Utilise authorisation filters or middleware to force all authenticated requests to undergo access control checks.

### Risk Statement

Failure to perform access control checks on authenticated requests increases the risk of unauthorised access to sensitive data or functionalities, potentially leading to data breaches and misuse of system resources.

## AS-8: Secrets Management

**Group:** Application Security

### Control Statement

Securely store secrets in an appropriate secrets management solution with access control enforcement, encryption, and monitoring.

### Control Recommendations

Secrets include API keys, access keys, and other static credentials. Do not store secrets unencrypted in source code or configuration files. Store secrets in cloud-native solutions like AWS Secrets Manager and Azure Key Vault or cloud-agnostic solutions like HashiCorp Vault and CyberArk Conjur. For SaaS or platforms, ensure that secrets are stored in an appropriate solution. For example, use GitHub Actions secrets instead of variables.

### Risk Statement

Exposure of sensitive information and unauthorised access to system credentials may occur if application secrets are stored insecurely or hard-coded in source code.

## AS-9: Content Security Policy (CSP)

**Group:** Application Security

### Control Statement

Set minimally permissive CSP response headers to mitigate cross-site scripting attacks.

### Control Recommendations

Utilise the relevant fetch directives such as `default-src`, `script-src`, `style-src`, `connect-src`, `img-src`, `media-src` and `object-src` to prevent loading of scripts from malicious sources. Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

### Risk Statement

Without minimally permissive Content Security Policy (CSP) headers, the risk of cross-site scripting attacks, leading to unauthorised script execution and potential data theft, is increased.

## AS-10: HTTP Strict Transport Security (HSTS)

**Group:** Application Security

### Control Statement

Set HTTP Strict Transport Security (HSTS) response headers with a maximum age value of at least 1 year (31536000 seconds) to mitigate protocol downgrade attacks.

### Control Recommendations

Refer to the [OWASP Secure Headers Project](https://owasp.org/www-project-secure-headers) Best Practices for recommended header values.

### Risk Statement

Failure to implement HTTP Strict Transport Security (HSTS) with a sufficient maximum age may expose the system to protocol downgrade attacks, compromising the security of communication channels.

## AS-11: Session Management

**Group:** Application Security

### Control Statement

Require [ insert: param, as-11_prm_2 ] to re-authenticate after their session exceeds [ insert: param, as-11_prm_1 ] hour(s) or terminate the session.

### Control Recommendations

NIST SP 800-63B recommends re-authentication once per 30 days for Authenticator Assurance Level 1, 12 hours or 30 minutes inactivity for Authenticator Assurance Level 2, and 12 hours or 15 minutes inactivity for Authenticator Assurance Level 3. In addition to time period, system can consider re-authentication when roles, authenticators or credentials change or when the execution of privileged functions occurs.

### Risk Statement

Not re-authenticating regularly and at suitable checkpoints could allow someone who has access to the account to carry out unauthorised actions.

### Parameters

| ID          | Type                      | Description                                               |
| ----------- | ------------------------- | --------------------------------------------------------- |
| as-11_prm_1 | time period (hours) (int) | The maximum time period in hours of a user&#39;s session. |
| as-11_prm_2 | type (str)                | The type of session.                                      |

## AS-12: Malware Scanning of Uploaded Files

**Group:** Application Security

### Control Statement

Scan file uploads for malware before further processing by the system.

### Control Recommendations

Consider uploading the files to temporary storage for malware scanning on ephemeral compute like serverless functions before moving safe files to another storage for further processing or unsafe files to quarantine storage.

### Risk Statement

Without scanning uploaded files for malware, there&#39;s an increased risk of exploits or infection for consumers of the files.

## AS-13: Exposure of Internal System Details

**Group:** Application Security

### Control Statement

Prevent the unnecessary disclosure of internal system details to Public Users.

### Control Recommendations

Ensure all system messages and notifications are informative yet secure. These messages should be contextually appropriate, providing relevant information without exposing internal system details such as debug information, stack traces, or software versioning.

### Risk Statement

Disclosure of internal system details or debug stack traces can expose vulnerabilities, software versions, and system architecture, potentially leading to targeted attacks, exploitation of known vulnerabilities, and unauthorised access to sensitive systems or data.

## AS-14: Secure Cryptographic Libraries

**Group:** Application Security

### Control Statement

Use reputable and secure cryptographic libraries and functions to handle cryptographic operations.

### Control Recommendations

Follow the OWASP Cryptographic Storage Cheat Sheet for best practices in securely implementing cryptographic operations. Regularly update libraries and prefer widely recognised ones such as OpenSSL. Consider using libraries that are FIPS 140-2 or FIPS 140-3 compliant for enhanced security assurance.

### Risk Statement

Using insecure cryptographic libraries and functions can expose applications to significant security risks, such as data breaches and unauthorised access, compromising sensitive information.

## AS-15: Password Change

**Group:** Application Security

### Control Statement

Enforce password change upon suspected account compromise.

### Control Recommendations

Implement mechanisms to detect signs of account compromise, such as unusual login activity or multiple failed login attempts. Notify users promptly to change their passwords and provide guidance on creating strong, unique passwords. Consider integrating multi-factor authentication to enhance security.

### Risk Statement

Failure to enforce password changes upon suspected account compromise increases the risk of prolonged unauthorised access, leading to potential data breaches and exploitation of systems.